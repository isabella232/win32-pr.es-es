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
# <a name="volume-tiled-resources-direct3d-12"></a>Recursos en mosaico de volumen (Direct3D 12)

Las texturas de volumen (3D) se pueden usar como recursos en mosaico, teniendo en cuenta que la resolución de mosaicos es tridimensional.

-   [Información general](#overview)
-   [API de recursos en mosaico](#tiled-resource-apis)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Los recursos en mosaico desacoplan un objeto de recurso D3D de la memoria de respaldo (los recursos en el pasado tenían una relación de 1:1 con la memoria de respaldo). Esto permite una variedad de escenarios interesantes, como la transmisión por secuencias de datos de textura y la reutilización o reducción del uso de memoria.

los recursos en mosaico de textura 2D se admiten en D3D 11.2. La compatibilidad opcional con las texturas en mosaico 3D está disponible para D3D12 y D3D 11.3 (consulte el [**nivel de recursos en mosaico de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

Las dimensiones de recursos típicas que se usan en el mosaico son 4 x 4 mosaicos para las texturas 2D y 4 x 4 x 4 mosaicos para las texturas 3D.



| Bits/píxel (1 ejemplo/píxel) | Dimensiones del mosaico (píxeles, w x h x d) |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1, 4                      | 128x64x16                           |
| BC 2, 3, 5, 6, 7                | 64x64x16                            |

Tenga en cuenta que los siguientes formatos no se admiten con recursos en mosaico: formatos de 96bpp, formatos de vídeo, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 UNORM \_ .

En los diagramas siguientes, el gris oscuro representa los mosaicos NULOs.

-   [Asignación predeterminada de recursos en mosaico 3D de textura (el MIP más detallado)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [Asignación predeterminada de recursos en mosaico 3D de textura (segundo MIP más detallado)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [Recurso en mosaico 3D de textura (el MIP más detallado)](#texture-3d-tiled-resource-most-detailed-mip)
-   [Recurso en mosaico 3D de textura (segundo MIP más detallado)](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [Recurso en mosaico 3D de textura (mosaico único)](#texture-3d-tiled-resource-single-tile)
-   [Recurso en mosaico 3D de textura (cuadro uniforme)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Asignación predeterminada de recursos en mosaico 3D de textura (el MIP más detallado)

![asignación predeterminada de un recurso de tres dimensiones en mosaico](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Asignación predeterminada de recursos en mosaico 3D de textura (segundo MIP más detallado)

![muestra el segundo MIP más detallado](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Recurso en mosaico 3D de textura (el MIP más detallado)

El código siguiente configura un recurso en mosaico 3D en el MIP más detallado.

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Recurso en mosaico 3D de textura (segundo MIP más detallado)

El código siguiente configura un recurso en mosaico 3D y el segundo MIP más detallado:

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

### <a name="texture-3d-tiled-resource-single-tile"></a>Recurso en mosaico 3D de textura (mosaico único)

En el código siguiente se configura un recurso de icono único:

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Recurso en mosaico 3D de textura (cuadro uniforme)

En el código siguiente se configura un recurso de cuadro uniforme en mosaico (tenga en cuenta la instrucción `trSize.bUseBox = true;) :`

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

## <a name="tiled-resource-apis"></a>API de recursos en mosaico

Se usan las mismas llamadas API para los recursos en mosaico 2D y 3D:

Enumeraciones

-   [**D3D12 \_ Nivel de \_ recursos \_ en mosaico**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determina el nivel de compatibilidad con los recursos en mosaico.
-   [**D3D12 \_ DAR formato al \_ cliente2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : se usa para probar la compatibilidad con los recursos en mosaico.
-   [**D3D12 \_ \_ \_ \_ Marcas de nivel de calidad Multimuestra**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determina la compatibilidad con los recursos en mosaico en un recurso de muestreo múltiple.
-   [**D3D12 \_ \_ \_ Marcas de copia de mosaicos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : contiene marcas para copiar desde y hacia los recursos en mosaico de swizzled y los búferes lineales.

Estructuras

-   [**D3D12 \_ Coordenada \_ de \_ recursos en mosaico**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : contiene la coordenada x, y y z, y la referencia de subrecurso. Tenga en cuenta que hay una estructura auxiliar: [**CD3DX12 \_ \_ \_ coordenada de recursos en mosaico**](cd3dx12-tiled-resource-coordinate.md).
-   [**D3D12 \_ \_ \_ Tamaño**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) de la región del mosaico: especifica el tamaño y el número de mosaicos de la región en mosaico.
-   [**D3D12 \_ \_Forma de mosaico**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : la forma de mosaico como ancho, alto y profundidad en textura.
-   [**D3D12 \_ \_Opciones de \_ D3D12 \_ de datos de características**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : contiene el nivel de nivel de recurso de mosaico compatible y un valor booleano, *VolumeTiledResourcesSupported*, que indica si se admiten los recursos en mosaico de volumen.

Métodos

-   [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : se usa para determinar qué características y en qué nivel se admiten en el hardware actual.
-   [**ID3D12GraphcisCommandList:: CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copia mosaicos desde el búfer a un recurso en mosaico, o viceversa.
-   [**ID3D12CommandQueue:: UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : actualiza las asignaciones de ubicaciones de iconos en recursos en mosaico a ubicaciones de memoria en un montón de recursos.
-   [**ID3D12CommandQueue:: CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copia las asignaciones de un recurso de origen en mosaico a un recurso en mosaico de destino.
-   [**ID3D12Device:: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : obtiene información sobre cómo un recurso en mosaico se divide en mosaicos.

## <a name="related-topics"></a>Temas relacionados
* [Enlace de recursos](resource-binding.md)
