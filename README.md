# Proyecto 1

## Parte 1

Disponemos de unos datos de entrada donde se indica en qué posición finalizó un piloto cada Gran Premio de una temporada de la siguiente forma:

```python
driver_season_data = {
        "Bahrain Grand Prix": {
            "position": "1",
            "is_fastestlap": False,
            "bestlap": "00:01:34.015000"
        },
        "Emilia Romagna Grand Prix": {
            "position": "2",
            "is_fastestlap": True,
            "bestlap": "00:01:16.702000"
        },
        "Portuguese Grand Prix": {
            "position": "1",
            "is_fastestlap": False,
            "bestlap": "00:01:20.933000"
        },
        ...
}
```

En dichos datos se echa en falta que se especifique el número de puntos que obtuvo el piloto en cada carrera, por los que nos piden que hagamos un función que complete dicho diccionario añadiendo una clave **points** donde se especifiquen los puntos obtenidos en cada carrera.

Para ello, lo primero que haremos será hacer una función que dada una posición en forma de str y no mediante un tipo int devolverá el número de puntos obtenidos y que tendrá la siguiente forma:

```python
def get_race_points_from_position(position: str) -> int:
    """
    Los puntos a otorgar se reparten según la siguiente tabla:

    | Posición  | Puntos |
    |-----------|--------|
    | "1"       | 25     |
    | "2"       | 18     |
    | "3"       | 15     |
    | "4"       | 12     |
    | "5"       | 10     |
    | "6"       | 8      |
    | "7"       | 6      |
    | "8"       | 4      |
    | "9"       | 2      |
    | "10"      | 1      |
    | otro caso | 0      |
    
    """
```

## Parte 2

Los datos nos indican también si el piloto fue el autor de la vuelta rápida. Vamos a hacer una función que nos devuelva los puntos que obtuvo un piloto en la carrera, considerando el punto extra por la vuelta rápido si el piloto quedó entre los 10 primeros.

```python

def get_race_points_from_position_and_fastest_lap(position: int, has_fastest_lap) -> int:
```

## Parte 3

Una vez disponemos de una función que nos indica los puntos que se obtienen según la posición y la vuelta rápida, vamos a hacer una función dadas las carreras realizadas por un piloto en una temporada nos indique el número de puntos que dicho piloto obtuvo esa temporada.

La función tendrá la siguiente interfaz:


```python
def get_driver_season_points(driver_season_data: {}) -> int:
```

El parámetro **driver_season_data** será un diccionario con la siguiente forma:

```python
{
        "Bahrain Grand Prix": {
            "position": 1,
            "is_fastestlap": False,
            "bestlap": "00:01:34.015000"
        },
        "Emilia Romagna Grand Prix": {
            "position": 2,
            "is_fastestlap": True,
            "bestlap": "00:01:16.702000"
        },
        "Portuguese Grand Prix": {
            "position": 1,
            "is_fastestlap": False,
            "bestlap": "00:01:20.933000"
        }
}
```