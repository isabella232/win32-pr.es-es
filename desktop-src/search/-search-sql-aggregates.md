---
description: Una función de agregado realiza un cálculo en un conjunto de valores y devuelve un valor. Esto permite generar estadísticas de resumen para grupos de varios niveles con poca sobrecarga.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Funciones de agregado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47eb73c5208fa5552073ef5cef0e85736cfdf45c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885367"
---
# <a name="aggregate-functions"></a>Funciones de agregado

Una función de agregado realiza un cálculo en un conjunto de valores y devuelve un valor. Esto permite generar estadísticas de resumen para grupos de varios niveles con poca sobrecarga.

## <a name="about-aggregate-functions"></a>Acerca de las funciones de agregado

Las funciones de agregado Windows Search Lenguaje de consulta estructurado (SQL) tienen la sintaxis siguiente:


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



La parte de la función puede incluir cualquiera de las siguientes funciones y sintaxis:



| Función                                                              | Descripción                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AVG( &lt; column &gt; )                                                   | Devuelve el promedio de los valores de un grupo. Solo se aplica a números.                                                                                                                                      |
| BYFREQUENCY( &lt; column , N &gt; &lt; &gt; )                                | Devuelve los valores de columna N más frecuentes de los resultados del grupo. También incluye un recuento del número de veces que se produjo cada valor y los identificadores de documento para los resultados que contienen cada valor devuelto. |
| CHILDCOUNT()                                                          | Devuelve el número de elementos de un grupo (excepto los subgrupos). Si hay varios niveles de agrupación, devuelve el número de grupos secundarios inmediatos.                                                  |
| COUNT()                                                               | Devuelve el número de elementos de un grupo y todos los subgrupos.                                                                                                                                                   |
| DATERANGE( &lt; column &gt; )                                             | Devuelve los límites inferior y superior de los valores de columna que se encuentran en el grupo de resultados del grupo. Solo es válido para las propiedades filetime.                                                                               |
| FIRST( &lt; column , N &gt; &lt; &gt; )                                      | Devuelve los primeros valores de columna N de los resultados hoja encontrados en un grupo.                                                                                                                                       |
| MAX( &lt; column &gt; )                                                   | Devuelve el valor máximo de la expresión. Solo se aplica a números o fechas.                                                                                                                              |
| MIN( &lt; column &gt; )                                                   | Devuelve el valor mínimo de la expresión. Solo se aplica a números o fechas.                                                                                                                              |
| REPRESENTATIVEOF( &lt; column &gt; , &lt; idRepresentative &gt; , N &lt; &gt; ) | Devuelve N valores idRepresentative, cada uno seleccionado de uno de los subconjuntos de resultados que tiene un valor de columna único. Cada valor también se devuelve con un identificador de documento que tiene el valor idRepresentative. |
| SUM( &lt; column &gt; )                                                   | Devuelve la suma de los valores de un grupo. Solo se aplica a números.                                                                                                                                          |



 

 

> [!Note]  
> Los agregados se devuelven como columnas individuales. Son principalmente tipos simples, excepto ByFrequency, First, DateRange y RepresentativeOf, que se devuelven como tipos compuestos.

 

Puede usar cualquier columna numérica o de fecha para las agregaciones, y no solo las que se encuentran en la cláusula SELECT. Sin embargo, no se puede agrupar en agregados. Se devuelve un error de sintaxis si el argumento de columna pasado no es un tipo numérico o de fecha.

La parte de la etiqueta es opcional y proporciona un alias más legible para la etiqueta. Si no incluye una etiqueta de alias, Windows Search transforma la función y el nombre de columna en una etiqueta. Por ejemplo, MAX(System.Document. WordCount) se convierte en MAX \_ SystemDocumentWordCount.

## <a name="multi-level-groups-and-counting"></a>Grupos y recuentos de varios niveles

Los agregados se definen sobre hojas y se duplican. Un agregado toma como entrada las hojas del grupo que lo define (documentos), en lugar de los subgrupos de sus secundarios. Esta funcionalidad se conoce como agrupación de varios niveles.

Además de los agregados que se definen sobre hojas y se duplican, solo se cuentan una vez. Aunque el mismo documento podría representarse varias veces en un grupo, los agregados solo lo considerarían una vez. En el gráfico siguiente se ilustra este concepto.

![diagrama que muestra que los agregados se definen sobre hojas y duplicados, y solo se cuentan una vez](images/aggregates.png)

## <a name="aggregate-examples"></a>Ejemplos agregados

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

El valor devuelto es una variante que se encuentra en el conjunto de filas como una propiedad personalizada, ya sea como alias especificados o como "Agregados" si no se especifica ninguna etiqueta de alias.

 

 



