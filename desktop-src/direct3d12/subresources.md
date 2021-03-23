---
title: Subrecursos (gráficos de Direct3D 12)
description: Describe cómo un recurso se divide en Subrecursos y cómo hacer referencia a un único, varios o un segmento de Subrecursos.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fa8ea0d48fea7ee8e192d9dcf1fe5e3d22423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104549128"
---
# <a name="subresources-direct3d-12-graphics"></a>Subrecursos (gráficos de Direct3D 12)

Describe cómo un recurso se divide en Subrecursos y cómo hacer referencia a un único, varios o un segmento de Subrecursos.

-   [Subrecursos de ejemplo](#example-subresources)
    -   [Indexación de Subrecursos](#subresource-indexing)
    -   [Segmento MIP](#mip-slice)
    -   [Segmento de matriz](#array-slice)
    -   [Segmento de plano](#plane-slice)
    -   [Varios Subrecursos](#multiple-subresources)
-   [API de subrecurso](#subresource-apis)
-   [Temas relacionados](#related-topics)

## <a name="example-subresources"></a>Subrecursos de ejemplo

Si un recurso contiene un búfer, simplemente contiene un subrecurso con un índice de 0. Si el recurso contiene una textura (o matriz de textura), la referencia a los Subrecursos es más compleja.

Algunas API acceden a un recurso completo (como el método [**ID3D12GraphicsCommandList:: CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) ), mientras que otras acceden a una parte de un recurso (por ejemplo, el método [**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ). Los métodos que tienen acceso a una parte de un recurso suelen usar una descripción de la vista (como la estructura SRV de la [**\_ \_ matriz \_ D3D12 TEX2D**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) ) para especificar los Subrecursos a los que se va a tener acceso. Consulte la sección [API de subrecurso](#subresource-apis) para obtener una lista completa.

### <a name="subresource-indexing"></a>Indexación de Subrecursos

Para indexar un subrecurso determinado, los niveles de MIP se indexan primero a medida que cada entrada de la matriz está indizada.

![indexación de Subrecursos](images/subresource-index.png)

### <a name="mip-slice"></a>Segmento MIP

Un segmento de MIP incluye un nivel de mipmap para cada textura de una matriz, como se muestra en la siguiente imagen.

![Subrecursos MIP slices](images/subresource-mip-slice.png)

### <a name="array-slice"></a>Segmento de matriz

Dada una matriz de texturas, cada textura con los mapas MIP, un segmento de matriz incluye una textura y todos sus niveles de MIP, tal como se muestra en la siguiente imagen.

![segmentos de la matriz de Subrecursos](images/subresource-array-slices.png)

### <a name="plane-slice"></a>Segmento de plano

Normalmente, los formatos planos no se usan para almacenar datos RGBA, pero en los casos en los que es (quizás 24 BPP datos RGB), un plano podría representar la imagen roja, una verde y una imagen azul. Aunque un plano no es necesariamente un color, se pueden combinar dos o más colores en un plano. Normalmente, se usan datos planos más para los datos YCbCr y Depth-Stencil submuestreados. Depth-Stencil es el único formato que admite totalmente los mapas MIP, las matrices y varios planos (a menudo, el plano 0 para la profundidad y el plano 1 para la galería de símbolos).

A continuación se muestra la indexación de Subrecursos para una matriz de dos Depth-Stencil imágenes, cada una con tres niveles de MIP.

![indexación de estarcido de profundidad](images/depth-stencil-indexing.png)

La submuestreada YCbCr admite matrices y tiene planos, pero no admite los mapas MIP. Las imágenes de YCbCr tienen dos planos, uno para la luminancia (Y) que el ojo humano es más sensible, y otro para la crominancia (ambos CB y CR, intercalados) que el ojo humano es menos sensible. Este formato habilita la compresión de los valores de crominancia para comprimir una imagen sin que afecte a la luminancia, y es un formato de compresión de vídeo común por esa razón, aunque se usa para comprimir imágenes fijas. La imagen siguiente muestra el formato NV12, teniendo en cuenta que la crominancia se ha comprimido a un cuarto de la resolución de la luminancia, lo que significa que el ancho de cada plano es idéntico y el plano de crominancia es la mitad del alto del plano de luminancia. Los planos se indexarían como Subrecursos de una manera idéntica al Depth-Stencil ejemplo anterior.

![el formato nv12](images/ycbcr.png)

Los formatos planos existían en Direct3D 11, pero los planos individuales no se pudieron direccionar individualmente, por ejemplo, para las operaciones de copia o asignación. Esto se ha cambiado en Direct3D 12 para que cada plano reciba su propio identificador de subrecurso. Compare los dos métodos siguientes para calcular el identificador del subrecurso.

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

La mayoría del hardware supone que la memoria para el plano N siempre se asigna inmediatamente después del plano N-1.

Una alternativa al uso de Subrecursos es que una aplicación podría asignar un recurso completamente independiente por plano. En este caso, la aplicación entiende que los datos son planos y utiliza varios recursos para representarlos.

### <a name="multiple-subresources"></a>Varios Subrecursos

Una vista de recursos del sombreador puede seleccionar cualquier región rectangular de Subrecursos, mediante uno de los segmentos descritos anteriormente y el uso prudente de los campos en las estructuras de la vista (como [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), tal como se muestra en la imagen.

![selección de varios recursos](images/subresource-multiple.png)

Una vista de destino de representación solo puede utilizar un solo subrecurso o segmento MIP y no puede incluir Subrecursos de más de un segmento de MIP. Es decir, cada textura de una vista de representación-destino debe tener el mismo tamaño. Una vista de recursos de sombreador puede seleccionar cualquier región rectangular de Subrecursos, tal como se muestra en la imagen.

## <a name="subresource-apis"></a>API de subrecurso

Las siguientes API hacen referencia y funcionan con Subrecursos:

Enumeraciones:

-   [**\_Tipo de \_ copia de textura D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

Las siguientes estructuras contienen índices de *PlaneSlice* , la mayoría de ellos contienen índices de *MipSlice* .

-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2D \_ matriz \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Las siguientes estructuras contienen índices de *ArraySlice* , la mayoría de ellos contienen índices de *MipSlice* .

-   [**D3D12 \_ TEX1D \_ array \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**D3D12 \_ TEX2D \_ array \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**D3D12 \_ TEX2DMS \_ array \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [**D3D12 \_ TEX1D \_ matriz \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ matriz \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ matriz \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX1D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX1D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Las siguientes estructuras contienen índices *MipSlice* , pero no *ArraySlice* ni *PlaneSlice* índices.

-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

Las siguientes estructuras también hacen referencia a Subrecursos:

-   [**D3D12 \_ Descartar \_ región**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : una estructura que se utiliza como preparación para descartar un recurso.
-   [**D3D12 \_ \_ \_ Superficie de subrecurso colocada**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : agrega un desplazamiento a un recurso a la superficie básica.
-   [**D3D12 \_ \_ \_ Barrera de transición de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : describe la transición de Subrecursos entre distintos usos (recursos del sombreador, destino de representación, etc.).
-   [**D3D12 \_ \_Datos de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : los datos del subrecurso incluyen los datos en sí y el paso de la fila y del segmento.
-   [**D3D12 \_ \_Superficie de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : una superficie incluye el formato, el ancho, el alto, la profundidad y el tono de fila del subrecurso.
-   [**D3D12 \_ \_Información de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contiene el desplazamiento, el paso de fila y el tono de profundidad del subrecurso.
-   [**D3D12 \_ \_Mosaico de Subrecursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : describe un volumen de Subrecursos en mosaico (consulte [los recursos en mosaico del volumen](volume-tiled-resources.md)).
-   [**D3D12 \_ \_ \_ Ubicación de copia de textura**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : describe una parte de una textura con el fin de copiar.
-   [**D3D12 \_ Coordenada \_ de \_ recursos en mosaico**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : describe las coordenadas de un recurso en mosaico.

Métodos:

-   [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : obtiene información sobre un recurso, para permitir que se realice una copia.
-   [**ID3D12Device:: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : obtiene información sobre cómo un recurso en mosaico se divide en mosaicos.
-   [**ID3D12GraphicsCommandList:: ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copia un subrecurso de muestreo múltiple en un subrecurso de muestreo no múltiple.
-   [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : devuelve un puntero a los datos especificados en el recurso y deniega el acceso de la GPU al subrecurso.
-   [**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copia datos de un subrecurso o de una región rectangular de un subrecurso.
-   [**ID3D12Resource::**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) desasignar: desasigna el intervalo de memoria especificado y invalida el puntero al recurso. Restablece el acceso de la GPU al subrecurso.
-   [**ID3D12Resource:: WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copia datos en un subrecurso o en una región rectangular de un subrecurso.

Las texturas deben estar en el estado de [**recurso de D3D12 estado \_ \_ \_ común**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) de acceso de CPU a través de [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) y [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) para ser legales, pero no los búferes. El acceso de CPU a un recurso se realiza normalmente a través de [**asignación de asignación**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

 




