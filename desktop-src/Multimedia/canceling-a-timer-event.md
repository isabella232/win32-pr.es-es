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
# <a name="canceling-a-timer-event"></a><span data-ttu-id="f511e-109">Cancelar un evento de temporizador</span><span class="sxs-lookup"><span data-stu-id="f511e-109">Canceling a Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="f511e-110">En este tema se describe una función obsoleta.</span><span class="sxs-lookup"><span data-stu-id="f511e-110">This topic describes an obsolete function.</span></span> <span data-ttu-id="f511e-111">Las nuevas aplicaciones deben usar la función [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para crear temporizadores.</span><span class="sxs-lookup"><span data-stu-id="f511e-111">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="f511e-112">Para cada temporizador periódico que se crea mediante una llamada a [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), la aplicación debe cancelar el temporizador mediante una llamada a la función [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) antes de liberar la memoria que contiene la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f511e-112">For every periodic timer creating by calling [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), the application must cancel the timer by calling the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function before it frees the memory that contains the callback function.</span></span> <span data-ttu-id="f511e-113">Para cancelar un evento de temporizador, podría llamar a la siguiente función.</span><span class="sxs-lookup"><span data-stu-id="f511e-113">To cancel a timer event, it might call the following function.</span></span>


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a><span data-ttu-id="f511e-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f511e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f511e-115">Usar temporizadores multimedia</span><span class="sxs-lookup"><span data-stu-id="f511e-115">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 