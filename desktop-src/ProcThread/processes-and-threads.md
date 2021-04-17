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
# <a name="processes-and-threads"></a><span data-ttu-id="9ae38-104">Procesos y subprocesos</span><span class="sxs-lookup"><span data-stu-id="9ae38-104">Processes and Threads</span></span>

<span data-ttu-id="9ae38-105">Una aplicación se compone de uno o más procesos.</span><span class="sxs-lookup"><span data-stu-id="9ae38-105">An application consists of one or more processes.</span></span> <span data-ttu-id="9ae38-106">Un *proceso*, en los términos más sencillos, es un programa en ejecución.</span><span class="sxs-lookup"><span data-stu-id="9ae38-106">A *process*, in the simplest terms, is an executing program.</span></span> <span data-ttu-id="9ae38-107">Uno o más subprocesos se ejecutan en el contexto del proceso.</span><span class="sxs-lookup"><span data-stu-id="9ae38-107">One or more threads run in the context of the process.</span></span> <span data-ttu-id="9ae38-108">Un *subproceso* es la unidad básica a la que el sistema operativo asigna tiempo de procesador.</span><span class="sxs-lookup"><span data-stu-id="9ae38-108">A *thread* is the basic unit to which the operating system allocates processor time.</span></span> <span data-ttu-id="9ae38-109">Un subproceso puede ejecutar cualquier parte del código del proceso, incluidos los elementos que se ejecutan actualmente en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="9ae38-109">A thread can execute any part of the process code, including parts currently being executed by another thread.</span></span>

<span data-ttu-id="9ae38-110">Un *objeto de trabajo* permite administrar grupos de procesos como una unidad.</span><span class="sxs-lookup"><span data-stu-id="9ae38-110">A *job object* allows groups of processes to be managed as a unit.</span></span> <span data-ttu-id="9ae38-111">Los objetos de trabajo son objetos Namable, protegibles y compartibles que controlan los atributos de los procesos asociados a ellos.</span><span class="sxs-lookup"><span data-stu-id="9ae38-111">Job objects are namable, securable, sharable objects that control attributes of the processes associated with them.</span></span> <span data-ttu-id="9ae38-112">Las operaciones realizadas en el objeto de trabajo afectan a todos los procesos asociados con el objeto de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9ae38-112">Operations performed on the job object affect all processes associated with the job object.</span></span>

<span data-ttu-id="9ae38-113">Un *grupo de subprocesos* es una colección de subprocesos de trabajo que ejecutan de forma eficaz las devoluciones de llamada asincrónicas en nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ae38-113">A *thread pool* is a collection of worker threads that efficiently execute asynchronous callbacks on behalf of the application.</span></span> <span data-ttu-id="9ae38-114">El grupo de subprocesos se usa principalmente para reducir el número de subprocesos de aplicación y proporcionar administración de los subprocesos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9ae38-114">The thread pool is primarily used to reduce the number of application threads and provide management of the worker threads.</span></span>

<span data-ttu-id="9ae38-115">Una *fibra* es una unidad de ejecución que debe ser programada manualmente por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ae38-115">A *fiber* is a unit of execution that must be manually scheduled by the application.</span></span> <span data-ttu-id="9ae38-116">Las fibras se ejecutan en el contexto de los subprocesos que las programan.</span><span class="sxs-lookup"><span data-stu-id="9ae38-116">Fibers run in the context of the threads that schedule them.</span></span>

<span data-ttu-id="9ae38-117">La *programación de modo de usuario* (UMS) es un mecanismo ligero que las aplicaciones pueden usar para programar sus propios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="9ae38-117">*User-mode scheduling* (UMS) is a lightweight mechanism that applications can use to schedule their own threads.</span></span> <span data-ttu-id="9ae38-118">Los subprocesos UMS se diferencian de las [fibras](fibers.md) en que cada subproceso UMS tiene su propio contexto de subproceso en lugar de compartir el contexto del subproceso de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="9ae38-118">UMS threads differ from [fibers](fibers.md) in that each UMS thread has its own thread context instead of sharing the thread context of a single thread.</span></span>

-   [<span data-ttu-id="9ae38-119">Novedades de procesos y subprocesos</span><span class="sxs-lookup"><span data-stu-id="9ae38-119">What's New in Processes and Threads</span></span>](what-s-new-in-processes-and-threads.md)
-   [<span data-ttu-id="9ae38-120">Acerca de los procesos y los subprocesos</span><span class="sxs-lookup"><span data-stu-id="9ae38-120">About Processes and Threads</span></span>](about-processes-and-threads.md)
-   [<span data-ttu-id="9ae38-121">Usar procesos y subprocesos</span><span class="sxs-lookup"><span data-stu-id="9ae38-121">Using Processes and Threads</span></span>](using-processes-and-threads.md)
-   [<span data-ttu-id="9ae38-122">Referencia de procesos y subprocesos</span><span class="sxs-lookup"><span data-stu-id="9ae38-122">Process and Thread Reference</span></span>](process-and-thread-reference.md)

 

 



