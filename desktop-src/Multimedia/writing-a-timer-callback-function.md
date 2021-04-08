---
title: Escribir una función de devolución de llamada del temporizador
description: Escribir una función de devolución de llamada del temporizador
ms.assetid: 85260b6b-42de-43f4-83b7-94edbf660006
keywords:
- temporizadores multimedia, funciones de devolución de llamada
- temporizadores, funciones de devolución de llamada
- escribir funciones de devolución de llamada del temporizador
- temporizadores multimedia, escribir funciones de devolución de llamada
- temporizadores, escribir funciones de devolución de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609cf2dda455897fb6cae0f3c48252016ba54cb9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995163"
---
# <a name="writing-a-timer-callback-function"></a><span data-ttu-id="c17c4-108">Escribir una función de devolución de llamada del temporizador</span><span class="sxs-lookup"><span data-stu-id="c17c4-108">Writing a Timer Callback Function</span></span>

> [!Note]  
> <span data-ttu-id="c17c4-109">En este tema se describe una función obsoleta.</span><span class="sxs-lookup"><span data-stu-id="c17c4-109">This topic describes an obsolete function.</span></span> <span data-ttu-id="c17c4-110">Las nuevas aplicaciones deben usar la función [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para crear temporizadores.</span><span class="sxs-lookup"><span data-stu-id="c17c4-110">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="c17c4-111">La siguiente función de devolución de llamada, OneShotTimer, invalida el identificador del evento de temporizador único y llama a una rutina de temporizador para controlar las tareas específicas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c17c4-111">The following callback function, OneShotTimer, invalidates the identifier for the single timer event and calls a timer routine to handle the application-specific tasks.</span></span> <span data-ttu-id="c17c4-112">Para obtener más información, vea [**TimeProc**](/previous-versions//dd757631(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c17c4-112">For more information, see [**TimeProc**](/previous-versions//dd757631(v=vs.85)).</span></span>


```C++
void CALLBACK OneShotTimer(UINT wTimerID, UINT msg, 
    DWORD dwUser, DWORD dw1, DWORD dw2) 
{ 
    NPSEQ npSeq;             // pointer to sequencer data 
    npSeq = (NPSEQ)dwUser;
    npSeq->wTimerID = 0;     // invalidate timer ID (no longer in use)
    TimerRoutine(npSeq);     // handle tasks 
} 
```



## <a name="related-topics"></a><span data-ttu-id="c17c4-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c17c4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c17c4-114">Usar temporizadores multimedia</span><span class="sxs-lookup"><span data-stu-id="c17c4-114">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 