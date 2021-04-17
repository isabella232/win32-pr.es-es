---
description: Las aplicaciones pueden encontrar problemas cuando se ejecutan en sistemas multiprocesador debido a suposiciones que son válidas solo en sistemas de un solo procesador.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Problemas de sincronización y multiprocesador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896dc240e76f1506bac2a6a2e95f101b05beca7
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "105670043"
---
# <a name="synchronization-and-multiprocessor-issues"></a><span data-ttu-id="379af-103">Problemas de sincronización y multiprocesador</span><span class="sxs-lookup"><span data-stu-id="379af-103">Synchronization and Multiprocessor Issues</span></span>

<span data-ttu-id="379af-104">Las aplicaciones pueden encontrar problemas cuando se ejecutan en sistemas multiprocesador debido a suposiciones que son válidas solo en sistemas de un solo procesador.</span><span class="sxs-lookup"><span data-stu-id="379af-104">Applications may encounter problems when run on multiprocessor systems due to assumptions they make which are valid only on single-processor systems.</span></span>

## <a name="thread-priorities"></a><span data-ttu-id="379af-105">Prioridades de subprocesos</span><span class="sxs-lookup"><span data-stu-id="379af-105">Thread Priorities</span></span>

<span data-ttu-id="379af-106">Considere un programa con dos subprocesos, uno con una prioridad más alta que el otro.</span><span class="sxs-lookup"><span data-stu-id="379af-106">Consider a program with two threads, one with a higher priority than the other.</span></span> <span data-ttu-id="379af-107">En un sistema de un solo procesador, el subproceso de prioridad más alta no liberará el control en el subproceso de prioridad inferior porque el programador da preferencia a los subprocesos de prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="379af-107">On a single-processor system, the higher priority thread will not relinquish control to the lower priority thread because the scheduler gives preference to higher priority threads.</span></span> <span data-ttu-id="379af-108">En un sistema con varios procesadores, ambos subprocesos se pueden ejecutar simultáneamente, cada uno en su propio procesador.</span><span class="sxs-lookup"><span data-stu-id="379af-108">On a multiprocessor system, both threads can run simultaneously, each on its own processor.</span></span>

<span data-ttu-id="379af-109">Las aplicaciones deben sincronizar el acceso a las estructuras de datos para evitar las condiciones de carrera.</span><span class="sxs-lookup"><span data-stu-id="379af-109">Applications should synchronize access to data structures to avoid race conditions.</span></span> <span data-ttu-id="379af-110">El código que supone que los subprocesos de prioridad más alta se ejecutan sin interferencias de subprocesos de menor prioridad producirán errores en los sistemas multiprocesador.</span><span class="sxs-lookup"><span data-stu-id="379af-110">Code that assumes that higher priority threads run without interference from lower priority threads will fail on multiprocessor systems.</span></span>

## <a name="memory-ordering"></a><span data-ttu-id="379af-111">Ordenación de memoria</span><span class="sxs-lookup"><span data-stu-id="379af-111">Memory Ordering</span></span>

<span data-ttu-id="379af-112">Cuando un procesador escribe en una ubicación de memoria, el valor se almacena en caché para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="379af-112">When a processor writes to a memory location, the value is cached to improve performance.</span></span> <span data-ttu-id="379af-113">Del mismo modo, el procesador intenta satisfacer las solicitudes de lectura de la memoria caché para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="379af-113">Similarly, the processor attempts to satisfy read requests from the cache to improve performance.</span></span> <span data-ttu-id="379af-114">Además, los procesadores comienzan a capturar los valores de la memoria antes de que la aplicación los solicite.</span><span class="sxs-lookup"><span data-stu-id="379af-114">Furthermore, processors begin to fetch values from memory before they are requested by the application.</span></span> <span data-ttu-id="379af-115">Esto puede ocurrir como parte de la ejecución especulativa o debido a problemas de línea de caché.</span><span class="sxs-lookup"><span data-stu-id="379af-115">This can happen as part of speculative execution or due to cache line issues.</span></span>

<span data-ttu-id="379af-116">Las memorias caché de la CPU se pueden particionar en bancos a los que se puede tener acceso en paralelo.</span><span class="sxs-lookup"><span data-stu-id="379af-116">CPU caches can be partitioned into banks that can be accessed in parallel.</span></span> <span data-ttu-id="379af-117">Esto significa que las operaciones de memoria se pueden completar de forma desordenada.</span><span class="sxs-lookup"><span data-stu-id="379af-117">This means that memory operations can be completed out of order.</span></span> <span data-ttu-id="379af-118">Para asegurarse de que las operaciones de memoria se completan en orden, la mayoría de los procesadores proporcionan instrucciones de barrera de memoria.</span><span class="sxs-lookup"><span data-stu-id="379af-118">To ensure that memory operations are completed in order, most processors provide memory-barrier instructions.</span></span> <span data-ttu-id="379af-119">Una *barrera de memoria completa* garantiza que las operaciones de lectura y escritura de memoria que aparecen antes de la instrucción de barrera de memoria se confirmen en la memoria antes que las operaciones de lectura y escritura de memoria que aparecen después de la instrucción de barrera de memoria.</span><span class="sxs-lookup"><span data-stu-id="379af-119">A *full memory barrier* ensures that memory read and write operations that appear before the memory barrier instruction are committed to memory before any memory read and write operations that appear after the memory barrier instruction.</span></span> <span data-ttu-id="379af-120">Una *barrera de memoria de lectura* solo ordena las operaciones de lectura de memoria y una *barrera de memoria de escritura* solo ordena las operaciones de escritura de memoria.</span><span class="sxs-lookup"><span data-stu-id="379af-120">A *read memory barrier* orders only the memory read operations and a *write memory barrier* orders only the memory write operations.</span></span> <span data-ttu-id="379af-121">Estas instrucciones también aseguran que el compilador deshabilita las optimizaciones que podrían reordenar las operaciones de memoria a través de las barreras.</span><span class="sxs-lookup"><span data-stu-id="379af-121">These instructions also ensure that the compiler disables any optimizations that could reorder memory operations across the barriers.</span></span>

<span data-ttu-id="379af-122">Los procesadores pueden admitir instrucciones para las barreras de memoria con la semántica de adquisición, liberación y barrera.</span><span class="sxs-lookup"><span data-stu-id="379af-122">Processors can support instructions for memory barriers with acquire, release, and fence semantics.</span></span> <span data-ttu-id="379af-123">Esta semántica describe el orden en el que los resultados de una operación están disponibles.</span><span class="sxs-lookup"><span data-stu-id="379af-123">These semantics describe the order in which results of an operation become available.</span></span> <span data-ttu-id="379af-124">Con la semántica de adquisición, los resultados de la operación están disponibles antes de los resultados de cualquier operación que aparece después del código.</span><span class="sxs-lookup"><span data-stu-id="379af-124">With acquire semantics, the results of the operation are available before the results of any operation that appears after it in code.</span></span> <span data-ttu-id="379af-125">Con la semántica de versión, los resultados de la operación están disponibles después de los resultados de cualquier operación que aparece antes en el código.</span><span class="sxs-lookup"><span data-stu-id="379af-125">With release semantics, the results of the operation are available after the results of any operation that appears before it in code.</span></span> <span data-ttu-id="379af-126">La semántica de barrera combina la semántica de adquisición y liberación.</span><span class="sxs-lookup"><span data-stu-id="379af-126">Fence semantics combine acquire and release semantics.</span></span> <span data-ttu-id="379af-127">Los resultados de una operación con semántica de barrera están disponibles antes de los de cualquier operación que aparece después de él en el código y después de los de cualquier operación que aparece antes.</span><span class="sxs-lookup"><span data-stu-id="379af-127">The results of an operation with fence semantics are available before those of any operation that appears after it in code and after those of any operation that appears before it.</span></span>

<span data-ttu-id="379af-128">En los procesadores x86 y x64 que admiten SSE2, las instrucciones son **mfence** (barrera de memoria), **lfence** (barrera de carga) y **sfence** (barrera de tienda).</span><span class="sxs-lookup"><span data-stu-id="379af-128">On x86 and x64 processors that support SSE2, the instructions are **mfence** (memory fence), **lfence** (load fence), and **sfence** (store fence).</span></span> <span data-ttu-id="379af-129">En los procesadores ARM, las inarticulaciones son de **d MB** y **DSB**.</span><span class="sxs-lookup"><span data-stu-id="379af-129">On ARM processors, the instrutions are **dmb** and **dsb**.</span></span> <span data-ttu-id="379af-130">Para obtener más información, consulte la documentación del procesador.</span><span class="sxs-lookup"><span data-stu-id="379af-130">For more information, see the documentation for the processor.</span></span>

<span data-ttu-id="379af-131">Las siguientes funciones de sincronización usan las barreras adecuadas para garantizar el orden de la memoria:</span><span class="sxs-lookup"><span data-stu-id="379af-131">The following synchronization functions use the appropriate barriers to ensure memory ordering:</span></span>

-   <span data-ttu-id="379af-132">Funciones que entran o salen de secciones críticas</span><span class="sxs-lookup"><span data-stu-id="379af-132">Functions that enter or leave critical sections</span></span>
-   <span data-ttu-id="379af-133">Funciones que adquieren o liberan bloqueos SRW</span><span class="sxs-lookup"><span data-stu-id="379af-133">Functions that acquire or release SRW locks</span></span>
-   <span data-ttu-id="379af-134">Inicio y finalización de una sola vez</span><span class="sxs-lookup"><span data-stu-id="379af-134">One-time initialization begin and completion</span></span>
-   <span data-ttu-id="379af-135">**EnterSynchronizationBarrier** función)</span><span class="sxs-lookup"><span data-stu-id="379af-135">**EnterSynchronizationBarrier** function</span></span>
-   <span data-ttu-id="379af-136">Funciones que señalan objetos de sincronización</span><span class="sxs-lookup"><span data-stu-id="379af-136">Functions that signal synchronization objects</span></span>
-   <span data-ttu-id="379af-137">Funciones de espera</span><span class="sxs-lookup"><span data-stu-id="379af-137">Wait functions</span></span>
-   <span data-ttu-id="379af-138">Funciones entrelazadas (excepto las funciones con el sufijo _nobarrera_ o intrínsecos con el sufijo _\_ NF_ )</span><span class="sxs-lookup"><span data-stu-id="379af-138">Interlocked functions (except functions with _NoFence_ suffix, or intrinsics with _\_nf_ suffix)</span></span>

## <a name="fixing-a-race-condition"></a><span data-ttu-id="379af-139">Corregir una condición de carrera</span><span class="sxs-lookup"><span data-stu-id="379af-139">Fixing a Race Condition</span></span>

<span data-ttu-id="379af-140">El siguiente código tiene una condición de carrera en sistemas con varios procesadores porque el procesador que se ejecuta `CacheComputedValue` la primera vez puede escribir `fValueHasBeenComputed` en la memoria principal antes de escribir `iValue` en la memoria principal.</span><span class="sxs-lookup"><span data-stu-id="379af-140">The following code has a race condition on a multiprocessor systems because the processor that executes `CacheComputedValue` the first time may write `fValueHasBeenComputed` to main memory before writing `iValue` to main memory.</span></span> <span data-ttu-id="379af-141">Por consiguiente, un segundo procesador `FetchComputedValue` que se ejecuta al mismo tiempo `fValueHasBeenComputed` indica que es **true**, pero el nuevo valor de `iValue` todavía está en la memoria caché del primer procesador y no se ha escrito en la memoria.</span><span class="sxs-lookup"><span data-stu-id="379af-141">Consequently, a second processor executing `FetchComputedValue` at the same time reads `fValueHasBeenComputed` as **TRUE**, but the new value of `iValue` is still in the first processor's cache and has not been written to memory.</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="379af-142">Esta condición de carrera anterior se puede reparar mediante la palabra clave **volatile** o la función [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) para asegurarse de que el valor de `iValue` se actualiza para todos los procesadores antes de que el valor de `fValueHasBeenComputed` esté establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="379af-142">This race condition above can be repaired by using the **volatile** keyword or the [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) function to ensure that the value of `iValue` is updated for all processors before the value of `fValueHasBeenComputed` is set to **TRUE**.</span></span>

<span data-ttu-id="379af-143">Al iniciar Visual Studio 2005, si se compila en el modo **/volatile: MS** , el compilador usa la semántica de adquisición para las operaciones de lectura en variables **volátiles** y la semántica de versión para operaciones de escritura en variables **volátiles** (cuando es compatible con la CPU).</span><span class="sxs-lookup"><span data-stu-id="379af-143">Starting Visual Studio 2005, if compiled in **/volatile:ms** mode, the compiler uses acquire semantics for read operations on **volatile** variables and release semantics for write operations on **volatile** variables (when supported by the CPU).</span></span> <span data-ttu-id="379af-144">Por lo tanto, puede corregir el ejemplo de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="379af-144">Therefore, you can correct the example as follows:</span></span>

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="379af-145">Con Visual Studio 2003, se ordenan las referencias **volátiles** a **volatile** ; el compilador no volverá a ordenar el acceso a variables **volátiles** .</span><span class="sxs-lookup"><span data-stu-id="379af-145">With Visual Studio 2003, **volatile** to **volatile** references are ordered; the compiler will not re-order **volatile** variable access.</span></span> <span data-ttu-id="379af-146">Sin embargo, estas operaciones se pueden volver a ordenar por el procesador.</span><span class="sxs-lookup"><span data-stu-id="379af-146">However, these operations could be re-ordered by the processor.</span></span> <span data-ttu-id="379af-147">Por lo tanto, puede corregir el ejemplo de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="379af-147">Therefore, you can correct the example as follows:</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a><span data-ttu-id="379af-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="379af-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="379af-149">Objetos de sección crítica</span><span class="sxs-lookup"><span data-stu-id="379af-149">Critical Section Objects</span></span>](critical-section-objects.md)
</dt> <dt>

[<span data-ttu-id="379af-150">Acceso a variables entrelazadas</span><span class="sxs-lookup"><span data-stu-id="379af-150">Interlocked Variable Access</span></span>](interlocked-variable-access.md)
</dt> <dt>

[<span data-ttu-id="379af-151">Funciones de espera</span><span class="sxs-lookup"><span data-stu-id="379af-151">Wait Functions</span></span>](wait-functions.md)
</dt> </dl>

 

 



