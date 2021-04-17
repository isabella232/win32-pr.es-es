---
description: Estructuras utilizadas para crear y usar recursos.
ms.assetid: d8fe2ebe-349a-456e-9a5a-16f2d3419800
title: Estructuras de recursos (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da964bf19c1ce5e1e5c4dfd0685df79b28ac5e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705281"
---
# <a name="resource-structures-direct3d-10-graphics"></a>Estructuras de recursos (gráficos de Direct3D 10)

Estructuras utilizadas para crear y usar [recursos](d3d10-graphics-programming-guide-resources-types.md).



| Estructuras                                                                 | Descripción                                                                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DESC. de búfer de D3D10 \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)                           | Descripción de un recurso de [búfer](d3d10-graphics-programming-guide-resources-types.md) .                                                                     |
| [**D3D10 \_ búfer \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_rtv)                             | Describe los elementos de un [búfer](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de destino de representación.                                |
| [**\_SRV de búfer de D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_srv)                             | Describe los elementos de un recurso de [búfer](d3d10-graphics-programming-guide-resources-types.md) para usar en una vista de recursos de sombreador.                         |
| [**D3D10 \_ de \_ estarcido de profundidad \_ vista \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_view_desc) | Describe una vista de galería de símbolos de profundidad.                                                                                                                               |
| [**\_TEXTURE2D asignado \_ D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture2d)                 | Proporciona acceso a los datos de subrecurso en una [textura 2D](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**\_TEXTURE3D asignado \_ D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture3d)                 | Proporciona acceso a los datos de subrecurso en una [textura 3D](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**Descripción de la vista de destino de \_ representación D3D10 \_ \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_render_target_view_desc) | Describe una vista de destino de representación.                                                                                                                               |
| [**\_Datos de SUBRECURSO D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)                 | Especifica los datos para inicializar un recurso.                                                                                                                   |
| [**D3D10 \_ TEX1D \_ array \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_dsv)                  | Especifica qué nivel de mipmap y texturas de una [matriz de textura 1D](d3d10-graphics-programming-guide-resources-types.md) se van a utilizar en una vista de galería de símbolos de profundidad.       |
| [**D3D10 \_ TEX1D \_ matriz \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_rtv)                  | Especifica los Subrecursos de una matriz de [texturas 1D](d3d10-graphics-programming-guide-resources-types.md) que se van a usar en una vista de destino de representación.             |
| [**D3D10 \_ TEX1D \_ array \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_srv)                  | Especifica los niveles y las texturas de mipmap en una [matriz de textura 1D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de recursos de sombreador.      |
| [**D3D10 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_dsv)                               | Especifica los Subrecursos de una [textura 1D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de galería de símbolos de profundidad.                        |
| [**D3D10 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_rtv)                               | Especifica los Subrecursos de una [textura 1D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de destino de representación.                        |
| [**D3D10 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_srv)                               | Especifica los Subrecursos de una [textura 1D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de recursos de sombreador.                      |
| [**D3D10 \_ TEX2D \_ array \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)                  | Especifica qué nivel de mipmap y qué texturas de una [matriz de textura 2D](d3d10-graphics-programming-guide-resources-types.md) se van a utilizar en una vista de galería de símbolos de profundidad. |
| [**D3D10 \_ TEX2D \_ matriz \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_rtv)                  | Especifica qué nivel de mipmap y qué texturas de una [matriz de textura 2D](d3d10-graphics-programming-guide-resources-types.md) se van a usar en una vista de destino de representación. |
| [**D3D10 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_srv)                  | Especifica los Subrecursos de una matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) que se van a usar en una vista de recursos de sombreador.           |
| [**D3D10 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_dsv)                               | Especifica los Subrecursos de una [textura 2D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de galería de símbolos de profundidad.                        |
| [**D3D10 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_rtv)                               | Especifica los Subrecursos de una [textura 2D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de destino de representación.                        |
| [**D3D10 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_srv)                               | Especifica los Subrecursos de una [textura 2D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de recursos de sombreador.                      |
| [**D3D10 \_ TEX2DMS \_ array \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_dsv)              | Especifica los Subrecursos de una matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) que se van a usar en una vista de galería de símbolos de profundidad.             |
| [**D3D10 \_ TEX2DMS \_ matriz \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_rtv)              | Especifica los Subrecursos de una matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) que se van a usar en una vista de destino de representación.             |
| [**D3D10 \_ TEX2DMS \_ array \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_srv)              | Especifica los Subrecursos de una matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) que se van a usar en una vista de recursos de sombreador.           |
| [**D3D10 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_dsv)                           | Especifica los Subrecursos de una [textura 2D](d3d10-graphics-programming-guide-resources-types.md) multimuestreada que se va a usar en una vista de galería de símbolos de profundidad.           |
| [**D3D10 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_rtv)                           | Especifica los Subrecursos de una [textura 2D](d3d10-graphics-programming-guide-resources-types.md) multimuestreada que se va a usar en una vista de destino de representación.           |
| [**D3D10 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_srv)                           | Especifica los Subrecursos de una [textura 2D](d3d10-graphics-programming-guide-resources-types.md) multimuestreada que se va a usar en una vista de recursos de sombreador.         |
| [**D3D10 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_rtv)                               | Especifica los Subrecursos de una [textura 3D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de destino de representación.                        |
| [**D3D10 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_srv)                               | Especifica los Subrecursos de una [textura 3D](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de recursos de sombreador.                      |
| [**D3D10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)            | Especifica los Subrecursos de una textura del [cubo](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de recursos de sombreador.                    |
| [**D3D10 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_texcube_srv)                           | Especifica los Subrecursos de una textura del [cubo](d3d10-graphics-programming-guide-resources-types.md) que se va a usar en una vista de recursos de sombreador.                    |
| [**D3D10 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture1d_desc)                     | Describe un recurso de [textura 1D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |
| [**D3D10 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture2d_desc)                     | Describe un recurso de [textura 2D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |
| [**D3D10 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture3d_desc)                     | Describe un recurso de [textura 3D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de recursos](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



