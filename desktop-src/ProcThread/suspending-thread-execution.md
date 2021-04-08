---
description: Un subproceso puede suspender y reanudar la ejecución de otro subproceso. Mientras se suspende un subproceso, no se programa para el tiempo en el procesador.
ms.assetid: b76d7af7-e3ec-4663-a9e7-832c01733c8c
title: Suspender la ejecución de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3688b0327ecf5fd21f07e9be6be6ecab17d64617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001942"
---
# <a name="suspending-thread-execution"></a>Suspender la ejecución de subprocesos

Un subproceso puede suspender y reanudar la ejecución de otro subproceso. Mientras se suspende un subproceso, no se programa para el tiempo en el procesador.

Si un subproceso se crea en un estado suspendido (con la marca [**Create \_ Suspended**](process-creation-flags.md) ), no comienza a ejecutarse hasta que otro subproceso llama a la función [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) con un identificador para el subproceso suspendido. Esto puede ser útil para inicializar el estado del subproceso antes de que empiece a ejecutarse. Suspender un subproceso en la creación puede ser útil para la sincronización única, ya que esto garantiza que el subproceso suspendido ejecute el punto de inicio de su código al llamar a **ResumeThread**.

La función [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) no está pensada para usarse para la sincronización de subprocesos porque no controla el punto en el código en el que se suspende la ejecución del subproceso. Esta función está diseñada principalmente para su uso por parte de los depuradores.

Un subproceso puede producir temporalmente su ejecución durante un intervalo especificado mediante una llamada a las funciones [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) o [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) resulta útil especialmente en los casos en los que el subproceso responde a la interacción del usuario, ya que puede retrasar la ejecución durante el tiempo suficiente para permitir que los usuarios respeten los resultados de sus acciones. Durante el intervalo de suspensión, el subproceso no está programado para el tiempo en el procesador.

La función [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) es similar a [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) y [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), salvo que no se puede especificar el intervalo. **SwitchToThread** permite que el subproceso entregue su intervalo de tiempo.

 

 
