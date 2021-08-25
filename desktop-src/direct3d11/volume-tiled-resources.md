---
title: Recursos en mosaico de volumen (gráficos de Direct3D 11)
description: Obtenga información sobre cómo se pueden usar texturas de volumen (3D) como recursos en mosaico. Tenga en cuenta que la resolución de mosaicos es tridimensional.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618de4243598cdd9da3e80b0fe8cfad9cef65903736c4ae647f46e38d85fb77c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857655"
---
# <a name="volume-tiled-resources"></a>Recursos en mosaico de volumen

Las texturas de volumen (3D) se pueden usar como recursos en mosaico, y se debe tener en cuenta que la resolución de mosaicos es tridimensional.

-   [Información general](#overview)
-   [API de recursos en mosaico de D3D11.3](#d3d113-tiled-resource-apis)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Los recursos en mosaico desacoplan un objeto de recurso D3D de su memoria de respaldo (los recursos del pasado tenían una relación 1:1 con su memoria de respaldo). Esto permite una variedad de escenarios interesantes, como el streaming en datos de textura y la utilización o reducción del uso de memoria.

Los recursos en mosaico de textura 2D se admiten en D3D11.2. D3D12 y D3D11.3 agregan compatibilidad con texturas en mosaico 3D.

Las dimensiones de recursos típicas que se usan en el mosaico son 4 mosaicos de 4 x 4 para texturas 2D y 4 mosaicos de 4 x 4 para texturas 3D.



| Bits/píxel (1 muestra/píxel)                            | Dimensiones de mosaico (píxeles, w x h x d)                                    |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1,4                      | 128x64x16                           |
| BC 2,3,5,6,7                | 64x64x16                            |



 

Tenga en cuenta que los siguientes formatos no se admiten con recursos en mosaico: formatos 96bpp, formatos de vídeo, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 \_ UNORM.

En los diagramas siguientes, el gris oscuro representa iconos NULL.

-   [Asignación predeterminada de recursos en mosaico de textura 3D (mip más detallado)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [Asignación predeterminada de recursos en mosaico de textura 3D (segundo mip más detallado)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [Recurso en mosaico de textura 3D (mip más detallado)](#texture-3d-tiled-resource-most-detailed-mip)
-   [Recurso en mosaico de textura 3D (segundo mip más detallado)](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [Recurso en mosaico de textura 3D (mosaico único)](#texture-3d-tiled-resource-single-tile)
-   [Recurso en mosaico de textura 3D (cuadro uniforme)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Asignación predeterminada de recursos en mosaico de textura 3D (mip más detallado)

![asignación predeterminada del mip más detallado](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Asignación predeterminada de recursos en mosaico de textura 3D (segundo mip más detallado)

![asignación predeterminada del segundo mip más detallado](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Recurso en mosaico de textura 3D (mip más detallado)

El código siguiente configura un recurso en mosaico 3D en el mip más detallado.

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

![asignación más detallada de un recurso en mosaico 3d](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Recurso en mosaico de textura 3D (segundo mip más detallado)

El código siguiente configura un recurso en mosaico 3D y el segundo mip más detallado:

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

![segunda asignación más detallada de un recurso en mosaico 3d](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>Recurso en mosaico de textura 3D (mosaico único)

El código siguiente configura un recurso de icono único:

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Recurso en mosaico de textura 3D (cuadro uniforme)

El código siguiente configura un recurso en mosaico de Uniforme Box (tenga en cuenta la instrucción `trSize.bUseBox = true;) :`

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

## <a name="d3d113-tiled-resource-apis"></a>API de recursos en mosaico de D3D11.3

Las mismas llamadas API se usan para los recursos en mosaico 2D y 3D:

Enumeraciones

-   [**D3D11 \_ NIVEL DE \_ RECURSOS \_ EN MOSAICO:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) determina el nivel de compatibilidad con recursos en mosaico.
-   [**D3D11 \_ FORMAT \_ SUPPORT2:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) se usa para probar la compatibilidad con recursos en mosaico.
-   [**D3D11 \_ CHECK \_ MULTISAMPLE \_ QUALITY LEVELS \_ \_ FLAG:**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) determina la compatibilidad con recursos en mosaico en un recurso de muestreo múltiple.
-   [**D3D11 \_ TILE \_ COPY \_ FLAGS:**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) contiene las marcas para copiar a y desde recursos en mosaico desdobados y búferes lineales.

Estructuras

-   [**D3D11 \_ \_ \_ COORDENADA DE RECURSOS EN**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) MOSAICO: contiene la referencia de coordenadas x, y y z y subrecursos. Tenga en cuenta que hay una clase auxiliar: CD3D11 \_ TILED \_ RESOURCE \_ COORDINATE.
-   [**D3D11 \_ TILE \_ REGION \_ SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : especifica el tamaño y el número de iconos de la región en mosaico.
-   [**D3D11 \_ FORMA \_ DE MOSAICO:**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) forma de mosaico como ancho, alto y profundidad en los elementos de textura.
-   [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1)contiene el nivel de nivel de recurso de icono admitido.

Métodos

-   [**ID3D11Device::CheckFeatureSupport:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) se usa para determinar qué características, y en qué nivel, son compatibles con el hardware actual.
-   [**ID3D11DeviceContext2::CopyTiles:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) copia iconos del búfer al recurso en mosaico o viceversa.
-   [**ID3D11DeviceContext2::UpdateTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) actualiza las asignaciones de ubicaciones de mosaico en recursos en mosaico a ubicaciones de memoria de un grupo de mosaicos.
-   [**ID3D11DeviceContext2::CopyTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) copia las asignaciones de un recurso en mosaico de origen a un recurso en mosaico de destino.
-   [**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : obtiene información sobre cómo un recurso en mosaico se divide en iconos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de Direct3D 11.3](direct3d-11-3-features.md)
</dt> </dl>

 

 




