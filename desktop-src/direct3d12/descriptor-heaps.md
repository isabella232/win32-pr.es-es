---
title: Montones de descriptores
description: Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104865"
---
# <a name="descriptor-heaps"></a><span data-ttu-id="d2ca7-103">Montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="d2ca7-103">Descriptor Heaps</span></span>

<span data-ttu-id="d2ca7-104">Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor.</span><span class="sxs-lookup"><span data-stu-id="d2ca7-104">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d2ca7-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d2ca7-105">In this section</span></span>



| <span data-ttu-id="d2ca7-106">Tema</span><span class="sxs-lookup"><span data-stu-id="d2ca7-106">Topic</span></span>                                                                                             | <span data-ttu-id="d2ca7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2ca7-107">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2ca7-108">Información general sobre montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="d2ca7-108">Descriptor Heaps Overview</span></span>](descriptor-heaps-overview.md)<br/>                             | <span data-ttu-id="d2ca7-109">Los montones descriptores contienen muchos tipos de objetos que no forman parte de un objeto de estado de canalización (PSO), como las vistas de recursos del sombreador (SRVs), las vistas de acceso desordenado (UAVs), las vistas de búfer de constantes (CBVs) y los muestreadores.</span><span class="sxs-lookup"><span data-stu-id="d2ca7-109">Descriptor heaps contain many object types that are not part of a Pipeline State Object (PSO), such as Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers.</span></span> <br/>                |
| [<span data-ttu-id="d2ca7-110">Niveles de hardware</span><span class="sxs-lookup"><span data-stu-id="d2ca7-110">Hardware Tiers</span></span>](hardware-support.md)<br/>                                                 | <span data-ttu-id="d2ca7-111">Los niveles de hardware del nivel 1 al nivel 3 tienen recursos crecientes disponibles para la canalización.</span><span class="sxs-lookup"><span data-stu-id="d2ca7-111">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span> <br/>                                                                                                                              |
| [<span data-ttu-id="d2ca7-112">Montones de descriptor visibles del sombreador</span><span class="sxs-lookup"><span data-stu-id="d2ca7-112">Shader Visible Descriptor Heaps</span></span>](shader-visible-descriptor-heaps.md)<br/>                 | <span data-ttu-id="d2ca7-113">Los montones de descriptor visibles del sombreador, son montones de descriptor a los que pueden hacer referencia los sombreadores a través de tablas de descriptores.</span><span class="sxs-lookup"><span data-stu-id="d2ca7-113">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="d2ca7-114">Montones de descriptor visibles sin sombreador</span><span class="sxs-lookup"><span data-stu-id="d2ca7-114">Non Shader Visible Descriptor Heaps</span></span>](non-shader-visible-descriptor-heaps.md)<br/>         | <span data-ttu-id="d2ca7-115">Los sombreadores no pueden hacer referencia a algunos montones de descriptor a través de tablas de descriptores, pero existen para ayudar a la aplicación a ensayar los descriptores antes de grabar una lista de comandos o porque no se requiere ningún montón visible del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d2ca7-115">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span><br/> |
| [<span data-ttu-id="d2ca7-116">Crear montones de descriptor</span><span class="sxs-lookup"><span data-stu-id="d2ca7-116">Creating Descriptor Heaps</span></span>](creating-descriptor-heaps.md)<br/>                             | <span data-ttu-id="d2ca7-117">Para crear y configurar un montón de descriptores, debe seleccionar un tipo de montón de descriptores, determinar el número de descriptores que contiene y establecer marcas que indiquen si es visible para la CPU o el sombreador.</span><span class="sxs-lookup"><span data-stu-id="d2ca7-117">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span> <br/>                    |
| [<span data-ttu-id="d2ca7-118">Establecer y rellenar montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="d2ca7-118">Setting and Populating Descriptor Heaps</span></span>](setting-descriptor-heaps.md)<br/>                | <span data-ttu-id="d2ca7-119">Los tipos de montón descriptor que se pueden establecer en una lista de comandos son aquellos que contienen descriptores para los que se pueden usar tablas de descriptor (como máximo una de cada cada vez).</span><span class="sxs-lookup"><span data-stu-id="d2ca7-119">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span> <br/>                                                        |
| [<span data-ttu-id="d2ca7-120">Resumen de la capacidad de configurar el montón de descriptores</span><span class="sxs-lookup"><span data-stu-id="d2ca7-120">Descriptor Heap Configurability Summary</span></span>](descriptor-heap-configurability-summary.md)<br/> | <span data-ttu-id="d2ca7-121">En la tabla siguiente se resume la información sobre el sombreador y la compatibilidad con el montón visible de no sombreador.</span><span class="sxs-lookup"><span data-stu-id="d2ca7-121">The following table summarizes information about Shader and non-Shader visible heap support.</span></span><br/>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="d2ca7-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d2ca7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2ca7-123">Descriptores de</span><span class="sxs-lookup"><span data-stu-id="d2ca7-123">Descriptors</span></span>](descriptors.md)
</dt> <dt>

[<span data-ttu-id="d2ca7-124">Tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="d2ca7-124">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="d2ca7-125">**ID3D12DescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="d2ca7-125">**ID3D12DescriptorHeap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[<span data-ttu-id="d2ca7-126">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="d2ca7-126">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="d2ca7-127">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="d2ca7-127">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





