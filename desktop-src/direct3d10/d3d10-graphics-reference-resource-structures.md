---
description: Estructuras utilizadas para crear y usar recursos.
ms.assetid: d8fe2ebe-349a-456e-9a5a-16f2d3419800
title: Estructuras de recursos (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb45ff5d77d7bb0417b54b88a4014e2a96f522d2e026c778efcd05d23f624bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635025"
---
# <a name="resource-structures-direct3d-10-graphics"></a>Estructuras de recursos (gráficos de Direct3D 10)

Estructuras utilizadas para crear y usar [recursos](d3d10-graphics-programming-guide-resources-types.md).



| Estructuras                                                                 | Descripción                                                                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D10 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)                           | Descripción de un [recurso de](d3d10-graphics-programming-guide-resources-types.md) búfer.                                                                     |
| [**D3D10 \_ BUFFER \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_rtv)                             | Describe los elementos de un [búfer que se](d3d10-graphics-programming-guide-resources-types.md) usarán en una vista de destino de representación.                                |
| [**D3D10 \_ BUFFER \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_srv)                             | Describe los elementos de un recurso [de búfer](d3d10-graphics-programming-guide-resources-types.md) que se usarán en una vista de recursos de sombreador.                         |
| [**D3D10 \_ DEPTH \_ STENCIL \_ VIEW \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_view_desc) | Describe una vista de galería de símbolos de profundidad.                                                                                                                               |
| [**TEXTURA ASIGNADA DE D3D102D \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture2d)                 | Proporciona acceso a los datos de subrecurso en una [textura 2D](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**TEXTURA ASIGNADA A D3D103D \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture3d)                 | Proporciona acceso a los datos de subrecursos en una [textura 3D.](d3d10-graphics-programming-guide-resources-types.md)                                                  |
| [**D3D10 \_ RENDER \_ TARGET \_ VIEW \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_render_target_view_desc) | Describe una vista render-target.                                                                                                                               |
| [**DATOS DE SUBRECURSOS D3D10 \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)                 | Especifica los datos para inicializar un recurso.                                                                                                                   |
| [**D3D10 \_ TEXAS1D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_dsv)                  | Especifica qué nivel de mapa mipmap y texturas de una matriz de textura [1D](d3d10-graphics-programming-guide-resources-types.md) se usarán en una vista de galería de símbolos de profundidad.       |
| [**D3D10 \_ TEXAS1D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_rtv)                  | Especifica los subrecursos de una matriz de [texturas 1D](d3d10-graphics-programming-guide-resources-types.md) que se usarán en una vista de destino de representación.             |
| [**D3D10 \_ TEXAS1D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_srv)                  | Especifica los niveles de mapa mip y las texturas de una matriz de textura [1D](d3d10-graphics-programming-guide-resources-types.md) que se usarán en una vista de recursos de sombreador.      |
| [**D3D10 \_ TEXAS1D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_dsv)                               | Especifica los subrecursos de una [textura 1D](d3d10-graphics-programming-guide-resources-types.md) que se usarán en una vista de galería de símbolos de profundidad.                        |
| [**D3D10 \_ TEXAS1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_rtv)                               | Especifica los subrecursos de una [textura 1D](d3d10-graphics-programming-guide-resources-types.md) que se usarán en una vista de destino de representación.                        |
| [**D3D10 \_ TEXAS1D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_srv)                               | Especifica los subrecursos de una [textura 1D](d3d10-graphics-programming-guide-resources-types.md) que se usarán en una vista de recursos de sombreador.                      |
| [**D3D10 \_ TEXAS2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)                  | Especifica qué nivel de mapa mip y qué texturas de una matriz de textura [2D](d3d10-graphics-programming-guide-resources-types.md) se usarán en una vista de galería de símbolos de profundidad. |
| [**D3D10 \_ TEXAS2D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_rtv)                  | Especifica qué nivel de mapa mip y qué texturas de una matriz de textura [2D](d3d10-graphics-programming-guide-resources-types.md) se usarán en una vista de destino de representación. |
| [**D3D10 \_ TEXAS2D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_srv)                  | Especifica los subrecursos de una matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) que se usarán en una vista de recursos de sombreador.           |
| [**D3D10 \_ TEXAS2D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_dsv)                               | Especifica los subrecursos de una [textura 2D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de galería de símbolos de profundidad.                        |
| [**D3D10 \_ TEXAS2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_rtv)                               | Especifica los subrecursos de una [textura 2D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de destino de representación.                        |
| [**D3D10 \_ TEXAS2D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_srv)                               | Especifica los subrecursos de una textura [2D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de recursos de sombreador.                      |
| [**D3D10 \_ TEXAS2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_dsv)              | Especifica los subrecursos de una matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) que se usarán en una vista de galería de símbolos de profundidad.             |
| [**D3D10 \_ TEXAS2DMS \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_rtv)              | Especifica los subrecursos de una matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) que se usarán en una vista de destino de representación.             |
| [**D3D10 \_ TEXAS2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_srv)              | Especifica los subrecursos de una matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) que se usarán en una vista de recursos de sombreador.           |
| [**D3D10 \_ TEXAS2DMS \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_dsv)                           | Especifica los subrecursos de una textura [2D](d3d10-graphics-programming-guide-resources-types.md) multimuestreo que se va a usar en una vista de galería de símbolos de profundidad.           |
| [**D3D10 \_ TEXAS2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_rtv)                           | Especifica los subrecursos de una textura [2D](d3d10-graphics-programming-guide-resources-types.md) multimuestreo que se va a usar en una vista de destino de representación.           |
| [**D3D10 \_ TEXAS2DMS \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_srv)                           | Especifica los subrecursos de una textura [2D](d3d10-graphics-programming-guide-resources-types.md) multimuestreo que se va a usar en una vista de recursos de sombreador.         |
| [**D3D10 \_ TEXAS3D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_rtv)                               | Especifica los subrecursos de una [textura 3D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de destino de representación.                        |
| [**D3D10 \_ TEXAS3D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_srv)                               | Especifica los subrecursos de una [textura 3D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de recursos de sombreador.                      |
| [**D3D10 \_ TEXASCUBE \_ ARRAY \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)            | Especifica los subrecursos de una textura [de cubo](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de recursos de sombreador.                    |
| [**D3D10 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_texcube_srv)                           | Especifica los subrecursos de una textura [de cubo](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de recursos de sombreador.                    |
| [**D3D10 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture1d_desc)                     | Describe un recurso [de textura 1D.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |
| [**D3D10 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture2d_desc)                     | Describe un recurso [de textura 2D.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |
| [**D3D10 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture3d_desc)                     | Describe un recurso [de textura 3D.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de recursos](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



