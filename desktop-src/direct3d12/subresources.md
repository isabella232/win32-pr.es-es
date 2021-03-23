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
# <a name="subresources-direct3d-12-graphics"></a><span data-ttu-id="a0a15-103">Subrecursos (gráficos de Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="a0a15-103">Subresources (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="a0a15-104">Describe cómo un recurso se divide en Subrecursos y cómo hacer referencia a un único, varios o un segmento de Subrecursos.</span><span class="sxs-lookup"><span data-stu-id="a0a15-104">Describes how a resource is divided into subresources, and how to reference a single, multiple or slice of subresources.</span></span>

-   [<span data-ttu-id="a0a15-105">Subrecursos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0a15-105">Example subresources</span></span>](#example-subresources)
    -   [<span data-ttu-id="a0a15-106">Indexación de Subrecursos</span><span class="sxs-lookup"><span data-stu-id="a0a15-106">Subresource indexing</span></span>](#subresource-indexing)
    -   [<span data-ttu-id="a0a15-107">Segmento MIP</span><span class="sxs-lookup"><span data-stu-id="a0a15-107">Mip slice</span></span>](#mip-slice)
    -   [<span data-ttu-id="a0a15-108">Segmento de matriz</span><span class="sxs-lookup"><span data-stu-id="a0a15-108">Array slice</span></span>](#array-slice)
    -   [<span data-ttu-id="a0a15-109">Segmento de plano</span><span class="sxs-lookup"><span data-stu-id="a0a15-109">Plane slice</span></span>](#plane-slice)
    -   [<span data-ttu-id="a0a15-110">Varios Subrecursos</span><span class="sxs-lookup"><span data-stu-id="a0a15-110">Multiple subresources</span></span>](#multiple-subresources)
-   [<span data-ttu-id="a0a15-111">API de subrecurso</span><span class="sxs-lookup"><span data-stu-id="a0a15-111">Subresource APIs</span></span>](#subresource-apis)
-   [<span data-ttu-id="a0a15-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0a15-112">Related topics</span></span>](#related-topics)

## <a name="example-subresources"></a><span data-ttu-id="a0a15-113">Subrecursos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0a15-113">Example subresources</span></span>

<span data-ttu-id="a0a15-114">Si un recurso contiene un búfer, simplemente contiene un subrecurso con un índice de 0.</span><span class="sxs-lookup"><span data-stu-id="a0a15-114">If a resource contains a buffer, then it simply contains one subresource with an index of 0.</span></span> <span data-ttu-id="a0a15-115">Si el recurso contiene una textura (o matriz de textura), la referencia a los Subrecursos es más compleja.</span><span class="sxs-lookup"><span data-stu-id="a0a15-115">If the resource contains a texture (or texture array), then referencing the subresources is more complex.</span></span>

<span data-ttu-id="a0a15-116">Algunas API acceden a un recurso completo (como el método [**ID3D12GraphicsCommandList:: CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) ), mientras que otras acceden a una parte de un recurso (por ejemplo, el método [**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ).</span><span class="sxs-lookup"><span data-stu-id="a0a15-116">Some APIs access an entire resource (such as the [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) method), others access a portion of a resource (for example the [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) method).</span></span> <span data-ttu-id="a0a15-117">Los métodos que tienen acceso a una parte de un recurso suelen usar una descripción de la vista (como la estructura SRV de la [**\_ \_ matriz \_ D3D12 TEX2D**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) ) para especificar los Subrecursos a los que se va a tener acceso.</span><span class="sxs-lookup"><span data-stu-id="a0a15-117">The methods that access a portion of a resource generally use a view description (such as the [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) structure) to specify the subresources to access.</span></span> <span data-ttu-id="a0a15-118">Consulte la sección [API de subrecurso](#subresource-apis) para obtener una lista completa.</span><span class="sxs-lookup"><span data-stu-id="a0a15-118">Refer to the [Subresource APIs](#subresource-apis) section for a complete list.</span></span>

### <a name="subresource-indexing"></a><span data-ttu-id="a0a15-119">Indexación de Subrecursos</span><span class="sxs-lookup"><span data-stu-id="a0a15-119">Subresource indexing</span></span>

<span data-ttu-id="a0a15-120">Para indexar un subrecurso determinado, los niveles de MIP se indexan primero a medida que cada entrada de la matriz está indizada.</span><span class="sxs-lookup"><span data-stu-id="a0a15-120">To index a particular subresource, the mip levels are indexed first as each array entry is indexed.</span></span>

![indexación de Subrecursos](images/subresource-index.png)

### <a name="mip-slice"></a><span data-ttu-id="a0a15-122">Segmento MIP</span><span class="sxs-lookup"><span data-stu-id="a0a15-122">Mip slice</span></span>

<span data-ttu-id="a0a15-123">Un segmento de MIP incluye un nivel de mipmap para cada textura de una matriz, como se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="a0a15-123">A mip slice includes one mipmap level for every texture in an array, as shown in the following image.</span></span>

![Subrecursos MIP slices](images/subresource-mip-slice.png)

### <a name="array-slice"></a><span data-ttu-id="a0a15-125">Segmento de matriz</span><span class="sxs-lookup"><span data-stu-id="a0a15-125">Array slice</span></span>

<span data-ttu-id="a0a15-126">Dada una matriz de texturas, cada textura con los mapas MIP, un segmento de matriz incluye una textura y todos sus niveles de MIP, tal como se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="a0a15-126">Given an array of textures, each texture with mipmaps, an array slice includes one texture and all of its mip levels, as shown in the following image.</span></span>

![segmentos de la matriz de Subrecursos](images/subresource-array-slices.png)

### <a name="plane-slice"></a><span data-ttu-id="a0a15-128">Segmento de plano</span><span class="sxs-lookup"><span data-stu-id="a0a15-128">Plane slice</span></span>

<span data-ttu-id="a0a15-129">Normalmente, los formatos planos no se usan para almacenar datos RGBA, pero en los casos en los que es (quizás 24 BPP datos RGB), un plano podría representar la imagen roja, una verde y una imagen azul.</span><span class="sxs-lookup"><span data-stu-id="a0a15-129">Typically planar formats are not used to store RGBA data, but in the cases where it is (perhaps 24bpp RGB data), one plane could represent the red image, one the green, and one the blue image.</span></span> <span data-ttu-id="a0a15-130">Aunque un plano no es necesariamente un color, se pueden combinar dos o más colores en un plano.</span><span class="sxs-lookup"><span data-stu-id="a0a15-130">One plane though is not necessarily one color, two or more colors could be combined into one plane.</span></span> <span data-ttu-id="a0a15-131">Normalmente, se usan datos planos más para los datos YCbCr y Depth-Stencil submuestreados.</span><span class="sxs-lookup"><span data-stu-id="a0a15-131">More typically planar data is used for sub-sampled YCbCr and Depth-Stencil data.</span></span> <span data-ttu-id="a0a15-132">Depth-Stencil es el único formato que admite totalmente los mapas MIP, las matrices y varios planos (a menudo, el plano 0 para la profundidad y el plano 1 para la galería de símbolos).</span><span class="sxs-lookup"><span data-stu-id="a0a15-132">Depth-Stencil is the only format that fully supports mipmaps, arrays, and multiple planes (often plane 0 for Depth and plane 1 for Stencil).</span></span>

<span data-ttu-id="a0a15-133">A continuación se muestra la indexación de Subrecursos para una matriz de dos Depth-Stencil imágenes, cada una con tres niveles de MIP.</span><span class="sxs-lookup"><span data-stu-id="a0a15-133">The subresource indexing for an array of two Depth-Stencil images, each with three mip levels, is shown below.</span></span>

![indexación de estarcido de profundidad](images/depth-stencil-indexing.png)

<span data-ttu-id="a0a15-135">La submuestreada YCbCr admite matrices y tiene planos, pero no admite los mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="a0a15-135">Sub-sampled YCbCr supports arrays and has planes, but does not support mipmaps.</span></span> <span data-ttu-id="a0a15-136">Las imágenes de YCbCr tienen dos planos, uno para la luminancia (Y) que el ojo humano es más sensible, y otro para la crominancia (ambos CB y CR, intercalados) que el ojo humano es menos sensible.</span><span class="sxs-lookup"><span data-stu-id="a0a15-136">YCbCr images have two planes, one for the luminance (Y) that the human eye is most sensitive to, and one for the chrominance (both Cb, and Cr, interleaved) which the human eye is less sensitive to.</span></span> <span data-ttu-id="a0a15-137">Este formato habilita la compresión de los valores de crominancia para comprimir una imagen sin que afecte a la luminancia, y es un formato de compresión de vídeo común por esa razón, aunque se usa para comprimir imágenes fijas.</span><span class="sxs-lookup"><span data-stu-id="a0a15-137">This format enables compression of the chrominance values in order to compress an image without affecting the luminance, and is a common video compression format for that reason, although it is used to compress still images.</span></span> <span data-ttu-id="a0a15-138">La imagen siguiente muestra el formato NV12, teniendo en cuenta que la crominancia se ha comprimido a un cuarto de la resolución de la luminancia, lo que significa que el ancho de cada plano es idéntico y el plano de crominancia es la mitad del alto del plano de luminancia.</span><span class="sxs-lookup"><span data-stu-id="a0a15-138">The image below shows the NV12 format, noting the chrominance has been compressed to one quarter of the resolution of the luminance, meaning the width of each plane is identical, and the chrominance plane is half the height of the luminance plane.</span></span> <span data-ttu-id="a0a15-139">Los planos se indexarían como Subrecursos de una manera idéntica al Depth-Stencil ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="a0a15-139">The planes would be indexed as subresources in an identical way to the Depth-Stencil example above.</span></span>

![el formato nv12](images/ycbcr.png)

<span data-ttu-id="a0a15-141">Los formatos planos existían en Direct3D 11, pero los planos individuales no se pudieron direccionar individualmente, por ejemplo, para las operaciones de copia o asignación.</span><span class="sxs-lookup"><span data-stu-id="a0a15-141">Planar formats existed in Direct3D 11, but individual planes could not be addressed individually, say for copy or mapping operations.</span></span> <span data-ttu-id="a0a15-142">Esto se ha cambiado en Direct3D 12 para que cada plano reciba su propio identificador de subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a0a15-142">This was changed in Direct3D 12 so that each plane received its own subresource ID.</span></span> <span data-ttu-id="a0a15-143">Compare los dos métodos siguientes para calcular el identificador del subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a0a15-143">Compare the following two methods for calculating the subresource ID.</span></span>

<span data-ttu-id="a0a15-144">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a0a15-144">Direct3D 11</span></span>

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

<span data-ttu-id="a0a15-145">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a0a15-145">Direct3D 12</span></span>

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

<span data-ttu-id="a0a15-146">La mayoría del hardware supone que la memoria para el plano N siempre se asigna inmediatamente después del plano N-1.</span><span class="sxs-lookup"><span data-stu-id="a0a15-146">Most hardware assumes that the memory for plane N is always immediately allocated after plane N-1.</span></span>

<span data-ttu-id="a0a15-147">Una alternativa al uso de Subrecursos es que una aplicación podría asignar un recurso completamente independiente por plano.</span><span class="sxs-lookup"><span data-stu-id="a0a15-147">An alternative to using subresources is that an app could allocate a completely separate resource per plane.</span></span> <span data-ttu-id="a0a15-148">En este caso, la aplicación entiende que los datos son planos y utiliza varios recursos para representarlos.</span><span class="sxs-lookup"><span data-stu-id="a0a15-148">In this case, the application understands the data is planar and uses multiple resources to represent it.</span></span>

### <a name="multiple-subresources"></a><span data-ttu-id="a0a15-149">Varios Subrecursos</span><span class="sxs-lookup"><span data-stu-id="a0a15-149">Multiple subresources</span></span>

<span data-ttu-id="a0a15-150">Una vista de recursos del sombreador puede seleccionar cualquier región rectangular de Subrecursos, mediante uno de los segmentos descritos anteriormente y el uso prudente de los campos en las estructuras de la vista (como [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), tal como se muestra en la imagen.</span><span class="sxs-lookup"><span data-stu-id="a0a15-150">A shader-resource view can select any rectangular region of subresources, using one of the slices described above and judicious use of fields in the view structures (such as [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), as shown in the image.</span></span>

![selección de varios recursos](images/subresource-multiple.png)

<span data-ttu-id="a0a15-152">Una vista de destino de representación solo puede utilizar un solo subrecurso o segmento MIP y no puede incluir Subrecursos de más de un segmento de MIP.</span><span class="sxs-lookup"><span data-stu-id="a0a15-152">A render-target view can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="a0a15-153">Es decir, cada textura de una vista de representación-destino debe tener el mismo tamaño.</span><span class="sxs-lookup"><span data-stu-id="a0a15-153">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="a0a15-154">Una vista de recursos de sombreador puede seleccionar cualquier región rectangular de Subrecursos, tal como se muestra en la imagen.</span><span class="sxs-lookup"><span data-stu-id="a0a15-154">A shader-resource view can select any rectangular region of subresources, as shown in the image.</span></span>

## <a name="subresource-apis"></a><span data-ttu-id="a0a15-155">API de subrecurso</span><span class="sxs-lookup"><span data-stu-id="a0a15-155">Subresource APIs</span></span>

<span data-ttu-id="a0a15-156">Las siguientes API hacen referencia y funcionan con Subrecursos:</span><span class="sxs-lookup"><span data-stu-id="a0a15-156">The following APIs reference and work with subresources:</span></span>

<span data-ttu-id="a0a15-157">Enumeraciones:</span><span class="sxs-lookup"><span data-stu-id="a0a15-157">Enumerations:</span></span>

-   [<span data-ttu-id="a0a15-158">**\_Tipo de \_ copia de textura D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="a0a15-158">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

<span data-ttu-id="a0a15-159">Las siguientes estructuras contienen índices de *PlaneSlice* , la mayoría de ellos contienen índices de *MipSlice* .</span><span class="sxs-lookup"><span data-stu-id="a0a15-159">The following structures contain *PlaneSlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="a0a15-160">**D3D12 \_ TEX2D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-160">**D3D12\_TEX2D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [<span data-ttu-id="a0a15-161">**D3D12 \_ TEX2D \_ matriz \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-161">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="a0a15-162">**D3D12 \_ TEX2D \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-162">**D3D12\_TEX2D\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [<span data-ttu-id="a0a15-163">**D3D12 \_ TEX2D \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-163">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="a0a15-164">**D3D12 \_ TEX2D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-164">**D3D12\_TEX2D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [<span data-ttu-id="a0a15-165">**D3D12 \_ TEX2D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-165">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="a0a15-166">Las siguientes estructuras contienen índices de *ArraySlice* , la mayoría de ellos contienen índices de *MipSlice* .</span><span class="sxs-lookup"><span data-stu-id="a0a15-166">The following structures contain *ArraySlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="a0a15-167">**D3D12 \_ TEX1D \_ array \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-167">**D3D12\_TEX1D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [<span data-ttu-id="a0a15-168">**D3D12 \_ TEX2D \_ array \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-168">**D3D12\_TEX2D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [<span data-ttu-id="a0a15-169">**D3D12 \_ TEX2DMS \_ array \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-169">**D3D12\_TEX2DMS\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [<span data-ttu-id="a0a15-170">**D3D12 \_ TEX1D \_ matriz \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-170">**D3D12\_TEX1D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [<span data-ttu-id="a0a15-171">**D3D12 \_ TEX2D \_ matriz \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-171">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="a0a15-172">**D3D12 \_ TEX2DMS \_ matriz \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-172">**D3D12\_TEX2DMS\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [<span data-ttu-id="a0a15-173">**D3D12 \_ TEX1D \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-173">**D3D12\_TEX1D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [<span data-ttu-id="a0a15-174">**D3D12 \_ TEX2D \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-174">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="a0a15-175">**D3D12 \_ TEX2DMS \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-175">**D3D12\_TEX2DMS\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [<span data-ttu-id="a0a15-176">**D3D12 \_ TEX1D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-176">**D3D12\_TEX1D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [<span data-ttu-id="a0a15-177">**D3D12 \_ TEX2D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-177">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="a0a15-178">Las siguientes estructuras contienen índices *MipSlice* , pero no *ArraySlice* ni *PlaneSlice* índices.</span><span class="sxs-lookup"><span data-stu-id="a0a15-178">The following structures contain *MipSlice* indexes, but neither *ArraySlice* nor *PlaneSlice* indexes.</span></span>

-   [<span data-ttu-id="a0a15-179">**D3D12 \_ TEX1D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-179">**D3D12\_TEX1D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [<span data-ttu-id="a0a15-180">**D3D12 \_ TEX2D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-180">**D3D12\_TEX2D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [<span data-ttu-id="a0a15-181">**D3D12 \_ TEX1D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-181">**D3D12\_TEX1D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [<span data-ttu-id="a0a15-182">**D3D12 \_ TEX3D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-182">**D3D12\_TEX3D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [<span data-ttu-id="a0a15-183">**D3D12 \_ TEX1D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-183">**D3D12\_TEX1D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [<span data-ttu-id="a0a15-184">**D3D12 \_ TEX3D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="a0a15-184">**D3D12\_TEX3D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

<span data-ttu-id="a0a15-185">Las siguientes estructuras también hacen referencia a Subrecursos:</span><span class="sxs-lookup"><span data-stu-id="a0a15-185">The following structures also reference subresources:</span></span>

-   <span data-ttu-id="a0a15-186">[**D3D12 \_ Descartar \_ región**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : una estructura que se utiliza como preparación para descartar un recurso.</span><span class="sxs-lookup"><span data-stu-id="a0a15-186">[**D3D12\_DISCARD\_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : a structure used in preparation for discarding a resource.</span></span>
-   <span data-ttu-id="a0a15-187">[**D3D12 \_ \_ \_ Superficie de subrecurso colocada**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : agrega un desplazamiento a un recurso a la superficie básica.</span><span class="sxs-lookup"><span data-stu-id="a0a15-187">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : adds an offset into a resource to the basic footprint.</span></span>
-   <span data-ttu-id="a0a15-188">[**D3D12 \_ \_ \_ Barrera de transición de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : describe la transición de Subrecursos entre distintos usos (recursos del sombreador, destino de representación, etc.).</span><span class="sxs-lookup"><span data-stu-id="a0a15-188">[**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : describes the transition of subresources between different usages (shader resource, render target, etc.).</span></span>
-   <span data-ttu-id="a0a15-189">[**D3D12 \_ \_Datos de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : los datos del subrecurso incluyen los datos en sí y el paso de la fila y del segmento.</span><span class="sxs-lookup"><span data-stu-id="a0a15-189">[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : subresource data includes the data itself, and the row and slice pitch.</span></span>
-   <span data-ttu-id="a0a15-190">[**D3D12 \_ \_Superficie de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : una superficie incluye el formato, el ancho, el alto, la profundidad y el tono de fila del subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a0a15-190">[**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : a footprint includes the format, width, height, depth and row-pitch of the subresource.</span></span>
-   <span data-ttu-id="a0a15-191">[**D3D12 \_ \_Información de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contiene el desplazamiento, el paso de fila y el tono de profundidad del subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a0a15-191">[**D3D12\_SUBRESOURCE\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contains the offset, row pitch and depth pitch of the subresource.</span></span>
-   <span data-ttu-id="a0a15-192">[**D3D12 \_ \_Mosaico de Subrecursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : describe un volumen de Subrecursos en mosaico (consulte [los recursos en mosaico del volumen](volume-tiled-resources.md)).</span><span class="sxs-lookup"><span data-stu-id="a0a15-192">[**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : describes a tiled subresource volume (refer to [Volume Tiled Resources](volume-tiled-resources.md)).</span></span>
-   <span data-ttu-id="a0a15-193">[**D3D12 \_ \_ \_ Ubicación de copia de textura**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : describe una parte de una textura con el fin de copiar.</span><span class="sxs-lookup"><span data-stu-id="a0a15-193">[**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : describes a portion of a texture for the purpose of copying.</span></span>
-   <span data-ttu-id="a0a15-194">[**D3D12 \_ Coordenada \_ de \_ recursos en mosaico**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : describe las coordenadas de un recurso en mosaico.</span><span class="sxs-lookup"><span data-stu-id="a0a15-194">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : describes the coordinates of a tiled resource.</span></span>

<span data-ttu-id="a0a15-195">Métodos:</span><span class="sxs-lookup"><span data-stu-id="a0a15-195">Methods:</span></span>

-   <span data-ttu-id="a0a15-196">[**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : obtiene información sobre un recurso, para permitir que se realice una copia.</span><span class="sxs-lookup"><span data-stu-id="a0a15-196">[**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : gets information on a resource, to enable a copy to be made.</span></span>
-   <span data-ttu-id="a0a15-197">[**ID3D12Device:: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : obtiene información sobre cómo un recurso en mosaico se divide en mosaicos.</span><span class="sxs-lookup"><span data-stu-id="a0a15-197">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>
-   <span data-ttu-id="a0a15-198">[**ID3D12GraphicsCommandList:: ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copia un subrecurso de muestreo múltiple en un subrecurso de muestreo no múltiple.</span><span class="sxs-lookup"><span data-stu-id="a0a15-198">[**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copies a multi-sampled subresource into a non-multi-sampled subresource.</span></span>
-   <span data-ttu-id="a0a15-199">[**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : devuelve un puntero a los datos especificados en el recurso y deniega el acceso de la GPU al subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a0a15-199">[**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : returns a pointer to the specified data in the resource, and denies the GPU access to the subresource.</span></span>
-   <span data-ttu-id="a0a15-200">[**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copia datos de un subrecurso o de una región rectangular de un subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a0a15-200">[**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copies data from a subresource, or a rectangular region of a subresource.</span></span>
-   <span data-ttu-id="a0a15-201">[**ID3D12Resource::**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) desasignar: desasigna el intervalo de memoria especificado y invalida el puntero al recurso.</span><span class="sxs-lookup"><span data-stu-id="a0a15-201">[**ID3D12Resource::Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : unmaps the specified range of memory and invalidates the pointer to the resource.</span></span> <span data-ttu-id="a0a15-202">Restablece el acceso de la GPU al subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a0a15-202">Reinstates GPU access to the subresource.</span></span>
-   <span data-ttu-id="a0a15-203">[**ID3D12Resource:: WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copia datos en un subrecurso o en una región rectangular de un subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a0a15-203">[**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copies data to a subresource, or a rectangular region of a subresource.</span></span>

<span data-ttu-id="a0a15-204">Las texturas deben estar en el estado de [**recurso de D3D12 estado \_ \_ \_ común**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) de acceso de CPU a través de [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) y [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) para ser legales, pero no los búferes.</span><span class="sxs-lookup"><span data-stu-id="a0a15-204">Textures must be in the [**D3D12\_RESOURCE\_STATE\_COMMON**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) state for CPU access through [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) and [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) to be legal; but buffers do not.</span></span> <span data-ttu-id="a0a15-205">El acceso de CPU a un recurso se realiza normalmente a través de [**asignación de asignación**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span><span class="sxs-lookup"><span data-stu-id="a0a15-205">CPU access to a resource is typically done through [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)/[**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0a15-206">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0a15-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0a15-207">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="a0a15-207">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 




