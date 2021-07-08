---
title: Administración de la memoria en Direct3D 12
description: El traslado a D3D12 implica realizar la sincronización y administración adecuadas de la residencia de memoria.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b8091c2893f8906fe2ab5baadbf1288a1474cd
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481810"
---
# <a name="memory-management-in-direct3d-12"></a><span data-ttu-id="1b9c6-103">Administración de la memoria en Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1b9c6-103">Memory Management in Direct3D 12</span></span>

<span data-ttu-id="1b9c6-104">El traslado a D3D12 implica realizar la sincronización y administración adecuadas de la residencia de memoria.</span><span class="sxs-lookup"><span data-stu-id="1b9c6-104">Moving to D3D12 involves doing proper synchronization and management of memory residency.</span></span> <span data-ttu-id="1b9c6-105">La administración de la residencia de memoria significa que se debe realizar aún más sincronización.</span><span class="sxs-lookup"><span data-stu-id="1b9c6-105">Managing memory residency means even more synchronization must be done.</span></span> <span data-ttu-id="1b9c6-106">En esta sección se tratan las estrategias de administración de memoria y la suballocation dentro de montones y búferes.</span><span class="sxs-lookup"><span data-stu-id="1b9c6-106">This section covers memory management strategies, and suballocation within heaps and buffers.</span></span>

-   [<span data-ttu-id="1b9c6-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1b9c6-107">In this section</span></span>](#in-this-section)
-   [<span data-ttu-id="1b9c6-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b9c6-108">Related topics</span></span>](#related-topics)

## <a name="in-this-section"></a><span data-ttu-id="1b9c6-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1b9c6-109">In this section</span></span>



| <span data-ttu-id="1b9c6-110">Tema</span><span class="sxs-lookup"><span data-stu-id="1b9c6-110">Topic</span></span>                                                                       | <span data-ttu-id="1b9c6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b9c6-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b9c6-112">Estrategias de administración de la memoria</span><span class="sxs-lookup"><span data-stu-id="1b9c6-112">Memory Management Strategies</span></span>](memory-management-strategies.md)<br/> | <span data-ttu-id="1b9c6-113">Un administrador de memoria para Direct3D 12 podría complicarse rápidamente con todos los distintos niveles de compatibilidad, para adaptadores UMA o discretos (no UMA) y con una gran variedad de diferencias de arquitectura entre los adaptadores de GPU.</span><span class="sxs-lookup"><span data-stu-id="1b9c6-113">A memory manager for Direct3D 12 could get very complicated quickly with all the different tiers of support, for UMA or discrete (non-UMA) adapters, and with a considerable range of architecture differences between GPU adapters.</span></span><br/> <span data-ttu-id="1b9c6-114">La estrategia recomendada para la administración de memoria de Direct3D 12, descrita en esta sección, es "clasificar, presupuesto y flujo".</span><span class="sxs-lookup"><span data-stu-id="1b9c6-114">The recommended strategy for Direct3D 12 memory management , described in this section, is "classify, budget and stream".</span></span><br/> |
| [<span data-ttu-id="1b9c6-115">Subasignación en los búferes</span><span class="sxs-lookup"><span data-stu-id="1b9c6-115">Suballocation Within Buffers</span></span>](large-buffers.md)<br/>                | <span data-ttu-id="1b9c6-116">Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU.</span><span class="sxs-lookup"><span data-stu-id="1b9c6-116">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="1b9c6-117">En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.</span><span class="sxs-lookup"><span data-stu-id="1b9c6-117">This section covers four common scenarios for the use and management of resources and buffers.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="1b9c6-118">Subasignación en los búferes</span><span class="sxs-lookup"><span data-stu-id="1b9c6-118">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)<br/>     | <span data-ttu-id="1b9c6-119">Los montones de recursos transfieren datos de la CPU a la GPU (carga) y de la GPU a la CPU (read back).</span><span class="sxs-lookup"><span data-stu-id="1b9c6-119">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span> <br/>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="1b9c6-120">Residencia</span><span class="sxs-lookup"><span data-stu-id="1b9c6-120">Residency</span></span>](residency.md)<br/>                                       | <span data-ttu-id="1b9c6-121">Se considera que un objeto es *residentes cuando* la GPU puede acceder a él.</span><span class="sxs-lookup"><span data-stu-id="1b9c6-121">An object is considered to be *resident* when it is accessible by the GPU.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="1b9c6-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b9c6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b9c6-123">Guía de programación de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1b9c6-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="1b9c6-124">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="1b9c6-124">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 





