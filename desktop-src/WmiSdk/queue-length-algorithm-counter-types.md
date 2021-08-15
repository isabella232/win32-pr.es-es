---
description: Los tipos de contadores de algoritmos de longitud de cola incrementan el número de elementos de una cola en cada intervalo de muestra según lo especificado por la propiedad frequency adecuada&\# 8212; Frequency \_ PerfTime, y así sucesivamente.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmo de longitud de cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9fd3019e9a5e7150402266fd206d3f460f3d0ae3b07f4c6c7d51e82473e9dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316542"
---
# <a name="queue-length-algorithm-counter-types"></a>Tipos de contadores de algoritmo de longitud de cola

Los tipos de contadores de algoritmos de longitud de cola incrementan el número de elementos de una cola en cada intervalo de muestra según lo especificado por la propiedad frequency adecuada Frequency \_ PerfTime, y así sucesivamente. El resultado preparado divide por el número de muestras para generar la longitud media de la cola.

Un ejemplo es la propiedad **AvgDiskQueueLength** del disco lógico [**\_ PerfRawData \_ PerfDisk \_ de Win32**](./retrieving-raw-and-formatted-performance-data.md) que usa el tipo de contador \_ PERF COUNTER \_ 100NS \_ QUEUELEN \_ TYPE.



| CounterType (Constante)                                                                                                 | Descripción                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ COUNTER \_ QUEUELEN \_ TYPE Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4523008<br/>            | Longitud media de una cola a un recurso a lo largo del tiempo. Muestra la diferencia entre las longitudes de cola observadas durante los dos últimos intervalos de muestra, dividida por la duración del intervalo.                       |
| [PERF \_ COUNTER \_ LARGE \_ QUEUELEN TYPE \_ Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4523264<br/>     | Longitud media de una cola a un recurso a lo largo del tiempo. Los contadores de este tipo muestran la diferencia entre las longitudes de cola observadas durante los dos últimos intervalos de muestra, dividida por la duración del intervalo. |
| [PERF \_ COUNTER \_ 100NS \_ QUEUELEN \_ TYPE Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))5571840<br/>     | Longitud media de una cola a un recurso a lo largo del tiempo en unidades de 100 nanosegundos.                                                                                                                                        |
| [PERF \_ COUNTER \_ OBJ \_ TIME \_ QUEUELEN TYPE \_ Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))6620416<br/> | Hora en que un objeto está en una cola.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contadores de rendimiento wmi](wmi-performance-counter-types.md)
</dt> </dl>

 

