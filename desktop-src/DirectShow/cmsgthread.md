---
description: La clase CMsgThread es una clase de subproceso de trabajo que pone en cola las solicitudes al subproceso de cola para su finalización asincrónica.
ms.assetid: 57e50abf-c90d-4c8f-afd8-25f29b6a0376
title: CMsgThread (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread
api_type:
- COM
api_location: ''
ms.openlocfilehash: 021683808900a7265f4708dae0bb29ff6d07f6619430ed5687eb77d5e2332a3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813705"
---
# <a name="cmsgthread-class"></a>CMsgThread (clase)

La clase es una clase de subproceso de trabajo que pone en cola las solicitudes al subproceso de cola para `CMsgThread` su finalización asincrónica. Para usar esta clase, derive la clase de ella e invalide la función miembro [**CMsgThread::ThreadMessageProc.**](cmsgthread-threadmessageproc.md) La **función miembro ThreadMessageProc** lleva a cabo cada solicitud. Las funciones de cliente y la **función miembro ThreadMessageProc** deben compartir una definición común de los parámetros en el [**objeto CMsg.**](cmsg.md)

Un mecanismo negociado indica al subproceso de trabajo que salga. Normalmente, este será un valor del código de mensaje uMsg de la **clase CMsg.** [](cmsg.md)

Es una buena idea enviar este mensaje desde el destructor de la clase derivada y llamar a la función miembro [**CMsgThread::WaitForThreadExit**](cmsgthread-waitforthreadexit.md) antes de completar la destrucción de la clase derivada.



| Miembros de datos protegidos                                    | Descripción                                                                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| m \_ hSem                                                   | Indica un identificador usado para la señalización.                                                                                                |
| m \_ Lock                                                   | Protege el acceso a las listas.                                                                                                             |
| m \_ lWaiting                                               | Indica la espera de un subproceso libre.                                                                                                  |
| m \_ ThreadQueue                                            | Invalida la función [**miembro CMsgThread::GetThreadMsg**](cmsgthread-getthreadmsg.md) y se bloquea en elementos distintos de esta cola. |
| Funciones de miembro                                          | Descripción                                                                                                                           |
| [**CMsgThread**](cmsgthread-cmsgthread.md)               | Construye un **objeto CMsgThread.**                                                                                                   |
| [**CreateThread**](cmsgthread-createthread.md)           | Crea un subproceso.                                                                                                                     |
| [**GetThreadHandle**](cmsgthread-getthreadhandle.md)     | Recupera el identificador del subproceso.                                                                                                          |
| [**GetThreadID**](cmsgthread-getthreadid.md)             | Recupera el identificador del subproceso.                                                                                               |
| [**GetThreadPriority**](cmsgthread-getthreadpriority.md) | Recupera la prioridad del subproceso actual.                                                                                                |
| [**PutThreadMsg**](cmsgthread-putthreadmsg.md)           | Pone en cola una solicitud de ejecución por parte del subproceso de trabajo.                                                                                  |
| [**ResumeThread**](cmsgthread-resumethread.md)           | Continúa el funcionamiento del subproceso de trabajo.                                                                                         |
| [**SetThreadPriority**](cmsgthread-setthreadpriority.md) | Establece la prioridad del subproceso en un nuevo valor.                                                                                       |
| [**SuspendThread**](cmsgthread-suspendthread.md)         | Suspende el funcionamiento de un subproceso en ejecución.                                                                                           |
| [**WaitForThreadExit**](cmsgthread-waitforthreadexit.md) | Se bloquea hasta que el subproceso ha salido después de una llamada a la función miembro [**CMsgThread::SuspendThread.**](cmsgthread-suspendthread.md) |
| Funciones miembro reemplazables                              | Descripción                                                                                                                           |
| [**GetThreadMsg**](cmsgthread-getthreadmsg.md)           | Recupera un objeto [**CMsg en**](cmsg.md) cola que contiene una solicitud.                                                                  |
| [**OnThreadInit**](cmsgthread-onthreadinit.md)           | Proporciona la inicialización en un subproceso.                                                                                                  |
| [**ThreadMessageProc**](cmsgthread-threadmessageproc.md) | Procesa las solicitudes. Se trata de una función miembro virtual pura.                                                                           |



 

 

 



