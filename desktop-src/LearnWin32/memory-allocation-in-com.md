---
title: Asignación de memoria en COM
description: Asignación de memoria en COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cb9913da55fab82f699ac05dae3998f7582224
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103893"
---
# <a name="memory-allocation-in-com"></a><span data-ttu-id="9b00d-103">Asignación de memoria en COM</span><span class="sxs-lookup"><span data-stu-id="9b00d-103">Memory Allocation in COM</span></span>

<span data-ttu-id="9b00d-104">A veces, un método asigna un búfer de memoria en el montón y devuelve la dirección del búfer al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9b00d-104">Sometimes a method allocates a memory buffer on the heap and returns the address of the buffer to the caller.</span></span> <span data-ttu-id="9b00d-105">COM define un par de funciones para asignar y liberar memoria en el montón.</span><span class="sxs-lookup"><span data-stu-id="9b00d-105">COM defines a pair of functions for allocating and freeing memory on the heap.</span></span>

-   <span data-ttu-id="9b00d-106">La [**función CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) asigna un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="9b00d-106">The [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) function allocates a block of memory.</span></span>
-   <span data-ttu-id="9b00d-107">La [**función CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libera un bloque de memoria que se asignó [**con CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span><span class="sxs-lookup"><span data-stu-id="9b00d-107">The [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function frees a block of memory that was allocated with [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span></span>

<span data-ttu-id="9b00d-108">Hemos visto un ejemplo de este patrón en el ejemplo [de cuadro de diálogo Abrir](example--the-open-dialog-box.md):</span><span class="sxs-lookup"><span data-stu-id="9b00d-108">We saw an example of this pattern in the [Open dialog box example](example--the-open-dialog-box.md):</span></span>


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



<span data-ttu-id="9b00d-109">El [**método GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) asigna memoria para una cadena.</span><span class="sxs-lookup"><span data-stu-id="9b00d-109">The [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method allocates memory for a string.</span></span> <span data-ttu-id="9b00d-110">Internamente, el método llama [**a CoTaskMemAlloc para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) asignar la cadena.</span><span class="sxs-lookup"><span data-stu-id="9b00d-110">Internally, the method calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate the string.</span></span> <span data-ttu-id="9b00d-111">Cuando el método vuelve, *pszFilePath* apunta a la ubicación de memoria del nuevo búfer.</span><span class="sxs-lookup"><span data-stu-id="9b00d-111">When the method returns, *pszFilePath* points to the memory location of the new buffer.</span></span> <span data-ttu-id="9b00d-112">El autor de la llamada es responsable de [**llamar a CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria.</span><span class="sxs-lookup"><span data-stu-id="9b00d-112">The caller is responsible for calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory.</span></span>

<span data-ttu-id="9b00d-113">¿Por qué COM define sus propias funciones de asignación de memoria?</span><span class="sxs-lookup"><span data-stu-id="9b00d-113">Why does COM define its own memory allocation functions?</span></span> <span data-ttu-id="9b00d-114">Una razón es proporcionar una capa de abstracción sobre el asignador del montón.</span><span class="sxs-lookup"><span data-stu-id="9b00d-114">One reason is to provide an abstraction layer over the heap allocator.</span></span> <span data-ttu-id="9b00d-115">De lo contrario, algunos métodos podrían llamar **a malloc** mientras que otros **llamaron a new**.</span><span class="sxs-lookup"><span data-stu-id="9b00d-115">Otherwise, some methods might call **malloc** while others called **new**.</span></span> <span data-ttu-id="9b00d-116">A continuación, el programa tendría  que llamar a **free** en algunos casos y eliminar en otros, y realizar un seguimiento de todo sería imposible rápidamente.</span><span class="sxs-lookup"><span data-stu-id="9b00d-116">Then your program would need to call **free** in some cases and **delete** in others, and keeping track of it all would quickly become impossible.</span></span> <span data-ttu-id="9b00d-117">Las funciones de asignación COM crean un enfoque uniforme.</span><span class="sxs-lookup"><span data-stu-id="9b00d-117">The COM allocation functions create a uniform approach.</span></span>

<span data-ttu-id="9b00d-118">Otra consideración es el hecho de que COM es *un estándar* binario, por lo que no está vinculado a un lenguaje de programación determinado.</span><span class="sxs-lookup"><span data-stu-id="9b00d-118">Another consideration is the fact that COM is a *binary* standard, so it is not tied to a particular programming language.</span></span> <span data-ttu-id="9b00d-119">Por lo tanto, COM no puede basarse en ninguna forma específica del lenguaje de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="9b00d-119">Therefore, COM cannot rely on any language-specific form of memory allocation.</span></span>

## <a name="next"></a><span data-ttu-id="9b00d-120">Siguientes</span><span class="sxs-lookup"><span data-stu-id="9b00d-120">Next</span></span>

[<span data-ttu-id="9b00d-121">Prácticas de codificación COM</span><span class="sxs-lookup"><span data-stu-id="9b00d-121">COM Coding Practices</span></span>](com-coding-practices.md)

 

 
