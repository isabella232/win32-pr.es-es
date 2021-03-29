---
title: Cancelar un evento de temporizador
description: Cancelar un evento de temporizador
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- temporizadores multimedia, eventos
- temporizadores, eventos
- timeKillEvent función)
- Cancelando eventos de temporizador
- temporizadores multimedia, cancelar eventos
- temporizadores, cancelar eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1380b2868596e0177e806f5df5217bb839abe61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077715"
---
# <a name="canceling-a-timer-event"></a>Cancelar un evento de temporizador

> [!Note]  
> En este tema se describe una función obsoleta. Las nuevas aplicaciones deben usar la función [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para crear temporizadores.

 

Para cada temporizador periódico que se crea mediante una llamada a [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), la aplicación debe cancelar el temporizador mediante una llamada a la función [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) antes de liberar la memoria que contiene la función de devolución de llamada. Para cancelar un evento de temporizador, podría llamar a la siguiente función.


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

[Usar temporizadores multimedia](using-multimedia-timers.md)
</dt> </dl>

 

 