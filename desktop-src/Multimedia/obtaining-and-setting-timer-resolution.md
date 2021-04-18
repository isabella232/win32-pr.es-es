---
title: Obtener y establecer la resolución del temporizador
description: Obtener y establecer la resolución del temporizador
ms.assetid: 237a6770-89b9-4922-b9e9-0e0bf3e0c9b6
keywords:
- temporizadores multimedia, resolución
- temporizadores, resolución
- resolución mínima del temporizador
- resolución máxima del temporizador
- temporizadores multimedia, resolución máxima
- temporizadores, resolución máxima
- temporizadores multimedia, resolución mínima
- temporizadores, resolución mínima
- timeGetDevCaps función)
- timeBeginPeriod función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5feca59e6fb4c528d6042b00eb7aa23263245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685520"
---
# <a name="obtaining-and-setting-timer-resolution"></a>Obtener y establecer la resolución del temporizador

En el ejemplo siguiente se llama a la función [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) para determinar las resoluciones de temporizador mínima y máxima admitidas por los servicios del temporizador. Antes de configurar los eventos de temporizador, en el ejemplo se establece la resolución mínima del temporizador mediante la función [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) .


```C++
#define TARGET_RESOLUTION 1         // 1-millisecond target resolution

TIMECAPS tc;
UINT     wTimerRes;

if (timeGetDevCaps(&tc, sizeof(TIMECAPS)) != TIMERR_NOERROR) 
{
    // Error; application can't continue.
}

wTimerRes = min(max(tc.wPeriodMin, TARGET_RESOLUTION), tc.wPeriodMax);
timeBeginPeriod(wTimerRes); 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar temporizadores multimedia](using-multimedia-timers.md)
</dt> </dl>

 

 




