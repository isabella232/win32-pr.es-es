---
title: Estrategias de dibujo de OpenGL multiproceso
description: GDI no admite varios subprocesos.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL en Windows, dibujo multiproceso
- dibujo OpenGL multiproceso OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bccb08d48bd8ccb62584f15911a1eb65080c4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356979"
---
# <a name="multithread-opengl-drawing-strategies"></a>Estrategias de dibujo de OpenGL multiproceso

GDI no admite varios subprocesos. Debe usar un contexto de dispositivo distinto y un contexto de representación distinto para cada subproceso. Esto tiende a limitar las ventajas de rendimiento del uso de varios subprocesos con sistemas de un solo procesador que ejecutan aplicaciones de OpenGL. Sin embargo, hay formas de usar subprocesos con un sistema de un solo procesador para aumentar considerablemente el rendimiento. Por ejemplo, puede utilizar un subproceso independiente para pasar las llamadas de representación de OpenGL al hardware 3D dedicado.

Los sistemas de multiproceso simétrico (SMP) se pueden beneficiar enormemente del uso de varios subprocesos. Una estrategia obvia es usar un subproceso independiente para cada procesador a fin de controlar la representación de OpenGL en ventanas independientes. Por ejemplo, en una aplicación de simulación de vuelos podría usar subprocesos y procesadores independientes para representar las vistas frontal, trasera y lateral.

Un subproceso solo puede tener un contexto de representación activo actual. Cuando se utilizan varios subprocesos y contextos de representación, se debe tener cuidado de sincronizar su uso. Por ejemplo, use un solo subproceso para llamar a [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) después de que todos los subprocesos finalicen el dibujo.

 

 




