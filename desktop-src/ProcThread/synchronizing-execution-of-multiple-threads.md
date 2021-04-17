---
description: Para evitar las condiciones de carrera y los interbloqueos, es necesario sincronizar el acceso de varios subprocesos a recursos compartidos. La sincronización también es necesaria para garantizar que el código interdependiente se ejecute en la secuencia adecuada.
ms.assetid: 74af0502-dae1-438c-8e4b-7663093b3fe3
title: Sincronizar la ejecución de varios subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a1b3dd51d666d507771476792e679f7980fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677828"
---
# <a name="synchronizing-execution-of-multiple-threads"></a>Sincronizar la ejecución de varios subprocesos

Para evitar las condiciones de carrera y los interbloqueos, es necesario sincronizar el acceso de varios subprocesos a recursos compartidos. La sincronización también es necesaria para garantizar que el código interdependiente se ejecute en la secuencia adecuada.

Hay una serie de objetos cuyos identificadores se pueden usar para sincronizar varios subprocesos. Estos objetos incluyen:

-   Búferes de entrada de la consola
-   Events
-   Mutexes
-   Procesos
-   Semáforos
-   Subprocesos
-   Temporizadores

El estado de cada uno de estos objetos es señalado o no señalizado. Cuando se especifica un identificador para cualquiera de estos objetos en una llamada a una de las [funciones de espera](../sync/wait-functions.md), la ejecución del subproceso que realiza la llamada se bloquea hasta que se señaliza el estado del objeto especificado.

Algunos de estos objetos son útiles para bloquear un subproceso hasta que se produce algún evento. Por ejemplo, un controlador de búfer de entrada de la consola se señaliza cuando hay una entrada sin leer, como un clic del botón del mouse o de pulsación de tecla. Los identificadores de proceso y de subproceso se señalan cuando finaliza el proceso o subproceso. Esto permite a un proceso, por ejemplo, crear un proceso secundario y, a continuación, bloquear su propia ejecución hasta que finalice el nuevo proceso.

Otros objetos son útiles para proteger los recursos compartidos de acceso simultáneo. Por ejemplo, varios subprocesos pueden tener un identificador a un objeto mutex. Antes de tener acceso a un recurso compartido, los subprocesos deben llamar a una de las [funciones de espera](../sync/wait-functions.md) para esperar a que se señale el estado de la exclusión mutua. Cuando se señala la exclusión mutua, solo se libera un subproceso en espera para tener acceso al recurso. El estado de la exclusión mutua se restablece inmediatamente a no señalizado, por lo que cualquier otro subproceso en espera permanece bloqueado. Cuando el subproceso finaliza con el recurso, debe establecer el estado de la exclusión mutua en señalizado para permitir que otros subprocesos tengan acceso al recurso.

En el caso de los subprocesos de un único proceso, los objetos de sección crítica proporcionan un medio más eficaz de sincronización que las exclusiones mutuas. Una sección crítica se usa como una exclusión mutua para permitir que un subproceso a la vez use el recurso protegido. Un subproceso puede usar la función [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) para solicitar la propiedad de una sección crítica. Si ya es propiedad de otro subproceso, el subproceso que lo solicita está bloqueado. Un subproceso puede usar la función [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) para solicitar la propiedad de una sección crítica, sin bloquearse si se produce un error al obtener la sección crítica. Una vez que recibe la propiedad, el subproceso es libre de usar el recurso protegido. La ejecución de los demás subprocesos del proceso no se ve afectada a menos que intenten entrar en la misma sección crítica.

La función [**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle) hace que un subproceso espere hasta que se inicializa un proceso especificado y se espera la entrada del usuario sin ninguna entrada pendiente. La llamada a **WaitForInputIdle** puede ser útil para sincronizar procesos primarios y secundarios, porque [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) devuelve sin esperar a que el proceso secundario complete su inicialización.

Para obtener más información, consulte [Synchronization](../sync/synchronization.md).

 

 
