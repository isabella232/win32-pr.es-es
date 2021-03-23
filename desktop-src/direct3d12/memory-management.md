---
title: Administración de memoria en Direct3D 12
description: Pasar a D3D12 implica realizar la sincronización y administración adecuadas de la residencia de memoria.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037a2d75adcde6ff03adf2ccee8ce30d33d090c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103926"
---
# <a name="memory-management-in-direct3d-12"></a><span data-ttu-id="5c797-103">Administración de memoria en Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5c797-103">Memory Management in Direct3D 12</span></span>

<span data-ttu-id="5c797-104">Pasar a D3D12 implica realizar la sincronización y administración adecuadas de la residencia de memoria.</span><span class="sxs-lookup"><span data-stu-id="5c797-104">Moving to D3D12 involves doing proper synchronization and management of memory residency.</span></span> <span data-ttu-id="5c797-105">La administración de la residencia de memoria significa que se debe realizar aún más sincronización.</span><span class="sxs-lookup"><span data-stu-id="5c797-105">Managing memory residency means even more synchronization must be done.</span></span> <span data-ttu-id="5c797-106">En esta sección se tratan las estrategias de administración de memoria y la subasignación en montones y búferes.</span><span class="sxs-lookup"><span data-stu-id="5c797-106">This section covers memory management strategies, and suballocation within heaps and buffers.</span></span>

-   [<span data-ttu-id="5c797-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5c797-107">In this section</span></span>](#in-this-section)
-   [<span data-ttu-id="5c797-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c797-108">Related topics</span></span>](#related-topics)

## <a name="in-this-section"></a><span data-ttu-id="5c797-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5c797-109">In this section</span></span>



| <span data-ttu-id="5c797-110">Tema</span><span class="sxs-lookup"><span data-stu-id="5c797-110">Topic</span></span>                                                                       | <span data-ttu-id="5c797-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c797-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c797-112">Estrategias de administración de memoria</span><span class="sxs-lookup"><span data-stu-id="5c797-112">Memory Management Strategies</span></span>](memory-management-strategies.md)<br/> | <span data-ttu-id="5c797-113">Un administrador de memoria para Direct3D 12 podría resultar muy complicado rápidamente con los distintos niveles de compatibilidad, para los adaptadores de UMA o discretos (no UMA), y con una gran variedad de diferencias de arquitectura entre los adaptadores de GPU.</span><span class="sxs-lookup"><span data-stu-id="5c797-113">A memory manager for Direct3D 12 could get very complicated quickly with all the different tiers of support, for UMA or discreet (non-UMA) adapters, and with a considerable range of architecture differences between GPU adapters.</span></span><br/> <span data-ttu-id="5c797-114">La estrategia recomendada para la administración de memoria de Direct3D 12, que se describe en esta sección, es "clasificación, presupuesto y flujo".</span><span class="sxs-lookup"><span data-stu-id="5c797-114">The recommended strategy for Direct3D 12 memory management , described in this section, is "classify, budget and stream".</span></span><br/> |
| [<span data-ttu-id="5c797-115">Subasignación dentro de búferes</span><span class="sxs-lookup"><span data-stu-id="5c797-115">Suballocation Within Buffers</span></span>](large-buffers.md)<br/>                | <span data-ttu-id="5c797-116">Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU.</span><span class="sxs-lookup"><span data-stu-id="5c797-116">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="5c797-117">En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.</span><span class="sxs-lookup"><span data-stu-id="5c797-117">This section covers four common scenarios for the use and management of resources and buffers.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="5c797-118">Subasignación dentro de montones</span><span class="sxs-lookup"><span data-stu-id="5c797-118">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)<br/>     | <span data-ttu-id="5c797-119">Los montones de recursos transfieren datos de la CPU a la GPU (carga) y de la GPU a la CPU (lectura inversa).</span><span class="sxs-lookup"><span data-stu-id="5c797-119">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span> <br/>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="5c797-120">Residencia</span><span class="sxs-lookup"><span data-stu-id="5c797-120">Residency</span></span>](residency.md)<br/>                                       | <span data-ttu-id="5c797-121">Un objeto se considera *residente* cuando es accesible para la GPU.</span><span class="sxs-lookup"><span data-stu-id="5c797-121">An object is considered to be *resident* when it is accessible by the GPU.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="5c797-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c797-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c797-123">Guía de programación de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5c797-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="5c797-124">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="5c797-124">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 





