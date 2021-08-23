---
description: Los tipos de contadores de algoritmo de contador pueden calcular velocidades o promedios de bytes para una muestra o durante un período de tiempo para una operación determinada.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmos de contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5568d4df0d1b50fd55a4f9d007d6506cf59a8f67a05885c21d64a6be8812536c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131446"
---
# <a name="counter-algorithm-counter-types"></a>Tipos de contadores de algoritmos de contador

Los tipos de contadores de algoritmo de contador pueden calcular velocidades o promedios de bytes para una muestra o durante un período de tiempo para una operación determinada.

La **propiedad AvgDiskBytesPerTransfer** de la clase [**\_ PerfRawData \_ PerfDisk \_ PhysicalDisk de Win32**](/previous-versions//aa394308(v=vs.85)) usa el tipo de contador \_ PERF AVERAGE \_ BULK. En este caso, la transferencia es la operación y el número acumulado de bytes que se envían son los datos del contador. Para dos muestras cualquiera, dividir la diferencia de bytes acumulados por la diferencia en la acumulación de transferencias producirá el número medio de bytes por transferencia durante el período entre las muestras.

Se proporcionan los siguientes algoritmos de contador:



| CounterType                                                                                              | Descripción                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ AVERAGE \_ BULK Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073874176<br/>       | Número de elementos procesados, de media, durante una operación. Este tipo de contador muestra una proporción de los elementos procesados (como los bytes enviados) con el número de operaciones completadas y requiere una propiedad base con PERF AVERAGE BASE como tipo \_ \_ de contador. |
| [PERF \_ Contador \_ contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 272696320<br/>     | Número medio de operaciones completadas durante cada segundo del intervalo de muestra. .                                                                                                                                                                          |
| [PERF \_ SAMPLE \_ COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864<br/>        | Número medio de operaciones completadas en un segundo. Este tipo de contador requiere una propiedad base con el tipo de contador PERF \_ SAMPLE \_ BASE.                                                                                                                   |
| [PERF \_ COUNTER \_ BULK \_ COUNT Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))272696576<br/> | Número medio de operaciones completadas durante cada segundo del intervalo de muestra. Este tipo de contador es el mismo que el tipo COUNTER de PERF, pero usa campos más grandes \_ para dar cabida a valores \_ mayores.                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contadores de rendimiento wmi](wmi-performance-counter-types.md)
</dt> </dl>

 

