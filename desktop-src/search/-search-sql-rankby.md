---
description: Los resultados de una consulta incluyen las filas devueltas por la consulta y un valor de rango para cada fila si la columna rank se incluye en la cláusula SELECT.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: RANK BY (cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33daf4865b0f7f08689802822d8c0d5b4d38702a1cb1f813563564e001811a6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462444"
---
# <a name="rank-by-clause"></a>RANK BY (cláusula)

Los resultados de una consulta incluyen las filas devueltas por la consulta y un valor de rango para cada fila si la columna rank se incluye en la cláusula SELECT. El motor de búsqueda calcula los valores de rango y se devuelven como enteros en el intervalo de cero a 1000. Para que los resultados de la clasificación sean más significativos, la consulta puede controlar cómo se calculan los valores de rango sin formato en la cláusula RANK BY.

Este tema se organiza de la siguiente manera:

-   [RANK BY (cláusula)](#rank-by-clause)
-   [Weight (Función)](#weight-function)
-   [Función COERCION](#coercion-function)

## <a name="rank-by-clause"></a>RANK BY (cláusula)

La sintaxis de la cláusula RANK BY es la siguiente:


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



La cláusula RANK BY se aplica a la condición de búsqueda inmediatamente anterior a ella, especificando eficazmente una clasificación inferior o superior para las filas devueltas por esa condición de búsqueda que las filas devueltas por otra condición \_ de búsqueda. Se requieren los paréntesis que rodean la \_ condición de búsqueda. Los paréntesis que rodean la especificación de rango son opcionales.

Se puede aplicar más de una cláusula RANK BY a una sola condición. Puede incluir cláusulas RANK BY adicionales una tras otra con paréntesis.

> [!Note]  
> Los predicados de texto completo devuelven valores de rango en el intervalo de 0 a 1000. Los valores de rango de todos los documentos coincidentes con un predicado que no es de texto completo son 1000. Las modificaciones en los valores de clasificación deben tener en cuenta esta información.

 

La parte de especificación de rango \_ de la cláusula RANKBY identifica una o varias funciones que se aplicarán a los valores de clasificación. La función WEIGHT aplica un multiplicador al valor de rango sin formato para una fila devuelta. Cuanto menor sea el multiplicador, menor es el valor de rango resultante. La función COERCION se puede usar para multiplicar, agregar o establecer un valor de rango específico para una fila devuelta. Cada especificación de rango puede incluir cero o una función WEIGHT y cero o más funciones COERCION. Si las funciones WEIGHT y COERCION se incluyen en una cláusula RANK BY, la función WEIGHT debe ser la primera.

## <a name="weight-function"></a>Weight (Función)

La sintaxis de la función WEIGHT es:


```
WEIGHT ( <weight_multipler> ) 
```



El multiplicador debe ser un decimal de 0,001 a 1,000. El valor de rango sin formato devuelto por el predicado de condición de búsqueda se multiplica por el multiplicador de peso para establecer un nuevo valor de rango.

En el ejemplo siguiente, la función WEIGHT proporciona documentos con la palabra "Theresa" en System.Document. Campo LastAuthor a la mitad del valor de rango de los documentos con "Theresa" en el campo System.Author:


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> Las características de ponderación de columnas de predicado CONTAINS y FREETEXT admiten un formato abreviado con dos puntos entre el término de búsqueda y el multiplicador ("software":0.25). La cláusula RANK BY no admite el formulario abreviado.

 

Hay una limitación al usar RANK BY WEIGHT: no funciona con cláusulas CONTAINS que usan condiciones booleanas; Por ejemplo, no se permite el ejemplo siguiente:


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a>Función COERCION

La función de coerción de rango se puede usar para cambiar el valor de rango devuelto por suma o multiplicación, o bien para asignarle un valor específico.

La sintaxis de la función COERCION es:


```
COERCION ( <coercion_operation> , <coercion_value> )
```



El valor de coerción es un valor entero.

En la tabla siguiente se describe la configuración de la operación de coerción disponible.



| Operación de coerción | Descripción                                                                                    | Intervalo de valores  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| ABSOLUTE           | El valor de rango devuelto es el valor especificado en el valor de coerción.                          | De 0 a 1000    |
| ADD                | El valor de rango devuelto es la suma del valor de rango sin formato y el valor de coerción especificado.     | De 0,001 a 1,0 |
| MULTIPLY           | El valor de rango devuelto es el producto del valor de rango sin formato y el valor de coerción especificado. | De 0,001 a 1,0 |



 

 

> [!IMPORTANT]
> La búsqueda solo puede devolver valores de rango en el intervalo de 0 a 1000.

 

 

En el ejemplo siguiente se usa la función COERCION para establecer que todos los documentos con "equipo" en el título tengan una clasificación de 1000, a la vez que se reduce en un cuarto el rango de documentos que contienen "equipo" y "software" en el título.


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



