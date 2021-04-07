---
Description: La siguiente es una breve comparación de los distintos métodos de asignación de memoria.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Comparar métodos de asignación de memoria
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104003749"
---
# <a name="comparing-memory-allocation-methods"></a><span data-ttu-id="b4a6f-103">Comparar métodos de asignación de memoria</span><span class="sxs-lookup"><span data-stu-id="b4a6f-103">Comparing Memory Allocation Methods</span></span>

<span data-ttu-id="b4a6f-104">La siguiente es una breve comparación de los distintos métodos de asignación de memoria:</span><span class="sxs-lookup"><span data-stu-id="b4a6f-104">The following is a brief comparison of the various memory allocation methods:</span></span>

-   [<span data-ttu-id="b4a6f-105">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4a6f-105">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [<span data-ttu-id="b4a6f-106">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4a6f-106">**GlobalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [<span data-ttu-id="b4a6f-107">**HeapAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4a6f-107">**HeapAlloc**</span></span>](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [<span data-ttu-id="b4a6f-108">**LocalAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4a6f-108">**LocalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   <span data-ttu-id="b4a6f-109">**malloc**</span><span class="sxs-lookup"><span data-stu-id="b4a6f-109">**malloc**</span></span>
-   <span data-ttu-id="b4a6f-110">**new**</span><span class="sxs-lookup"><span data-stu-id="b4a6f-110">**new**</span></span>
-   [<span data-ttu-id="b4a6f-111">**VirtualAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4a6f-111">**VirtualAlloc**</span></span>](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

<span data-ttu-id="b4a6f-112">Aunque las funciones [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)y [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) asignan memoria en última instancia del montón, cada una proporciona un conjunto de funcionalidad ligeramente diferente.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-112">Although the [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), and [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) functions ultimately allocate memory from the same heap, each provides a slightly different set of functionality.</span></span> <span data-ttu-id="b4a6f-113">Por ejemplo, se puede indicar a **HeapAlloc** que genere una excepción si no se pudo asignar memoria, una funcionalidad que no esté disponible con **LocalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-113">For example, **HeapAlloc** can be instructed to raise an exception if memory could not be allocated, a capability not available with **LocalAlloc**.</span></span> <span data-ttu-id="b4a6f-114">**LocalAlloc** admite la asignación de identificadores que permiten que la memoria subyacente se mueva mediante una reasignación sin cambiar el valor de identificador, una funcionalidad no disponible con **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-114">**LocalAlloc** supports allocation of handles which permit the underlying memory to be moved by a reallocation without changing the handle value, a capability not available with **HeapAlloc**.</span></span>

<span data-ttu-id="b4a6f-115">A partir de Windows de 32 bits, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) se implementan como funciones contenedoras que llaman a [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) mediante un identificador del montón predeterminado del proceso.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-115">Starting with 32-bit Windows, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) and [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) are implemented as wrapper functions that call [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) using a handle to the process's default heap.</span></span> <span data-ttu-id="b4a6f-116">Por lo tanto, **GlobalAlloc** y **LocalAlloc** tienen una mayor sobrecarga que **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-116">Therefore, **GlobalAlloc** and **LocalAlloc** have greater overhead than **HeapAlloc**.</span></span>

<span data-ttu-id="b4a6f-117">Dado que los distintos asignadores de montón proporcionan una funcionalidad distintiva mediante el uso de diferentes mecanismos, debe liberar memoria con la función correcta.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-117">Because the different heap allocators provide distinctive functionality by using different mechanisms, you must free memory with the correct function.</span></span> <span data-ttu-id="b4a6f-118">Por ejemplo, la memoria asignada con [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) se debe liberar con [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) y no con [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) o [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span><span class="sxs-lookup"><span data-stu-id="b4a6f-118">For example, memory allocated with [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) must be freed with [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) and not [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) or [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span></span> <span data-ttu-id="b4a6f-119">La memoria asignada con [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) o [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) se debe consultar, validar y liberar con la función global o local correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-119">Memory allocated with [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) or [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) must be queried, validated, and released with the corresponding global or local function.</span></span>

<span data-ttu-id="b4a6f-120">La función [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) le permite especificar opciones adicionales para la asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-120">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function allows you to specify additional options for memory allocation.</span></span> <span data-ttu-id="b4a6f-121">Sin embargo, sus asignaciones usan una granularidad de página, por lo que el uso de **VirtualAlloc** puede dar lugar a un mayor uso de la memoria.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-121">However, its allocations use a page granularity, so using **VirtualAlloc** can result in higher memory usage.</span></span>

<span data-ttu-id="b4a6f-122">La función **malloc** tiene la desventaja de que depende del tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-122">The **malloc** function has the disadvantage of being run-time dependent.</span></span> <span data-ttu-id="b4a6f-123">El operador **New** tiene la desventaja de que dependen del compilador y del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-123">The **new** operator has the disadvantage of being compiler dependent and language dependent.</span></span>

<span data-ttu-id="b4a6f-124">La función [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) tiene la ventaja de que funciona bien en C, C++ o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-124">The [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function has the advantage of working well in either C, C++, or Visual Basic.</span></span> <span data-ttu-id="b4a6f-125">También es la única manera de compartir la memoria en una aplicación basada en COM, ya que MIDL usa **CoTaskMemAlloc** y [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para calcular las referencias de la memoria.</span><span class="sxs-lookup"><span data-stu-id="b4a6f-125">It is also the only way to share memory in a COM-based application, since MIDL uses **CoTaskMemAlloc** and [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to marshal memory.</span></span>


## <a name="examples"></a><span data-ttu-id="b4a6f-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b4a6f-126">Examples</span></span>

* [<span data-ttu-id="b4a6f-127">Reservar y confirmar memoria</span><span class="sxs-lookup"><span data-stu-id="b4a6f-127">Reserving and Committing Memory</span></span>](./reserving-and-committing-memory.md)

* [<span data-ttu-id="b4a6f-128">Ejemplo de AWE</span><span class="sxs-lookup"><span data-stu-id="b4a6f-128">AWE Example</span></span>](./awe-example.md)

## <a name="related-topics"></a><span data-ttu-id="b4a6f-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4a6f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4a6f-130">Funciones globales y locales</span><span class="sxs-lookup"><span data-stu-id="b4a6f-130">Global and Local Functions</span></span>](global-and-local-functions.md)
</dt> <dt>

[<span data-ttu-id="b4a6f-131">Funciones del montón</span><span class="sxs-lookup"><span data-stu-id="b4a6f-131">Heap Functions</span></span>](heap-functions.md)
</dt> <dt>

[<span data-ttu-id="b4a6f-132">Funciones de memoria virtual</span><span class="sxs-lookup"><span data-stu-id="b4a6f-132">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
</dt> </dl>

 

 