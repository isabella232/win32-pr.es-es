---
title: Asignación de memoria en COM
description: .
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62227f78287f184b019eee3e498ec8a25f25a03c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685706"
---
# <a name="memory-allocation-in-com"></a><span data-ttu-id="34c20-103">Asignación de memoria en COM</span><span class="sxs-lookup"><span data-stu-id="34c20-103">Memory Allocation in COM</span></span>

<span data-ttu-id="34c20-104">A veces, un método asigna un búfer de memoria en el montón y devuelve la dirección del búfer al llamador.</span><span class="sxs-lookup"><span data-stu-id="34c20-104">Sometimes a method allocates a memory buffer on the heap and returns the address of the buffer to the caller.</span></span> <span data-ttu-id="34c20-105">COM define un par de funciones para asignar y liberar memoria en el montón.</span><span class="sxs-lookup"><span data-stu-id="34c20-105">COM defines a pair of functions for allocating and freeing memory on the heap.</span></span>

-   <span data-ttu-id="34c20-106">La función [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) asigna un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="34c20-106">The [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) function allocates a block of memory.</span></span>
-   <span data-ttu-id="34c20-107">La función [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libera un bloque de memoria que se asignó con [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span><span class="sxs-lookup"><span data-stu-id="34c20-107">The [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function frees a block of memory that was allocated with [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span></span>

<span data-ttu-id="34c20-108">Vimos un ejemplo de este patrón en el [ejemplo de cuadro de diálogo Abrir](example--the-open-dialog-box.md):</span><span class="sxs-lookup"><span data-stu-id="34c20-108">We saw an example of this pattern in the [Open dialog box example](example--the-open-dialog-box.md):</span></span>


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



<span data-ttu-id="34c20-109">El método [**getDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) asigna memoria para una cadena.</span><span class="sxs-lookup"><span data-stu-id="34c20-109">The [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method allocates memory for a string.</span></span> <span data-ttu-id="34c20-110">Internamente, el método llama a [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar la cadena.</span><span class="sxs-lookup"><span data-stu-id="34c20-110">Internally, the method calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate the string.</span></span> <span data-ttu-id="34c20-111">Cuando el método devuelve, *pszFilePath* apunta a la ubicación de memoria del nuevo búfer.</span><span class="sxs-lookup"><span data-stu-id="34c20-111">When the method returns, *pszFilePath* points to the memory location of the new buffer.</span></span> <span data-ttu-id="34c20-112">El autor de la llamada es responsable de llamar a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="34c20-112">The caller is responsible for calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory.</span></span>

<span data-ttu-id="34c20-113">¿Por qué COM define sus propias funciones de asignación de memoria?</span><span class="sxs-lookup"><span data-stu-id="34c20-113">Why does COM define its own memory allocation functions?</span></span> <span data-ttu-id="34c20-114">Una razón es proporcionar una capa de abstracción sobre el asignador del montón.</span><span class="sxs-lookup"><span data-stu-id="34c20-114">One reason is to provide an abstraction layer over the heap allocator.</span></span> <span data-ttu-id="34c20-115">De lo contrario, algunos métodos podrían llamar a **malloc** mientras que otros llamados **New**.</span><span class="sxs-lookup"><span data-stu-id="34c20-115">Otherwise, some methods might call **malloc** while others called **new**.</span></span> <span data-ttu-id="34c20-116">Después, el programa tendría que llamar a **Free** en algunos casos y **eliminar** en otros, y realizar un seguimiento de todo lo haría rápidamente.</span><span class="sxs-lookup"><span data-stu-id="34c20-116">Then your program would need to call **free** in some cases and **delete** in others, and keeping track of it all would quickly become impossible.</span></span> <span data-ttu-id="34c20-117">Las funciones de asignación COM crean un enfoque uniforme.</span><span class="sxs-lookup"><span data-stu-id="34c20-117">The COM allocation functions create a uniform approach.</span></span>

<span data-ttu-id="34c20-118">Otro aspecto que se debe tener en cuenta es el hecho de que COM es un estándar *binario* , por lo que no está asociado a un lenguaje de programación determinado.</span><span class="sxs-lookup"><span data-stu-id="34c20-118">Another consideration is the fact that COM is a *binary* standard, so it is not tied to a particular programming language.</span></span> <span data-ttu-id="34c20-119">Por lo tanto, COM no puede depender de ninguna forma específica del lenguaje de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="34c20-119">Therefore, COM cannot rely on any language-specific form of memory allocation.</span></span>

## <a name="next"></a><span data-ttu-id="34c20-120">Siguientes</span><span class="sxs-lookup"><span data-stu-id="34c20-120">Next</span></span>

[<span data-ttu-id="34c20-121">Prácticas de codificación COM</span><span class="sxs-lookup"><span data-stu-id="34c20-121">COM Coding Practices</span></span>](com-coding-practices.md)

 

 