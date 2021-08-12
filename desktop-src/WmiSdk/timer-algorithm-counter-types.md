---
description: Los tipos de contadores de algoritmo de temporizador se basan en la cantidad de mayor uso del objeto de rendimiento durante un período de ejemplo.
ms.assetid: 4ec49efc-2b0f-4205-8b58-fb121da32b4e
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmos de temporizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e3a606babb005eca7f01f75f735cd6d6a9da29c9c1427c56614c318f9465f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554019"
---
# <a name="timer-algorithm-counter-types"></a>Tipos de contadores de algoritmos de temporizador

Los tipos de contadores de algoritmo de temporizador se basan en la cantidad de mayor uso del objeto de rendimiento durante un período de ejemplo. Los datos del contador son una medida cuántica creciente de la actividad total de un objeto hasta el momento en que se realiza la muestra. La diferencia entre los dos ejemplos indica el tiempo total que el objeto está activo durante el período de tiempo de la muestra.

La división por el período de ejemplo da como resultado una proporción de tiempo que el objeto está activo durante un período de tiempo. La división por el número de interrupciones de sondeo internas determina el uso medio entre las muestras de sondeo.

Por ejemplo, la propiedad **AvgDiskSecPerRead** de la clase [**\_ \_ \_ PhysicalDisk PerfDisk PerfDisk de Win32 PerfRawData**](/previous-versions//aa394308(v=vs.85)) usa el tipo de contador **PERF \_ AVERAGE \_ TIMER.** Calcula el tiempo medio en segundos de una lectura de datos del disco y requiere la propiedad base **AvgDiskSecPerRead \_ Base**. A diferencia de **PERF \_ COUNTER \_ TIMER**, la base de temporizador promedio representa un número acumulado de operaciones y los datos del contador son un valor de tiempo de ejecución, lo que significa que, cuando se divide por la base de tiempo, produce el tiempo total de todas las operaciones en segundos.



| Constante de tipo de contador                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TEMPORIZADOR DE \_ CONTADOR DE RENDIMIENTO \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 541132032<br/>             | Tiempo medio que un componente está activo como porcentaje del tiempo total de la muestra.<br/>                                                                                                                                                                                                                                                                                                         |
| [INV DEL \_ TEMPORIZADOR DE CONTADOR DE \_ \_ RENDIMIENTO](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 557909248<br/>        | Porcentaje medio de tiempo observado durante el intervalo de muestra que el objeto no está activo. Este tipo de contador es el mismo que EL INV DEL TEMPORIZADOR DE **PERF \_ \_ \_ 100NSEC,** salvo que mide el tiempo en unidades de tics del temporizador de rendimiento del sistema en lugar de en unidades de 100ns.<br/>                                                                                                                       |
| [TEMPORIZADOR PROMEDIO DE RENDIMIENTO \_ \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 805438464<br/>             | Tiempo promedio para completar un proceso u operación. Este tipo de contador muestra una proporción del tiempo total transcurrido del intervalo de muestra con el número de procesos u operaciones completados durante ese tiempo.<br/> Este tipo de contador requiere una propiedad base con **PERF \_ AVERAGE \_ BASE** como tipo de contador.<br/>                                                                         |
| [TEMPORIZADOR DE \_ PERF 100NSEC \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 542180608<br/>             | Tiempo activo de un componente como porcentaje del tiempo total transcurrido en unidades de 100ns del intervalo de muestra.<br/>                                                                                                                                                                                                                                                                          |
| [INV \_ del TEMPORIZADOR PERF 100NSEC \_ \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 558957824<br/>        | Porcentaje de tiempo que el objeto no estaba en uso. Este tipo de contador es el mismo que el DE INV del TEMPORIZADOR DE CONTADOR DE **\_ \_ \_ PERF,** salvo que mide el tiempo en unidades de 100ns en lugar de en los tics del temporizador de rendimiento del sistema.<br/>                                                                                                                                                                                   |
| [TEMPORIZADOR MÚLTIPLE \_ DE CONTADOR \_ DE RENDIMIENTO \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 574686464<br/>      | Tiempo activo de uno o varios componentes como porcentaje del tiempo total del intervalo de muestra. Este tipo de contador difiere de **PERF \_ 100NSEC \_ MULTI \_ TIMER** en que mide el tiempo en unidades de tics del temporizador de rendimiento del sistema, en lugar de en unidades de 100ns.<br/> Este tipo de contador requiere una propiedad base con el tipo de contador **\_ PERF COUNTER \_ MULTI \_ BASE.**<br/>        |
| [INV DE \_ VARIOS \_ \_ TEMPORIZADORES DE CONTADOR \_ DE RENDIMIENTO](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 591463680<br/> | Tiempo inactivo de uno o varios componentes como porcentaje del tiempo total del intervalo de muestra. Este tipo de contador difiere de **PERF \_ 100NSEC \_ MULTI TIMER \_ \_ INV** en que mide el tiempo en unidades de tics del temporizador de rendimiento del sistema, en lugar de en unidades de 100ns.<br/> Este tipo de contador requiere una propiedad base con el tipo de contador **\_ PERF COUNTER \_ MULTI \_ BASE.**<br/> |
| [TEMPORIZADOR MÚLTIPLE \_ DE PERF 100NSEC \_ \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 575735040<br/>      | Este tipo de contador muestra el tiempo activo de uno o varios componentes como porcentaje del tiempo total (100ns unidades) del intervalo de muestra.<br/> Este tipo de contador requiere una propiedad base con el tipo de contador **\_ PERF COUNTER \_ MULTI \_ BASE.**<br/>                                                                                                                                     |
| [INV DE VARIOS TEMPORIZADORES DE PERF \_ 100NSEC \_ \_ \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 592512256<br/> | Tiempo inactivo de uno o varios componentes como porcentaje del tiempo total del intervalo de muestra. Los contadores de este tipo miden el tiempo en unidades de 100ns.<br/> Este tipo de contador requiere una propiedad base con el tipo de contador **\_ PERF COUNTER \_ MULTI \_ BASE.**<br/>                                                                                                                          |
| [TEMPORIZADOR DE \_ TIEMPO DE PERF OBJ \_ \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 543229184<br/>           | Temporizador de 64 bits en unidades específicas del objeto.<br/>                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contadores de rendimiento wmi](wmi-performance-counter-types.md)
</dt> </dl>

 

