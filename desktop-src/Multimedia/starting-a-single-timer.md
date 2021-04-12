---
title: Iniciar un evento de temporizador único
description: Iniciar un evento de temporizador único
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- temporizadores multimedia, eventos
- temporizadores, eventos
- temporizadores multimedia, eventos de inicio
- temporizadores, eventos de inicio
- timeSetEvent función)
- iniciar eventos de temporizador
- eventos de temporizador único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9d0024e3dfa9b0bda79f209abd9b81e89ad11c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420592"
---
# <a name="starting-a-single-timer-event"></a><span data-ttu-id="8a2e2-110">Iniciar un evento de temporizador único</span><span class="sxs-lookup"><span data-stu-id="8a2e2-110">Starting a Single Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="8a2e2-111">En este tema se describe una función obsoleta.</span><span class="sxs-lookup"><span data-stu-id="8a2e2-111">This topic describes an obsolete function.</span></span> <span data-ttu-id="8a2e2-112">Las nuevas aplicaciones deben usar la función [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para crear temporizadores.</span><span class="sxs-lookup"><span data-stu-id="8a2e2-112">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="8a2e2-113">Para iniciar un evento de temporizador único, llame a la función [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) , especificando la cantidad de tiempo antes de que se produzca la devolución de llamada, la resolución, la dirección de la función de devolución de llamada (vea [**TimeProc**](/previous-versions//dd757631(v=vs.85))) y los datos de usuario que se suministrarán con la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8a2e2-113">To start a single timer event, call the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function, specifying the amount of time before the callback occurs, the resolution, the address of the callback function (see [**TimeProc**](/previous-versions//dd757631(v=vs.85))), and the user data to supply with the callback function.</span></span> <span data-ttu-id="8a2e2-114">Una aplicación puede utilizar una función como la siguiente para iniciar un evento de temporizador único.</span><span class="sxs-lookup"><span data-stu-id="8a2e2-114">An application can use a function like the following to start a single timer event.</span></span>


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



<span data-ttu-id="8a2e2-115">Para obtener un ejemplo de la función de devolución de llamada OneShotCallback, vea [escribir una función de devolución de llamada de temporizador](writing-a-timer-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="8a2e2-115">For an example of the callback function OneShotCallback, see [Writing a Timer Callback Function](writing-a-timer-callback-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a2e2-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a2e2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a2e2-117">Usar temporizadores multimedia</span><span class="sxs-lookup"><span data-stu-id="8a2e2-117">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 