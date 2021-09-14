---
description: Implemente multitarea, programe prioridades y trabaje con procesos, subprocesos, grupos de subprocesos, objetos de trabajo y fibras. Use la programación en modo de usuario para programar subprocesos.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Procesos y subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062811"
---
# <a name="processes-and-threads"></a>Procesos y subprocesos

Una aplicación consta de uno o varios procesos. Un *proceso*, en los términos más sencillos, es un programa en ejecución. Uno o varios subprocesos se ejecutan en el contexto del proceso. Un *subproceso* es la unidad básica a la que el sistema operativo asigna tiempo de procesador. Un subproceso puede ejecutar cualquier parte del código de proceso, incluidas las partes que ejecuta actualmente otro subproceso.

Un *objeto de trabajo* permite administrar grupos de procesos como una unidad. Los objetos de trabajo son objetos utilizables, protegibles y compartibles que controlan los atributos de los procesos asociados a ellos. Las operaciones realizadas en el objeto de trabajo afectan a todos los procesos asociados al objeto de trabajo.

Un *grupo de subprocesos* es una colección de subprocesos de trabajo que ejecutan eficazmente devoluciones de llamada asincrónicas en nombre de la aplicación. El grupo de subprocesos se usa principalmente para reducir el número de subprocesos de aplicación y proporcionar administración de los subprocesos de trabajo.

Una *fibra* es una unidad de ejecución que la aplicación debe programar manualmente. Las fibras se ejecutan en el contexto de los subprocesos que las programan.

*La programación en modo de* usuario (UMS) es un mecanismo ligero que las aplicaciones pueden usar para programar sus propios subprocesos. Los subprocesos UMS difieren de las [fibras](fibers.md) en que cada subproceso UMS tiene su propio contexto de subproceso en lugar de compartir el contexto de subproceso de un único subproceso.

-   [Novedades de procesos y subprocesos](what-s-new-in-processes-and-threads.md)
-   [Acerca de los procesos y los subprocesos](about-processes-and-threads.md)
-   [Uso de procesos y subprocesos](using-processes-and-threads.md)
-   [Referencia de procesos y subprocesos](process-and-thread-reference.md)

 

 



