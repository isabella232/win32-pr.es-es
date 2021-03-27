---
title: Recursos en mosaico de volumen (gráficos Direct3D 11)
description: Las texturas de volumen (3D) se pueden usar como recursos en mosaico, teniendo en cuenta que la resolución de mosaicos es tridimensional.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb8b35e522ef3298abad1322d6fb7a2fe65bfcf
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "103784817"
---
# <a name="volume-tiled-resources"></a><span data-ttu-id="48046-103">Recursos en mosaico de volumen</span><span class="sxs-lookup"><span data-stu-id="48046-103">Volume Tiled Resources</span></span>

<span data-ttu-id="48046-104">Las texturas de volumen (3D) se pueden usar como recursos en mosaico, teniendo en cuenta que la resolución de mosaicos es tridimensional.</span><span class="sxs-lookup"><span data-stu-id="48046-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="48046-105">Información general</span><span class="sxs-lookup"><span data-stu-id="48046-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="48046-106">API de recursos en mosaico de D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="48046-106">D3D11.3 Tiled Resource APIs</span></span>](#d3d113-tiled-resource-apis)
-   [<span data-ttu-id="48046-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="48046-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="48046-108">Información general</span><span class="sxs-lookup"><span data-stu-id="48046-108">Overview</span></span>

<span data-ttu-id="48046-109">Los recursos en mosaico desacoplan un objeto de recurso D3D de la memoria de respaldo (los recursos en el pasado tenían una relación de 1:1 con la memoria de respaldo).</span><span class="sxs-lookup"><span data-stu-id="48046-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="48046-110">Esto permite una variedad de escenarios interesantes, como la transmisión por secuencias de datos de textura y la reutilización o reducción del uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="48046-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage</span></span>

<span data-ttu-id="48046-111">los recursos en mosaico de textura 2D se admiten en D3D 11.2.</span><span class="sxs-lookup"><span data-stu-id="48046-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="48046-112">D3D12 y D3D 11.3 agregan compatibilidad con las texturas en mosaico 3D.</span><span class="sxs-lookup"><span data-stu-id="48046-112">D3D12 and D3D11.3 add support for 3D tiled textures.</span></span>

<span data-ttu-id="48046-113">Las dimensiones de recursos típicas que se usan en el mosaico son 4 x 4 mosaicos para las texturas 2D y 4 x 4 x 4 mosaicos para las texturas 3D.</span><span class="sxs-lookup"><span data-stu-id="48046-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



|                             |                                     |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="48046-114">Bits/píxel (1 ejemplo/píxel)</span><span class="sxs-lookup"><span data-stu-id="48046-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="48046-115">Dimensiones del mosaico (píxeles, w x h x d)</span><span class="sxs-lookup"><span data-stu-id="48046-115">Tile dimensions (pixels, w x h x d)</span></span> |
| <span data-ttu-id="48046-116">8</span><span class="sxs-lookup"><span data-stu-id="48046-116">8</span></span>                           | <span data-ttu-id="48046-117">64x32x32</span><span class="sxs-lookup"><span data-stu-id="48046-117">64x32x32</span></span>                            |
| <span data-ttu-id="48046-118">16</span><span class="sxs-lookup"><span data-stu-id="48046-118">16</span></span>                          | <span data-ttu-id="48046-119">32x32x32</span><span class="sxs-lookup"><span data-stu-id="48046-119">32x32x32</span></span>                            |
| <span data-ttu-id="48046-120">32</span><span class="sxs-lookup"><span data-stu-id="48046-120">32</span></span>                          | <span data-ttu-id="48046-121">32x32x16</span><span class="sxs-lookup"><span data-stu-id="48046-121">32x32x16</span></span>                            |
| <span data-ttu-id="48046-122">64</span><span class="sxs-lookup"><span data-stu-id="48046-122">64</span></span>                          | <span data-ttu-id="48046-123">32x16x16</span><span class="sxs-lookup"><span data-stu-id="48046-123">32x16x16</span></span>                            |
| <span data-ttu-id="48046-124">128</span><span class="sxs-lookup"><span data-stu-id="48046-124">128</span></span>                         | <span data-ttu-id="48046-125">16x16x16</span><span class="sxs-lookup"><span data-stu-id="48046-125">16x16x16</span></span>                            |
| <span data-ttu-id="48046-126">BC 1, 4</span><span class="sxs-lookup"><span data-stu-id="48046-126">BC 1,4</span></span>                      | <span data-ttu-id="48046-127">128x64x16</span><span class="sxs-lookup"><span data-stu-id="48046-127">128x64x16</span></span>                           |
| <span data-ttu-id="48046-128">BC 2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="48046-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="48046-129">64x64x16</span><span class="sxs-lookup"><span data-stu-id="48046-129">64x64x16</span></span>                            |



 

<span data-ttu-id="48046-130">Tenga en cuenta que los siguientes formatos no se admiten con recursos en mosaico: formatos de 96bpp, formatos de vídeo, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 UNORM \_ .</span><span class="sxs-lookup"><span data-stu-id="48046-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="48046-131">En los diagramas siguientes, el gris oscuro representa los mosaicos NULOs.</span><span class="sxs-lookup"><span data-stu-id="48046-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="48046-132">Asignación predeterminada de recursos en mosaico 3D de textura (el MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="48046-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="48046-133">Asignación predeterminada de recursos en mosaico 3D de textura (segundo MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="48046-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="48046-134">Recurso en mosaico 3D de textura (el MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="48046-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="48046-135">Recurso en mosaico 3D de textura (segundo MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="48046-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="48046-136">Recurso en mosaico 3D de textura (mosaico único)</span><span class="sxs-lookup"><span data-stu-id="48046-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="48046-137">Recurso en mosaico 3D de textura (cuadro uniforme)</span><span class="sxs-lookup"><span data-stu-id="48046-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="48046-138">Asignación predeterminada de recursos en mosaico 3D de textura (el MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="48046-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![asignación predeterminada del MIP más detallado](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="48046-140">Asignación predeterminada de recursos en mosaico 3D de textura (segundo MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="48046-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![asignación predeterminada del segundo MIP más detallado](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="48046-142">Recurso en mosaico 3D de textura (el MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="48046-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="48046-143">El código siguiente configura un recurso en mosaico 3D en el MIP más detallado.</span><span class="sxs-lookup"><span data-stu-id="48046-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="48046-145">Recurso en mosaico 3D de textura (segundo MIP más detallado)</span><span class="sxs-lookup"><span data-stu-id="48046-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="48046-146">El código siguiente configura un recurso en mosaico 3D y el segundo MIP más detallado:</span><span class="sxs-lookup"><span data-stu-id="48046-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

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

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="48046-148">Recurso en mosaico 3D de textura (mosaico único)</span><span class="sxs-lookup"><span data-stu-id="48046-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="48046-149">En el código siguiente se configura un recurso de icono único:</span><span class="sxs-lookup"><span data-stu-id="48046-149">The following code sets up a Single Tile resource:</span></span>

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

![un solo mosaico](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="48046-151">Recurso en mosaico 3D de textura (cuadro uniforme)</span><span class="sxs-lookup"><span data-stu-id="48046-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="48046-152">En el código siguiente se configura un recurso de cuadro uniforme en mosaico (tenga en cuenta la instrucción `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="48046-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

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

![cuadro uniforme](images/vtr-tex3d-uniform.png)

## <a name="d3d113-tiled-resource-apis"></a><span data-ttu-id="48046-154">API de recursos en mosaico de D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="48046-154">D3D11.3 Tiled Resource APIs</span></span>

<span data-ttu-id="48046-155">Se usan las mismas llamadas API para los recursos en mosaico 2D y 3D:</span><span class="sxs-lookup"><span data-stu-id="48046-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="48046-156">Enumeraciones</span><span class="sxs-lookup"><span data-stu-id="48046-156">Enums</span></span>

-   <span data-ttu-id="48046-157">[**D3D11 \_ Nivel de \_ recursos \_ en mosaico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determina el nivel de compatibilidad con los recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="48046-157">[**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="48046-158">[**D3D11 \_ DAR formato al \_ cliente2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : se usa para probar la compatibilidad con los recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="48046-158">[**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="48046-159">[**D3D11 \_ Marque la \_ marca de niveles de calidad Multimuestra: determina la compatibilidad con \_ \_ los \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) recursos en mosaico en un recurso de muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="48046-159">[**D3D11\_CHECK\_MULTISAMPLE\_QUALITY\_LEVELS\_FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="48046-160">[**D3D11 \_ \_ \_ Marcas de copia de mosaicos**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : contiene marcas para copiar desde y hacia los recursos en mosaico de swizzled y los búferes lineales.</span><span class="sxs-lookup"><span data-stu-id="48046-160">[**D3D11\_TILE\_COPY\_FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="48046-161">Estructuras</span><span class="sxs-lookup"><span data-stu-id="48046-161">Structures</span></span>

-   <span data-ttu-id="48046-162">[**D3D11 \_ Coordenada \_ de \_ recursos en mosaico**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : contiene la coordenada x, y y z, y la referencia de subrecurso.</span><span class="sxs-lookup"><span data-stu-id="48046-162">[**D3D11\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="48046-163">Tenga en cuenta que hay una clase auxiliar: CD3D11 \_ \_ coordenada de recursos en mosaico \_ .</span><span class="sxs-lookup"><span data-stu-id="48046-163">Note there is a helper class: CD3D11\_TILED\_RESOURCE\_COORDINATE.</span></span>
-   <span data-ttu-id="48046-164">[**D3D11 \_ \_ \_ Tamaño**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) de la región del mosaico: especifica el tamaño y el número de mosaicos de la región en mosaico.</span><span class="sxs-lookup"><span data-stu-id="48046-164">[**D3D11\_TILE\_REGION\_SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="48046-165">[**D3D11 \_ \_Forma de mosaico**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : la forma de mosaico como ancho, alto y profundidad en textura.</span><span class="sxs-lookup"><span data-stu-id="48046-165">[**D3D11\_TILE\_SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="48046-166">[**D3D11 \_ \_Data Data \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): contiene el nivel de nivel de recurso de mosaico compatible.</span><span class="sxs-lookup"><span data-stu-id="48046-166">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): holds the supported tile resource tier level.</span></span>

<span data-ttu-id="48046-167">Métodos</span><span class="sxs-lookup"><span data-stu-id="48046-167">Methods</span></span>

-   <span data-ttu-id="48046-168">[**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : se usa para determinar qué características y en qué nivel se admiten en el hardware actual.</span><span class="sxs-lookup"><span data-stu-id="48046-168">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="48046-169">[**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copia mosaicos desde el búfer a un recurso en mosaico, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="48046-169">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="48046-170">[**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : actualiza las asignaciones de ubicaciones de los mosaicos en los recursos en mosaico a las ubicaciones de memoria de un grupo de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="48046-170">[**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a tile pool.</span></span>
-   <span data-ttu-id="48046-171">[**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copia las asignaciones de un recurso de origen en mosaico a un recurso en mosaico de destino.</span><span class="sxs-lookup"><span data-stu-id="48046-171">[**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="48046-172">[**ID3D11DeviceContext2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : obtiene información sobre cómo un recurso en mosaico se divide en mosaicos.</span><span class="sxs-lookup"><span data-stu-id="48046-172">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48046-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="48046-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48046-174">Características de Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="48046-174">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




