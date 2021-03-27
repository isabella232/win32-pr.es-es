---
title: Acceso de canalización a recursos en mosaico
description: Los recursos en mosaico se pueden usar en las vistas de recursos del sombreador (SRV), las vistas de destino de representación (RTV), las vistas de estarcido de profundidad (DSV) y las vistas de acceso desordenado (UAV), así como algunos puntos de enlace donde no se usan vistas, como los enlaces de búfer de vértices.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793090"
---
# <a name="pipeline-access-to-tiled-resources"></a><span data-ttu-id="ea7e7-103">Acceso de canalización a recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="ea7e7-103">Pipeline access to tiled resources</span></span>

<span data-ttu-id="ea7e7-104">Los recursos en mosaico se pueden usar en las vistas de recursos del sombreador (SRV), las vistas de destino de representación (RTV), las vistas de estarcido de profundidad (DSV) y las vistas de acceso desordenado (UAV), así como algunos puntos de enlace donde no se usan vistas, como los enlaces de búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="ea7e7-104">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <span data-ttu-id="ea7e7-105">Para obtener la lista de enlaces admitidos, consulte [parámetros de creación de recursos en mosaico](tiled-resource-creation-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ea7e7-105">For the list of supported bindings, see [Tiled resource creation parameters](tiled-resource-creation-parameters.md).</span></span> <span data-ttu-id="ea7e7-106">\*Las operaciones de copia también funcionan en recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="ea7e7-106">Copy\* operations also work on tiled resources.</span></span>

<span data-ttu-id="ea7e7-107">Si varias coordenadas del mosaico de una o varias vistas están enlazadas a la misma ubicación de memoria, las lecturas y escrituras de diferentes rutas de acceso a la misma memoria se producirán en un orden no determinista y no repetible de accesos a la memoria.</span><span class="sxs-lookup"><span data-stu-id="ea7e7-107">If multiple tile coordinates in one or more views is bound to the same memory location, reads and writes from different paths to the same memory will occur in a non-deterministic and non-repeatable order of memory accesses.</span></span>

<span data-ttu-id="ea7e7-108">Si todos los mosaicos detrás de una superficie de acceso a memoria desde un sombreador se asignan a mosaicos únicos, el comportamiento es idéntico en todas las implementaciones a la superficie que tiene el mismo contenido de memoria en un modo no mosaico.</span><span class="sxs-lookup"><span data-stu-id="ea7e7-108">If all tiles behind a memory access footprint from a shader are mapped to unique tiles, behavior is identical on all implementations to the surface having the same memory contents in a non-tiled fashion.</span></span>

<span data-ttu-id="ea7e7-109">En esta sección se proporciona más información sobre el acceso de canalización a los recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="ea7e7-109">This section provides more info about pipeline access to tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ea7e7-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ea7e7-110">In this section</span></span>



| <span data-ttu-id="ea7e7-111">Tema</span><span class="sxs-lookup"><span data-stu-id="ea7e7-111">Topic</span></span>                                                                                                              | <span data-ttu-id="ea7e7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea7e7-112">Description</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea7e7-113">Comportamiento SRV con iconos sin asignar</span><span class="sxs-lookup"><span data-stu-id="ea7e7-113">SRV behavior with non-mapped tiles</span></span>](srv-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="ea7e7-114">El comportamiento de las lecturas de vista de recursos del sombreador (SRV) que impliquen mosaicos no asignados depende del nivel de compatibilidad de hardware.</span><span class="sxs-lookup"><span data-stu-id="ea7e7-114">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <br/>                                          |
| [<span data-ttu-id="ea7e7-115">Comportamiento UAV con iconos sin asignar</span><span class="sxs-lookup"><span data-stu-id="ea7e7-115">UAV behavior with non-mapped tiles</span></span>](uav-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="ea7e7-116">El comportamiento de las lecturas y escrituras de la vista de acceso desordenado (UAV) depende del nivel de compatibilidad de hardware.</span><span class="sxs-lookup"><span data-stu-id="ea7e7-116">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <br/>                                                            |
| [<span data-ttu-id="ea7e7-117">Comportamiento de rasterizador con iconos sin asignar</span><span class="sxs-lookup"><span data-stu-id="ea7e7-117">Rasterizer behavior with non-mapped tiles</span></span>](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | <span data-ttu-id="ea7e7-118">En esta sección se describe el comportamiento de rasterizador con mosaicos no asignados.</span><span class="sxs-lookup"><span data-stu-id="ea7e7-118">This section describes rasterizer behavior with non-mapped tiles.</span></span><br/>                                                                                              |
| [<span data-ttu-id="ea7e7-119">Limitaciones de acceso de iconos con asignaciones duplicadas</span><span class="sxs-lookup"><span data-stu-id="ea7e7-119">Tile access limitations with duplicate mappings</span></span>](tile-access-limitations-with-duplicate-mappings-.md)<br/> | <span data-ttu-id="ea7e7-120">En esta sección se describen las limitaciones de acceso a los mosaicos con asignaciones duplicadas.</span><span class="sxs-lookup"><span data-stu-id="ea7e7-120">This section describes tile access limitations with duplicate mappings.</span></span><br/>                                                                                        |
| [<span data-ttu-id="ea7e7-121">Características de muestreo de textura de recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="ea7e7-121">Tiled resources texture sampling features</span></span>](tiled-resources-texture-sampling-features.md)<br/>              | <span data-ttu-id="ea7e7-122">En esta sección se describen las características de muestreo de textura de recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="ea7e7-122">This section describes tiled resources texture sampling features.</span></span><br/>                                                                                              |
| [<span data-ttu-id="ea7e7-123">Exposición de recursos en mosaico de HLSL</span><span class="sxs-lookup"><span data-stu-id="ea7e7-123">HLSL tiled resources exposure</span></span>](hlsl-tiled-resources-exposure.md)<br/>                                      | <span data-ttu-id="ea7e7-124">Se requiere una nueva sintaxis de lenguaje de sombreado de alto nivel (HLSL) de Microsoft para admitir recursos en mosaico en el [modelo de sombreador 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).</span><span class="sxs-lookup"><span data-stu-id="ea7e7-124">New Microsoft High Level Shader Language (HLSL) syntax is required to support tiled resources in [Shader Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ea7e7-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea7e7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea7e7-126">Recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="ea7e7-126">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

