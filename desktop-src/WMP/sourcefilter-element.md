---
title: Elemento sourceFilter
description: El elemento sourceFilter contiene elementos que seleccionan elementos de una biblioteca.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Elemento sourceFilter Media Player Windows
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653868"
---
# <a name="sourcefilter-element"></a><span data-ttu-id="090a8-104">Elemento sourceFilter</span><span class="sxs-lookup"><span data-stu-id="090a8-104">sourceFilter Element</span></span>

<span data-ttu-id="090a8-105">El elemento **sourceFilter** contiene elementos que seleccionan elementos de una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="090a8-105">The **sourceFilter** element contains elements that select items from a library.</span></span>

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a><span data-ttu-id="090a8-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="090a8-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="090a8-107"><span id="type"></span><span id="TYPE"></span>**automáticamente**</span><span class="sxs-lookup"><span data-stu-id="090a8-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="090a8-108">Tipo de objeto de filtro.</span><span class="sxs-lookup"><span data-stu-id="090a8-108">The type of filter object.</span></span> <span data-ttu-id="090a8-109">No hay valores predefinidos para este atributo.</span><span class="sxs-lookup"><span data-stu-id="090a8-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="090a8-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="090a8-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="090a8-111">GUID que identifica de forma única el objeto de filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="090a8-111">The GUID that uniquely identifies the source filter object.</span></span> <span data-ttu-id="090a8-112">Los métodos del objeto de filtro de origen se invocan para interpretar los elementos de **fragmento** contenidos en el elemento **sourceFilter** .</span><span class="sxs-lookup"><span data-stu-id="090a8-112">The source filter object's methods are invoked to interpret the **fragment** elements contained in the **sourceFilter** element.</span></span>



| <span data-ttu-id="090a8-113">Value</span><span class="sxs-lookup"><span data-stu-id="090a8-113">Value</span></span>                                  | <span data-ttu-id="090a8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="090a8-114">Description</span></span>                                              |
|----------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="090a8-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span><span class="sxs-lookup"><span data-stu-id="090a8-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span></span> | <span data-ttu-id="090a8-116">El GUID para el filtro de origen "música en mi biblioteca".</span><span class="sxs-lookup"><span data-stu-id="090a8-116">The GUID for the "Music in my library" source filter.</span></span>    |
| <span data-ttu-id="090a8-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span><span class="sxs-lookup"><span data-stu-id="090a8-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span></span> | <span data-ttu-id="090a8-118">El GUID para el filtro de origen "vídeo en mi biblioteca".</span><span class="sxs-lookup"><span data-stu-id="090a8-118">The GUID for the "Video in my library" source filter.</span></span>    |
| <span data-ttu-id="090a8-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span><span class="sxs-lookup"><span data-stu-id="090a8-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span></span> | <span data-ttu-id="090a8-120">El GUID para el filtro de origen "imágenes en mi biblioteca".</span><span class="sxs-lookup"><span data-stu-id="090a8-120">The GUID for the "Pictures in my library" source filter.</span></span> |
| <span data-ttu-id="090a8-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span><span class="sxs-lookup"><span data-stu-id="090a8-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span></span> | <span data-ttu-id="090a8-122">El GUID para el filtro de origen "programas de TV en mi biblioteca".</span><span class="sxs-lookup"><span data-stu-id="090a8-122">The GUID for the "TV shows in my library" source filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="090a8-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nombre** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="090a8-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="090a8-124">Nombre del objeto de filtro.</span><span class="sxs-lookup"><span data-stu-id="090a8-124">The name of the filter object.</span></span>



| <span data-ttu-id="090a8-125">Value</span><span class="sxs-lookup"><span data-stu-id="090a8-125">Value</span></span>                  | <span data-ttu-id="090a8-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="090a8-126">Description</span></span>                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="090a8-127">Música en mi biblioteca</span><span class="sxs-lookup"><span data-stu-id="090a8-127">Music in my library</span></span>    | <span data-ttu-id="090a8-128">Objeto de filtro que selecciona los elementos especificados del conjunto de elementos de música de la biblioteca del usuario.</span><span class="sxs-lookup"><span data-stu-id="090a8-128">A filter object that selects specified items from the set of music items in the user's library.</span></span> |
| <span data-ttu-id="090a8-129">Vídeo en mi biblioteca</span><span class="sxs-lookup"><span data-stu-id="090a8-129">Video in my library</span></span>    | <span data-ttu-id="090a8-130">Un objeto de filtro que selecciona los elementos especificados del conjunto de elementos de vídeo en la biblioteca del usuario.</span><span class="sxs-lookup"><span data-stu-id="090a8-130">A filter object that selects specified items from the set of video items in the user's library.</span></span> |
| <span data-ttu-id="090a8-131">Imágenes en mi biblioteca</span><span class="sxs-lookup"><span data-stu-id="090a8-131">Pictures in my library</span></span> | <span data-ttu-id="090a8-132">Un objeto de filtro que selecciona los elementos especificados del conjunto de elementos de fotografía en la biblioteca del usuario.</span><span class="sxs-lookup"><span data-stu-id="090a8-132">A filter object that selects specified items from the set of photo items in the user's library.</span></span> |
| <span data-ttu-id="090a8-133">Programas de TV en mi biblioteca</span><span class="sxs-lookup"><span data-stu-id="090a8-133">TV shows in my library</span></span> | <span data-ttu-id="090a8-134">Un objeto de filtro que selecciona los elementos especificados del conjunto de elementos de TV en la biblioteca del usuario.</span><span class="sxs-lookup"><span data-stu-id="090a8-134">A filter object that selects specified items from the set of TV items in the user's library.</span></span>    |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="090a8-135">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="090a8-135">Parent/Child Elements</span></span>



| <span data-ttu-id="090a8-136">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="090a8-136">Hierarchy</span></span> | <span data-ttu-id="090a8-137">Elementos</span><span class="sxs-lookup"><span data-stu-id="090a8-137">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="090a8-138">Parent</span><span class="sxs-lookup"><span data-stu-id="090a8-138">Parent</span></span>    | [<span data-ttu-id="090a8-139">querySet</span><span class="sxs-lookup"><span data-stu-id="090a8-139">querySet</span></span>](queryset-element.md) |
| <span data-ttu-id="090a8-140">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="090a8-140">Child</span></span>     | [<span data-ttu-id="090a8-141">Fragment</span><span class="sxs-lookup"><span data-stu-id="090a8-141">fragment</span></span>](fragment-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="090a8-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="090a8-142">Remarks</span></span>

<span data-ttu-id="090a8-143">El elemento **sourceFilter** selecciona los elementos de la biblioteca sin tener en cuenta el tamaño del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="090a8-143">The **sourceFilter** element selects items from the library without regard for the size of the result set.</span></span> <span data-ttu-id="090a8-144">Por otro lado, el elemento **Filter** limita el tamaño del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="090a8-144">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="090a8-145">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="090a8-145">Examples</span></span>


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
    name = "Music in my library">
        <fragment name = "Genre">
            <argument name = "condition">Is</argument>
            <argument name = "value">Rock</argument>
        </fragment>
        <fragment name = "Album Artist">
            <argument name = "condition">Is Not</argument>
            <argument name = "value">Brenda Diaz</argument>
        </fragment>
</sourceFilter>
```



## <a name="requirements"></a><span data-ttu-id="090a8-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="090a8-146">Requirements</span></span>



| <span data-ttu-id="090a8-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="090a8-147">Requirement</span></span> | <span data-ttu-id="090a8-148">Value</span><span class="sxs-lookup"><span data-stu-id="090a8-148">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="090a8-149">Versión</span><span class="sxs-lookup"><span data-stu-id="090a8-149">Version</span></span><br/> | <span data-ttu-id="090a8-150">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="090a8-150">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="090a8-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="090a8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090a8-152">**Elemento Filter**</span><span class="sxs-lookup"><span data-stu-id="090a8-152">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="090a8-153">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="090a8-153">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="090a8-154">**Elemento querySet**</span><span class="sxs-lookup"><span data-stu-id="090a8-154">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="090a8-155">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="090a8-155">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





