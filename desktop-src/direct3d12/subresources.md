---
title: Subrecursos (gráficos de Direct3D 12)
description: Describe cómo se divide un recurso en subcursos y cómo hacer referencia a un único, varios o segmentos de subrecursos.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fa8ea0d48fea7ee8e192d9dcf1fe5e3d22423
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072866"
---
# <a name="subresources-direct3d-12-graphics"></a>Subrecursos (gráficos de Direct3D 12)

Describe cómo se divide un recurso en subcursos y cómo hacer referencia a un único, varios o segmentos de subrecursos.

-   [Subrecursos de ejemplo](#example-subresources)
    -   [Indexación de subrecursos](#subresource-indexing)
    -   [Segmento mip](#mip-slice)
    -   [Segmento de matriz](#array-slice)
    -   [Segmento de plano](#plane-slice)
    -   [Varios subrecursos](#multiple-subresources)
-   [API de subrecursos](#subresource-apis)
-   [Temas relacionados](#related-topics)

## <a name="example-subresources"></a>Subrecursos de ejemplo

Si un recurso contiene un búfer, simplemente contiene un subrecurso con un índice de 0. Si el recurso contiene una textura (o matriz de textura), la referencia a los subrecursos es más compleja.

Algunas API acceden a un recurso completo (como el método [**ID3D12GraphicsCommandList::CopyResource), otras**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) acceden a una parte de un recurso (por ejemplo, el método [**ID3D12Resource::ReadFromSubresource).**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) Los métodos que acceden a una parte de un recurso suelen usar una descripción de vista (como la estructura [**SRV D3D12 \_ TEX2D \_ ARRAY) \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) para especificar los subrecursos a los que se va a acceder. Consulte la sección [Api de subrecursos](#subresource-apis) para obtener una lista completa.

### <a name="subresource-indexing"></a>Indexación de subrecursos

Para indexar un subrecurso determinado, los niveles de mip se indexa primero a medida que se indexa cada entrada de matriz.

![indexación de subrecursos](images/subresource-index.png)

### <a name="mip-slice"></a>Segmento mip

Un segmento mip incluye un nivel de mapa mip para cada textura de una matriz, como se muestra en la siguiente imagen.

![segmentos mip de subrecursos](images/subresource-mip-slice.png)

### <a name="array-slice"></a>Segmento de matriz

Dada una matriz de texturas, cada textura con mapas MIP, un segmento de matriz incluye una textura y todos sus niveles de mip, como se muestra en la siguiente imagen.

![segmentos de matriz de subrecursos](images/subresource-array-slices.png)

### <a name="plane-slice"></a>Segmento de plano

Normalmente, los formatos planas no se usan para almacenar datos RGBA, pero en los casos en los que se encuentran (quizás 24bpp RGB data), un plano podría representar la imagen roja, una la verde y otra la imagen azul. Sin embargo, un plano no es necesariamente un color, dos o más colores se pueden combinar en un plano. Normalmente, se usan datos planas para YCbCr sub sampled y Depth-Stencil datos. Depth-Stencil es el único formato que admite completamente mapas MIP, matrices y varios planos (a menudo plano 0 para profundidad y plano 1 para galería de símbolos).

A continuación se muestra la indexación de subrecursos para una matriz de dos Depth-Stencil imágenes, cada una con tres niveles de mip.

![indexación de galería de símbolos de profundidad](images/depth-stencil-indexing.png)

YCbCr sub sampled admite matrices y tiene planos, pero no admite mapas mip. Las imágenes YCbCr tienen dos planos, uno para la luminosidad (Y) a la que el ojo humano es más sensible y otro para la cromonidad (cb y cr, intercalada) a la que el ojo humano es menos sensible. Este formato permite la compresión de los valores de chrominance para comprimir una imagen sin afectar a la luminosidad, y es un formato de compresión de vídeo común por ese motivo, aunque se usa para comprimir imágenes fijas. En la imagen siguiente se muestra el formato NV12, que indica que la chrominance se comprimió a un cuarto de la resolución de la luminosidad, lo que significa que el ancho de cada plano es idéntico y que el plano de cromo es la mitad de la altura del plano de luminosidad. Los planos se indexarán como subrecursos de una manera idéntica a la Depth-Stencil ejemplo anterior.

![el formato nv12](images/ycbcr.png)

Los formatos planas existían en Direct3D 11, pero los planos individuales no se podían abordar individualmente, por ejemplo, para las operaciones de copia o asignación. Esto se cambió en Direct3D 12 para que cada plano recibiera su propio identificador de subrecurso. Compare los dos métodos siguientes para calcular el identificador de subrecurso.

Direct3D 11

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

Direct3D 12

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

La mayoría del hardware asume que la memoria del plano N siempre se asigna inmediatamente después del plano N-1.

Una alternativa al uso de subrecursos es que una aplicación podría asignar un recurso completamente independiente por plano. En este caso, la aplicación entiende que los datos son planas y usa varios recursos para representarlo.

### <a name="multiple-subresources"></a>Varios subrecursos

Una vista de recursos de sombreador puede seleccionar cualquier región rectangular de subrecursos, mediante uno de los segmentos descritos anteriormente y el uso de campos en las estructuras de vista (como [**D3D12 \_ TEX2D \_ ARRAY \_ SRV),**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)como se muestra en la imagen.

![selección de varios subrecursos](images/subresource-multiple.png)

Una vista de destino de representación solo puede usar un único subcurso o segmento mip y no puede incluir subrecursos de más de un segmento mip. Es decir, todas las texturas de una vista de destino de representación deben tener el mismo tamaño. Una vista de sombreador y recurso puede seleccionar cualquier región rectangular de subrecursos, como se muestra en la imagen.

## <a name="subresource-apis"></a>API de subrecursos

Las siguientes API hacen referencia y funcionan con recursos subcursos:

Enumeraciones:

-   [**TIPO DE COPIA DE TEXTURA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

Las siguientes estructuras contienen *índices PlaneSlice,* la mayoría de *ellos índices MipSlice.*

-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEXAS2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEXAS2D \_ ARRAY \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Las estructuras siguientes contienen *índices ArraySlice,* la mayoría contienen *índices MipSlice.*

-   [**D3D12 \_ TEXAS1D \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEXAS1D \_ ARRAY \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEXAS2D \_ ARRAY \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Las estructuras siguientes contienen *índices MipSlice,* pero no *índices ArraySlice* ni *PlaneSlice.*

-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [**D3D12 \_ TEXAS1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEXAS3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

Las estructuras siguientes también hacen referencia a los subrecursos:

-   [**D3D12 \_ DISCARD \_ REGION:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) estructura que se usa como preparación para descartar un recurso.
-   [**D3D12 \_ PLACED \_ SUBRESOURCE \_ FOOTPRINT :**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) agrega un desplazamiento en un recurso a la superficie básica.
-   [**D3D12 \_ BARRERA \_ DE \_ TRANSICIÓN DE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) RECURSOS: describe la transición de los subrecursos entre distintos usos (recurso de sombreador, destino de representación, etc.).
-   [**D3D12 \_ SUBRESOURCE \_ DATA:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) los datos de subrecurso incluyen los propios datos y el tono de fila y segmento.
-   [**D3D12 \_ SUBRESOURCE \_ FOOTPRINT:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) una superficie incluye el formato, el ancho, el alto, la profundidad y el tono de fila del subrecurso.
-   [**D3D12 \_ SUBRESOURCE \_ INFO:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) contiene el desplazamiento, el paso de fila y el tono de profundidad del subrecurso.
-   [**D3D12 \_ SUBRESOURCE \_ TILING:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) describe un volumen de subrecursos en mosaico (consulte Recursos en mosaico [de volumen).](volume-tiled-resources.md)
-   [**D3D12 \_ TEXTURE \_ COPY \_ LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : describe una parte de una textura con el fin de copiar.
-   [**D3D12 \_ \_ \_ COORDENADA DE RECURSOS EN MOSAICO:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) describe las coordenadas de un recurso en mosaico.

Métodos:

-   [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : obtiene información sobre un recurso para permitir que se haga una copia.
-   [**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : obtiene información sobre cómo un recurso en mosaico se divide en iconos.
-   [**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copia un subrecurso de varias muestras en un subrecurso que no tiene varias muestras.
-   [**ID3D12Resource::Map:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) devuelve un puntero a los datos especificados en el recurso y deniega el acceso de GPU al subrecurso.
-   [**ID3D12Resource::ReadFromSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) copia datos de un subrecurso o de una región rectangular de un subrecurso.
-   [**ID3D12Resource::Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : desmapa el intervalo de memoria especificado e invalida el puntero al recurso. Restablece el acceso de GPU al subrecurso.
-   [**ID3D12Resource::WriteToSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) copia los datos en un subrecurso o en una región rectangular de un subrecurso.

Las texturas deben estar en el estado [**D3D12 \_ RESOURCE \_ STATE \_ COMMON**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) para que el acceso de CPU a través de [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) y [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) sea legal, pero los búferes no. El acceso de LA CPU a un recurso normalmente se realiza a través [**de Asignar**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

 




