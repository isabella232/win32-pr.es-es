---
description: Implementar la multitarea, programar prioridades y trabajar con procesos, subprocesos, grupos de subprocesos, objetos de trabajo y fibras. Utilice la programación de modo de usuario para programar subprocesos.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Procesos y subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677839"
---
# <a name="processes-and-threads"></a>Procesos y subprocesos

Una aplicación se compone de uno o más procesos. Un *proceso*, en los términos más sencillos, es un programa en ejecución. Uno o más subprocesos se ejecutan en el contexto del proceso. Un *subproceso* es la unidad básica a la que el sistema operativo asigna tiempo de procesador. Un subproceso puede ejecutar cualquier parte del código del proceso, incluidos los elementos que se ejecutan actualmente en otro subproceso.

Un *objeto de trabajo* permite administrar grupos de procesos como una unidad. Los objetos de trabajo son objetos Namable, protegibles y compartibles que controlan los atributos de los procesos asociados a ellos. Las operaciones realizadas en el objeto de trabajo afectan a todos los procesos asociados con el objeto de trabajo.

Un *grupo de subprocesos* es una colección de subprocesos de trabajo que ejecutan de forma eficaz las devoluciones de llamada asincrónicas en nombre de la aplicación. El grupo de subprocesos se usa principalmente para reducir el número de subprocesos de aplicación y proporcionar administración de los subprocesos de trabajo.

Una *fibra* es una unidad de ejecución que debe ser programada manualmente por la aplicación. Las fibras se ejecutan en el contexto de los subprocesos que las programan.

La *programación de modo de usuario* (UMS) es un mecanismo ligero que las aplicaciones pueden usar para programar sus propios subprocesos. Los subprocesos UMS se diferencian de las [fibras](fibers.md) en que cada subproceso UMS tiene su propio contexto de subproceso en lugar de compartir el contexto del subproceso de un solo subproceso.

-   [Novedades de procesos y subprocesos](what-s-new-in-processes-and-threads.md)
-   [Acerca de los procesos y los subprocesos](about-processes-and-threads.md)
-   [Usar procesos y subprocesos](using-processes-and-threads.md)
-   [Referencia de procesos y subprocesos](process-and-thread-reference.md)

 

 



