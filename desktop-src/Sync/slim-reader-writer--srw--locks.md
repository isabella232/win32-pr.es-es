---
description: Los bloqueos finos de lector/escritor (SRW) permiten a los subprocesos de un único proceso tener acceso a recursos compartidos. están optimizadas para acelerar y ocupan muy poca memoria.
ms.assetid: 2d439b21-291f-4ff0-910a-c1c27e800019
title: Bloqueos SRW (bloqueos finos de lector/escritor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d76d956e1425531eae43b0daa6817002a92bc
ms.sourcegitcommit: 663239b4560bfd5314e86901c65805c9bbcab07d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/15/2021
ms.locfileid: "105670041"
---
# <a name="slim-readerwriter-srw-locks"></a>Bloqueos SRW (bloqueos finos de lector/escritor)

Los bloqueos finos de lector/escritor (SRW) permiten a los subprocesos de un único proceso tener acceso a recursos compartidos. están optimizadas para acelerar y ocupan muy poca memoria. Los bloqueos ligeros de lectura y escritura no se pueden compartir entre los procesos.

Los subprocesos de lectura leen los datos de un recurso compartido, mientras que los subprocesos de escritura escriben datos en un recurso compartido. Cuando varios subprocesos leen y escriben con un recurso compartido, los bloqueos exclusivos, como una sección crítica o una exclusión mutua, pueden convertirse en un cuello de botella si los subprocesos de lectura se ejecutan de forma continua pero las operaciones de escritura son poco frecuentes.

Los bloqueos SRW proporcionan dos modos en los que los subprocesos pueden tener acceso a un recurso compartido:

-   **Modo compartido**, que concede acceso compartido de solo lectura a varios subprocesos de lectura, lo que les permite leer datos del recurso compartido simultáneamente. Si las operaciones de lectura superan las operaciones de escritura, esta simultaneidad aumenta el rendimiento y el rendimiento en comparación con las secciones críticas.
    > [!NOTE]
    > No se deben adquirir bloqueos SRW de modo compartido de forma recursiva, ya que esto puede provocar interbloqueos cuando se combinan con la adquisición exclusiva.

-   **Modo exclusivo**, que concede acceso de lectura y escritura a un subproceso de escritura a la vez. Cuando el bloqueo se ha adquirido en modo exclusivo, ningún otro subproceso puede tener acceso al recurso compartido hasta que el escritor libera el bloqueo.
    > [!NOTE]
    > No se pueden adquirir bloqueos SRW de modo exclusivo de forma recursiva. Si un subproceso intenta adquirir un bloqueo que ya contiene, se producirá un error en el intento (por [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)) o en el interbloqueo (para [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)).

Se puede adquirir un bloqueo SRW único en cualquier modo; los subprocesos de lector pueden adquirirlo en modo compartido, mientras que los subprocesos de escritura pueden adquirirlo en modo exclusivo. No hay ninguna garantía sobre el orden en el que los subprocesos que solicitan la propiedad se les concederá propiedad; Los bloqueos SRW no son equitativos ni FIFO.

Un bloqueo SRW es el tamaño de un puntero. La ventaja es que es rápido actualizar el estado de bloqueo. La desventaja es que se puede almacenar muy poca información de estado, de modo que los bloqueos SRW no detectan un uso recursivo incorrecto en el modo compartido. Además, un subproceso que posee un bloqueo SRW en modo compartido no puede actualizar su propiedad del bloqueo al modo exclusivo.

El autor de la llamada debe asignar una estructura SRWLOCK e inicializarla mediante una llamada a [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock) (para inicializar la estructura dinámicamente) o asignar la constante **SRWLOCK \_ init** a la variable de estructura (para inicializar la estructura estáticamente).

Puede usar [Comprobador de aplicaciones](/windows-hardware/drivers/devtest/application-verifier) para buscar el uso recursivo (reentrante) de bloqueos SRW.

A continuación se indican las funciones de bloqueo SRW.

| SRW Lock (función)                                                | Descripción                                                                                                                                       |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)       | Adquiere un bloqueo SRW en modo exclusivo.                                                                                                           |
| [**AcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockshared)             | Adquiere un bloqueo SRW en modo compartido.                                                                                                              |
| [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock)                   | Inicializa un bloqueo SRW.                                                                                                                           |
| [**ReleaseSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockexclusive)       | Libera un bloqueo SRW que se abrió en modo exclusivo.                                                                                           |
| [**ReleaseSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockshared)             | Libera un bloqueo SRW que se abrió en modo compartido.                                                                                              |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)   | Suspende en la variable de condición especificada y libera el bloqueo especificado como una operación atómica.                                                |
| [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive) | Intenta adquirir un bloqueo delgado de lector/escritor (SRW) en modo exclusivo. Si la llamada se realiza correctamente, el subproceso que realiza la llamada toma la propiedad del bloqueo. |
| [**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)       | Intenta adquirir un bloqueo delgado de lector/escritor (SRW) en modo compartido. Si la llamada se realiza correctamente, el subproceso que realiza la llamada toma la propiedad del bloqueo.    |

 
