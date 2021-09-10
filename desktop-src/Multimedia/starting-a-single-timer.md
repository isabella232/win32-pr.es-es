---
title: Iniciar un evento de temporizador único
description: Iniciar un evento de temporizador único
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- temporizadores multimedia, eventos
- timers,events
- temporizadores multimedia, eventos de inicio
- timers,starting events
- función timeSetEvent
- eventos de temporizador de inicio
- eventos de temporizador único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9d0024e3dfa9b0bda79f209abd9b81e89ad11c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370976"
---
# <a name="starting-a-single-timer-event"></a>Iniciar un evento de temporizador único

> [!Note]  
> En este tema se describe una función obsoleta. Las nuevas aplicaciones deben usar [**la función CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para crear temporizadores.

 

Para iniciar un evento de temporizador único, llame a la función [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) y especifique la cantidad de tiempo antes de que se produzca la devolución de llamada, la resolución, la dirección de la función de devolución de llamada (vea [**TimeProc)**](/previous-versions//dd757631(v=vs.85))y los datos de usuario que se suministrarán con la función de devolución de llamada. Una aplicación puede usar una función como la siguiente para iniciar un evento de temporizador único.


```C++
UINT SetTimerCallback(NPSEQ npSeq,  // sequencer data
    UINT msInterval)                // event interval
{ 
    npSeq->wTimerID = timeSetEvent(
        msInterval,                    // delay
        wTimerRes,                     // resolution (global variable)
        OneShotCallback,               // callback function
        (DWORD)npSeq,                  // user data
        TIME_ONESHOT );                // single timer event
    if(! npSeq->wTimerID)
        return ERR_TIMER;
    else
        return ERR_NOERROR;
} 

```



Para obtener un ejemplo de la función de devolución de llamada OneShotCallback, vea Escribir una función de devolución [de llamada de temporizador.](writing-a-timer-callback-function.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de temporizadores multimedia](using-multimedia-timers.md)
</dt> </dl>

 

 