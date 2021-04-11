---
description: Cada subproceso tiene una prioridad dinámica.
ms.assetid: bcc6cec7-2d85-4810-98d0-7d99486f4924
title: Aumentos de prioridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f463f30b0abffb24daadb4241ad32c5b51f123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276820"
---
# <a name="priority-boosts"></a>Aumentos de prioridad

Cada subproceso tiene una *prioridad dinámica*. Esta es la prioridad que el programador usa para determinar qué subproceso se debe ejecutar. Inicialmente, la prioridad dinámica de un subproceso es igual que su prioridad base. El sistema puede aumentar y disminuir la prioridad dinámica, para asegurarse de que responde y de que no hay ningún subproceso en el tiempo de procesador. El sistema no aumenta la prioridad de los subprocesos con un nivel de prioridad base entre 16 y 31. Solo los subprocesos con una prioridad base entre 0 y 15 reciben aumentos de prioridad dinámica.

El sistema aumenta la prioridad dinámica de un subproceso para mejorar su capacidad de respuesta como se indica a continuación.

-   Cuando un proceso que usa la \_ clase de prioridad normal \_ se pone en primer plano, el programador aumenta la clase de prioridad del proceso asociado a la ventana de primer plano, por lo que es mayor o igual que la clase de prioridad de cualquier proceso en segundo plano. La clase Priority vuelve a su valor original cuando el proceso ya no está en primer plano.
-   Cuando una ventana recibe una entrada, como mensajes del temporizador, mensajes del mouse o entrada de teclado, el programador aumenta la prioridad del subproceso que posee la ventana.
-   Cuando se cumplen las condiciones de espera de un subproceso bloqueado, el programador aumenta la prioridad del subproceso. Por ejemplo, cuando finaliza una operación de espera asociada a la e/s de disco o de teclado, el subproceso recibe un aumento de prioridad.

    Puede deshabilitar la característica de aumento de prioridad llamando a la función [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost) o [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost) . Para determinar si esta característica se ha deshabilitado, llame a la función [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost) o [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost) .

Después de generar la prioridad dinámica de un subproceso, el programador reduce esa prioridad en un nivel cada vez que el subproceso completa un intervalo de tiempo, hasta que el subproceso vuelve a su prioridad base. La prioridad dinámica de un subproceso nunca es menor que su prioridad base.

 

 
