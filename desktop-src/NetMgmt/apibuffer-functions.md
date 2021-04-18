---
title: Funciones de ApiBuffer
description: Las funciones de ApiBuffer de administración de red se usan para administrar la asignación de memoria utilizada por una aplicación con funciones de administración de red.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665848"
---
# <a name="apibuffer-functions"></a><span data-ttu-id="b9f4f-103">Funciones de ApiBuffer</span><span class="sxs-lookup"><span data-stu-id="b9f4f-103">ApiBuffer Functions</span></span>

<span data-ttu-id="b9f4f-104">Las funciones de ApiBuffer de administración de red se usan para administrar la asignación de memoria utilizada por una aplicación con funciones de administración de red.</span><span class="sxs-lookup"><span data-stu-id="b9f4f-104">The network management ApiBuffer functions are used to manage memory allocation used by an application with network management functions.</span></span> <span data-ttu-id="b9f4f-105">Sin embargo, en general, para otra memoria utilizada por una aplicación, debe usar las [funciones de administración de memoria](/windows/desktop/Memory/memory-management-functions) en lugar de estas funciones ApiBuffer.</span><span class="sxs-lookup"><span data-stu-id="b9f4f-105">However, in general, for other memory used by an application you should use the [memory management functions](/windows/desktop/Memory/memory-management-functions) instead of these ApiBuffer functions.</span></span>

<span data-ttu-id="b9f4f-106">A continuación se enumeran las funciones de ApiBuffer.</span><span class="sxs-lookup"><span data-stu-id="b9f4f-106">The ApiBuffer functions are listed following.</span></span>



| <span data-ttu-id="b9f4f-107">Función</span><span class="sxs-lookup"><span data-stu-id="b9f4f-107">Function</span></span>                                                 | <span data-ttu-id="b9f4f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9f4f-108">Description</span></span>                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9f4f-109">**NetApiBufferAllocate**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-109">**NetApiBufferAllocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | <span data-ttu-id="b9f4f-110">Asigna memoria del montón.</span><span class="sxs-lookup"><span data-stu-id="b9f4f-110">Allocates memory from the heap.</span></span> <span data-ttu-id="b9f4f-111">Llame a esta función cuando necesite compatibilidad con la función **NetApiBufferFree** .</span><span class="sxs-lookup"><span data-stu-id="b9f4f-111">Call this function when you require compatibility with the **NetApiBufferFree** function.</span></span> |
| [<span data-ttu-id="b9f4f-112">**NetApiBufferFree**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-112">**NetApiBufferFree**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | <span data-ttu-id="b9f4f-113">Libera memoria asignada por la función **NetApiBufferAllocate** y otras funciones de administración de redes.</span><span class="sxs-lookup"><span data-stu-id="b9f4f-113">Frees memory allocated by the **NetApiBufferAllocate** function and other network management functions.</span></span>                   |
| [<span data-ttu-id="b9f4f-114">**NetApiBufferReallocate**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-114">**NetApiBufferReallocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | <span data-ttu-id="b9f4f-115">Cambia el tamaño de un búfer asignado por una llamada a la función **NetApiBufferAllocate** .</span><span class="sxs-lookup"><span data-stu-id="b9f4f-115">Changes the size of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                                |
| [<span data-ttu-id="b9f4f-116">**NetApiBufferSize**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-116">**NetApiBufferSize**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | <span data-ttu-id="b9f4f-117">Devuelve el tamaño, en bytes, de un búfer asignado por una llamada a la función **NetApiBufferAllocate** .</span><span class="sxs-lookup"><span data-stu-id="b9f4f-117">Returns the size, in bytes, of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                     |



 

<span data-ttu-id="b9f4f-118">En el caso de las funciones de uso remoto que devuelven información al llamador, la biblioteca en tiempo de ejecución de RPC asigna el búfer que contiene la información de devolución.</span><span class="sxs-lookup"><span data-stu-id="b9f4f-118">For remotable functions that return information to the caller, the RPC run-time library allocates the buffer containing the return information.</span></span> <span data-ttu-id="b9f4f-119">Cuando el autor de la llamada ha terminado de procesar la información, debe llamar a la función [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) para liberar el búfer asignado.</span><span class="sxs-lookup"><span data-stu-id="b9f4f-119">When the caller has finished processing the information, it must call the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function to free the allocated buffer.</span></span>

 

 