---
title: Recursos en mosaico de volumen (Direct3D 12)
description: Las texturas de volumen (3D) se pueden usar como recursos en mosaico, teniendo en cuenta que la resolución de mosaicos es tridimensional.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42679155bbd8dc2cec560d2724e430c860f54bc0
ms.sourcegitcommit: 05e7efd3d8de6926d08802669f37e825a2fa2f46
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2020
ms.locfileid: "104549080"
---
# <a name="volume-tiled-resources-direct3d-12"></a><span data-ttu-id="cf0b1-103">Recursos en mosaico de volumen (Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-103">Volume tiled resources (Direct3D 12)</span></span>

<span data-ttu-id="cf0b1-104">Las texturas de volumen (3D) se pueden usar como recursos en mosaico, teniendo en cuenta que la resolución de mosaicos es tridimensional.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="cf0b1-105">Información general</span><span class="sxs-lookup"><span data-stu-id="cf0b1-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="cf0b1-106">API de recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="cf0b1-106">Tiled Resource APIs</span></span>](#tiled-resource-apis)
-   [<span data-ttu-id="cf0b1-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf0b1-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="cf0b1-108">Información general</span><span class="sxs-lookup"><span data-stu-id="cf0b1-108">Overview</span></span>

<span data-ttu-id="cf0b1-109">Los recursos en mosaico desacoplan un objeto de recurso D3D de la memoria de respaldo (los recursos en el pasado tenían una relación de 1:1 con la memoria de respaldo).</span><span class="sxs-lookup"><span data-stu-id="cf0b1-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="cf0b1-110">Esto permite una variedad de escenarios interesantes, como la transmisión por secuencias de datos de textura y la reutilización o reducción del uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage.</span></span>

<span data-ttu-id="cf0b1-111">los recursos en mosaico de textura 2D se admiten en D3D 11.2.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="cf0b1-112">La compatibilidad opcional con las texturas en mosaico 3D está disponible para D3D12 y D3D 11.3 (consulte el [**nivel de recursos en mosaico de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).</span><span class="sxs-lookup"><span data-stu-id="cf0b1-112">Optional support for 3D tiled textures is available for D3D12 and D3D11.3 (refer to [**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).</span></span>

<span data-ttu-id="cf0b1-113">Las dimensiones de recursos típicas que se usan en el mosaico son 4 x 4 mosaicos para las texturas 2D y 4 x 4 x 4 mosaicos para las texturas 3D.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



| <span data-ttu-id="cf0b1-114">Bits/píxel (1 ejemplo/píxel)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="cf0b1-115">Dimensiones del mosaico (píxeles, w x h x d)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-115">Tile dimensions (pixels, w x h x d)</span></span> |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="cf0b1-116">8</span><span class="sxs-lookup"><span data-stu-id="cf0b1-116">8</span></span>                           | <span data-ttu-id="cf0b1-117">64x32x32</span><span class="sxs-lookup"><span data-stu-id="cf0b1-117">64x32x32</span></span>                            |
| <span data-ttu-id="cf0b1-118">16</span><span class="sxs-lookup"><span data-stu-id="cf0b1-118">16</span></span>                          | <span data-ttu-id="cf0b1-119">32x32x32</span><span class="sxs-lookup"><span data-stu-id="cf0b1-119">32x32x32</span></span>                            |
| <span data-ttu-id="cf0b1-120">32</span><span class="sxs-lookup"><span data-stu-id="cf0b1-120">32</span></span>                          | <span data-ttu-id="cf0b1-121">32x32x16</span><span class="sxs-lookup"><span data-stu-id="cf0b1-121">32x32x16</span></span>                            |
| <span data-ttu-id="cf0b1-122">64</span><span class="sxs-lookup"><span data-stu-id="cf0b1-122">64</span></span>                          | <span data-ttu-id="cf0b1-123">32x16x16</span><span class="sxs-lookup"><span data-stu-id="cf0b1-123">32x16x16</span></span>                            |
| <span data-ttu-id="cf0b1-124">128</span><span class="sxs-lookup"><span data-stu-id="cf0b1-124">128</span></span>                         | <span data-ttu-id="cf0b1-125">16x16x16</span><span class="sxs-lookup"><span data-stu-id="cf0b1-125">16x16x16</span></span>                            |
| <span data-ttu-id="cf0b1-126">BC 1, 4</span><span class="sxs-lookup"><span data-stu-id="cf0b1-126">BC 1,4</span></span>                      | <span data-ttu-id="cf0b1-127">128x64x16</span><span class="sxs-lookup"><span data-stu-id="cf0b1-127">128x64x16</span></span>                           |
| <span data-ttu-id="cf0b1-128">BC 2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="cf0b1-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="cf0b1-129">64x64x16</span><span class="sxs-lookup"><span data-stu-id="cf0b1-129">64x64x16</span></span>                            |

<span data-ttu-id="cf0b1-130">Tenga en cuenta que los siguientes formatos no se admiten con recursos en mosaico: formatos de 96bpp, formatos de vídeo, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 UNORM \_ .</span><span class="sxs-lookup"><span data-stu-id="cf0b1-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="cf0b1-131">En los diagramas siguientes, el gris oscuro representa los mosaicos NULOs.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="cf0b1-132">Asignación predeterminada de recursos en mosaico 3D de textura (el MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="cf0b1-133">Asignación predeterminada de recursos en mosaico 3D de textura (segundo MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="cf0b1-134">Recurso en mosaico 3D de textura (el MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="cf0b1-135">Recurso en mosaico 3D de textura (segundo MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="cf0b1-136">Recurso en mosaico 3D de textura (mosaico único)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="cf0b1-137">Recurso en mosaico 3D de textura (cuadro uniforme)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="cf0b1-138">Asignación predeterminada de recursos en mosaico 3D de textura (el MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![asignación predeterminada de un recurso de tres dimensiones en mosaico](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="cf0b1-140">Asignación predeterminada de recursos en mosaico 3D de textura (segundo MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![muestra el segundo MIP más detallado](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="cf0b1-142">Recurso en mosaico 3D de textura (el MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="cf0b1-143">El código siguiente configura un recurso en mosaico 3D en el MIP más detallado.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![MIP más detallado para una textura tridimensional](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="cf0b1-145">Recurso en mosaico 3D de textura (segundo MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="cf0b1-146">El código siguiente configura un recurso en mosaico 3D y el segundo MIP más detallado:</span><span class="sxs-lookup"><span data-stu-id="cf0b1-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![segundo MIP más detallado para una textura tridimensional](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="cf0b1-148">Recurso en mosaico 3D de textura (mosaico único)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="cf0b1-149">En el código siguiente se configura un recurso de icono único:</span><span class="sxs-lookup"><span data-stu-id="cf0b1-149">The following code sets up a Single Tile resource:</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![un único recurso de tres dimensiones en mosaico](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="cf0b1-151">Recurso en mosaico 3D de textura (cuadro uniforme)</span><span class="sxs-lookup"><span data-stu-id="cf0b1-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="cf0b1-152">En el código siguiente se configura un recurso de cuadro uniforme en mosaico (tenga en cuenta la instrucción `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="cf0b1-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![cuadro uniforme](images/vtr-tex3d-uniform.png)

## <a name="tiled-resource-apis"></a><span data-ttu-id="cf0b1-154">API de recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="cf0b1-154">Tiled Resource APIs</span></span>

<span data-ttu-id="cf0b1-155">Se usan las mismas llamadas API para los recursos en mosaico 2D y 3D:</span><span class="sxs-lookup"><span data-stu-id="cf0b1-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="cf0b1-156">Enumeraciones</span><span class="sxs-lookup"><span data-stu-id="cf0b1-156">Enums</span></span>

-   <span data-ttu-id="cf0b1-157">[**D3D12 \_ Nivel de \_ recursos \_ en mosaico**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determina el nivel de compatibilidad con los recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-157">[**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="cf0b1-158">[**D3D12 \_ DAR formato al \_ cliente2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : se usa para probar la compatibilidad con los recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-158">[**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="cf0b1-159">[**D3D12 \_ \_ \_ \_ Marcas de nivel de calidad Multimuestra**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determina la compatibilidad con los recursos en mosaico en un recurso de muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-159">[**D3D12\_MULTISAMPLE\_QUALITY\_LEVEL\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="cf0b1-160">[**D3D12 \_ \_ \_ Marcas de copia de mosaicos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : contiene marcas para copiar desde y hacia los recursos en mosaico de swizzled y los búferes lineales.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-160">[**D3D12\_TILE\_COPY\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="cf0b1-161">Estructuras</span><span class="sxs-lookup"><span data-stu-id="cf0b1-161">Structs</span></span>

-   <span data-ttu-id="cf0b1-162">[**D3D12 \_ Coordenada \_ de \_ recursos en mosaico**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : contiene la coordenada x, y y z, y la referencia de subrecurso.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-162">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="cf0b1-163">Tenga en cuenta que hay una estructura auxiliar: [**CD3DX12 \_ \_ \_ coordenada de recursos en mosaico**](cd3dx12-tiled-resource-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="cf0b1-163">Note there is a helper structure: [**CD3DX12\_TILED\_RESOURCE\_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).</span></span>
-   <span data-ttu-id="cf0b1-164">[**D3D12 \_ \_ \_ Tamaño**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) de la región del mosaico: especifica el tamaño y el número de mosaicos de la región en mosaico.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-164">[**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="cf0b1-165">[**D3D12 \_ \_Forma de mosaico**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : la forma de mosaico como ancho, alto y profundidad en textura.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-165">[**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="cf0b1-166">[**D3D12 \_ \_Opciones de \_ D3D12 \_ de datos de características**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : contiene el nivel de nivel de recurso de mosaico compatible y un valor booleano, *VolumeTiledResourcesSupported*, que indica si se admiten los recursos en mosaico de volumen.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-166">[**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : holds the supported tile resource tier level and a boolean, *VolumeTiledResourcesSupported*, indicated whether volume tiled resources are supported.</span></span>

<span data-ttu-id="cf0b1-167">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf0b1-167">Methods</span></span>

-   <span data-ttu-id="cf0b1-168">[**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : se usa para determinar qué características y en qué nivel se admiten en el hardware actual.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-168">[**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="cf0b1-169">[**ID3D12GraphcisCommandList:: CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copia mosaicos desde el búfer a un recurso en mosaico, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-169">[**ID3D12GraphcisCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="cf0b1-170">[**ID3D12CommandQueue:: UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : actualiza las asignaciones de ubicaciones de iconos en recursos en mosaico a ubicaciones de memoria en un montón de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-170">[**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a resource heap.</span></span>
-   <span data-ttu-id="cf0b1-171">[**ID3D12CommandQueue:: CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copia las asignaciones de un recurso de origen en mosaico a un recurso en mosaico de destino.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-171">[**ID3D12CommandQueue::CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="cf0b1-172">[**ID3D12Device:: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : obtiene información sobre cómo un recurso en mosaico se divide en mosaicos.</span><span class="sxs-lookup"><span data-stu-id="cf0b1-172">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf0b1-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf0b1-173">Related topics</span></span>
* [<span data-ttu-id="cf0b1-174">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="cf0b1-174">Resource Binding</span></span>](resource-binding.md)
