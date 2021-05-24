---
title: Recursos en mosaico de volumen (gráficos de Direct3D 11)
description: Obtenga información sobre cómo se pueden usar texturas de volumen (3D) como recursos en mosaico. Tenga en cuenta que la resolución de mosaicos es tridimensional.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf9b3ed8b1db89d9718fa904eefd23ce2e871db
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335439"
---
# <a name="volume-tiled-resources"></a><span data-ttu-id="54543-104">Recursos en mosaico de volumen</span><span class="sxs-lookup"><span data-stu-id="54543-104">Volume Tiled Resources</span></span>

<span data-ttu-id="54543-105">Las texturas de volumen (3D) se pueden usar como recursos en mosaico, y se debe tener en cuenta que la resolución de mosaicos es tridimensional.</span><span class="sxs-lookup"><span data-stu-id="54543-105">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="54543-106">Información general</span><span class="sxs-lookup"><span data-stu-id="54543-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="54543-107">API de recursos en mosaico de D3D11.3</span><span class="sxs-lookup"><span data-stu-id="54543-107">D3D11.3 Tiled Resource APIs</span></span>](#d3d113-tiled-resource-apis)
-   [<span data-ttu-id="54543-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54543-108">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="54543-109">Información general</span><span class="sxs-lookup"><span data-stu-id="54543-109">Overview</span></span>

<span data-ttu-id="54543-110">Los recursos en mosaico desacoplan un objeto de recurso D3D de su memoria de respaldo (los recursos del pasado tenían una relación 1:1 con su memoria de respaldo).</span><span class="sxs-lookup"><span data-stu-id="54543-110">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="54543-111">Esto permite una variedad de escenarios interesantes, como el streaming en datos de textura y la utilización o reducción del uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="54543-111">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage</span></span>

<span data-ttu-id="54543-112">Los recursos en mosaico de textura 2D se admiten en D3D11.2.</span><span class="sxs-lookup"><span data-stu-id="54543-112">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="54543-113">D3D12 y D3D11.3 agregan compatibilidad con texturas en mosaico 3D.</span><span class="sxs-lookup"><span data-stu-id="54543-113">D3D12 and D3D11.3 add support for 3D tiled textures.</span></span>

<span data-ttu-id="54543-114">Las dimensiones de recursos típicas que se usan en el mosaico son 4 mosaicos de 4 x 4 para texturas 2D y 4 mosaicos de 4 x 4 para texturas 3D.</span><span class="sxs-lookup"><span data-stu-id="54543-114">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



| <span data-ttu-id="54543-115">Bits/píxel (1 muestra/píxel)</span><span class="sxs-lookup"><span data-stu-id="54543-115">Bits/pixel (1 sample/pixel)</span></span>                            | <span data-ttu-id="54543-116">Dimensiones de mosaico (píxeles, w x h x d)</span><span class="sxs-lookup"><span data-stu-id="54543-116">Tile dimensions (pixels, w x h x d)</span></span>                                    |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="54543-117">8</span><span class="sxs-lookup"><span data-stu-id="54543-117">8</span></span>                           | <span data-ttu-id="54543-118">64x32x32</span><span class="sxs-lookup"><span data-stu-id="54543-118">64x32x32</span></span>                            |
| <span data-ttu-id="54543-119">16</span><span class="sxs-lookup"><span data-stu-id="54543-119">16</span></span>                          | <span data-ttu-id="54543-120">32x32x32</span><span class="sxs-lookup"><span data-stu-id="54543-120">32x32x32</span></span>                            |
| <span data-ttu-id="54543-121">32</span><span class="sxs-lookup"><span data-stu-id="54543-121">32</span></span>                          | <span data-ttu-id="54543-122">32x32x16</span><span class="sxs-lookup"><span data-stu-id="54543-122">32x32x16</span></span>                            |
| <span data-ttu-id="54543-123">64</span><span class="sxs-lookup"><span data-stu-id="54543-123">64</span></span>                          | <span data-ttu-id="54543-124">32x16x16</span><span class="sxs-lookup"><span data-stu-id="54543-124">32x16x16</span></span>                            |
| <span data-ttu-id="54543-125">128</span><span class="sxs-lookup"><span data-stu-id="54543-125">128</span></span>                         | <span data-ttu-id="54543-126">16x16x16</span><span class="sxs-lookup"><span data-stu-id="54543-126">16x16x16</span></span>                            |
| <span data-ttu-id="54543-127">BC 1,4</span><span class="sxs-lookup"><span data-stu-id="54543-127">BC 1,4</span></span>                      | <span data-ttu-id="54543-128">128x64x16</span><span class="sxs-lookup"><span data-stu-id="54543-128">128x64x16</span></span>                           |
| <span data-ttu-id="54543-129">BC 2,3,5,6,7</span><span class="sxs-lookup"><span data-stu-id="54543-129">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="54543-130">64x64x16</span><span class="sxs-lookup"><span data-stu-id="54543-130">64x64x16</span></span>                            |



 

<span data-ttu-id="54543-131">Tenga en cuenta que los siguientes formatos no se admiten con recursos en mosaico: formatos 96bpp, formatos de vídeo, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="54543-131">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="54543-132">En los diagramas siguientes, el gris oscuro representa iconos NULL.</span><span class="sxs-lookup"><span data-stu-id="54543-132">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="54543-133">Asignación predeterminada de recursos en mosaico de textura 3D (mip más detallado)</span><span class="sxs-lookup"><span data-stu-id="54543-133">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="54543-134">Asignación predeterminada de recursos en mosaico de textura 3D (segundo mip más detallado)</span><span class="sxs-lookup"><span data-stu-id="54543-134">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="54543-135">Recurso en mosaico de textura 3D (mip más detallado)</span><span class="sxs-lookup"><span data-stu-id="54543-135">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="54543-136">Recurso en mosaico de textura 3D (segundo mip más detallado)</span><span class="sxs-lookup"><span data-stu-id="54543-136">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="54543-137">Recurso en mosaico de textura 3D (mosaico único)</span><span class="sxs-lookup"><span data-stu-id="54543-137">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="54543-138">Recurso en mosaico de textura 3D (cuadro uniforme)</span><span class="sxs-lookup"><span data-stu-id="54543-138">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="54543-139">Asignación predeterminada de recursos en mosaico de textura 3D (mip más detallado)</span><span class="sxs-lookup"><span data-stu-id="54543-139">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![asignación predeterminada del mip más detallado](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="54543-141">Asignación predeterminada de recursos en mosaico de textura 3D (segundo mip más detallado)</span><span class="sxs-lookup"><span data-stu-id="54543-141">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![asignación predeterminada del segundo mip más detallado](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="54543-143">Recurso en mosaico de textura 3D (mip más detallado)</span><span class="sxs-lookup"><span data-stu-id="54543-143">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="54543-144">El código siguiente configura un recurso en mosaico 3D en el mip más detallado.</span><span class="sxs-lookup"><span data-stu-id="54543-144">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![asignación más detallada de un recurso en mosaico 3D](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="54543-146">Recurso en mosaico de textura 3D (segundo mip más detallado)</span><span class="sxs-lookup"><span data-stu-id="54543-146">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="54543-147">El código siguiente configura un recurso en mosaico 3D y el segundo mip más detallado:</span><span class="sxs-lookup"><span data-stu-id="54543-147">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![segunda asignación más detallada de un recurso en mosaico 3D](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="54543-149">Recurso en mosaico de textura 3D (mosaico único)</span><span class="sxs-lookup"><span data-stu-id="54543-149">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="54543-150">El código siguiente configura un recurso de icono único:</span><span class="sxs-lookup"><span data-stu-id="54543-150">The following code sets up a Single Tile resource:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![un solo icono](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="54543-152">Recurso en mosaico de textura 3D (cuadro uniforme)</span><span class="sxs-lookup"><span data-stu-id="54543-152">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="54543-153">El código siguiente configura un recurso en mosaico de Uniforme Box (tenga en cuenta la instrucción `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="54543-153">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![un cuadro uniforme](images/vtr-tex3d-uniform.png)

## <a name="d3d113-tiled-resource-apis"></a><span data-ttu-id="54543-155">API de recursos en mosaico de D3D11.3</span><span class="sxs-lookup"><span data-stu-id="54543-155">D3D11.3 Tiled Resource APIs</span></span>

<span data-ttu-id="54543-156">Las mismas llamadas API se usan para los recursos en mosaico 2D y 3D:</span><span class="sxs-lookup"><span data-stu-id="54543-156">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="54543-157">Enumeraciones</span><span class="sxs-lookup"><span data-stu-id="54543-157">Enums</span></span>

-   <span data-ttu-id="54543-158">[**D3D11 \_ NIVEL DE \_ RECURSOS \_ EN MOSAICO:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) determina el nivel de compatibilidad con recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="54543-158">[**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="54543-159">[**D3D11 \_ FORMAT \_ SUPPORT2:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) se usa para probar la compatibilidad con recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="54543-159">[**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="54543-160">[**D3D11 \_ CHECK \_ MULTISAMPLE \_ QUALITY LEVELS \_ \_ FLAG:**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) determina la compatibilidad con recursos en mosaico en un recurso de muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="54543-160">[**D3D11\_CHECK\_MULTISAMPLE\_QUALITY\_LEVELS\_FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="54543-161">[**D3D11 \_ TILE \_ COPY \_ FLAGS:**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) contiene marcas para copiar recursos en mosaico y búferes lineales hacia y desde estos.</span><span class="sxs-lookup"><span data-stu-id="54543-161">[**D3D11\_TILE\_COPY\_FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="54543-162">Estructuras</span><span class="sxs-lookup"><span data-stu-id="54543-162">Structures</span></span>

-   <span data-ttu-id="54543-163">[**D3D11 \_ \_ \_ COORDENADA DE RECURSOS EN**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) MOSAICO: contiene la referencia de coordenadas y subrecursos x, y y z.</span><span class="sxs-lookup"><span data-stu-id="54543-163">[**D3D11\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="54543-164">Tenga en cuenta que hay una clase auxiliar: CD3D11 \_ TILED \_ RESOURCE \_ COORDINATE.</span><span class="sxs-lookup"><span data-stu-id="54543-164">Note there is a helper class: CD3D11\_TILED\_RESOURCE\_COORDINATE.</span></span>
-   <span data-ttu-id="54543-165">[**D3D11 \_ TILE \_ REGION \_ SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : especifica el tamaño y el número de iconos de la región en mosaico.</span><span class="sxs-lookup"><span data-stu-id="54543-165">[**D3D11\_TILE\_REGION\_SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="54543-166">[**D3D11 \_ FORMA \_ DE MOSAICO:**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) forma de mosaico como ancho, alto y profundidad en los elementos de textura.</span><span class="sxs-lookup"><span data-stu-id="54543-166">[**D3D11\_TILE\_SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="54543-167">[**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1)contiene el nivel de recurso de icono admitido.</span><span class="sxs-lookup"><span data-stu-id="54543-167">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): holds the supported tile resource tier level.</span></span>

<span data-ttu-id="54543-168">Métodos</span><span class="sxs-lookup"><span data-stu-id="54543-168">Methods</span></span>

-   <span data-ttu-id="54543-169">[**ID3D11Device::CheckFeatureSupport:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) se usa para determinar qué características, y en qué nivel, son compatibles con el hardware actual.</span><span class="sxs-lookup"><span data-stu-id="54543-169">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="54543-170">[**ID3D11DeviceContext2::CopyTiles:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) copia iconos del búfer al recurso en mosaico o viceversa.</span><span class="sxs-lookup"><span data-stu-id="54543-170">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="54543-171">[**ID3D11DeviceContext2::UpdateTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) actualiza las asignaciones de ubicaciones de mosaico de recursos en mosaico a ubicaciones de memoria de un grupo de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="54543-171">[**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a tile pool.</span></span>
-   <span data-ttu-id="54543-172">[**ID3D11DeviceContext2::CopyTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) copia las asignaciones de un recurso en mosaico de origen a un recurso en mosaico de destino.</span><span class="sxs-lookup"><span data-stu-id="54543-172">[**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="54543-173">[**ID3D11DeviceContext2::GetResourceTiling:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) obtiene información sobre cómo un recurso en mosaico se divide en iconos.</span><span class="sxs-lookup"><span data-stu-id="54543-173">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54543-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54543-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54543-175">Características de Direct3D 11.3</span><span class="sxs-lookup"><span data-stu-id="54543-175">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




