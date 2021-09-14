---
description: Representa las diferencias entre las muestras a lo largo del tiempo y, a menudo, usa un valor base para el cálculo.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmos básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073070"
---
# <a name="basic-algorithm-counter-types"></a>Tipos de contadores de algoritmos básicos

Los tipos de contadores de algoritmos básicos suelen representar diferencias entre las muestras a lo largo del tiempo y, a menudo, usan un valor base para el cálculo. Por ejemplo, la propiedad **PercentFreeSpace** de la clase [**\_ \_ \_ PhysicalDisk PerfDisk PerfDisk de Win32 Representa**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) la proporción del espacio disponible en la unidad de disco físico con respecto al espacio total utilizable proporcionado por la unidad de disco físico seleccionada. Esta clase también contiene el valor base, **PercentFreeSpace \_ Base.** El porcentaje de espacio libre en disco se obtiene dividiendo **PercentFreeSpace** por **PercentFreeSpace \_ Base** y multiplicando por 100 %.

Se proporcionan los algoritmos básicos de la tabla siguiente.



| CounterType (constante)                                                                                    | Descripción                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ RAW \_ FRACTION Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))537003008<br/>       | Proporción de un subconjunto con respecto a su conjunto como porcentaje. Este tipo de contador muestra solo el porcentaje actual, no un promedio a lo largo del tiempo.                                    |
| [PERF \_ SAMPLE \_ FRACTION Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))549585920<br/>    | Proporción media de aciertos con todas las operaciones durante los dos últimos intervalos de muestra. Este tipo de contador requiere una propiedad base con el tipo de contador \_ PERF SAMPLE \_ BASE. |
| [PERF \_ Counter \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195328<br/>        | Este tipo de contador muestra la variación del atributo que se ha medido entre los dos intervalos de muestra más recientes.                                                         |
| [PERF \_ Contador \_ grande \_ delta decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4195584<br/> | Igual que PERF \_ COUNTER \_ DELTA, pero una representación de 64 bits para valores mayores.                                                                                        |
| [PERF \_ TIEMPO \_ TRANSCURRIDO Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))807666944<br/>       | Tiempo total entre el momento en que se inició el proceso y el momento en que se calcula este valor.                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contadores de rendimiento wmi](wmi-performance-counter-types.md)
</dt> </dl>

 

