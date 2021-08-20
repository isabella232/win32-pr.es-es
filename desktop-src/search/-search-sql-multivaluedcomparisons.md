---
description: Las columnas almacenadas en el índice de contenido pueden tener varios valores y esas columnas multivalor se pueden comparar mediante el predicado de comparación ARRAY.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Comparaciones multivalor (ARRAY)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043ed6744717ac3156d9dd64f2f6806f2ffc509107f5bcdc8a66980e5cdd0012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863374"
---
# <a name="multi-valued-array-comparisons"></a>Comparaciones multivalor (ARRAY)

Las columnas almacenadas en el índice de contenido pueden tener varios valores y esas columnas multivalor se pueden comparar mediante el predicado de comparación ARRAY.

El predicado de comparación ARRAY tiene la sintaxis siguiente:


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



Se devuelve un error si la referencia de columna no es una columna de varios valores. El tipo de datos de columna debe ser compatible con los elementos de la lista de comparación. Si es necesario, la referencia de columna se [puede convertir](-search-sql-castingdatacolumntype.md) como otro tipo de datos.

El operador de comparación (comp \_ op) puede ser cualquiera de los operadores de comparación normales. En una comparación de varios valores, los operadores de comparación tienen significados ligeramente diferentes en función de si se usa un cuantificador. Los cuantificadores identifican si se debe realizar una comparación con todos o algunos de los valores de la lista de comparación. Las funciones de los operadores de comparación se dan en las tablas que describen cada cuantificador (ALL y SOME) más adelante en este documento.

El valor después del operador especifica un valor literal único que se compara con todos los elementos de la columna de varios valores. Si algún elemento coincide con el valor , el predicado es true.

La lista de comparación especifica una matriz de valores literales que se comparan con la columna de varios valores. La sintaxis de la lista de comparación es la siguiente:


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> Tenga en cuenta la sintaxis de la lista de comparación. El grupo de literales que forma la lista de comparación debe estar entre corchetes. No envolve los elementos individuales de la lista de comparación entre corchetes. Por lo tanto, ARRAY \[ 1 \] y ARRAY \[ 1,2,3 son válidos, pero \] ARRAY \[ \[ 1,2,3 \] \[ \] \] no.

 

El cuantificador opcional especifica el método utilizado para determinar si la comparación multivalor devuelve true o false. En las secciones siguientes se describe cada cuantificador y cómo funciona cada operador de comparación cuando se usa el cuantificador.

## <a name="absent-quantifier"></a>Cuantificador ausente

Si no se especifica ningún cuantificador, cada elemento del lado izquierdo de la comparación se compara con el elemento situado en la misma posición del lado derecho. La comparación comienza con el primer elemento de las matrices y progresa por el último elemento. Si todos los elementos del lado izquierdo son equivalentes a los elementos correspondientes del lado derecho, se usa el número de elementos de matriz para determinar qué matriz es mayor.

En la tabla siguiente se muestra el funcionamiento de los operadores de comparación cuando no se especifica ningún cuantificador y se proporciona una breve descripción de cada uno.



| Operador       | Descripción                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | 'Equal to' devuelve true cuando cada elemento del lado izquierdo tiene el mismo valor que el elemento del lado derecho correspondiente y ambas matrices tienen el mismo número de elementos.                                                                                                                                                                                                                     |
| != o <> | 'Not equal to' devuelve true cuando uno o varios elementos del lado izquierdo tienen valores que difieren de los elementos del lado derecho correspondientes, o cuando las matrices del lado izquierdo y derecho no tienen el mismo número de elementos.                                                                                                                                                              |
| >           | 'Greater than' devuelve true cuando el valor de cada elemento del lado izquierdo es mayor que el valor del elemento del lado derecho correspondiente. Si todos los valores del elemento del lado izquierdo coinciden exactamente con los elementos del lado derecho correspondientes y la matriz del lado izquierdo tiene más elementos que la matriz del lado derecho, 'greater than' devuelve true.                                                     |
| >=          | 'Greater than or equal to' devuelve true cuando el valor de cada elemento del lado izquierdo es mayor o igual que el valor del elemento del lado derecho correspondiente. Si todos los valores del elemento del lado izquierdo son iguales o mayores que los elementos del lado derecho correspondientes y la matriz del lado izquierdo tiene los mismos elementos o más que la matriz del lado derecho, 'greater than' devuelve true. |
| <           | 'Less than' devuelve true cuando el valor de cada elemento del lado izquierdo es menor que el valor del elemento del lado derecho correspondiente. 'Less than' también devuelve true cuando el lado izquierdo tiene menos elementos que el lado derecho.                                                                                                                                                  |
| <=          | 'Menor o igual que' devuelve true cuando el valor de cada elemento del lado izquierdo es menor o igual que el valor del elemento del lado derecho correspondiente. Si todos los valores del elemento del lado izquierdo son iguales o menores que los elementos del lado derecho correspondientes y la matriz del lado izquierdo tiene los mismos elementos o menos que la matriz del lado derecho, 'greater than' devuelve true.         |



 

## <a name="all-quantifier"></a>CUANTIFICADOR ALL

El cuantificador ALL especifica que cada elemento del lado izquierdo se compara con cada elemento del lado derecho. Para devolver true, la comparación debe ser verdadera para cada elemento del lado izquierdo en comparación con cada elemento del lado derecho. El número de elementos de los lados de la matriz izquierda y derecha no tiene ningún efecto en el resultado.

En la tabla siguiente se muestra cómo funciona cada operador de comparación con el cuantificador ALL.



| Operador       | Descripción                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | 'Equal to' devuelve true cuando cada valor de elemento del lado izquierdo es el mismo que cada valor de elemento del lado derecho.                              |
| != o <> | 'Not equal to' devuelve true cuando al menos uno de los valores de elemento del lado izquierdo es diferente de cualquiera de los valores del elemento del lado derecho. |
| >           | 'Greater than' devuelve true cuando cada valor de elemento del lado izquierdo es mayor que cada valor de elemento del lado derecho.                         |
| >=          | 'Greater than or equal to' devuelve true cuando cada valor de elemento del lado izquierdo es mayor o igual que cada valor de elemento del lado derecho. |
| <           | 'Less than' devuelve true cuando cada valor de elemento del lado izquierdo es menor que cada valor de elemento del lado derecho.                               |
| <=          | 'Menor o igual que' devuelve true cuando cada valor de elemento del lado izquierdo es menor o igual que cada valor de elemento del lado derecho.       |



 

## <a name="some-or-any-quantifier"></a>CUANTIFICADOR SOME (o ANY)

El cuantificador SOME y el cuantificador ANY se pueden usar indistintamente. Al igual que el cuantificador ALL, el cuantificador SOME especifica que cada elemento del lado izquierdo se compara con cada elemento del lado derecho. Para devolver true, la comparación debe ser verdadera para al menos uno de los elementos del lado izquierdo en comparación con cualquier elemento del lado derecho. El número de elementos de las matrices izquierda y derecha no tiene ningún efecto en el resultado.

En la tabla siguiente se muestra cómo funciona cada operador de comparación con el cuantificador SOME.



| Operador       | Descripción                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | 'Equal to' devuelve true cuando al menos uno de los valores de elemento del lado izquierdo es el mismo que cualquiera de los valores del elemento del lado derecho.                                  |
| != o <> | 'Not equal to' devuelve true cuando ninguno de los valores del elemento del lado izquierdo es el mismo que cualquiera de los valores del elemento del lado derecho.                                      |
| >           | 'Greater than' devuelve true cuando al menos uno de los valores de elemento del lado izquierdo es mayor que cualquiera de los valores de los elementos del lado derecho.                         |
| >=          | 'Mayor o igual que' devuelve true cuando al menos uno de los valores de elemento del lado izquierdo es mayor o igual que cualquiera de los valores de elemento del lado derecho. |
| <           | 'Less than' devuelve true cuando al menos uno de los valores de elemento del lado izquierdo es menor que cualquiera de los valores de los elementos del lado derecho.                               |
| <=          | 'Menor o igual que' devuelve true cuando al menos uno de los valores de elemento del lado izquierdo es menor o igual que cualquiera de los valores de elemento del lado derecho.       |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se comprueba si los documentos están en las categorías "Finance" o "Planning":


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



Todas las comparaciones siguientes evalúan true. Recuerde que, en el uso real, la sintaxis de consulta de búsqueda requiere que el lado izquierdo sea una propiedad, no un valor literal.


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

[Predicado LIKE](-search-sql-like.md)
</dt> <dt>

[Comparación de valores literales](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Predicado NULL](-search-sql-null.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



