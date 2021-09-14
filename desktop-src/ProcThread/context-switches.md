---
description: El programador mantiene una cola de subprocesos ejecutables para cada nivel de prioridad.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Cambios de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161059"
---
# <a name="context-switches"></a>Cambios de contexto

El programador mantiene una cola de subprocesos ejecutables para cada nivel de prioridad. Se conocen como *subprocesos listos.* Cuando un procesador está disponible, el sistema realiza un cambio *de contexto*. Los pasos de un cambio de contexto son:

1.  Guarde el contexto del subproceso que acaba de terminar de ejecutarse.
2.  Coloque el subproceso que acaba de terminar de ejecutarse al final de la cola para su prioridad.
3.  Busque la cola de prioridad más alta que contiene subprocesos listos.
4.  Quite el subproceso en el centro de la cola, cargue su contexto y ejectílo.

Las siguientes clases de subprocesos no son subprocesos listos.

-   Subprocesos creados con la marca CREATE \_ SUSPENDED
-   Subprocesos detenidos durante la ejecución [**con las funciones SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) [**o SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)
-   Subprocesos que esperan un objeto de sincronización o una entrada.

Hasta que los subprocesos suspendidos o bloqueados estén listos para ejecutarse, el programador no les asigna tiempo de procesador, independientemente de su prioridad.

Las razones más comunes para un cambio de contexto son:

-   El intervalo de tiempo ha transcurrido.
-   Un subproceso con mayor prioridad está listo para ejecutarse.
-   Un subproceso en ejecución debe esperar.

Cuando un subproceso en ejecución tiene que esperar, se relincha el resto de su segmento de tiempo.

 

 
