---
description: Los resultados de una consulta incluyen las filas devueltas por la consulta y un valor de clasificación para cada fila si la columna Rank se incluye en la cláusula SELECT.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: RANK BY (cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275263"
---
# <a name="rank-by-clause"></a>RANK BY (cláusula)

Los resultados de una consulta incluyen las filas devueltas por la consulta y un valor de clasificación para cada fila si la columna Rank se incluye en la cláusula SELECT. Los valores de rango se calculan mediante el motor de búsqueda y se devuelven como enteros en el intervalo comprendido entre cero y 1000. Para que los resultados de la clasificación sean más significativos, la consulta puede controlar cómo se calculan los valores de clasificación sin formato en la cláusula RANK BY.

Este tema se organiza de la siguiente manera:

-   [RANK BY (cláusula)](#rank-by-clause)
-   [Función WEIGHT](#weight-function)
-   [Función de coerción](#coercion-function)

## <a name="rank-by-clause"></a>RANK BY (cláusula)

La sintaxis de la cláusula RANK BY es la siguiente:


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



La cláusula RANK BY se aplica a la condición de búsqueda \_ inmediatamente anterior, especificando de forma eficaz un rango inferior o superior para las filas devueltas por esa condición de búsqueda que las filas devueltas por otra condición de búsqueda. Los paréntesis que rodean la \_ condición de búsqueda son obligatorios. Los paréntesis que rodean la especificación de rango son opcionales.

Se puede aplicar más de una cláusula RANK BY a una única condición. Puede incluir cláusulas RANK BY adicionales una tras otra mediante paréntesis.

> [!Note]  
> Los predicados de texto completo devuelven valores de rango en el intervalo comprendido entre 0 y 1000. Los valores de rango para todos los documentos que coincidan con un predicado de texto no completo son 1000. Las modificaciones en los valores de clasificación deben tener en cuenta esta información.

 

La \_ parte de la especificación de rango de la cláusula RANKBY identifica una o más funciones que se van a aplicar a los valores de clasificación. La función WEIGHT aplica un multiplicador al valor de rango sin formato de una fila devuelta. Cuanto menor sea el multiplicador, menor será el valor de rango resultante. La función de coerción se puede usar para multiplicar, agregar o establecer un valor de rango específico para una fila devuelta. Cada especificación de rango puede incluir una función de peso o cero, y cero o más funciones de coerción. Si las funciones de peso y de coerción se incluyen en una cláusula RANK BY, la función WEIGHT debe ser primero.

## <a name="weight-function"></a>Función WEIGHT

La sintaxis de la función WEIGHT es la siguiente:


```
WEIGHT ( <weight_multipler> ) 
```



El multiplicador debe ser un decimal comprendido entre 0,001 y 1,000. El valor de rango sin formato devuelto por el predicado de la condición de búsqueda se multiplica por el multiplicador de peso para establecer un nuevo valor de rango.

En el ejemplo siguiente, la función WEIGHT proporciona documentos con la palabra "Theresa" en la System.Document. Campo LastAuthor mitad del valor de rango de los documentos con "Theresa" en el campo System. Author:


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> Las características de ponderación de columnas de predicado CONTAINS y FREETEXT admiten un formato abreviado con un signo de dos puntos entre el término de búsqueda y el multiplicador ("software": 0,25). La cláusula RANK BY no admite la forma abreviada.

 

Existe una limitación al usar RANK BY WEIGHT: no funciona con cláusulas Contains que usan condiciones booleanas; por ejemplo, no se permite el siguiente ejemplo:


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a>Función de coerción

La función de conversión de rangos se puede usar para cambiar el valor de rango devuelto por la suma o la multiplicación o mediante la asignación de un valor específico.

La sintaxis de la función de coerción es:


```
COERCION ( <coercion_operation> , <coercion_value> )
```



El valor de coerción es un valor entero.

En la tabla siguiente se describe la configuración de la operación de conversión disponible.



| Operación de coerción | Descripción                                                                                    | Intervalo de valores  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| ABSOLUTE           | El valor de rango devuelto es el valor especificado en el valor de coerción.                          | de 0 a 1000    |
| ADD                | El valor de rango devuelto es la suma del valor de rango sin formato y el valor de coerción especificado.     | de 0,001 a 1,0 |
| MULTIPLY           | El valor de rango devuelto es el producto del valor de rango sin formato y el valor de coerción especificado. | de 0,001 a 1,0 |



 

 

> [!IMPORTANT]
> La búsqueda solo puede devolver valores de rango en el intervalo de 0 a 1000.

 

 

En el ejemplo siguiente se usa la función de coerción para establecer todos los documentos con "Computer" en el título para que tengan un rango de 1000, mientras que se reduce en un trimestre el rango de documentos que contienen "Computer" y "software" en el título.


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



