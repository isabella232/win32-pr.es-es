---
description: Para evitar condiciones de carrera e interbloqueos, es necesario sincronizar el acceso de varios subprocesos a los recursos compartidos. La sincronización también es necesaria para asegurarse de que el código interdependiente se ejecuta en la secuencia adecuada.
ms.assetid: 74af0502-dae1-438c-8e4b-7663093b3fe3
title: Sincronización de la ejecución de varios subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a1b3dd51d666d507771476792e679f7980fab8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062796"
---
# <a name="synchronizing-execution-of-multiple-threads"></a>Sincronización de la ejecución de varios subprocesos

Para evitar condiciones de carrera e interbloqueos, es necesario sincronizar el acceso de varios subprocesos a los recursos compartidos. La sincronización también es necesaria para asegurarse de que el código interdependiente se ejecuta en la secuencia adecuada.

Hay una serie de objetos cuyos identificadores se pueden usar para sincronizar varios subprocesos. Estos objetos incluyen:

-   Búferes de entrada de la consola
-   Eventos
-   Mutexes
-   Procesos
-   Semáforos
-   Subprocesos
-   Temporizadores

El estado de cada uno de estos objetos se señala o no. Cuando se especifica un identificador para cualquiera de estos objetos en una llamada a una de las funciones de espera [,](../sync/wait-functions.md)la ejecución del subproceso que realiza la llamada se bloquea hasta que se señala el estado del objeto especificado.

Algunos de estos objetos son útiles para bloquear un subproceso hasta que se produzca algún evento. Por ejemplo, se señala un identificador de búfer de entrada de la consola cuando hay entradas no leídas, como una pulsación de tecla o un clic del botón del mouse. Los identificadores de procesos y subprocesos se señalizan cuando finaliza el proceso o subproceso. Esto permite que un proceso, por ejemplo, cree un proceso secundario y, a continuación, bloquee su propia ejecución hasta que finalice el nuevo proceso.

Otros objetos son útiles para proteger los recursos compartidos del acceso simultáneo. Por ejemplo, varios subprocesos pueden tener cada uno un identificador para un objeto mutex. Antes de acceder a un recurso compartido, los subprocesos deben llamar a una de las funciones de espera para esperar a que se señale el estado de la exclusión mutua. [](../sync/wait-functions.md) Cuando se señala la exclusión mutua, solo se libera un subproceso en espera para acceder al recurso. El estado de la exclusión mutua se restablece inmediatamente a no señalizado, por lo que cualquier otro subproceso en espera permanece bloqueado. Cuando el subproceso finaliza con el recurso, debe establecer el estado de la exclusión mutua en señalado para permitir que otros subprocesos accedan al recurso.

Para los subprocesos de un único proceso, los objetos de sección crítica proporcionan un medio de sincronización más eficaz que las exclusiones mutuas. Se usa una sección crítica como una exclusión mutua para permitir que un subproceso a la vez use el recurso protegido. Un subproceso puede usar la [**función EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) para solicitar la propiedad de una sección crítica. Si ya es propiedad de otro subproceso, se bloquea el subproceso solicitante. Un subproceso puede usar la [**función TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) para solicitar la propiedad de una sección crítica, sin bloquear si no se obtiene la sección crítica. Una vez que recibe la propiedad, el subproceso es libre de usar el recurso protegido. La ejecución de los demás subprocesos del proceso no se ve afectada a menos que intenten entrar en la misma sección crítica.

La [**función WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle) hace que un subproceso espere hasta que se inicialice un proceso especificado y espere la entrada del usuario sin ninguna entrada pendiente. Llamar **a WaitForInputIdle** puede ser útil para sincronizar procesos primarios y secundarios, ya que [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) devuelve sin esperar a que el proceso secundario complete su inicialización.

Para obtener más información, vea [Synchronization](../sync/synchronization.md).

 

 
