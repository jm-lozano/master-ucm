# Funciones de conteo con fuciones perezosas y map-reduce

En las siguientes funciones se deben solucionar usando funciones
perezosas y evitando el uso de bucles.

1.- Realiza una función read_words que devuelva un iterador con las
palabras de un fichero de texto

def read_words(filename: str) -> Iterator[str]:
    '''
    Returns an iterator with the words in a file

>>> read_words('mi_texto2.txt') # doctest: +ELLIPSIS
<generator object read_words ...>

>>> list(read_words('mi_texto2.txt')) # doctest: +NORMALIZE_WHITESPACE
['Con',  'cien', 'cañones', 'por', 'banda', 'Viento',
 'en', 'popa', 'a', 'toda', 'vela']
    '''

2. Haz una función que dado un fichero de texto y una palabra, nos
   indique cuántas veces aparece la palabra en el fichero.

def occurrences(filename: str, word: str) -> int:
    '''
    Returns the number of times a word appears in a file
>>> occurrences('mi_texto.txt', 'banda')
3

>>> occurrences('mi_texto.txt', 'patata')
0

>>> occurrences('mi_texto.txt', 'vela')
2
    '''

3. Haz una función que cuente cuántas veces aparece una palabra en un
   fichero
def count_all(filename: str) -> dict[str, int]:
    '''
    Returns a dictionary with the number of occurrences of each word in a file

>>> count_all('mi_texto.txt') # doctest: +ELLIPSIS +NORMALIZE_WHITESPACE
{'Con': 3, 'cien': 3, 'cañones': 3, 'por': 3, 'banda': 3, 'Viento': 3,
 'en': 3, 'popa': 3, 'a': 2, 'toda': 2, 'vela': 2}

    '''
