---
description: Los tipos de contador del algoritmo del temporizador se basan en la cantidad de uso mayor del objeto de rendimiento durante un período de ejemplo.
ms.assetid: 4ec49efc-2b0f-4205-8b58-fb121da32b4e
ms.tgt_platform: multiple
title: Tipos de contadores del algoritmo Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee815e6740c8736d0a7f2194b25e521368bbe96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707345"
---
# <a name="timer-algorithm-counter-types"></a>Tipos de contadores del algoritmo Timer

Los tipos de contador del algoritmo del temporizador se basan en la cantidad de uso mayor del objeto de rendimiento durante un período de ejemplo. Los datos del contador son una medida Quantum creciente de la actividad total de un objeto hasta el momento en que se produce el ejemplo. La diferencia entre los dos ejemplos indica el tiempo total que el objeto está activo durante el período de tiempo de ejemplo.

La división por el período de ejemplo da lugar a una proporción de tiempo que el objeto está activo durante un período de tiempo. La división por el número de interrupciones de sondeo interno determina el uso medio entre los ejemplos de sondeo.

Por ejemplo, la propiedad **AvgDiskSecPerRead** de la clase [**Win32 \_ PerfRawData \_ perfdisk \_ DiscoFísico**](/previous-versions//aa394308(v=vs.85)) usa el tipo de valor de **\_ \_ temporizador de promedio de rendimiento** . Calcula el tiempo medio en segundos de una lectura de datos del disco y requiere la propiedad base **AvgDiskSecPerRead \_ base**. A diferencia **del \_ \_ temporizador de contadores de rendimiento**, la base del temporizador promedio representa un número acumulado de operaciones y los datos del contador son un valor de tiempo de ejecución, lo que significa que, cuando se divide por la base de tiempo, produce el tiempo total de todas las operaciones en segundos.



| Constante de tipo de contador                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_temporizador de contadores de rendimiento \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 541132032<br/>             | Promedio de tiempo que un componente está activo como un porcentaje del tiempo total de muestra.<br/>                                                                                                                                                                                                                                                                                                         |
| [\_ \_ INV del contador de rendimiento \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 557909248<br/>        | Porcentaje medio de tiempo observado durante el intervalo de muestra en el que el objeto no está activo. Este tipo de contador es el mismo que el del **\_ temporizador de 100NSEC \_ \_** de rendimiento, salvo que mide el tiempo en unidades de pasos del temporizador de rendimiento del sistema en lugar de en unidades de 100 NS.<br/>                                                                                                                       |
| [\_temporizador de promedio de rendimiento \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 805438464<br/>             | Promedio de tiempo para completar un proceso u operación. Este tipo de contador muestra la relación entre el tiempo total transcurrido del intervalo de muestra y el número de procesos u operaciones completadas durante ese tiempo.<br/> Este tipo de contador requiere una propiedad base con el **promedio de rendimiento \_ \_ base** como el tipo de contador.<br/>                                                                         |
| [\_Temporizador de 100NSEC de rendimiento \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 542180608<br/>             | Tiempo activo de un componente como un porcentaje del tiempo total transcurrido en unidades de 100 ns del intervalo de ejemplo.<br/>                                                                                                                                                                                                                                                                          |
| [\_INV 100NSEC \_ del temporizador \_ de rendimiento](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 558957824<br/>        | Porcentaje de tiempo que el objeto no estaba en uso. Este tipo de contador es igual que **el \_ temporizador de contadores \_ \_** de rendimiento, salvo que mide el tiempo en unidades de 100 NS en lugar de TICs del temporizador de rendimiento del sistema.<br/>                                                                                                                                                                                   |
| [contador de rendimiento de \_ \_ varios \_ temporizadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 574686464<br/>      | Tiempo activo de uno o más componentes como un porcentaje del tiempo total del intervalo de muestra. Este tipo de contador se diferencia **del \_ \_ \_ temporizador múltiple de Perf 100NSEC** en que mide el tiempo en unidades de pasos del temporizador de rendimiento del sistema, en lugar de en unidades de 100 NS.<br/> Este tipo de contador requiere una propiedad base con el tipo de contador de **\_ \_ \_ base múltiple de contador de rendimiento** .<br/>        |
| [contador de rendimiento de \_ \_ varios \_ temporizadores \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 591463680<br/> | Tiempo de inactividad de uno o más componentes como un porcentaje del tiempo total del intervalo de muestra. Este tipo de contador se diferencia de la **\_ \_ inv de varios \_ temporizadores \_ de rendimiento 100NSEC** en que mide el tiempo en unidades de pasos del temporizador de rendimiento del sistema, en lugar de en unidades de 100 NS.<br/> Este tipo de contador requiere una propiedad base con el tipo de contador de **\_ \_ \_ base múltiple de contador de rendimiento** .<br/> |
| [\_ \_ Temporizador múltiple de rendimiento 100NSEC \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 575735040<br/>      | Este tipo de contador muestra el tiempo activo de uno o más componentes como un porcentaje del tiempo total (unidades de 100 NS) del intervalo de muestra.<br/> Este tipo de contador requiere una propiedad base con el tipo de contador de **\_ \_ \_ base múltiple de contador de rendimiento** .<br/>                                                                                                                                     |
| [\_Inv de \_ \_ temporizador múltiple \_ de rendimiento 100NSEC](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 592512256<br/> | Tiempo de inactividad de uno o más componentes como un porcentaje del tiempo total del intervalo de muestra. Los contadores de este tipo miden el tiempo en unidades de 100 NS.<br/> Este tipo de contador requiere una propiedad base con el tipo de contador de **\_ \_ \_ base múltiple de contador de rendimiento** .<br/>                                                                                                                          |
| [\_temporizador de \_ tiempo de Perf \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 543229184<br/>           | Un temporizador de 64 bits en unidades específicas del objeto.<br/>                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

