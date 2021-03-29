---
description: La clase CMsgThread es una clase de subproceso de trabajo que pone en cola las solicitudes al subproceso de cola para su finalización de forma asincrónica.
ms.assetid: 57e50abf-c90d-4c8f-afd8-25f29b6a0376
title: Clase CMsgThread
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
ms.openlocfilehash: 307b24e1563fe0545ee6f9405f9fb53e1b6d61b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806812"
---
# <a name="cmsgthread-class"></a>Clase CMsgThread

La `CMsgThread` clase es una clase de subproceso de trabajo que pone en cola las solicitudes al subproceso de cola para su finalización de forma asincrónica. Para usar esta clase, derive la clase a partir de ella e invalide la función miembro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) . La función miembro **ThreadMessageProc** lleva a cabo cada solicitud. Las funciones de cliente y la función miembro **ThreadMessageProc** deben compartir una definición común de los parámetros en el objeto [**CMsg**](cmsg.md) .

Un mecanismo negociado indica al subproceso de trabajo que se cierre. Normalmente, será un valor del código de mensaje **uMsg** de la clase [**CMsg**](cmsg.md) .

Es una buena idea enviar este mensaje desde el destructor de la clase derivada y llamar a la función miembro [**CMsgThread:: WaitForThreadExit**](cmsgthread-waitforthreadexit.md) antes de completar la destrucción de la clase derivada.



| Miembros de datos protegidos                                    | Descripción                                                                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| m \_ hSem                                                   | Indica un identificador usado para la señalización.                                                                                                |
| \_bloqueo m                                                   | Protege el acceso a las listas.                                                                                                             |
| m \_ lWaiting                                               | Indica la espera de un subproceso libre.                                                                                                  |
| m \_ ThreadQueue                                            | Invalida la función miembro [**CMsgThread:: GetThreadMsg**](cmsgthread-getthreadmsg.md) y se bloquea en otras cosas que no sean esta cola. |
| Funciones de miembro                                          | Descripción                                                                                                                           |
| [**CMsgThread**](cmsgthread-cmsgthread.md)               | Construye un objeto **CMsgThread** .                                                                                                   |
| [**CreateThread**](cmsgthread-createthread.md)           | Crea un subproceso.                                                                                                                     |
| [**GetThreadHandle**](cmsgthread-getthreadhandle.md)     | Recupera el identificador del subproceso.                                                                                                          |
| [**GetThreadID**](cmsgthread-getthreadid.md)             | Recupera el identificador del subproceso.                                                                                               |
| [**GetThreadPriority**](cmsgthread-getthreadpriority.md) | Recupera la prioridad actual del subproceso.                                                                                                |
| [**PutThreadMsg**](cmsgthread-putthreadmsg.md)           | Pone en cola una solicitud de ejecución por parte del subproceso de trabajo.                                                                                  |
| [**ResumeThread**](cmsgthread-resumethread.md)           | Continúa la operación del subproceso de trabajo.                                                                                         |
| [**SetThreadPriority**](cmsgthread-setthreadpriority.md) | Establece la prioridad del subproceso en un nuevo valor.                                                                                       |
| [**SuspendThread**](cmsgthread-suspendthread.md)         | Suspende la operación de un subproceso en ejecución.                                                                                           |
| [**WaitForThreadExit**](cmsgthread-waitforthreadexit.md) | Se bloquea hasta que el subproceso termina después de una llamada a la función miembro [**CMsgThread:: SuspendThread**](cmsgthread-suspendthread.md) . |
| Funciones miembro reemplazables                              | Descripción                                                                                                                           |
| [**GetThreadMsg**](cmsgthread-getthreadmsg.md)           | Recupera un objeto [**CMsg**](cmsg.md) en cola que contiene una solicitud.                                                                  |
| [**OnThreadInit**](cmsgthread-onthreadinit.md)           | Proporciona la inicialización en un subproceso.                                                                                                  |
| [**ThreadMessageProc**](cmsgthread-threadmessageproc.md) | Procesa las solicitudes. Se trata de una función miembro virtual pura.                                                                           |



 

 

 



