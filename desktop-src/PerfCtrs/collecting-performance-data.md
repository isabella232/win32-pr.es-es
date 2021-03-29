---
description: Después de crear una consulta y agregarle contadores, llame a la función PdhCollectQueryData para recuperar los datos sin procesar actuales de todos los contadores de la consulta.
ms.assetid: 2534d387-a280-4716-9a9d-3e42f40e2f92
title: Recopilación de datos de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99bd2c0e22553245e87d3844694051c88c57895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360703"
---
# <a name="collecting-performance-data"></a>Recopilación de datos de rendimiento

Después de [crear una consulta](creating-a-query.md) y agregarle contadores, llame a la función [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) para recuperar los datos sin procesar actuales de todos los contadores de la consulta.

Muchos contadores, como los contadores de tasa, requieren dos muestras de datos para calcular un valor de datos con formato. PDH mantiene los datos para el ejemplo actual y el ejemplo recopilado anteriormente. En el procedimiento siguiente se describe cómo recopilar valores de contador que requieren dos ejemplos para calcular un valor que se pueda mostrar.

**Para recopilar valores de contador que requieren dos ejemplos para calcular un valor que se pueda mostrar**

1.  Llame a [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) para recopilar el primer ejemplo.
2.  Llame a la función [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) para esperar un mínimo de un segundo entre las colecciones.
3.  Vuelva a llamar a [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) para recopilar el segundo ejemplo.
4.  Llame a la función [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) para calcular un valor que se pueda mostrar.
5.  Repita los pasos del 2 al 4.

Como alternativa a la implementación de un período de espera, puede llamar a la función [**PdhCollectQueryDataEx**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex) , que crea un subproceso de control de tiempo que espera una cantidad de tiempo especificada, recopila el ejemplo y, a continuación, desencadena un evento definido por la aplicación.

Si desea consultar los datos de rendimiento de un archivo de registro, también puede definir un intervalo de tiempo. El intervalo de tiempo limita la consulta a las muestras que se recopilaron en el intervalo de tiempo (cada muestra contiene una marca de tiempo para el momento en que se recopiló). Para obtener más información sobre cómo establecer y recuperar intervalos de tiempo, vea [establecer un intervalo de tiempo para una consulta](setting-a-time-range-for-a-query.md).

Si desea recopilar datos de rendimiento y escribirlos en un archivo de registro, debe llamar a la función [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) en lugar de llamar a [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata). Para obtener más información, vea [trabajar con archivos de registro](working-with-log-files.md) y [escribir datos de rendimiento en un archivo de registro](writing-performance-data-to-a-log-file.md).

Para obtener más información sobre cómo calcular un valor de ejemplo que se pueda mostrar, vea [Mostrar datos de rendimiento](displaying-performance-data.md).

## <a name="understanding-multiple-processor-counters"></a>Descripción de varios contadores de procesador

Algunos contadores de rendimiento se diseñaron para sistemas de un solo procesador y es posible que no sean precisos para equipos con varios procesadores. Por ejemplo, un proceso está limitado al 100 por ciento de un solo procesador; sin embargo, sus subprocesos pueden usar varios procesadores, con un total superior al 100 por ciento.

El \\ valor del contador "procesador ( \_ total) \\ % de tiempo de procesador" es el uso promedio de todos los procesadores. Por ejemplo, si tiene dos procesadores, uno en 100 por ciento y otro en 0 por ciento, este contador informará del 50 por ciento. Por lo tanto, el intervalo está comprendido entre 0 y 100.

El \\ valor del contador "proceso (X) \\ % de tiempo de proceso" es la suma del uso del procesador de todos los subprocesos del proceso X. Por ejemplo, en un equipo con dos procesadores, si un proceso tiene dos subprocesos, uno que ocupa el 75 por ciento de una CPU y otro que toma el 80 por ciento de otra CPU, este contador informará del 155 por ciento. El intervalo de este contador es de 0 a 100 \* ProcessorCount.

* * Windows Server 2003 y Windows XP: * *

Puede recibir valores fuera del intervalo de valores esperado para el uso de la CPU. Para calcular el porcentaje de uso de CPU, PDH necesita dos muestras (cada una con un valor sin formato y una marca de tiempo). Dado que PDH solo usa el nombre de instancia para que coincida con los procesos, a veces puede usar dos ejemplos de diferentes procesos. Por ejemplo, si se muestrean tres procesos y se termina un proceso después del tercer ejemplo, otro proceso se moverá a la ranura que queda anulada por ese proceso terminado. Como resultado, un contador con formato proporcionará un valor incorrecto al dar formato al cuarto ejemplo, porque se está usando el tercer ejemplo del proceso terminado y el cuarto ejemplo del proceso que se ha pasado a la ranura terminada del proceso.

En la tabla siguiente se muestra cómo puede ocurrir esto si se termina un proceso mientras se recopilan los datos. En la tabla se muestran cinco ejemplos de valores de contador para tres instancias del proceso X. Los ejemplos se recopilan en intervalos de un segundo. Después de recopilar el tercer ejemplo, se termina el proceso X en la ranura 1. Cuando termina el proceso X en la ranura 1, el proceso X de la ranura 2 se mueve a la ranura 1. Al recopilar el cuarto ejemplo para el proceso X en la ranura 2, el primer valor es ahora 20 en lugar de 1.000 y el segundo valor es 1.500. Al dar formato al valor del contador, obtendrá 1.480 milisegundos en lugar de los 500 milisegundos esperados. Al dar formato al quinto valor de ejemplo, debe obtener el valor esperado.

| Muestra   | Ranura 0 para el proceso X | Ranura 1 para el proceso X           | Ranura 2 para el proceso X                     |
|----------|----------------------|--------------------------------|------------------------------------------|
| Ejemplo 1 | 0                    | 0                              | 0                                        |
| Ejemplo 2 | 20                   | 10                             | 500                                      |
| Ejemplo 3 | 40                   | 20                             | 1,000                                    |
| Ejemplo 4 | 60                   | 1.500 (desde la ranura 2 anterior) | No es aplicable. Ahora se recopila en la ranura 1. |
| Ejemplo 5 | 80                   | 2\.000                          | No es aplicable. Ahora se recopila en la ranura 1. |



 

 

 
