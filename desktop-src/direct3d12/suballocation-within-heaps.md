---
title: Subasignación dentro de montones
description: Los montones de recursos transfieren datos de la CPU a la GPU (carga) y de la GPU a la CPU (lectura inversa).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105027"
---
# <a name="suballocation-within-heaps"></a><span data-ttu-id="963bf-103">Subasignación dentro de montones</span><span class="sxs-lookup"><span data-stu-id="963bf-103">Suballocation Within Heaps</span></span>

<span data-ttu-id="963bf-104">Los montones de recursos transfieren datos de la CPU a la GPU (carga) y de la GPU a la CPU (lectura inversa).</span><span class="sxs-lookup"><span data-stu-id="963bf-104">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="963bf-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="963bf-105">In this section</span></span>



| <span data-ttu-id="963bf-106">Tema</span><span class="sxs-lookup"><span data-stu-id="963bf-106">Topic</span></span>                                                                                       | <span data-ttu-id="963bf-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="963bf-107">Description</span></span>                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="963bf-108">Alias de memoria y herencia de datos</span><span class="sxs-lookup"><span data-stu-id="963bf-108">Memory Aliasing and Data Inheritance</span></span>](memory-aliasing-and-data-inheritance.md)<br/> | <span data-ttu-id="963bf-109">Los recursos colocados y reservados pueden asignar un alias a la memoria física dentro de un montón.</span><span class="sxs-lookup"><span data-stu-id="963bf-109">Placed and reserved resource may alias physical memory within a heap.</span></span> <span data-ttu-id="963bf-110">Los recursos colocados permiten más escenarios de herencia de datos que los recursos reservados cuando el montón tiene establecida la marca compartida o cuando los recursos con alias tienen diseños de memoria totalmente definidos.</span><span class="sxs-lookup"><span data-stu-id="963bf-110">Placed resources enable more data inheritance scenarios than reserved resources when the heap has the shared flag set or when the aliased resources have fully defined memory layouts.</span></span> <br/> |
| [<span data-ttu-id="963bf-111">Montones compartidos</span><span class="sxs-lookup"><span data-stu-id="963bf-111">Shared Heaps</span></span>](shared-heaps.md)<br/>                                                 | <span data-ttu-id="963bf-112">Compartir es útil para arquitecturas multiproceso y multiadaptador.</span><span class="sxs-lookup"><span data-stu-id="963bf-112">Sharing is useful for multi-process and multi-adapter architectures.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="963bf-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="963bf-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="963bf-114">**ID3D12Device::CreateHeap**</span><span class="sxs-lookup"><span data-stu-id="963bf-114">**ID3D12Device::CreateHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[<span data-ttu-id="963bf-115">**ID3D12Heap**</span><span class="sxs-lookup"><span data-stu-id="963bf-115">**ID3D12Heap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[<span data-ttu-id="963bf-116">Administración de memoria</span><span class="sxs-lookup"><span data-stu-id="963bf-116">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





