---
title: Cancelar un evento de temporizador
description: Cancelar un evento de temporizador
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- temporizadores multimedia, eventos
- timers,events
- función timeKillEvent
- cancelación de eventos de temporizador
- temporizadores multimedia, cancelación de eventos
- timers,cancelling events
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1380b2868596e0177e806f5df5217bb839abe61c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370975"
---
# <a name="canceling-a-timer-event"></a>Cancelar un evento de temporizador

> [!Note]  
> En este tema se describe una función obsoleta. Las nuevas aplicaciones deben usar [**la función CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para crear temporizadores.

 

Para cada temporizador periódico que se crea mediante una llamada [**a timeSetEvent**](/previous-versions//dd757634(v=vs.85)), la aplicación debe cancelar el temporizador llamando a la función [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) antes de liberar la memoria que contiene la función de devolución de llamada. Para cancelar un evento de temporizador, podría llamar a la siguiente función.


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de temporizadores multimedia](using-multimedia-timers.md)
</dt> </dl>

 

 