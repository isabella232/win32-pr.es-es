---
description: Asignador de memoria
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Asignador de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537804"
---
# <a name="memory-allocator"></a><span data-ttu-id="78854-103">Asignador de memoria</span><span class="sxs-lookup"><span data-stu-id="78854-103">Memory Allocator</span></span>

<span data-ttu-id="78854-104">El objeto de asignador de memoria asigna búferes para los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="78854-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="78854-105">Los filtros pueden utilizar este objeto para asignar búferes de memoria compartida; sin embargo, un filtro con requisitos especiales también puede implementar su propio objeto de asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="78854-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="78854-106">Cree este objeto llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="78854-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="78854-107">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="78854-107">Class Identifier</span></span> | <span data-ttu-id="78854-108">CLSID \_ MemoryAllocator</span><span class="sxs-lookup"><span data-stu-id="78854-108">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="78854-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="78854-109">Interfaces</span></span>       | [<span data-ttu-id="78854-110">**IMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="78854-110">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="78854-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78854-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78854-112">Objetos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="78854-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



