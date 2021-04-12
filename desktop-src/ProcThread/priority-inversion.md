---
description: La inversión de prioridad se produce cuando dos o más subprocesos con prioridades diferentes están en la contención que se va a programar.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversión de prioridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a0f4c9d57000e9e81429ee882e70dc14f63ae4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360690"
---
# <a name="priority-inversion"></a><span data-ttu-id="5ec11-103">Inversión de prioridad</span><span class="sxs-lookup"><span data-stu-id="5ec11-103">Priority Inversion</span></span>

<span data-ttu-id="5ec11-104">La inversión de prioridad se produce cuando dos o más subprocesos con prioridades diferentes están en la contención que se va a programar.</span><span class="sxs-lookup"><span data-stu-id="5ec11-104">Priority inversion occurs when two or more threads with different priorities are in contention to be scheduled.</span></span> <span data-ttu-id="5ec11-105">Considere un caso sencillo con tres subprocesos: el subproceso 1, el subproceso 2 y el subproceso 3.</span><span class="sxs-lookup"><span data-stu-id="5ec11-105">Consider a simple case with three threads: thread 1, thread 2, and thread 3.</span></span> <span data-ttu-id="5ec11-106">El subproceso 1 tiene prioridad alta y está listo para ser programado.</span><span class="sxs-lookup"><span data-stu-id="5ec11-106">Thread 1 is high priority and becomes ready to be scheduled.</span></span> <span data-ttu-id="5ec11-107">Thread 2, un subproceso de prioridad baja, ejecuta código en una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="5ec11-107">Thread 2, a low-priority thread, is executing code in a critical section.</span></span> <span data-ttu-id="5ec11-108">El subproceso 1, el subproceso de prioridad alta, comienza a esperar a un recurso compartido del subproceso 2.</span><span class="sxs-lookup"><span data-stu-id="5ec11-108">Thread 1, the high-priority thread, begins waiting for a shared resource from thread 2.</span></span> <span data-ttu-id="5ec11-109">El subproceso 3 tiene prioridad media.</span><span class="sxs-lookup"><span data-stu-id="5ec11-109">Thread 3 has medium priority.</span></span> <span data-ttu-id="5ec11-110">El subproceso 3 recibe todo el tiempo de procesador, porque el subproceso de prioridad alta (subproceso 1) está esperando los recursos compartidos del subproceso de prioridad baja (subproceso 2).</span><span class="sxs-lookup"><span data-stu-id="5ec11-110">Thread 3 receives all the processor time, because the high-priority thread (thread 1) is waiting for shared resources from the low-priority thread (thread 2).</span></span> <span data-ttu-id="5ec11-111">El subproceso 2 no abandonará la sección crítica porque no tiene la prioridad más alta y no se programará.</span><span class="sxs-lookup"><span data-stu-id="5ec11-111">Thread 2 will not leave the critical section, because it does not have the highest priority and will not be scheduled.</span></span>

<span data-ttu-id="5ec11-112">El programador resuelve este problema al aumentar aleatoriamente la prioridad de los subprocesos listos (en este caso, los bloqueadores de baja prioridad).</span><span class="sxs-lookup"><span data-stu-id="5ec11-112">The scheduler solves this problem by randomly boosting the priority of the ready threads (in this case, the low priority lock-holders).</span></span> <span data-ttu-id="5ec11-113">Los subprocesos de prioridad baja se ejecutan el tiempo suficiente para salir de la sección crítica y el subproceso de prioridad alta puede entrar en la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="5ec11-113">The low priority threads run long enough to exit the critical section, and the high-priority thread can enter the critical section.</span></span> <span data-ttu-id="5ec11-114">Si el subproceso de prioridad baja no obtiene suficiente tiempo de CPU para salir de la sección crítica la primera vez, obtendrá otra oportunidad durante la siguiente ronda de programación.</span><span class="sxs-lookup"><span data-stu-id="5ec11-114">If the low-priority thread does not get enough CPU time to exit the critical section the first time, it will get another chance during the next round of scheduling.</span></span>

 

 



