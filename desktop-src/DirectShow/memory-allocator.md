---
description: Asignador de memoria
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Asignador de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909432"
---
# <a name="memory-allocator"></a><span data-ttu-id="bfbd8-103">Asignador de memoria</span><span class="sxs-lookup"><span data-stu-id="bfbd8-103">Memory Allocator</span></span>

<span data-ttu-id="bfbd8-104">El objeto Asignador de memoria asigna búferes para ejemplos multimedia.</span><span class="sxs-lookup"><span data-stu-id="bfbd8-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="bfbd8-105">Los filtros pueden usar este objeto para asignar búferes de memoria compartida. sin embargo, un filtro con requisitos especiales también puede implementar su propio objeto de asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="bfbd8-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="bfbd8-106">Cree este objeto mediante una llamada **a CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="bfbd8-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="bfbd8-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="bfbd8-107">Label</span></span> | <span data-ttu-id="bfbd8-108">Value</span><span class="sxs-lookup"><span data-stu-id="bfbd8-108">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="bfbd8-109">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="bfbd8-109">Class Identifier</span></span> | <span data-ttu-id="bfbd8-110">CLSID \_ MemoryAllocator</span><span class="sxs-lookup"><span data-stu-id="bfbd8-110">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="bfbd8-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="bfbd8-111">Interfaces</span></span>       | [<span data-ttu-id="bfbd8-112">**IMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="bfbd8-112">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="bfbd8-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bfbd8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfbd8-114">Objetos DirectShow</span><span class="sxs-lookup"><span data-stu-id="bfbd8-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



