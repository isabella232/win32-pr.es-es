---
description: Un subproceso puede suspender y reanudar la ejecución de otro subproceso. Mientras se suspende un subproceso, no está programado para el tiempo en el procesador.
ms.assetid: b76d7af7-e3ec-4663-a9e7-832c01733c8c
title: Suspender la ejecución de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3688b0327ecf5fd21f07e9be6be6ecab17d64617
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062805"
---
# <a name="suspending-thread-execution"></a>Suspender la ejecución de subprocesos

Un subproceso puede suspender y reanudar la ejecución de otro subproceso. Mientras se suspende un subproceso, no está programado para el tiempo en el procesador.

Si se crea un subproceso en un estado suspendido (con la marca [**CREATE \_ SUSPENDED),**](process-creation-flags.md) no comienza a ejecutarse hasta que otro subproceso llama a la función [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) con un identificador para el subproceso suspendido. Esto puede ser útil para inicializar el estado del subproceso antes de comenzar a ejecutarse. Suspender un subproceso durante la creación puede ser útil para la sincronización única, ya que esto garantiza que el subproceso suspendido ejecutará el punto inicial de su código al llamar a **ResumeThread**.

La [**función SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) no está pensada para usarse para la sincronización de subprocesos porque no controla el punto del código en el que se suspende la ejecución del subproceso. Esta función está diseñada principalmente para su uso por los depuradores.

Un subproceso puede producir temporalmente su ejecución durante un intervalo especificado llamando a las funciones [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) o [**SleepEx.**](/windows/win32/api/synchapi/nf-synchapi-sleepex) Esto resulta útil especialmente en los casos en los que el subproceso responde a la interacción del usuario, ya que puede retrasar la ejecución lo suficiente como para permitir que los usuarios observen los resultados de sus acciones. Durante el intervalo de suspensión, el subproceso no está programado para el tiempo en el procesador.

La [**función SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) es similar a [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) y [**SleepEx,**](/windows/win32/api/synchapi/nf-synchapi-sleepex)salvo que no se puede especificar el intervalo. **SwitchToThread permite** al subproceso dejar su segmento de tiempo.

 

 
