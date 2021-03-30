---
description: Los tipos de contador del algoritmo de contador pueden calcular las tasas o promedios de bytes para una muestra o un período de tiempo para una operación determinada.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Tipos de contador del algoritmo Counter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bd55a2a9cc9cc9193a86ffe740ebfa856c0ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360948"
---
# <a name="counter-algorithm-counter-types"></a>Tipos de contador del algoritmo Counter

Los tipos de contador del algoritmo de contador pueden calcular las tasas o promedios de bytes para una muestra o un período de tiempo para una operación determinada.

La propiedad **AvgDiskBytesPerTransfer** de la clase [**Win32 \_ PerfRawData \_ perfdisk \_ DiscoFísico**](/previous-versions//aa394308(v=vs.85)) usa el tipo de valor medio de la media de rendimiento \_ \_ . En este caso, la transferencia es la operación y el número acumulado de bytes que se envían son los datos del contador. En el caso de dos muestras cualesquiera, la división de la diferencia de los bytes acumulados por la diferencia en el acumulado de transferencias producirá el número promedio de bytes por transferencia durante el período de tiempo entre los ejemplos.

Se proporcionan los siguientes algoritmos de contador:



| Tipo                                                                                              | Descripción                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rendimiento \_ de PROMEDIO \_ ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))de Decimal bulk 1073874176<br/>       | Número de elementos procesados, como promedio, durante una operación. Este tipo de contador muestra la relación entre los elementos procesados (por ejemplo, bytes enviados) y el número de operaciones completadas, y requiere una propiedad base con \_ el promedio de rendimiento \_ base como el tipo de contador. |
| [Rendimiento \_ de Contador \_ Decimal 272696320](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/>     | Número promedio de operaciones completadas durante cada segundo del intervalo de ejemplo. .                                                                                                                                                                          |
| [Rendimiento \_ de EJEMPLO de \_ contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4260864<br/>        | Número promedio de operaciones completadas en un segundo. Este tipo de contador requiere una propiedad base con el tipo de contador base de ejemplo de rendimiento \_ \_ .                                                                                                                   |
| [Rendimiento \_ de CONTADOR \_ de \_ recuento](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 272696576<br/> | Número promedio de operaciones completadas durante cada segundo del intervalo de ejemplo. Este tipo de contador es igual que el \_ tipo de contador de contadores de rendimiento \_ , pero utiliza campos de mayor tamaño para acomodar valores mayores.                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

