---
description: Los bloqueos de lector/escritor (SRW) de Kindle permiten que los subprocesos de un único proceso accedan a recursos compartidos. están optimizados para la velocidad y ocupan muy poca memoria.
ms.assetid: 2d439b21-291f-4ff0-910a-c1c27e800019
title: Bloqueos SRW (bloqueos finos de lector/escritor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc478d5f9bbfec1268f65b3e4a7f562b9bdca3d2df21f4570a52782eec9f028
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959985"
---
# <a name="slim-readerwriter-srw-locks"></a>Bloqueos SRW (bloqueos finos de lector/escritor)

Los bloqueos de lector/escritor (SRW) de Kindle permiten que los subprocesos de un único proceso accedan a recursos compartidos. están optimizados para la velocidad y ocupan muy poca memoria. Los bloqueos de lector y escritor no se pueden compartir entre procesos.

Los subprocesos de lector leen datos de un recurso compartido, mientras que los subprocesos de escritura escriben datos en un recurso compartido. Cuando varios subprocesos leen y escriben mediante un recurso compartido, los bloqueos exclusivos, como una sección crítica o la exclusión mutua, pueden convertirse en un cuello de botella si los subprocesos del lector se ejecutan continuamente, pero las operaciones de escritura son poco frecuentes.

Los bloqueos SRW proporcionan dos modos en los que los subprocesos pueden acceder a un recurso compartido:

-   **Modo compartido**, que concede acceso de solo lectura compartido a varios subprocesos de lector, lo que les permite leer datos del recurso compartido simultáneamente. Si las operaciones de lectura superan las operaciones de escritura, esta simultaneidad aumenta el rendimiento y el rendimiento en comparación con las secciones críticas.
    > [!NOTE]
    > Los bloqueos SRW en modo compartido no deben adquirirse de forma recursiva, ya que esto puede provocar interbloqueos cuando se combinan con la adquisición exclusiva.

-   **Modo exclusivo**, que concede acceso de lectura y escritura a un subproceso de escritor a la vez. Cuando el bloqueo se ha adquirido en modo exclusivo, ningún otro subproceso puede acceder al recurso compartido hasta que el escritor libere el bloqueo.
    > [!NOTE]
    > Los bloqueos SRW en modo exclusivo no se pueden adquirir de forma recursiva. Si un subproceso intenta adquirir un bloqueo que ya contiene, se producirá un error en ese intento (para [**TryAcquireSRWLockExclusive)**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)o interbloqueo (para [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)).

Se puede adquirir un único bloqueo SRW en cualquier modo; los subprocesos de lector pueden adquirirlo en modo compartido, mientras que los subprocesos de escritura pueden adquirirlo en modo exclusivo. No hay ninguna garantía sobre el orden en el que se concederá la propiedad a los subprocesos que solicitan la propiedad. Los bloqueos SRW no son justos ni FIFO.

Un bloqueo SRW es el tamaño de un puntero. La ventaja es que es rápido actualizar el estado de bloqueo. La desventaja es que se puede almacenar muy poca información de estado, por lo que los bloqueos SRW no detectan un uso recursivo incorrecto en modo compartido. Además, un subproceso que posee un bloqueo SRW en modo compartido no puede actualizar su propiedad del bloqueo al modo exclusivo.

El autor de la llamada debe asignar una estructura SRWLOCK e inicializar mediante una llamada a [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock) (para inicializar la estructura dinámicamente) o asignar la constante **SRWLOCK \_ INIT** a la variable de estructura (para inicializar la estructura estáticamente).

Puede usar [Application Verifier](/windows-hardware/drivers/devtest/application-verifier) para buscar el uso recursivo (reentrante) de bloqueos SRW.

Las siguientes son las funciones de bloqueo SRW.

| Función de bloqueo SRW                                                | Descripción                                                                                                                                       |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)       | Adquiere un bloqueo SRW en modo exclusivo.                                                                                                           |
| [**AcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockshared)             | Adquiere un bloqueo SRW en modo compartido.                                                                                                              |
| [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock)                   | Inicialice un bloqueo SRW.                                                                                                                           |
| [**ReleaseSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockexclusive)       | Libera un bloqueo SRW que se abrió en modo exclusivo.                                                                                           |
| [**ReleaseSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockshared)             | Libera un bloqueo SRW que se abrió en modo compartido.                                                                                              |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)   | Se bloquea en la variable de condición especificada y libera el bloqueo especificado como una operación atómica.                                                |
| [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive) | Intenta adquirir un bloqueo de lector/escritor (SRW) en modo exclusivo. Si la llamada se realiza correctamente, el subproceso que realiza la llamada toma posesión del bloqueo. |
| [**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)       | Intenta adquirir un bloqueo de lector/escritor (SRW) en modo compartido. Si la llamada se realiza correctamente, el subproceso que realiza la llamada toma posesión del bloqueo.    |

 
