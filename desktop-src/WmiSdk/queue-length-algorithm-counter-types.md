---
description: Los tipos de contadores del algoritmo de longitud de cola aumentan el número de elementos de una cola en cada intervalo de muestra según se especifica en la propiedad de frecuencia adecuada&\# 8212; Frequency \_ PerfTime, etc.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Tipos de contador del algoritmo de longitud de cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06665c2fb8fca014c7d722f0ea22cf7e86833ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276150"
---
# <a name="queue-length-algorithm-counter-types"></a>Tipos de contador del algoritmo de longitud de cola

Los tipos de contadores del algoritmo de longitud de cola aumentan el número de elementos de una cola en cada intervalo de muestra según lo especificado por la frecuencia de propiedad de frecuencia adecuada \_ PerfTime, etc. El resultado cocido divide el número de muestras para generar la longitud media de la cola.

Un ejemplo es la propiedad **AvgDiskQueueLength** en el [**PerfRawData de Win32 de Win32 \_ \_ \_**](./retrieving-raw-and-formatted-performance-data.md) que usa el \_ tipo de \_ contador Perf \_ QUEUELEN \_ Type.



| Contratipo (constante)                                                                                                 | Descripción                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rendimiento \_ de COUNTER \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4523008<br/>            | Promedio de longitud de una cola a un recurso a lo largo del tiempo. Muestra la diferencia entre las longitudes de cola observadas durante los dos últimos intervalos de muestra, dividida por la duración del intervalo.                       |
| [Rendimiento \_ de COUNTER \_ Large \_ QUEUELEN \_ Type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4523264<br/>     | Promedio de longitud de una cola a un recurso a lo largo del tiempo. Los contadores de este tipo muestran la diferencia entre las longitudes de cola observadas durante los dos últimos intervalos de muestra, dividida por la duración del intervalo. |
| [Rendimiento \_ de CONTADOR de \_ 100 NS \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 5571840<br/>     | Promedio de longitud de una cola a un recurso a lo largo del tiempo en unidades de 100 nanosegundos.                                                                                                                                        |
| [Rendimiento \_ de COUNTER \_ obj \_ Time \_ QUEUELEN \_ Type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 6620416<br/> | Hora en la que un objeto está en una cola.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

