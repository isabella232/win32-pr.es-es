---
title: Subrecursos (gráficos de Direct3D 11)
description: En este tema se describen los Subrecursos de textura o partes de un recurso.
ms.assetid: 57444cb5-6c8b-4dac-8d6b-ca2b45eafac9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a432dbfbcbf08c4359ea436a3e8fa025c801d12
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078672"
---
# <a name="subresources-direct3d-11-graphics"></a>Subrecursos (gráficos de Direct3D 11)

En este tema se describen los Subrecursos de textura o partes de un recurso.

Direct3D puede hacer referencia a un recurso completo o puede hacer referencia a subconjuntos de un recurso. El término subresource hace referencia a un subconjunto de un recurso.

Un búfer se define como un subrecurso único. Las texturas son un poco más complicadas porque existen varios tipos de textura diferentes (1D, 2D, etc.), algunos de los cuales admiten niveles de mipmap o matrices de texturas. A partir del caso más simple, una textura 1D se define como un subrecurso único, tal como se muestra en la siguiente ilustración.

![Ilustración de una textura 1D](images/d3d10-1d-texture.png)

Esto significa que la matriz de textura que componen una textura 1D está contenida en un solo subrecurso.

Si expande una textura 1D con tres niveles de mipmap, se puede visualizar como la siguiente ilustración.

![Ilustración de una textura 1D con tres niveles de mipmap](images/d3d10-resource-texture1d.png)

Piense en esto como una sola textura que se compone de tres Subrecursos. Un subrecurso se puede indizar mediante el nivel de detalle (LOD) para una sola textura. Cuando se usa una matriz de texturas, el acceso a un subrecurso determinado requiere el LOD y la textura determinada. Como alternativa, la API combina estos dos fragmentos de información en un único índice de subrecurso basado en cero, tal como se muestra en la siguiente ilustración.

![Ilustración de un índice de subrecurso basado en cero](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a>Selección de Subrecursos

Algunas API acceden a un recurso completo (por ejemplo, el método [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) ), otros tienen acceso a una parte de un recurso (por ejemplo, el método [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) o el método [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) ). Los métodos que tienen acceso a una parte de un recurso suelen usar una descripción de la vista (como la estructura DSV de la [**\_ \_ matriz \_ D3D11 TEX2D**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) ) para especificar los Subrecursos a los que se va a tener acceso.

En las ilustraciones de las secciones siguientes se muestran los términos utilizados por una descripción de la vista al obtener acceso a una matriz de texturas.

### <a name="array-slice"></a>Segmento de matriz

Dada una matriz de texturas, cada textura con los mapas MIP, un *segmento de matriz* (representado por el rectángulo blanco) incluye una textura y todos sus Subrecursos, tal como se muestra en la siguiente ilustración.

![Ilustración de un segmento de matriz](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Segmento MIP

Un *segmento de MIP* (representado por el rectángulo blanco) incluye un nivel de mipmap para cada textura de una matriz, como se muestra en la siguiente ilustración.

![Ilustración de un segmento MIP](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Selección de un único subrecurso

Puede usar estos dos tipos de segmentos para elegir un solo subrecurso, tal como se muestra en la siguiente ilustración.

![Ilustración de cómo elegir un subrecurso mediante un segmento de matriz y un segmento de MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Seleccionar varios Subrecursos

También puede usar estos dos tipos de segmentos con el número de niveles de mipmap y/o el número de texturas para elegir varios Subrecursos, tal como se muestra en la siguiente ilustración.

![Ilustración de la elección de varios Subrecursos](images/d3d10-resource-subresources-2.png)

> [!Note]  
> Una [**vista de destino de representación**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) solo puede utilizar un solo subrecurso o segmento MIP y no puede incluir Subrecursos de más de un segmento de MIP. Es decir, cada textura de una vista de representación-destino debe tener el mismo tamaño. Una [**vista de recursos de sombreador**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) puede seleccionar cualquier región rectangular de Subrecursos, tal como se muestra en la ilustración.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




