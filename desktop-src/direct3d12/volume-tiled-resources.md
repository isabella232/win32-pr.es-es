---
title: Recursos en mosaico de volumen (Direct3D 12)
description: Las texturas de volumen (3D) se pueden usar como recursos en mosaico, y se debe tener en cuenta que la resolución de mosaicos es tridimensional.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d6e9b4d7ae9ad4b93bae5cf29749c293bf7f55ea7fa35a1e1ca71040218e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123544"
---
# <a name="volume-tiled-resources-direct3d-12"></a>Recursos en mosaico de volumen (Direct3D 12)

Las texturas de volumen (3D) se pueden usar como recursos en mosaico, y se debe tener en cuenta que la resolución de mosaicos es tridimensional.

## <a name="overview"></a>Información general

Los recursos en mosaico desacoplan un objeto de recurso de Direct3D de su memoria de respaldo (los recursos del pasado tenían una relación 1:1 con su memoria de respaldo). Esto permite una variedad de escenarios interesantes, como el streaming en datos de textura y la utilización o reducción del uso de memoria.

Los recursos en mosaico de textura 2D se admiten en Direct3D 11.2. La compatibilidad opcional con texturas en mosaico 3D está disponible para Direct3D 12 y Direct3D 11.3 (consulte [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

Las dimensiones de recursos típicas que se usan en el mosaico son 4 mosaicos x 4 para texturas 2D y 4 mosaicos de 4 x 4 para texturas 3D.

| Bits/píxel (1 muestra/píxel) | Dimensiones de mosaico (píxeles, w x h x d) |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1,4                      | 128x64x16                           |
| BC 2,3,5,6,7                | 64x64x16                            |

Tenga en cuenta que los siguientes formatos no se admiten con recursos en mosaico: formatos de 96bpp, formatos de vídeo, **R1_UNORM**, **R8G8_B8G8_UNORM**, **R8R8_G8B8_UNORM**.

En los diagramas siguientes, el gris oscuro representa iconos NULL.

* [Asignación predeterminada de recursos en mosaico de textura 3D (mip más detallado)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
* [Asignación predeterminada de recursos en mosaico de textura 3D (segundo mip más detallado)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
* [Recurso en mosaico de textura 3D (mip más detallado)](#texture-3d-tiled-resource-most-detailed-mip)
* [Recurso en mosaico de textura 3D (segundo mip más detallado)](#texture-3d-tiled-resource-second-most-detailed-mip)
* [Recurso en mosaico de textura 3D (mosaico único)](#texture-3d-tiled-resource-single-tile)
* [Recurso en mosaico de textura 3D (cuadro uniforme)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Asignación predeterminada de recursos en mosaico de textura 3D (mip más detallado)

![asignación predeterminada de un recurso tridimensional en mosaico](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Asignación predeterminada de recursos en mosaico de textura 3D (segundo mip más detallado)

![muestra el segundo mip más detallado](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Recurso en mosaico de textura 3D (mip más detallado)

El código siguiente configura un recurso en mosaico 3D en el mip más detallado.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord{};
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize{};
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![mip más detallado para una textura tridimensional](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Recurso en mosaico de textura 3D (segundo mip más detallado)

El código siguiente configura un recurso en mosaico 3D y el segundo mip más detallado.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![segundo mip más detallado para una textura tridimensional](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>Recurso en mosaico texture 3D (un solo icono)

El código siguiente configura un único recurso de icono.

```cpp
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

![un recurso tridimensional en mosaico único](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a>Recurso en mosaico de textura 3D (cuadro uniforme)

El código siguiente configura un recurso en mosaico de cuadro uniforme (tenga en cuenta la instrucción `trSize.bUseBox = true;) :`

```cpp
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

![un cuadro uniforme](images/vtr-tex3d-uniform.png)

## <a name="tiled-resource-apis"></a>API de recursos en mosaico

Las mismas llamadas API se usan para recursos en mosaico 2D y 3D.

Enumeraciones

* [**D3D12_TILED_RESOURCES_TIER:**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) determina el nivel de compatibilidad de los recursos en mosaico.
* [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2) : se usa para probar la compatibilidad con recursos en mosaico.
* [**D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS:**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) determina la compatibilidad con recursos en mosaico en un recurso de muestreo múltiple.
* [**D3D12_TILE_COPY_FLAGS:**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) contiene marcas para copiar hacia y desde recursos en mosaico y búferes lineales.

Estructuras

* [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : contiene la referencia de coordenadas x, y y z y subcursos. Tenga en cuenta que hay una estructura auxiliar: [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).
* [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) : especifica el tamaño y el número de mosaicos de la región en mosaico.
* [**D3D12_TILE_SHAPE:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) forma de mosaico como ancho, alto y profundidad en texturas.
* [**D3D12_FEATURE_DATA_D3D12_OPTIONS:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) contiene el nivel de recurso de icono admitido y un valor booleano, *VolumeTiledResourcesSupported*, que indica si se admiten recursos en mosaico de volumen.

Métodos

* [**ID3D12Device::CheckFeatureSupport:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) se usa para determinar qué características y en qué nivel son compatibles con el hardware actual.
* [**ID3D12GraphicsCommandList::CopyTiles:**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) copia iconos del búfer al recurso en mosaico o viceversa.
* [**ID3D12CommandQueue::UpdateTileMappings:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) actualiza las asignaciones de ubicaciones de mosaico de los recursos en mosaico a las ubicaciones de memoria de un montón de recursos.
* [**ID3D12CommandQueue::CopyTileMappings:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) copia las asignaciones de un recurso en mosaico de origen a un recurso en mosaico de destino.
* [**ID3D12Device::GetResourceTiling:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) obtiene información sobre cómo un recurso en mosaico se divide en iconos.

## <a name="related-topics"></a>Temas relacionados

* [Enlace de recursos](resource-binding.md)
