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
# <a name="subresources-direct3d-11-graphics"></a><span data-ttu-id="037c5-103">Subrecursos (gráficos de Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="037c5-103">Subresources (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="037c5-104">En este tema se describen los Subrecursos de textura o partes de un recurso.</span><span class="sxs-lookup"><span data-stu-id="037c5-104">This topic describes texture subresources, or portions of a resource.</span></span>

<span data-ttu-id="037c5-105">Direct3D puede hacer referencia a un recurso completo o puede hacer referencia a subconjuntos de un recurso.</span><span class="sxs-lookup"><span data-stu-id="037c5-105">Direct3D can reference an entire resource or it can reference subsets of a resource.</span></span> <span data-ttu-id="037c5-106">El término subresource hace referencia a un subconjunto de un recurso.</span><span class="sxs-lookup"><span data-stu-id="037c5-106">The term subresource refers to a subset of a resource.</span></span>

<span data-ttu-id="037c5-107">Un búfer se define como un subrecurso único.</span><span class="sxs-lookup"><span data-stu-id="037c5-107">A buffer is defined as a single subresource.</span></span> <span data-ttu-id="037c5-108">Las texturas son un poco más complicadas porque existen varios tipos de textura diferentes (1D, 2D, etc.), algunos de los cuales admiten niveles de mipmap o matrices de texturas.</span><span class="sxs-lookup"><span data-stu-id="037c5-108">Textures are a little more complicated because there are several different texture types (1D, 2D, etc.) some of which support mipmap levels and/or texture arrays.</span></span> <span data-ttu-id="037c5-109">A partir del caso más simple, una textura 1D se define como un subrecurso único, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="037c5-109">Beginning with the simplest case, a 1D texture is defined as a single subresource, as shown in the following illustration.</span></span>

![Ilustración de una textura 1D](images/d3d10-1d-texture.png)

<span data-ttu-id="037c5-111">Esto significa que la matriz de textura que componen una textura 1D está contenida en un solo subrecurso.</span><span class="sxs-lookup"><span data-stu-id="037c5-111">This means that the array of texels that make up a 1D texture are contained in a single subresource.</span></span>

<span data-ttu-id="037c5-112">Si expande una textura 1D con tres niveles de mipmap, se puede visualizar como la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="037c5-112">If you expand a 1D texture with three mipmap levels, it can be visualized like the following illustration.</span></span>

![Ilustración de una textura 1D con tres niveles de mipmap](images/d3d10-resource-texture1d.png)

<span data-ttu-id="037c5-114">Piense en esto como una sola textura que se compone de tres Subrecursos.</span><span class="sxs-lookup"><span data-stu-id="037c5-114">Think of this as a single texture that is made up of three subresources.</span></span> <span data-ttu-id="037c5-115">Un subrecurso se puede indizar mediante el nivel de detalle (LOD) para una sola textura.</span><span class="sxs-lookup"><span data-stu-id="037c5-115">A subresource can be indexed using the level-of-detail (LOD) for a single texture.</span></span> <span data-ttu-id="037c5-116">Cuando se usa una matriz de texturas, el acceso a un subrecurso determinado requiere el LOD y la textura determinada.</span><span class="sxs-lookup"><span data-stu-id="037c5-116">When using an array of textures, accessing a particular subresource requires both the LOD and the particular texture.</span></span> <span data-ttu-id="037c5-117">Como alternativa, la API combina estos dos fragmentos de información en un único índice de subrecurso basado en cero, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="037c5-117">Alternately, the API combines these two pieces of information into a single zero-based subresource index, as shown in the following illustration.</span></span>

![Ilustración de un índice de subrecurso basado en cero](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a><span data-ttu-id="037c5-119">Selección de Subrecursos</span><span class="sxs-lookup"><span data-stu-id="037c5-119">Selecting Subresources</span></span>

<span data-ttu-id="037c5-120">Algunas API acceden a un recurso completo (por ejemplo, el método [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) ), otros tienen acceso a una parte de un recurso (por ejemplo, el método [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) o el método [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) ).</span><span class="sxs-lookup"><span data-stu-id="037c5-120">Some APIs access an entire resource (for example the [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) method), others access a portion of a resource (for example the [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) method or the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method).</span></span> <span data-ttu-id="037c5-121">Los métodos que tienen acceso a una parte de un recurso suelen usar una descripción de la vista (como la estructura DSV de la [**\_ \_ matriz \_ D3D11 TEX2D**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) ) para especificar los Subrecursos a los que se va a tener acceso.</span><span class="sxs-lookup"><span data-stu-id="037c5-121">The methods that access a portion of a resource generally use a view description (such as the [**D3D11\_TEX2D\_ARRAY\_DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) structure) to specify the subresources to access.</span></span>

<span data-ttu-id="037c5-122">En las ilustraciones de las secciones siguientes se muestran los términos utilizados por una descripción de la vista al obtener acceso a una matriz de texturas.</span><span class="sxs-lookup"><span data-stu-id="037c5-122">The illustrations in the following sections show the terms used by a view description when accessing an array of textures.</span></span>

### <a name="array-slice"></a><span data-ttu-id="037c5-123">Segmento de matriz</span><span class="sxs-lookup"><span data-stu-id="037c5-123">Array Slice</span></span>

<span data-ttu-id="037c5-124">Dada una matriz de texturas, cada textura con los mapas MIP, un *segmento de matriz* (representado por el rectángulo blanco) incluye una textura y todos sus Subrecursos, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="037c5-124">Given an array of textures, each texture with mipmaps, an *array slice* (represented by the white rectangle) includes one texture and all of its subresources, as shown in the following illustration.</span></span>

![Ilustración de un segmento de matriz](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a><span data-ttu-id="037c5-126">Segmento MIP</span><span class="sxs-lookup"><span data-stu-id="037c5-126">Mip Slice</span></span>

<span data-ttu-id="037c5-127">Un *segmento de MIP* (representado por el rectángulo blanco) incluye un nivel de mipmap para cada textura de una matriz, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="037c5-127">A *mip slice* (represented by the white rectangle) includes one mipmap level for every texture in an array, as shown in the following illustration.</span></span>

![Ilustración de un segmento MIP](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a><span data-ttu-id="037c5-129">Selección de un único subrecurso</span><span class="sxs-lookup"><span data-stu-id="037c5-129">Selecting a Single Subresource</span></span>

<span data-ttu-id="037c5-130">Puede usar estos dos tipos de segmentos para elegir un solo subrecurso, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="037c5-130">You can use these two types of slices to choose a single subresource, as shown in the following illustration.</span></span>

![Ilustración de cómo elegir un subrecurso mediante un segmento de matriz y un segmento de MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a><span data-ttu-id="037c5-132">Seleccionar varios Subrecursos</span><span class="sxs-lookup"><span data-stu-id="037c5-132">Selecting Multiple Subresources</span></span>

<span data-ttu-id="037c5-133">También puede usar estos dos tipos de segmentos con el número de niveles de mipmap y/o el número de texturas para elegir varios Subrecursos, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="037c5-133">Or you can use these two types of slices with the number of mipmap levels and/or number of textures, to choose multiple subresources, as shown in the following illustration.</span></span>

![Ilustración de la elección de varios Subrecursos](images/d3d10-resource-subresources-2.png)

> [!Note]  
> <span data-ttu-id="037c5-135">Una [**vista de destino de representación**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) solo puede utilizar un solo subrecurso o segmento MIP y no puede incluir Subrecursos de más de un segmento de MIP.</span><span class="sxs-lookup"><span data-stu-id="037c5-135">A [**render-target view**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="037c5-136">Es decir, cada textura de una vista de representación-destino debe tener el mismo tamaño.</span><span class="sxs-lookup"><span data-stu-id="037c5-136">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="037c5-137">Una [**vista de recursos de sombreador**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) puede seleccionar cualquier región rectangular de Subrecursos, tal como se muestra en la ilustración.</span><span class="sxs-lookup"><span data-stu-id="037c5-137">A [**shader-resource view**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) can select any rectangular region of subresources, as shown in the figure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="037c5-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="037c5-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="037c5-139">Recursos</span><span class="sxs-lookup"><span data-stu-id="037c5-139">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




