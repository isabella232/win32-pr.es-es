---
description: Una función de agregado realiza un cálculo en un conjunto de valores y devuelve un valor. Si lo hace, es posible generar estadísticas de resumen para los grupos de varios niveles con poca sobrecarga.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Funciones de agregado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570305"
---
# <a name="aggregate-functions"></a>Funciones de agregado

Una función de agregado realiza un cálculo en un conjunto de valores y devuelve un valor. Si lo hace, es posible generar estadísticas de resumen para los grupos de varios niveles con poca sobrecarga.

## <a name="about-aggregate-functions"></a>Acerca de las funciones de agregado

Las funciones de agregado en Lenguaje de consulta estructurado de Windows Search (SQL) tienen la siguiente sintaxis:


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



La parte de la función puede incluir cualquiera de las siguientes funciones y sintaxis:



| Función                                                              | Descripción                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AVG ( <column> )                                                   | Devuelve el promedio de los valores de un grupo. Solo se aplica a números.                                                                                                                                      |
| BYFREQUENCY ( <column> , <N> )                                | Devuelve los valores de columna N más frecuentes de los resultados del grupo. También incluye un recuento del número de veces que se produjo cada valor y los identificadores de documento de los resultados que contienen cada valor devuelto. |
| CHILDCOUNT ()                                                          | Devuelve el número de elementos de un grupo (sin incluir los subgrupos). Si hay varios niveles de agrupación, devuelve el número de grupos secundarios inmediatos.                                                  |
| COUNT ()                                                               | Devuelve el número de elementos de un grupo y todos los subgrupos.                                                                                                                                                   |
| DATERANGE ( <column> )                                             | Devuelve los límites inferior y superior de los valores de columna que se encuentran en el grupo de resultados del grupo. Solo es válido para las propiedades de FILETIME.                                                                               |
| PRIMERO ( <column> , <N> )                                      | Devuelve los N primeros valores de columna de los resultados hoja encontrados en un grupo.                                                                                                                                       |
| MAX ( <column> )                                                   | Devuelve el valor máximo de la expresión. Solo se aplica a números o fechas.                                                                                                                              |
| MIN ( <column> )                                                   | Devuelve el valor mínimo de la expresión. Solo se aplica a números o fechas.                                                                                                                              |
| Representador ( <column> , <idRepresentative> , <N> ) | Devuelve N valores idRepresentative, cada uno de los cuales se selecciona de uno de los subconjuntos de resultados que tiene un valor de columna único. Cada valor también se devuelve con un identificador de documento que tiene el valor idRepresentative. |
| SUM ( <column> )                                                   | Devuelve la suma de los valores de un grupo. Solo se aplica a números.                                                                                                                                          |



 

 

> [!Note]  
> Los agregados se devuelven como columnas individuales. Son principalmente tipos simples, excepto ByFrequency, First, DateRange y representativo, que se devuelven como tipos compuestos.

 

Puede usar cualquier columna numérica o de fecha para las agregaciones, y no solo las que se encuentran en la cláusula SELECT. Sin embargo, no se puede agrupar en agregados. Si el argumento de columna pasado no es un tipo numérico o de fecha, se devuelve un error de sintaxis.

La parte de la etiqueta es opcional y proporciona un alias más legible para la etiqueta. Si no incluye una etiqueta de alias, Windows Search transforma el nombre de la función y de la columna en una etiqueta. Por ejemplo, MAX (System.Document. WordCount) se convierte en MAX \_ SystemDocumentWordCount.

## <a name="multi-level-groups-and-counting"></a>Agrupación y recuento de varios niveles

Los agregados se definen en hojas y se duplican. Un agregado toma como entrada las hojas del grupo que lo define (documentos), en lugar de los subgrupos de sus elementos secundarios. Esta funcionalidad se conoce como agrupación de varios niveles.

Además de los agregados que se definen en hojas y duplicados, se cuentan solo una vez. Aunque el mismo documento puede representarse varias veces en un grupo, los agregados solo lo considerarían una vez. En el siguiente gráfico se ilustra este concepto.

![diagrama que muestra que los agregados se definen en hojas y se duplican, y se cuentan solo una vez](images/aggregates.png)

## <a name="aggregate-examples"></a>Ejemplos de agregado

A continuación se muestran ejemplos de funciones de agregado dentro de la cláusula GROUP ON:


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a>Valor devuelto

El valor devuelto es una variante que se encuentra en el conjunto de filas como una propiedad personalizada, ya sea como alias especificados o como "agregados" si no se especifica ninguna etiqueta de alias.

 

 



