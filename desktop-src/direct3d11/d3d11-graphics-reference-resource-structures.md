---
title: Estructuras de recursos (gráficos de Direct3D 11)
description: Las estructuras se usan para crear y usar recursos.
ms.assetid: a29e01ac-8aa1-4a40-ad4d-3b738e129436
keywords:
- estructuras, recurso de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acff7e10538910082dcd15220cb41a2ec360c24472837a569530f0b306313db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125129"
---
# <a name="resource-structures-direct3d-11-graphics"></a>Estructuras de recursos (gráficos de Direct3D 11)

Las estructuras se usan para crear y usar recursos.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                         | Descripción                                                                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)<br/>                                   | Describe un recurso de búfer.<br/>                                                                           |
| [**D3D11 \_ BUFFER \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_rtv)<br/>                                     | Especifica los elementos de un recurso de búfer que se usarán en una vista de destino de representación.<br/>                            |
| [**D3D11 \_ BUFFER \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_srv)<br/>                                     | Especifica los elementos de un recurso de búfer que se usarán en una vista de recursos de sombreador.<br/>                          |
| [**D3D11 \_ BUFFER \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav)<br/>                                     | Describe los elementos de un búfer que se usarán en una vista de acceso desordenado.<br/>                                  |
| [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv)<br/>                                 | Describe los elementos de un recurso de búfer sin formato que se usarán en una vista de sombreador y recurso.<br/>                      |
| [**D3D11 \_ DEPTH \_ STENCIL \_ VIEW \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)<br/>         | Especifica los subrecursos de una textura a los que se puede acceder desde una vista de galería de símbolos de profundidad.<br/>                 |
| [**SUBRECURSO ASIGNADO DE D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource)<br/>                     | Proporciona acceso a los datos de subrecursos.<br/>                                                                   |
| [**D3D11 \_ PACKED \_ MIP \_ DESC**](/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_packed_mip_desc)<br/>                          | Describe la estructura de mosaico de un recurso en mosaico con mapas MIP. <br/>                                        |
| [**D3D11 \_ RENDER \_ TARGET \_ VIEW \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc)<br/>         | Especifica los subrecursos de un recurso al que se puede acceder mediante una vista render-target.<br/>             |
| [**D3D11 \_ RENDER \_ TARGET \_ VIEW \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_render_target_view_desc1)<br/>       | Describe los subrecursos de un recurso al que se puede acceder mediante una vista de destino de representación.<br/>             |
| [**D3D11 \_ SHADER \_ RESOURCE \_ VIEW \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)<br/>     | Describe una vista de recursos de sombreador.<br/>                                                                      |
| [**D3D11 \_ SHADER \_ RESOURCE \_ VIEW \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_shader_resource_view_desc1)<br/>   | Describe una vista de recursos de sombreador.<br/>                                                                      |
| [**DATOS DE SUBRECURSOS D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)<br/>                         | Especifica los datos para inicializar un subrecurso.<br/>                                                         |
| [**ETIQUETADO DE SUBRECURSOS D3D11 \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_subresource_tiling)<br/>                     | Describe un volumen de subrecurso en mosaico.<br/>                                                                  |
| [**D3D11 \_ TEXAS1D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_dsv)<br/>                          | Especifica los subrecursos de una matriz de texturas 1D que se usarán en una vista de galería de símbolos de profundidad.<br/>                |
| [**D3D11 \_ TEXAS1D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_rtv)<br/>                          | Especifica los subrecursos de una matriz de texturas 1D que se usarán en una vista de destino de representación.<br/>                |
| [**D3D11 \_ TEXAS1D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_srv)<br/>                          | Especifica los subrecursos de una matriz de texturas 1D que se usarán en una vista de recursos de sombreador.<br/>              |
| [**D3D11 \_ TEXAS1D \_ ARRAY \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_uav)<br/>                          | Describe una matriz de recursos de textura 1D de acceso desordenado.<br/>                                           |
| [**D3D11 \_ TEXAS1D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_dsv)<br/>                                       | Especifica el subrecurso de una textura 1D a la que puede acceder una vista de galería de símbolos de profundidad.<br/>                |
| [**D3D11 \_ TEXAS1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_rtv)<br/>                                       | Especifica el subrecurso de una textura 1D que se usará en una vista de destino de representación.<br/>                            |
| [**D3D11 \_ TEXAS1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)<br/>                                       | Especifica el subrecurso de una textura 1D que se usará en una vista de recursos de sombreador.<br/>                          |
| [**D3D11 \_ TEXAS1D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_uav)<br/>                                       | Describe un recurso de textura 1D de acceso desordenado.<br/>                                                      |
| [**D3D11 \_ TEXAS2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv)<br/>                          | Especifica los recursos de una matriz de texturas 2D que son accesibles para una vista de galería de símbolos de profundidad.<br/>      |
| [**D3D11 \_ TEXAS2D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_rtv)<br/>                          | Especifica los subrecursos de una matriz de texturas 2D que se usarán en una vista de destino de representación.<br/>                |
| [**D3D11 \_ TEXAS2D \_ ARRAY \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_rtv1)<br/>                        | Describe los subrecursos de una matriz de texturas 2D que se usarán en una vista de destino de representación.<br/>                |
| [**D3D11 \_ TEXAS2D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_srv)<br/>                          | Especifica los subrecursos de una matriz de texturas 2D que se usarán en una vista de recursos de sombreador.<br/>              |
| [**D3D11 \_ TEXAS2D \_ ARRAY \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_srv1)<br/>                        | Describe los subrecursos de una matriz de texturas 2D que se usarán en una vista de recursos de sombreador.<br/>              |
| [**D3D11 \_ TEXAS2D \_ ARRAY \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_uav)<br/>                          | Describe una matriz de recursos de textura 2D de acceso desordenado.<br/>                                           |
| [**D3D11 \_ TEXAS2D \_ ARRAY \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_uav1)<br/>                        | Describe una matriz de recursos de textura 2D de acceso desordenado.<br/>                                           |
| [**D3D11 \_ TEXAS2D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_dsv)<br/>                                       | Especifica el subrecurso de una textura 2D accesible para una vista de galería de símbolos de profundidad.<br/>                |
| [**D3D11 \_ TEXAS2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_rtv)<br/>                                       | Especifica el subrecurso de una textura 2D que se usará en una vista de destino de representación.<br/>                            |
| [**D3D11 \_ TEXAS2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_rtv1)<br/>                                     | Describe el subrecurso de una textura 2D que se usará en una vista de destino de representación.<br/>                            |
| [**D3D11 \_ TEXAS2D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_srv)<br/>                                       | Especifica el subrecurso de una textura 2D que se usará en una vista de recursos de sombreador.<br/>                          |
| [**D3D11 \_ TEXAS2D \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_srv1)<br/>                                     | Describe el subrecurso de una textura 2D que se usará en una vista de recursos de sombreador.<br/>                          |
| [**D3D11 \_ TEXAS2D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_uav)<br/>                                       | Describe un recurso de textura 2D de acceso desordenado.<br/>                                                      |
| [**D3D11 \_ TEXAS2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_uav1)<br/>                                     | Describe un recurso de textura 2D de acceso desordenado.<br/>                                                      |
| [**D3D11 \_ TEXAS2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_dsv)<br/>                      | Especifica los subrecursos de una matriz de texturas 2D multimuestreo para una vista de galería de símbolos de profundidad.<br/>         |
| [**D3D11 \_ TEXAS2DMS \_ ARRAY \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_rtv)<br/>                      | Especifica los subrecursos de una matriz de texturas 2D multimuestreo que se usarán en una vista de destino de representación.<br/> |
| [**D3D11 \_ TEXAS2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_srv)<br/>                      | Especifica los subrecursos de una matriz de texturas 2D multimuestreo que se usarán en una vista de recursos de sombreador.<br/> |
| [**D3D11 \_ TEXAS2DMS \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_dsv)<br/>                                   | Especifica el subrecurso de una textura 2D de varios muestreos a la que puede acceder una vista de galería de símbolos de profundidad.<br/>   |
| [**D3D11 \_ TEXAS2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_rtv)<br/>                                   | Especifica el subrecurso de una textura 2D de varios muestreos que se usará en una vista de destino de representación.<br/>               |
| [**D3D11 \_ TEXAS2DMS \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_srv)<br/>                                   | Especifica los subrecursos de una textura 2D multimuestreo que se usará en una vista de recursos de sombreador.<br/>            |
| [**D3D11 \_ TEXAS3D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_rtv)<br/>                                       | Especifica los subrecursos de una textura 3D que se usarán en una vista de destino de representación.<br/>                           |
| [**D3D11 \_ TEXAS3D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_srv)<br/>                                       | Especifica los subrecursos de una textura 3D que se usarán en una vista de recursos de sombreador.<br/>                         |
| [**D3D11 \_ TEXAS3D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_uav)<br/>                                       | Describe un recurso de textura 3D de acceso desordenado.<br/>                                                      |
| [**D3D11 \_ TEXASCUBE \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_array_srv)<br/>                      | Especifica los subrecursos de una matriz de texturas de cubo que se usarán en una vista de recursos de sombreador.<br/>            |
| [**D3D11 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_srv)<br/>                                   | Especifica el subrecurso de una textura de cubo que se usará en una vista de recursos de sombreador.<br/>                        |
| [**D3D11 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture1d_desc)<br/>                             | Describe una textura 1D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)<br/>                             | Describe una textura 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1)<br/>                           | Describe una textura 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture3d_desc)<br/>                             | Describe una textura 3D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1)<br/>                           | Describe una textura 3D.<br/>                                                                                |
| [**TAMAÑO DE LA REGIÓN DEL ICONO D3D11 \_ \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size)<br/>                        | Describe el tamaño de una región en mosaico.<br/>                                                                  |
| [**COORDENADA DE RECURSOS EN MOSAICO DE D3D11 \_ \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate)<br/>      | Describe las coordenadas de un recurso en mosaico.<br/>                                                         |
| [**FORMA DE MOSAICO D3D11 \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape)<br/>                                     | Describe la forma de un icono especificando sus dimensiones.<br/>                                            |
| [**D3D11 \_ UNORDERED \_ ACCESS \_ VIEW \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc)<br/>   | Especifica los subrecursos de un recurso al que se puede acceder mediante una vista de acceso desordenado.<br/>         |
| [**D3D11 \_ UNORDERED \_ ACCESS \_ VIEW \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_unordered_access_view_desc1)<br/> | Describe los subrecursos de un recurso al que se puede acceder mediante una vista de acceso desordenado.<br/>         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de recursos](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





