---
title: Estructuras de recursos (gráficos de Direct3D 11)
description: Las estructuras se usan para crear y usar recursos.
ms.assetid: a29e01ac-8aa1-4a40-ad4d-3b738e129436
keywords:
- estructuras, recurso de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5020792e1fb56a52e7a4354964c45bb5d65bbba4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904962"
---
# <a name="resource-structures-direct3d-11-graphics"></a>Estructuras de recursos (gráficos de Direct3D 11)

Las estructuras se usan para crear y usar recursos.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                         | Descripción                                                                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**DESC. de búfer de D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)<br/>                                   | Describe un recurso de búfer.<br/>                                                                           |
| [**D3D11 \_ búfer \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_rtv)<br/>                                     | Especifica los elementos de un recurso de búfer que se usarán en una vista de destino de representación.<br/>                            |
| [**\_SRV de búfer de D3D11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_srv)<br/>                                     | Especifica los elementos de un recurso de búfer que se usarán en una vista de recursos de sombreador.<br/>                          |
| [**\_UAV de búfer de D3D11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav)<br/>                                     | Describe los elementos de un búfer que se van a usar en una vista de acceso desordenado.<br/>                                  |
| [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv)<br/>                                 | Describe los elementos de un recurso de búfer sin procesar que se va a usar en una vista de recursos de sombreador.<br/>                      |
| [**D3D11 \_ de \_ estarcido de profundidad \_ vista \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)<br/>         | Especifica los Subrecursos de una textura a la que se puede tener acceso desde una vista de galería de símbolos de profundidad.<br/>                 |
| [**Subrecurso asignado de D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource)<br/>                     | Proporciona acceso a los datos del subrecurso.<br/>                                                                   |
| [**\_Descripción de \_ MIP EMPAQUETAda D3D11 \_**](/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_packed_mip_desc)<br/>                          | Describe la estructura de mosaico de un recurso en mosaico con mapas MIP. <br/>                                        |
| [**Descripción de la vista de destino de \_ representación D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc)<br/>         | Especifica los Subrecursos de un recurso al que se puede tener acceso mediante una vista de destino de representación.<br/>             |
| [**D3D11 \_ vista de destino de presentación \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_render_target_view_desc1)<br/>       | Describe los Subrecursos de un recurso al que se puede tener acceso mediante una vista de destino de representación.<br/>             |
| [**\_Vista de recursos del sombreador de D3D11 \_ \_ \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)<br/>     | Describe una vista de recursos de sombreador.<br/>                                                                      |
| [**\_Vista de recursos del sombreador de D3D11 \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_shader_resource_view_desc1)<br/>   | Describe una vista de recursos de sombreador.<br/>                                                                      |
| [**\_Datos de SUBRECURSO D3D11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)<br/>                         | Especifica los datos para inicializar un subrecurso.<br/>                                                         |
| [**\_Mosaico de SUBrecursos de D3D11 \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_subresource_tiling)<br/>                     | Describe un volumen de Subrecursos en mosaico.<br/>                                                                  |
| [**D3D11 \_ TEX1D \_ array \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_dsv)<br/>                          | Especifica los Subrecursos de una matriz de texturas 1D que se van a usar en una vista de galería de símbolos de profundidad.<br/>                |
| [**D3D11 \_ TEX1D \_ matriz \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_rtv)<br/>                          | Especifica los Subrecursos de una matriz de texturas 1D que se van a usar en una vista de destino de representación.<br/>                |
| [**D3D11 \_ TEX1D \_ array \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_srv)<br/>                          | Especifica los Subrecursos de una matriz de texturas 1D que se van a usar en una vista de recursos de sombreador.<br/>              |
| [**D3D11 \_ TEX1D \_ array \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_uav)<br/>                          | Describe una matriz de recursos de textura 1D de acceso desordenado.<br/>                                           |
| [**D3D11 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_dsv)<br/>                                       | Especifica el subrecurso de una textura 1D que es accesible para una vista de galería de símbolos de profundidad.<br/>                |
| [**D3D11 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_rtv)<br/>                                       | Especifica el subrecurso de una textura 1D que se va a usar en una vista de destino de representación.<br/>                            |
| [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)<br/>                                       | Especifica el subrecurso de una textura 1D que se va a usar en una vista de recursos de sombreador.<br/>                          |
| [**D3D11 \_ TEX1D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_uav)<br/>                                       | Describe un recurso de textura 1D de acceso desordenado.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ array \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv)<br/>                          | Especifica los Subrecursos de las texturas 2D de una matriz a las que se puede tener acceso desde una vista de galería de símbolos de profundidad.<br/>      |
| [**D3D11 \_ TEX2D \_ matriz \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_rtv)<br/>                          | Especifica los Subrecursos de una matriz de texturas 2D que se van a usar en una vista de destino de representación.<br/>                |
| [**D3D11 \_ TEX2D \_ array \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_rtv1)<br/>                        | Describe los Subrecursos de una matriz de texturas 2D que se van a usar en una vista de destino de representación.<br/>                |
| [**D3D11 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_srv)<br/>                          | Especifica los Subrecursos de una matriz de texturas 2D que se van a usar en una vista de recursos de sombreador.<br/>              |
| [**D3D11 \_ TEX2D \_ array \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_srv1)<br/>                        | Describe los Subrecursos de una matriz de texturas 2D que se van a usar en una vista de recursos de sombreador.<br/>              |
| [**D3D11 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_uav)<br/>                          | Describe una matriz de recursos de textura 2D de acceso desordenado.<br/>                                           |
| [**D3D11 \_ TEX2D \_ array \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_uav1)<br/>                        | Describe una matriz de recursos de textura 2D de acceso desordenado.<br/>                                           |
| [**D3D11 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_dsv)<br/>                                       | Especifica el subrecurso de una textura 2D que es accesible para una vista de galería de símbolos de profundidad.<br/>                |
| [**D3D11 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_rtv)<br/>                                       | Especifica el subrecurso de una textura 2D que se va a usar en una vista de destino de representación.<br/>                            |
| [**D3D11 \_ TEX2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_rtv1)<br/>                                     | Describe el subrecurso de una textura 2D para usarlo en una vista de destino de representación.<br/>                            |
| [**D3D11 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_srv)<br/>                                       | Especifica el subrecurso de una textura 2D que se va a usar en una vista de recursos de sombreador.<br/>                          |
| [**D3D11 \_ TEX2D \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_srv1)<br/>                                     | Describe el subrecurso de una textura 2D para usarlo en una vista de recursos de sombreador.<br/>                          |
| [**D3D11 \_ TEX2D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_uav)<br/>                                       | Describe un recurso de textura 2D de acceso desordenado.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_uav1)<br/>                                     | Describe un recurso de textura 2D de acceso desordenado.<br/>                                                      |
| [**D3D11 \_ TEX2DMS \_ array \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_dsv)<br/>                      | Especifica los Subrecursos de una matriz de texturas 2D multimuestreadas para una vista de galería de símbolos de profundidad.<br/>         |
| [**D3D11 \_ TEX2DMS \_ matriz \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_rtv)<br/>                      | Especifica los Subrecursos de una matriz de texturas 2D multimuestreadas que se van a usar en una vista de destino de representación.<br/> |
| [**D3D11 \_ TEX2DMS \_ array \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_srv)<br/>                      | Especifica los Subrecursos de una matriz de texturas 2D multimuestreadas que se van a usar en una vista de recursos de sombreador.<br/> |
| [**D3D11 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_dsv)<br/>                                   | Especifica el subrecurso de una textura 2D multimuestreada a la que se puede acceder desde una vista de galería de símbolos de profundidad.<br/>   |
| [**D3D11 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_rtv)<br/>                                   | Especifica el subrecurso de una textura 2D multimuestreada que se va a usar en una vista de destino de representación.<br/>               |
| [**D3D11 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_srv)<br/>                                   | Especifica los Subrecursos de una textura 2D multimuestreada que se va a usar en una vista de recursos de sombreador.<br/>            |
| [**D3D11 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_rtv)<br/>                                       | Especifica los Subrecursos de una textura 3D que se usará en una vista de destino de representación.<br/>                           |
| [**D3D11 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_srv)<br/>                                       | Especifica los Subrecursos de una textura 3D que se va a usar en una vista de recursos de sombreador.<br/>                         |
| [**D3D11 \_ TEX3D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_uav)<br/>                                       | Describe un recurso de textura 3D de acceso desordenado.<br/>                                                      |
| [**D3D11 \_ TEXCUBE \_ array \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_array_srv)<br/>                      | Especifica los Subrecursos de una matriz de texturas de cubo que se van a usar en una vista de recursos de sombreador.<br/>            |
| [**D3D11 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_srv)<br/>                                   | Especifica el subrecurso de una textura del cubo que se va a usar en una vista de recursos del sombreador.<br/>                        |
| [**D3D11 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture1d_desc)<br/>                             | Describe una textura 1D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)<br/>                             | Describe una textura 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1)<br/>                           | Describe una textura 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture3d_desc)<br/>                             | Describe una textura 3D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1)<br/>                           | Describe una textura 3D.<br/>                                                                                |
| [**D3D11 \_ tamaño de la región de mosaico \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size)<br/>                        | Describe el tamaño de una región en mosaico.<br/>                                                                  |
| [**D3D11 \_ \_ coordenada de recursos en mosaico \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate)<br/>      | Describe las coordenadas de un recurso en mosaico.<br/>                                                         |
| [**\_Forma de mosaico D3D11 \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape)<br/>                                     | Describe la forma de un mosaico mediante la especificación de sus dimensiones.<br/>                                            |
| [**Descripción de la \_ \_ vista de acceso DESordenado D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc)<br/>   | Especifica los Subrecursos de un recurso al que se puede tener acceso mediante una vista de acceso desordenado.<br/>         |
| [**D3D11 \_ vista de acceso desordenado \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_unordered_access_view_desc1)<br/> | Describe los Subrecursos de un recurso al que se puede tener acceso mediante una vista de acceso desordenado.<br/>         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de recursos](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





