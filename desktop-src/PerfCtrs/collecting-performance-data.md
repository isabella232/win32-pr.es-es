---
description: Después de crear una consulta y agregarle contadores, llame a la función PdhCollectQueryData para recuperar los datos sin procesar actuales de todos los contadores de la consulta.
ms.assetid: 2534d387-a280-4716-9a9d-3e42f40e2f92
title: Recopilación de datos de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99bd2c0e22553245e87d3844694051c88c57895
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073901"
---
# <a name="collecting-performance-data"></a>Recopilación de datos de rendimiento

Después [de crear una](creating-a-query.md) consulta y agregarle contadores, llame a la función [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) para recuperar los datos sin procesar actuales de todos los contadores de la consulta.

Muchos contadores, como los contadores de velocidad, requieren dos ejemplos de datos para calcular un valor de datos con formato. PDH mantiene los datos para el ejemplo actual y el ejemplo recopilado previamente. En el procedimiento siguiente se describe cómo recopilar valores de contador que requieren dos muestras para calcular un valor que se puede mostrar.

**Para recopilar valores de contador que requieren dos muestras para calcular un valor que se puede mostrar**

1.  Llame [**a PdhCollectQueryData para**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) recopilar el primer ejemplo.
2.  Llame a [**la función Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) para esperar un mínimo de un segundo entre colecciones.
3.  Llame [**de nuevo a PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) para recopilar el segundo ejemplo.
4.  Llame a [**la función PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) para calcular un valor que se puede mostrar.
5.  Repita los pasos del 2 al 4.

Como alternativa a la implementación de un período de espera, puede llamar a la función [**PdhCollectQueryDataEx,**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex) que crea un subproceso de tiempo que espera una cantidad de tiempo especificada, recopila el ejemplo y, a continuación, desencadena un evento definido por la aplicación.

Si desea consultar datos de rendimiento desde un archivo de registro, también puede definir un intervalo de tiempo. El intervalo de tiempo limita la consulta a las muestras recopiladas dentro del intervalo de tiempo (cada muestra contiene una marca de tiempo para cuando se recopiló). Para obtener más información sobre cómo establecer y recuperar intervalos de tiempo, vea [Establecer un intervalo de tiempo para una consulta](setting-a-time-range-for-a-query.md).

Si desea recopilar datos de rendimiento y escribir en un archivo de registro, llamaría a la función [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) en lugar de llamar a [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata). Para obtener más información, vea [Trabajar con archivos de registro y](working-with-log-files.md) Escribir datos de rendimiento en un archivo de [registro.](writing-performance-data-to-a-log-file.md)

Para obtener más información sobre cómo calcular un valor de ejemplo que se puede mostrar, vea [Mostrar datos de rendimiento.](displaying-performance-data.md)

## <a name="understanding-multiple-processor-counters"></a>Descripción de varios contadores de procesador

Algunos contadores de rendimiento se diseñaron para sistemas de procesador único y es posible que no sean precisos para equipos con varios procesadores. Por ejemplo, un proceso se limita al 100 % de un único procesador; sin embargo, sus subprocesos pueden usar varios procesadores, lo que suma más del 100 %.

El valor \\ del contador \_ "Processor( Total) % Processor Time" es \\ el uso medio de todos los procesadores. Por ejemplo, si tiene dos procesadores, uno al 100 por ciento y otro al 0 por ciento, este contador informará del 50 por ciento. Por lo tanto, el intervalo está entre 0 y 100.

El valor \\ del contador "Process(X) % Process Time" es la suma del uso del procesador por todos los subprocesos \\ del proceso X. Por ejemplo, en un equipo con dos procesadores, si un proceso tiene dos subprocesos, uno que toma el 75 % de una CPU y el otro que toma el 80 % de otra CPU, este contador informará del 155 %. El intervalo de este contador está entre 0 y 100 \* ProcessorCount.

**Windows Server 2003 y Windows XP: **

Puede recibir valores fuera del intervalo esperado de valores para el uso de CPU. Para calcular el porcentaje de uso de CPU, PDH necesita dos muestras (cada una con un valor sin procesar y una marca de tiempo). Dado que PDH solo usa el nombre de instancia para coincidir con los procesos, a veces puede usar dos ejemplos de procesos diferentes. Por ejemplo, si se muestrea tres procesos y un proceso finaliza después de la tercera muestra, otro proceso se moverá a la ranura que ese proceso final ha anulado. Como resultado, un contador con formato proporcionará un valor incorrecto al dar formato a la cuarta muestra, ya que usa la tercera muestra del proceso finalizado y la cuarta muestra del proceso que se movió a la ranura del proceso finalizado.

En la tabla siguiente se muestra cómo puede ocurrir esto si un proceso finaliza mientras se recopilan datos. En la tabla se muestran cinco ejemplos de valores de contador para tres instancias del proceso X. Las muestras se recopilan en intervalos de un segundo. Una vez recopilada la tercera muestra, finaliza el proceso X en la ranura 1. Cuando finaliza el proceso X en la ranura 1, el proceso X de la ranura 2 se mueve a la ranura 1. Cuando se recopila el cuarto ejemplo para el proceso X en la ranura 2, el primer valor es ahora 20 en lugar de 1000 y el segundo valor es 1500. Al dar formato al valor del contador, obtiene 1480 milisegundos en lugar de los 500 milisegundos esperados. Al dar formato al quinto valor de ejemplo, debería obtener el valor esperado.

| Muestra   | Ranura 0 para el proceso X | Ranura 1 para el proceso X           | Ranura 2 para el proceso X                     |
|----------|----------------------|--------------------------------|------------------------------------------|
| Ejemplo 1 | 0                    | 0                              | 0                                        |
| Ejemplo 2 | 20                   | 10                             | 500                                      |
| Ejemplo 3 | 40                   | 20                             | 1,000                                    |
| Ejemplo 4 | 60                   | 1500 (desde la ranura 2 anterior) | No aplicable. Ahora se recopilan en la ranura 1. |
| Ejemplo 5 | 80                   | 2\.000                          | No aplicable. Ahora se recopilan en la ranura 1. |



 

 

 
