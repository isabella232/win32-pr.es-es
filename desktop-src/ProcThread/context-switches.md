---
description: Scheduler mantiene una cola de subprocesos ejecutables para cada nivel de prioridad.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Cambios de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276825"
---
# <a name="context-switches"></a>Cambios de contexto

Scheduler mantiene una cola de subprocesos ejecutables para cada nivel de prioridad. Estos se conocen como *subprocesos listos*. Cuando un procesador está disponible, el sistema realiza un *cambio de contexto*. Los pasos de un cambio de contexto son:

1.  Guarde el contexto del subproceso que acaba de ejecutarse.
2.  Coloque el subproceso que acaba de ejecutarse al final de la cola para su prioridad.
3.  Busque la cola de prioridad más alta que contiene los subprocesos listos.
4.  Quite el subproceso en el encabezado de la cola, cargue su contexto y ejecútelo.

Las siguientes clases de subprocesos no son subprocesos listos.

-   Subprocesos creados con la marca de creación \_ suspendida
-   Subprocesos detenidos durante la ejecución con la función [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) o [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)
-   Subprocesos que esperan un objeto de sincronización o una entrada.

Hasta que los subprocesos suspendidos o bloqueados estén listos para ejecutarse, el programador no asigna ningún tiempo de procesador a ellos, independientemente de su prioridad.

Los motivos más comunes para un cambio de contexto son:

-   El intervalo de tiempo ha transcurrido.
-   Un subproceso con una prioridad más alta está listo para ejecutarse.
-   Un subproceso en ejecución debe esperar.

Cuando un subproceso en ejecución debe esperar, abandona el resto de su intervalo de tiempo.

 

 
