---
title: Escribir una función de devolución de llamada de temporizador
description: Escribir una función de devolución de llamada de temporizador
ms.assetid: 85260b6b-42de-43f4-83b7-94edbf660006
keywords:
- temporizadores multimedia, funciones de devolución de llamada
- temporizadores, funciones de devolución de llamada
- escribir funciones de devolución de llamada de temporizador
- temporizadores multimedia, escribir funciones de devolución de llamada
- timers,writing callback functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b8680fc4d697c33514276276daaa2a4d75577bfbd78fa3caffc7f426ca9d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891785"
---
# <a name="writing-a-timer-callback-function"></a>Escribir una función de devolución de llamada de temporizador

> [!Note]  
> En este tema se describe una función obsoleta. Las nuevas aplicaciones deben usar [**la función CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para crear temporizadores.

 

La siguiente función de devolución de llamada, OneShotTimer, invalida el identificador del evento de temporizador único y llama a una rutina de temporizador para controlar las tareas específicas de la aplicación. Para obtener más información, vea [**TimeProc**](/previous-versions//dd757631(v=vs.85)).


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de temporizadores multimedia](using-multimedia-timers.md)
</dt> </dl>

 

 