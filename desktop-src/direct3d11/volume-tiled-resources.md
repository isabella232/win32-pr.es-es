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
# <a name="volume-tiled-resources"></a>Recursos en mosaico de volumen

Las texturas de volumen (3D) se pueden usar como recursos en mosaico, teniendo en cuenta que la resolución de mosaicos es tridimensional.

-   [Información general](#overview)
-   [API de recursos en mosaico de D3D 11.3](#d3d113-tiled-resource-apis)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Los recursos en mosaico desacoplan un objeto de recurso D3D de la memoria de respaldo (los recursos en el pasado tenían una relación de 1:1 con la memoria de respaldo). Esto permite una variedad de escenarios interesantes, como la transmisión por secuencias de datos de textura y la reutilización o reducción del uso de memoria.

los recursos en mosaico de textura 2D se admiten en D3D 11.2. D3D12 y D3D 11.3 agregan compatibilidad con las texturas en mosaico 3D.

Las dimensiones de recursos típicas que se usan en el mosaico son 4 x 4 mosaicos para las texturas 2D y 4 x 4 x 4 mosaicos para las texturas 3D.



|                             |                                     |
|-----------------------------|-------------------------------------|
| Bits/píxel (1 ejemplo/píxel) | Dimensiones del mosaico (píxeles, w x h x d) |
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

![asignación predeterminada del MIP más detallado](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Asignación predeterminada de recursos en mosaico 3D de textura (segundo MIP más detallado)

![asignación predeterminada del segundo MIP más detallado](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Recurso en mosaico 3D de textura (el MIP más detallado)

El código siguiente configura un recurso en mosaico 3D en el MIP más detallado.

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Recurso en mosaico 3D de textura (segundo MIP más detallado)

El código siguiente configura un recurso en mosaico 3D y el segundo MIP más detallado:

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

### <a name="texture-3d-tiled-resource-single-tile"></a>Recurso en mosaico 3D de textura (mosaico único)

En el código siguiente se configura un recurso de icono único:

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Recurso en mosaico 3D de textura (cuadro uniforme)

En el código siguiente se configura un recurso de cuadro uniforme en mosaico (tenga en cuenta la instrucción `trSize.bUseBox = true;) :`

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

## <a name="d3d113-tiled-resource-apis"></a>API de recursos en mosaico de D3D 11.3

Se usan las mismas llamadas API para los recursos en mosaico 2D y 3D:

Enumeraciones

-   [**D3D11 \_ Nivel de \_ recursos \_ en mosaico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determina el nivel de compatibilidad con los recursos en mosaico.
-   [**D3D11 \_ DAR formato al \_ cliente2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : se usa para probar la compatibilidad con los recursos en mosaico.
-   [**D3D11 \_ Marque la \_ marca de niveles de calidad Multimuestra: determina la compatibilidad con \_ \_ los \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) recursos en mosaico en un recurso de muestreo múltiple.
-   [**D3D11 \_ \_ \_ Marcas de copia de mosaicos**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : contiene marcas para copiar desde y hacia los recursos en mosaico de swizzled y los búferes lineales.

Estructuras

-   [**D3D11 \_ Coordenada \_ de \_ recursos en mosaico**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : contiene la coordenada x, y y z, y la referencia de subrecurso. Tenga en cuenta que hay una clase auxiliar: CD3D11 \_ \_ coordenada de recursos en mosaico \_ .
-   [**D3D11 \_ \_ \_ Tamaño**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) de la región del mosaico: especifica el tamaño y el número de mosaicos de la región en mosaico.
-   [**D3D11 \_ \_Forma de mosaico**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : la forma de mosaico como ancho, alto y profundidad en textura.
-   [**D3D11 \_ \_Data Data \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): contiene el nivel de nivel de recurso de mosaico compatible.

Métodos

-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : se usa para determinar qué características y en qué nivel se admiten en el hardware actual.
-   [**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copia mosaicos desde el búfer a un recurso en mosaico, o viceversa.
-   [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : actualiza las asignaciones de ubicaciones de los mosaicos en los recursos en mosaico a las ubicaciones de memoria de un grupo de mosaicos.
-   [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copia las asignaciones de un recurso de origen en mosaico a un recurso en mosaico de destino.
-   [**ID3D11DeviceContext2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : obtiene información sobre cómo un recurso en mosaico se divide en mosaicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




