# Criba de Eratóstenes perezosa

Considera la el generador de números primos vista en clase
`def all_natural_numbers() -> Generator[int]`

Define ahora una función de dado un número arbitrario `p`, devuelva
una función que compruebe si un número es divisible por `p`:
`def div(p: int) -> Callable[[int], bool]`

Usando esa función, define ahora un generador de números primos.
`def gen_primes() -> Generator[int]`

Dicha función debe partir de todos los números naturales. En primer
lugar filtra el número uno, es decir usa la función filter para
filtrar todos los elementos que no sean 1. El primer elemento que
queda es el 2, que es primo (lo llamamos p).
Se devuelve ese primo con `yield`. A continuación,
nos quedamos con los números que no sean divisibles por `p`.
El siguiente elemento es 3 y se repite el proceso *por siempre*.

Un ejemplo de uso de ese generador es una función que devuele los `n`
primeros números primos

`
def first_primes(n: int) -> list[int]:
    gen = gen_primes()
    return [next(gen) for _ in range(n)]
`
