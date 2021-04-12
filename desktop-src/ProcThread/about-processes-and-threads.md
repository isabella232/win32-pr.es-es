---
description: Cada proceso proporciona los recursos necesarios para ejecutar un programa.
ms.assetid: 055458cf-9fc7-4a16-be14-1122b3cf0251
title: Acerca de los procesos y subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650eab4421971bdc08e71c031aec433ed84471bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276827"
---
# <a name="about-processes-and-threads"></a>Acerca de los procesos y subprocesos

Cada *proceso* proporciona los recursos necesarios para ejecutar un programa. Un proceso tiene un espacio de direcciones virtuales, código ejecutable, identificadores abiertos a objetos del sistema, un contexto de seguridad, un identificador de proceso único, variables de entorno, una clase de prioridad, tamaños de espacio de trabajo mínimo y máximo, y al menos un subproceso de ejecución. Cada proceso se inicia con un único subproceso, a menudo denominado *subproceso principal*, pero puede crear subprocesos adicionales a partir de cualquiera de sus subprocesos.

Un *subproceso* es la entidad dentro de un proceso que se puede programar para su ejecución. Todos los subprocesos de un proceso comparten su espacio de direcciones virtuales y los recursos del sistema. Además, cada subproceso mantiene controladores de excepciones, una prioridad de programación, almacenamiento local para el subproceso, un identificador de subproceso único y un conjunto de estructuras que el sistema utilizará para guardar el contexto del subproceso hasta que se programe. El *contexto del subproceso* incluye el conjunto de registros de equipo del subproceso, la pila de kernel, un bloque de entorno de subprocesos y una pila de usuario en el espacio de direcciones del proceso del subproceso. Los subprocesos también pueden tener su propio contexto de seguridad, que se puede usar para suplantar a los clientes.

Microsoft Windows admite la *multitarea preferente*, que crea el efecto de la ejecución simultánea de varios subprocesos desde varios procesos. En un equipo con varios procesadores, el sistema puede ejecutar simultáneamente tantos subprocesos como procesadores haya en el equipo.

Un *objeto de trabajo* permite administrar grupos de procesos como una unidad. Los objetos de trabajo son objetos Namable, protegibles y compartibles que controlan los atributos de los procesos asociados a ellos. Las operaciones realizadas en el objeto de trabajo afectan a todos los procesos asociados con el objeto de trabajo.

Una aplicación puede utilizar el *grupo de subprocesos* para reducir el número de subprocesos de aplicación y proporcionar la administración de los subprocesos de trabajo. Las aplicaciones pueden poner en cola los elementos de trabajo, asociar el trabajo con los identificadores de espera, poner en cola automáticamente en función de un temporizador y enlazar con e/s.

La *programación de modo de usuario* (UMS) es un mecanismo ligero que las aplicaciones pueden usar para programar sus propios subprocesos. Una aplicación puede cambiar entre los subprocesos UMS en modo de usuario sin que intervenga el [programador del sistema](scheduling.md) y recuperar el control del procesador si un SUBproceso UMS se bloquea en el kernel. Cada subproceso UMS tiene su propio contexto de subproceso en lugar de compartir el contexto del subproceso de un solo subproceso. La capacidad de cambiar entre subprocesos en modo de usuario hace que UMS sea más eficaz que los grupos de subprocesos para los elementos de trabajo de corta duración que requieren pocas llamadas del sistema.

Una *fibra* es una unidad de ejecución que debe ser programada manualmente por la aplicación. Las fibras se ejecutan en el contexto de los subprocesos que las programan. Cada subproceso puede programar varios fibras. En general, las fibras no proporcionan ventajas en una aplicación multiproceso bien diseñada. Sin embargo, el uso de fibras puede facilitar el traslado de aplicaciones diseñadas para programar sus propios subprocesos.

Para obtener más información, vea los temas siguientes:

-   [Multitarea](multitasking.md)
-   [Programación](scheduling.md)
-   [Varios subprocesos](multiple-threads.md)
-   [Procesos secundarios](child-processes.md)
-   [Grupos de subprocesos](thread-pools.md)
-   [Objetos de trabajo](job-objects.md)
-   [Programación de modo de usuario](user-mode-scheduling.md)
-   [Fibra](fibers.md)

 

 



