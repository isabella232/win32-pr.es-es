---
title: Administración de memoria en WOW64
description: La administración de memoria bajo WOW64 depende de la arquitectura del procesador.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64 bits programación de Windows, administración de memoria
- Administración de memoria 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8602bf6e7e7d9e55894215938932559cfadc6848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421273"
---
# <a name="memory-management-under-wow64"></a><span data-ttu-id="df7ec-105">Administración de memoria en WOW64</span><span class="sxs-lookup"><span data-stu-id="df7ec-105">Memory Management Under WOW64</span></span>

<span data-ttu-id="df7ec-106">La administración de memoria bajo WOW64 depende de la arquitectura del procesador.</span><span class="sxs-lookup"><span data-stu-id="df7ec-106">Memory management under WOW64 depends on the processor architecture.</span></span>

## <a name="itanium-support"></a><span data-ttu-id="df7ec-107">Compatibilidad con Itanium</span><span class="sxs-lookup"><span data-stu-id="df7ec-107">Itanium Support</span></span>

<span data-ttu-id="df7ec-108">WOW64 simula páginas de 4 KB sobre las páginas nativas de 8 KB que usa el procesador Itanium.</span><span class="sxs-lookup"><span data-stu-id="df7ec-108">WOW64 simulates 4 KB pages on top of the native 8 KB pages that the Itanium processor uses.</span></span> <span data-ttu-id="df7ec-109">El procesador ayuda a proporcionar una simulación excelente con poca sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="df7ec-109">The processor assists by providing excellent simulation with low overhead.</span></span> <span data-ttu-id="df7ec-110">El código de simulación no puede controlar los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="df7ec-110">The simulation code cannot handle the following cases:</span></span>

-   <span data-ttu-id="df7ec-111">Seguimiento de escritura.</span><span class="sxs-lookup"><span data-stu-id="df7ec-111">Write tracking.</span></span> <span data-ttu-id="df7ec-112">Las funciones [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) y [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) se implementan en el kernel con la granularidad de tamaño de página nativa, lo que significa que la simulación de páginas de WOW64 de 4 KB no puede determinar qué páginas de 4 KB simuladas se escriben en la página de 8 KB subyacente.</span><span class="sxs-lookup"><span data-stu-id="df7ec-112">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are implemented in the kernel using native page-size granularity, which means the WOW64 4 KB page simulation cannot determine which simulated 4 KB pages are written within the underlying 8 KB page.</span></span>
-   <span data-ttu-id="df7ec-113">[Extensiones de ventana de dirección (AWE)](/windows/desktop/Memory/address-windowing-extensions).</span><span class="sxs-lookup"><span data-stu-id="df7ec-113">[Address Windowing Extensions (AWE)](/windows/desktop/Memory/address-windowing-extensions).</span></span> <span data-ttu-id="df7ec-114">Las funciones AWE operan en números de página y no hay forma de asignar números de página de 64 bits a números de página de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="df7ec-114">The AWE functions operate on page numbers, and there is no way to map 64-bit page numbers to 32-bit page numbers.</span></span>
-   <span data-ttu-id="df7ec-115">Alineación de la sección.</span><span class="sxs-lookup"><span data-stu-id="df7ec-115">Section alignment.</span></span> <span data-ttu-id="df7ec-116">En el caso de las imágenes ejecutables con una alineación de sección inferior a 8 KB (el valor predeterminado es 4 KB para imágenes x86), WOW64 debe haber modificado todas las páginas de imagen.</span><span class="sxs-lookup"><span data-stu-id="df7ec-116">For executable images with section alignment smaller than 8 KB (the default is 4 KB for x86 images), WOW64 must dirty all image pages.</span></span> <span data-ttu-id="df7ec-117">Esto copia eficazmente cada página en el archivo de paginación y evita que las páginas de imagen de solo lectura se compartan entre los procesos.</span><span class="sxs-lookup"><span data-stu-id="df7ec-117">This effectively copies each page to the page file, and prevents read-only image pages from being shared between processes.</span></span>
-   <span data-ttu-id="df7ec-118">No se admiten las funciones [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) y [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .</span><span class="sxs-lookup"><span data-stu-id="df7ec-118">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are not supported.</span></span>

## <a name="x64-and-arm64-support"></a><span data-ttu-id="df7ec-119">Compatibilidad con x64 y ARM64</span><span class="sxs-lookup"><span data-stu-id="df7ec-119">x64 and ARM64 Support</span></span>

<span data-ttu-id="df7ec-120">El tamaño de página nativo es 4 KB.</span><span class="sxs-lookup"><span data-stu-id="df7ec-120">The native page size is 4 KB.</span></span> <span data-ttu-id="df7ec-121">Por lo tanto, se admite lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="df7ec-121">Therefore, the following are supported:</span></span>

-   <span data-ttu-id="df7ec-122">Se admiten las funciones [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) y [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) .</span><span class="sxs-lookup"><span data-stu-id="df7ec-122">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are supported.</span></span>
-   <span data-ttu-id="df7ec-123">Se admiten las funciones [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) y [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .</span><span class="sxs-lookup"><span data-stu-id="df7ec-123">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are supported.</span></span>
-   <span data-ttu-id="df7ec-124">El uso de direcciones grandes tiene ventajas porque x64 WOW64 admite un espacio de direcciones virtuales de 4 GB.</span><span class="sxs-lookup"><span data-stu-id="df7ec-124">There are advantages to using large addresses because x64 WOW64 supports a 4 GB virtual address space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df7ec-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df7ec-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df7ec-126">Límites de memoria para las versiones de Windows</span><span class="sxs-lookup"><span data-stu-id="df7ec-126">Memory Limits for Windows Releases</span></span>](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[<span data-ttu-id="df7ec-127">Optimización de la RAM de 4GT</span><span class="sxs-lookup"><span data-stu-id="df7ec-127">4GT RAM Tuning</span></span>](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 