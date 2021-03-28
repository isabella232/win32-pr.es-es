---
title: Características de Direct3D 11,3
description: En las secciones siguientes se describe la funcionalidad que se ha agregado en Direct3D 11,3. Estas características también están disponibles en Direct3D 12.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421658"
---
# <a name="direct3d-113-features"></a><span data-ttu-id="32a3c-104">Características de Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="32a3c-104">Direct3D 11.3 Features</span></span>

<span data-ttu-id="32a3c-105">En las secciones siguientes se describe la funcionalidad que se ha agregado en Direct3D 11,3.</span><span class="sxs-lookup"><span data-stu-id="32a3c-105">The following sections describe the functionality has been added in Direct3D 11.3.</span></span> <span data-ttu-id="32a3c-106">Estas características también están disponibles en Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="32a3c-106">These features are also available in Direct3D 12.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="32a3c-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="32a3c-107">In this section</span></span>



| <span data-ttu-id="32a3c-108">Tema</span><span class="sxs-lookup"><span data-stu-id="32a3c-108">Topic</span></span>                                                                                               | <span data-ttu-id="32a3c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="32a3c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32a3c-110">Rasterización conservadora</span><span class="sxs-lookup"><span data-stu-id="32a3c-110">Conservative Rasterization</span></span>](conservative-rasterization.md)<br/>                             | <span data-ttu-id="32a3c-111">La rasterización conservadora agrega cierta certeza a la representación en píxeles, lo que resulta útil en especial a los algoritmos de detección de colisiones.</span><span class="sxs-lookup"><span data-stu-id="32a3c-111">Conservative rasterization adds some certainty to pixel rendering, which is helpful in particular to collision detection algorithms.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="32a3c-112">Asignación de textura predeterminada</span><span class="sxs-lookup"><span data-stu-id="32a3c-112">Default Texture Mapping</span></span>](default-texture-mapping.md)<br/>                                   | <span data-ttu-id="32a3c-113">El uso de la asignación de texturas predeterminada reduce la copia y el uso de memoria mientras se comparten datos de imagen entre la GPU y la CPU.</span><span class="sxs-lookup"><span data-stu-id="32a3c-113">The use of default texture mapping reduces copying and memory usage while sharing image data between the GPU and the CPU.</span></span> <span data-ttu-id="32a3c-114">Sin embargo, solo se debe usar en situaciones específicas.</span><span class="sxs-lookup"><span data-stu-id="32a3c-114">However, it should only be used in specific situations.</span></span> <span data-ttu-id="32a3c-115">El diseño de swizzle estándar evita copiar o permutación datos en varios diseños.</span><span class="sxs-lookup"><span data-stu-id="32a3c-115">The standard swizzle layout avoids copying or swizzling data in multiple layouts.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="32a3c-116">Vistas de orden de rasterizador</span><span class="sxs-lookup"><span data-stu-id="32a3c-116">Rasterizer Order Views</span></span>](rasterizer-order-views.md)<br/>                                     | <span data-ttu-id="32a3c-117">Las vistas ordenadas de rasterizador (ROVs) permiten que el código del sombreador de píxeles marque los enlaces de UAV con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para UAVs.</span><span class="sxs-lookup"><span data-stu-id="32a3c-117">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="32a3c-118">Esto permite que funcionen los algoritmos de transparencia independiente de orden (OIT), que proporcionan resultados de representación mucho mejores cuando varios objetos transparentes están alineados entre sí en una vista.</span><span class="sxs-lookup"><span data-stu-id="32a3c-118">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span> <br/> |
| [<span data-ttu-id="32a3c-119">Valor de la referencia de galería de símbolos especificado por el sombreador</span><span class="sxs-lookup"><span data-stu-id="32a3c-119">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)<br/> | <span data-ttu-id="32a3c-120">Habilitar los sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control pormenorizado muy fino sobre las operaciones de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="32a3c-120">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="32a3c-121">Cargas de vista de acceso no ordenada con tipo</span><span class="sxs-lookup"><span data-stu-id="32a3c-121">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)<br/>               | <span data-ttu-id="32a3c-122">La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad para que un sombreador lea desde un UAV con un formato de DXGI específico \_ .</span><span class="sxs-lookup"><span data-stu-id="32a3c-122">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="32a3c-123">Arquitectura de memoria unificada</span><span class="sxs-lookup"><span data-stu-id="32a3c-123">Unified Memory Architecture</span></span>](unified-memory-architecture.md)<br/>                           | <span data-ttu-id="32a3c-124">La consulta de si se admite la arquitectura de memoria unificada (UMA) puede ayudar a determinar cómo administrar algunos recursos.</span><span class="sxs-lookup"><span data-stu-id="32a3c-124">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="32a3c-125">Recursos en mosaico de volumen</span><span class="sxs-lookup"><span data-stu-id="32a3c-125">Volume Tiled Resources</span></span>](volume-tiled-resources.md)<br/>                                     | <span data-ttu-id="32a3c-126">Las texturas de volumen (3D) se pueden usar como recursos en mosaico, teniendo en cuenta que la resolución de mosaicos es tridimensional.</span><span class="sxs-lookup"><span data-stu-id="32a3c-126">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="32a3c-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32a3c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32a3c-128">Novedades de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="32a3c-128">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





