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
# <a name="multithread-opengl-drawing-strategies"></a><span data-ttu-id="69861-105">Estrategias de dibujo de OpenGL multiproceso</span><span class="sxs-lookup"><span data-stu-id="69861-105">Multithread OpenGL Drawing Strategies</span></span>

<span data-ttu-id="69861-106">GDI no admite varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="69861-106">The GDI does not support multiple threads.</span></span> <span data-ttu-id="69861-107">Debe usar un contexto de dispositivo distinto y un contexto de representación distinto para cada subproceso.</span><span class="sxs-lookup"><span data-stu-id="69861-107">You must use a distinct device context and a distinct rendering context for each thread.</span></span> <span data-ttu-id="69861-108">Esto tiende a limitar las ventajas de rendimiento del uso de varios subprocesos con sistemas de un solo procesador que ejecutan aplicaciones de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="69861-108">This tends to limit the performance advantages of using multiple threads with single-processor systems running OpenGL applications.</span></span> <span data-ttu-id="69861-109">Sin embargo, hay formas de usar subprocesos con un sistema de un solo procesador para aumentar considerablemente el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="69861-109">However, there are ways to use threads with a single processor system to greatly increase performance.</span></span> <span data-ttu-id="69861-110">Por ejemplo, puede utilizar un subproceso independiente para pasar las llamadas de representación de OpenGL al hardware 3D dedicado.</span><span class="sxs-lookup"><span data-stu-id="69861-110">For example, you can use a separate thread to pass OpenGL rendering calls to dedicated 3-D hardware.</span></span>

<span data-ttu-id="69861-111">Los sistemas de multiproceso simétrico (SMP) se pueden beneficiar enormemente del uso de varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="69861-111">Symmetric multiprocessing (SMP) systems can greatly benefit from using multiple threads.</span></span> <span data-ttu-id="69861-112">Una estrategia obvia es usar un subproceso independiente para cada procesador a fin de controlar la representación de OpenGL en ventanas independientes.</span><span class="sxs-lookup"><span data-stu-id="69861-112">An obvious strategy is to use a separate thread for each processor to handle OpenGL rendering in separate windows.</span></span> <span data-ttu-id="69861-113">Por ejemplo, en una aplicación de simulación de vuelos podría usar subprocesos y procesadores independientes para representar las vistas frontal, trasera y lateral.</span><span class="sxs-lookup"><span data-stu-id="69861-113">For example, in a flight-simulation application you could use separate processors and threads to render the front, back, and side views.</span></span>

<span data-ttu-id="69861-114">Un subproceso solo puede tener un contexto de representación activo actual.</span><span class="sxs-lookup"><span data-stu-id="69861-114">A thread can have only one current, active rendering context.</span></span> <span data-ttu-id="69861-115">Cuando se utilizan varios subprocesos y contextos de representación, se debe tener cuidado de sincronizar su uso.</span><span class="sxs-lookup"><span data-stu-id="69861-115">When you use multiple threads and multiple rendering contexts, you must be careful to synchronize their use.</span></span> <span data-ttu-id="69861-116">Por ejemplo, use un solo subproceso para llamar a [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) después de que todos los subprocesos finalicen el dibujo.</span><span class="sxs-lookup"><span data-stu-id="69861-116">For example, use one thread only to call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) after all threads finish drawing.</span></span>

 

 




