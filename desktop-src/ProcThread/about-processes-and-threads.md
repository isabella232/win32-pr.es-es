---
description: Cada proceso proporciona los recursos necesarios para ejecutar un programa.
ms.assetid: 055458cf-9fc7-4a16-be14-1122b3cf0251
title: Acerca de los procesos y subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cbce9375d3c27fd58d6bab48c11fe2bdb825dfc729c2176dd2f14eba0a958e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032625"
---
# <a name="about-processes-and-threads"></a>Acerca de los procesos y subprocesos

Cada *proceso* proporciona los recursos necesarios para ejecutar un programa. Un proceso tiene un espacio de direcciones virtuales, código ejecutable, identificadores abiertos para objetos del sistema, un contexto de seguridad, un identificador de proceso único, variables de entorno, una clase de prioridad, tamaños mínimos y máximos del espacio de trabajo y al menos un subproceso de ejecución. Cada proceso se inicia con un único subproceso, a menudo denominado subproceso *principal,* pero puede crear subprocesos adicionales a partir de cualquiera de sus subprocesos.

Un *subproceso* es la entidad dentro de un proceso que se puede programar para su ejecución. Todos los subprocesos de un proceso comparten su espacio de direcciones virtuales y los recursos del sistema. Además, cada subproceso mantiene controladores de excepciones, una prioridad de programación, almacenamiento local de subprocesos, un identificador de subproceso único y un conjunto de estructuras que el sistema usará para guardar el contexto del subproceso hasta que se programe. El *contexto del subproceso* incluye el conjunto de registros de máquina del subproceso, la pila de kernel, un bloque de entorno de subproceso y una pila de usuario en el espacio de direcciones del proceso del subproceso. Los subprocesos también pueden tener su propio contexto de seguridad, que se puede usar para suplantar a los clientes.

Microsoft Windows admite *la multitarea* preferente, lo que crea el efecto de la ejecución simultánea de varios subprocesos de varios procesos. En un equipo con varios procesadores, el sistema puede ejecutar simultáneamente tantos subprocesos como haya procesadores en el equipo.

Un *objeto de trabajo* permite administrar grupos de procesos como una unidad. Los objetos de trabajo son objetos utilizables, protegibles y compartibles que controlan los atributos de los procesos asociados a ellos. Las operaciones realizadas en el objeto de trabajo afectan a todos los procesos asociados al objeto de trabajo.

Una aplicación puede usar el grupo *de subprocesos* para reducir el número de subprocesos de aplicación y proporcionar administración de los subprocesos de trabajo. Las aplicaciones pueden poner en cola los elementos de trabajo, asociar el trabajo con identificadores que se pueden esperar, poner en cola automáticamente en función de un temporizador y enlazar con E/S.

*La programación en modo de* usuario (UMS) es un mecanismo ligero que las aplicaciones pueden usar para programar sus propios subprocesos. Una aplicación puede cambiar entre subprocesos UMS [](scheduling.md) en modo de usuario sin implicar al programador del sistema y recuperar el control del procesador si un subproceso UMS se bloquea en el kernel. Cada subproceso UMS tiene su propio contexto de subproceso en lugar de compartir el contexto de subproceso de un único subproceso. La capacidad de cambiar entre subprocesos en modo de usuario hace que UMS sea más eficaz que los grupos de subprocesos para los elementos de trabajo de corta duración que requieren pocas llamadas del sistema.

Una *fibra* es una unidad de ejecución que la aplicación debe programar manualmente. Las fibras se ejecutan en el contexto de los subprocesos que las programan. Cada subproceso puede programar varias fibras. En general, las fibras no proporcionan ventajas con respecto a una aplicación multiproceso bien diseñada. Sin embargo, el uso de fibras puede facilitar el puerto de las aplicaciones diseñadas para programar sus propios subprocesos.

Para obtener más información, vea los temas siguientes:

-   [Multitarea](multitasking.md)
-   [Programación](scheduling.md)
-   [Varios subprocesos](multiple-threads.md)
-   [Procesos secundarios](child-processes.md)
-   [Grupos de subprocesos](thread-pools.md)
-   [Objetos de trabajo](job-objects.md)
-   [Programación en modo de usuario](user-mode-scheduling.md)
-   [Fibras](fibers.md)

 

 



