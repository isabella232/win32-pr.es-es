---
description: Con el almacenamiento local para el subproceso (TLS), puede proporcionar datos únicos para cada subproceso al que el proceso puede tener acceso mediante un índice global. Un subproceso asigna el índice, que puede ser utilizado por otros subprocesos para recuperar los datos únicos asociados al índice.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: Almacenamiento local para el subproceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104556041"
---
# <a name="thread-local-storage"></a><span data-ttu-id="08ddc-104">Almacenamiento local para el subproceso</span><span class="sxs-lookup"><span data-stu-id="08ddc-104">Thread Local Storage</span></span>

<span data-ttu-id="08ddc-105">Todos los subprocesos de un proceso comparten su espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="08ddc-105">All threads of a process share its virtual address space.</span></span> <span data-ttu-id="08ddc-106">Las variables locales de una función son únicas para cada subproceso que ejecuta la función.</span><span class="sxs-lookup"><span data-stu-id="08ddc-106">The local variables of a function are unique to each thread that runs the function.</span></span> <span data-ttu-id="08ddc-107">Sin embargo, todos los subprocesos del proceso comparten las variables estáticas y globales.</span><span class="sxs-lookup"><span data-stu-id="08ddc-107">However, the static and global variables are shared by all threads in the process.</span></span> <span data-ttu-id="08ddc-108">Con el *almacenamiento local para el subproceso* (TLS), puede proporcionar datos únicos para cada subproceso al que el proceso puede tener acceso mediante un índice global.</span><span class="sxs-lookup"><span data-stu-id="08ddc-108">With *thread local storage* (TLS), you can provide unique data for each thread that the process can access using a global index.</span></span> <span data-ttu-id="08ddc-109">Un subproceso asigna el índice, que puede ser utilizado por otros subprocesos para recuperar los datos únicos asociados al índice.</span><span class="sxs-lookup"><span data-stu-id="08ddc-109">One thread allocates the index, which can be used by the other threads to retrieve the unique data associated with the index.</span></span>

<span data-ttu-id="08ddc-110">La constante TLS \_ mínima \_ disponible define el número mínimo de índices TLS disponibles en cada proceso.</span><span class="sxs-lookup"><span data-stu-id="08ddc-110">The constant TLS\_MINIMUM\_AVAILABLE defines the minimum number of TLS indexes available in each process.</span></span> <span data-ttu-id="08ddc-111">Se garantiza que este mínimo sea al menos 64 para todos los sistemas.</span><span class="sxs-lookup"><span data-stu-id="08ddc-111">This minimum is guaranteed to be at least 64 for all systems.</span></span> <span data-ttu-id="08ddc-112">El número máximo de índices por proceso es 1.088.</span><span class="sxs-lookup"><span data-stu-id="08ddc-112">The maximum number of indexes per process is 1,088.</span></span>

<span data-ttu-id="08ddc-113">Cuando se crean los subprocesos, el sistema asigna una matriz de valores de **LPVOID** para TLS, que se inicializan en NULL.</span><span class="sxs-lookup"><span data-stu-id="08ddc-113">When the threads are created, the system allocates an array of **LPVOID** values for TLS, which are initialized to NULL.</span></span> <span data-ttu-id="08ddc-114">Antes de que se pueda usar un índice, debe asignarse mediante uno de los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="08ddc-114">Before an index can be used, it must be allocated by one of the threads.</span></span> <span data-ttu-id="08ddc-115">Cada subproceso almacena sus datos para un índice TLS en una *ranura TLS* de la matriz.</span><span class="sxs-lookup"><span data-stu-id="08ddc-115">Each thread stores its data for a TLS index in a *TLS slot* in the array.</span></span> <span data-ttu-id="08ddc-116">Si los datos asociados a un índice caben en un valor de **LPVOID** , puede almacenar los datos directamente en la ranura de TLS.</span><span class="sxs-lookup"><span data-stu-id="08ddc-116">If the data associated with an index will fit in an **LPVOID** value, you can store the data directly in the TLS slot.</span></span> <span data-ttu-id="08ddc-117">Sin embargo, si usa un gran número de índices de esta manera, es mejor asignar almacenamiento independiente, consolidar los datos y minimizar el número de ranuras TLS en uso.</span><span class="sxs-lookup"><span data-stu-id="08ddc-117">However, if you are using a large number of indexes in this way, it is better to allocate separate storage, consolidate the data, and minimize the number of TLS slots in use.</span></span>

<span data-ttu-id="08ddc-118">En el diagrama siguiente se muestra cómo funciona TLS.</span><span class="sxs-lookup"><span data-stu-id="08ddc-118">The following diagram illustrates how TLS works.</span></span> <span data-ttu-id="08ddc-119">Para obtener un ejemplo de código que ilustra el uso del almacenamiento local de subprocesos, vea [usar el almacenamiento local para el subproceso](using-thread-local-storage.md).</span><span class="sxs-lookup"><span data-stu-id="08ddc-119">For a code example illustrating the use of thread local storage, see [Using Thread Local Storage](using-thread-local-storage.md).</span></span>

![Diagrama que muestra cómo funciona el proceso T L S.](images/tls.png)

<span data-ttu-id="08ddc-121">El proceso tiene dos subprocesos, el subproceso 1 y el subproceso 2.</span><span class="sxs-lookup"><span data-stu-id="08ddc-121">The process has two threads, Thread 1 and Thread 2.</span></span> <span data-ttu-id="08ddc-122">Asigna dos índices para su uso con TLS, gdwTlsIndex1 y gdwTlsIndex2.</span><span class="sxs-lookup"><span data-stu-id="08ddc-122">It allocates two indexes for use with TLS, gdwTlsIndex1 and gdwTlsIndex2.</span></span> <span data-ttu-id="08ddc-123">Cada subproceso asigna dos bloques de memoria (uno para cada índice) en el que se almacenan los datos y almacena los punteros a estos bloques de memoria en las ranuras TLS correspondientes.</span><span class="sxs-lookup"><span data-stu-id="08ddc-123">Each thread allocates two memory blocks (one for each index) in which to store the data, and stores the pointers to these memory blocks in the corresponding TLS slots.</span></span> <span data-ttu-id="08ddc-124">Para tener acceso a los datos asociados a un índice, el subproceso recupera el puntero al bloque de memoria desde la ranura TLS y lo almacena en la variable local lpvData.</span><span class="sxs-lookup"><span data-stu-id="08ddc-124">To access the data associated with an index, the thread retrieves the pointer to the memory block from the TLS slot and stores it in the lpvData local variable.</span></span>

<span data-ttu-id="08ddc-125">Es ideal usar TLS en una biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="08ddc-125">It is ideal to use TLS in a dynamic-link library (DLL).</span></span> <span data-ttu-id="08ddc-126">Para obtener un ejemplo, vea [usar el almacenamiento local para el subproceso en una biblioteca de vínculos dinámicos](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span><span class="sxs-lookup"><span data-stu-id="08ddc-126">For an example, see [Using Thread Local Storage in a Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="08ddc-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08ddc-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08ddc-128">Almacenamiento local para el subproceso (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="08ddc-128">Thread Local Storage (Visual C++)</span></span>](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="08ddc-129">Uso del almacenamiento local de subprocesos</span><span class="sxs-lookup"><span data-stu-id="08ddc-129">Using Thread Local Storage</span></span>](using-thread-local-storage.md)
</dt> <dt>

[<span data-ttu-id="08ddc-130">Usar el almacenamiento local de subprocesos en una biblioteca de vínculos dinámicos</span><span class="sxs-lookup"><span data-stu-id="08ddc-130">Using Thread Local Storage in a Dynamic Link Library</span></span>](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
