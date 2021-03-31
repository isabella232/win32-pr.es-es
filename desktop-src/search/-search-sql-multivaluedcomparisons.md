---
description: Las columnas almacenadas en el índice de contenido pueden tener varios valores, y esas columnas multivalor se pueden comparar utilizando el predicado de comparación de matrices.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Comparaciones de varios valores (matriz)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77710ecdddcf289c9a5c64d0c5f57ca449311097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808930"
---
# <a name="multi-valued-array-comparisons"></a>Comparaciones de varios valores (matriz)

Las columnas almacenadas en el índice de contenido pueden tener varios valores, y esas columnas multivalor se pueden comparar utilizando el predicado de comparación de matrices.

El predicado de comparación de matrices tiene la siguiente sintaxis:


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



Se devuelve un error si la referencia de columna no es una columna de varios valores. El tipo de datos de la columna debe ser compatible con los elementos de la lista de comparación. Si es necesario, la referencia de columna se puede [convertir](-search-sql-castingdatacolumntype.md) en otro tipo de datos.

El operador de comparación (COMP \_ OP) puede ser cualquiera de los operadores de comparación normales. En una comparación de varios valores, los operadores de comparación tienen significados ligeramente diferentes en función de si se usa un cuantificador. Los cuantificadores identifican si se debe realizar una comparación con todos o algunos de los valores de la lista de comparación. Las funciones de los operadores de comparación se proporcionan en las tablas que describen cada cuantificador (todos y algunos) más adelante en este documento.

El valor después del operador especifica un único valor literal que se compara con todos los elementos de la columna de varios valores. Si algún elemento coincide con el valor, el predicado es true.

La lista de comparación especifica una matriz de valores literales que se comparan con la columna de varios valores. La sintaxis de la lista de comparación es la siguiente:


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> Tenga en cuenta la sintaxis de la lista de comparación. El grupo de literales que conforman la lista de comparación debe ir entre corchetes. No incluya los elementos individuales de la lista de comparación entre corchetes. Por lo tanto, las matrices \[ 1 \] y \[ 1, 2, 3 \] son válidas, pero la matriz \[ 1 \[ , 2 \] \[ , 3 \] \] no.

 

El método que se usa para determinar si la comparación multivalor devuelve true o false lo especifica el cuantificador opcional. En las secciones siguientes se describe cada cuantificador y cómo funciona cada operador de comparación cuando se utiliza el cuantificador.

## <a name="absent-quantifier"></a>Cuantificador ausente

Si no se especifica ningún cuantificador, cada elemento en el lado izquierdo de la comparación se compara con el elemento de la misma posición del lado derecho. La comparación comienza con el primer elemento de las matrices y progresa a través del último elemento. Si todos los elementos del lado izquierdo son equivalentes a los elementos correspondientes del lado derecho, se usa el número de elementos de matriz para determinar qué matriz es mayor.

En la tabla siguiente se muestra la operación de los operadores de comparación cuando no se especifica ningún cuantificador y se proporciona una breve descripción de cada uno.



| Operator       | Descripción                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | ' Igual a ' devuelve true cuando cada elemento del lado izquierdo tiene el mismo valor que el elemento de la derecha correspondiente, y ambas matrices tienen el mismo número de elementos.                                                                                                                                                                                                                     |
| ! = o <> | ' No es igual a ' devuelve true cuando uno o más elementos del lado izquierdo tienen valores que difieren de los elementos del lado derecho correspondientes, o cuando las matrices del lado izquierdo y derecho no tienen el mismo número de elementos.                                                                                                                                                              |
| >           | ' Mayor que ' devuelve true cuando el valor de cada elemento de la izquierda es mayor que el valor del elemento correspondiente del lado derecho. Si todos los valores de los elementos del lado izquierdo coinciden exactamente con los elementos del lado derecho correspondientes y la matriz del lado izquierdo tiene más elementos que la matriz del lado derecho, ' mayor que ' devuelve true.                                                     |
| >=          | ' Mayor o igual que ' devuelve true cuando el valor de cada elemento del lado izquierdo es mayor o igual que el valor del elemento correspondiente del lado derecho. Si todos los valores de los elementos del lado izquierdo son iguales o mayores que los elementos correspondientes del lado derecho y la matriz del lado izquierdo tiene los mismos elementos que la matriz del lado derecho, ' Greater Than ' devuelve true. |
| <           | ' Less than ' devuelve true cuando el valor de cada elemento de la izquierda es menor que el valor del elemento correspondiente del lado derecho. ' Menor que ' también devuelve true cuando el lado izquierdo tiene menos elementos que el lado derecho.                                                                                                                                                  |
| <=          | ' Menor o igual que ' devuelve true cuando el valor de todos los elementos del lado izquierdo es menor o igual que el valor del elemento correspondiente del lado derecho. Si todos los valores de los elementos del lado izquierdo son iguales o menores que los elementos correspondientes del lado derecho y la matriz del lado izquierdo tiene el mismo o menos elementos que la matriz del lado derecho, ' mayor que ' devuelve true.         |



 

## <a name="all-quantifier"></a>Todos los cuantificadores

El cuantificador ALL especifica que cada elemento del lado izquierdo se compara con cada elemento del lado derecho. Para devolver true, la comparación debe ser true para cada elemento del lado izquierdo cuando se comparan con cada elemento del lado derecho. El número de elementos de los lados izquierdo y derecho de la matriz no tiene ningún efecto en el resultado.

En la tabla siguiente se muestra cómo cada operador de comparación funciona con el cuantificador todos.



| Operator       | Descripción                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | ' Igual a ' devuelve true cuando cada valor del elemento de la izquierda es igual que todos los valores de elemento del lado derecho.                              |
| ! = o <> | ' No es igual a ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es diferente de cualquiera de los valores de los elementos del lado derecho. |
| >           | ' Mayor que ' devuelve true cuando cada valor del elemento de la izquierda es mayor que todos los valores de elemento del lado derecho.                         |
| >=          | ' Mayor o igual que ' devuelve true cuando cada valor del elemento de la izquierda es mayor o igual que cada valor de elemento del lado derecho. |
| <           | ' Less than ' devuelve true cuando cada valor de elemento del lado izquierdo es menor que cada valor de elemento del lado derecho.                               |
| <=          | ' Menor o igual que ' devuelve true cuando cada valor del elemento de la izquierda es menor o igual que cada valor de elemento del lado derecho.       |



 

## <a name="some-or-any-quantifier"></a>UN cuantificador (o cualquiera)

El cuantificador y el cuantificador ANY se pueden usar indistintamente. Al igual que el cuantificador ALL, el cuantificador SOME especifica que cada elemento del lado izquierdo se compara con cada elemento del lado derecho. Para devolver true, la comparación debe ser true para al menos uno de los elementos del lado izquierdo cuando se comparan con cualquier elemento del lado derecho. El número de elementos de las matrices de la izquierda y la derecha no tiene ningún efecto en el resultado.

En la tabla siguiente se muestra cómo cada operador de comparación funciona con el cuantificador.



| Operator       | Descripción                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | ' Equal to ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es igual que cualquiera de los valores de los elementos del lado derecho.                                  |
| ! = o <> | ' No es igual a ' devuelve true cuando ninguno de los valores de los elementos del lado izquierdo es igual que ninguno de los valores de elemento del lado derecho.                                      |
| >           | ' Greater Than ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es mayor que uno de los valores de los elementos del lado derecho.                         |
| >=          | ' Mayor o igual que ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es mayor o igual que uno de los valores de los elementos del lado derecho. |
| <           | ' Less than ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es menor que uno de los valores de los elementos del lado derecho.                               |
| <=          | ' Menor o igual que ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es menor o igual que uno de los valores de los elementos del lado derecho.       |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se comprueba si los documentos se encuentran en las categorías "Finance" o "Planning":


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



Las siguientes comparaciones se evalúan como true. Recuerde que, en el uso real, la sintaxis de consulta de búsqueda requiere que el lado izquierdo sea una propiedad, no un valor literal.


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[LIKE (predicado)](-search-sql-like.md)
</dt> <dt>

[Comparación de valores literales](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Predicado NULL](-search-sql-null.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



