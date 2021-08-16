---
title: Estrategias de dibujo openGL multiproceso
description: El GDI no admite varios subprocesos.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL en Windows,dibujo multiproceso
- multithread OpenGL drawing OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d928a481e4334f97cad2f7009f008c899ad8378f3fd15cf9e117e6b9599393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937260"
---
# <a name="multithread-opengl-drawing-strategies"></a>Estrategias de dibujo openGL multiproceso

El GDI no admite varios subprocesos. Debe usar un contexto de dispositivo distinto y un contexto de representación distinto para cada subproceso. Esto tiende a limitar las ventajas de rendimiento de usar varios subprocesos con sistemas de un solo procesador que ejecutan aplicaciones OpenGL. Sin embargo, hay maneras de usar subprocesos con un único sistema de procesador para aumentar considerablemente el rendimiento. Por ejemplo, puede usar un subproceso independiente para pasar llamadas de representación openGL al hardware 3D dedicado.

Los sistemas de multiprocesamiento simétrico (SMP) pueden beneficiarse en gran parte del uso de varios subprocesos. Una estrategia obvia es usar un subproceso independiente para cada procesador para controlar la representación de OpenGL en ventanas independientes. Por ejemplo, en una aplicación de simulación de vuelo podría usar procesadores y subprocesos independientes para representar las vistas frontal, posterior y lateral.

Un subproceso solo puede tener un contexto de representación activo actual. Cuando se usan varios subprocesos y varios contextos de representación, debe tener cuidado de sincronizar su uso. Por ejemplo, use un subproceso solo para llamar a [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) después de que todos los subprocesos terminen de dibujarse.

 

 




