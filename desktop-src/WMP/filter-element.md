---
title: Elemento Filter
description: El elemento Filter contiene elementos que limitan el tamaño de una lista de reproducción, la duración de una lista de reproducción o el número de elementos multimedia de una lista de reproducción.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- filtro de ventanas de elementos Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699534"
---
# <a name="filter-element"></a><span data-ttu-id="d3712-104">Elemento Filter</span><span class="sxs-lookup"><span data-stu-id="d3712-104">filter Element</span></span>

<span data-ttu-id="d3712-105">El elemento **Filter** contiene elementos que limitan el tamaño de una lista de reproducción, la duración de una lista de reproducción o el número de elementos multimedia de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d3712-105">The **filter** element contains elements that limit the size of a playlist, duration of a playlist, or number of media items in a playlist.</span></span>

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a><span data-ttu-id="d3712-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="d3712-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="d3712-107"><span id="type"></span><span id="TYPE"></span>**automáticamente**</span><span class="sxs-lookup"><span data-stu-id="d3712-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="d3712-108">Tipo de objeto de filtro.</span><span class="sxs-lookup"><span data-stu-id="d3712-108">The type of filter object.</span></span> <span data-ttu-id="d3712-109">No hay valores predefinidos para este atributo.</span><span class="sxs-lookup"><span data-stu-id="d3712-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="d3712-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="d3712-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="d3712-111">GUID que identifica de forma única un objeto de filtro.</span><span class="sxs-lookup"><span data-stu-id="d3712-111">The GUID that uniquely identifies a filter object.</span></span> <span data-ttu-id="d3712-112">Los métodos del objeto Filter se invocan para interpretar los elementos **Fragment** contenidos en el elemento **Filter** .</span><span class="sxs-lookup"><span data-stu-id="d3712-112">The filter object's methods are invoked to interpret the **fragment** elements contained in the **filter** element.</span></span>



| <span data-ttu-id="d3712-113">Value</span><span class="sxs-lookup"><span data-stu-id="d3712-113">Value</span></span>                                  | <span data-ttu-id="d3712-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3712-114">Description</span></span>                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3712-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span><span class="sxs-lookup"><span data-stu-id="d3712-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span></span> | <span data-ttu-id="d3712-116">El identificador del filtro "filtro de lista de reproducción automática de Microsoft--limita las listas de reproducción automáticas por recuento, tamaño o duración".</span><span class="sxs-lookup"><span data-stu-id="d3712-116">The id for the "Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration" filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d3712-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nombre** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="d3712-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="d3712-118">Nombre del objeto de filtro.</span><span class="sxs-lookup"><span data-stu-id="d3712-118">The name of the filter object.</span></span>



| <span data-ttu-id="d3712-119">Value</span><span class="sxs-lookup"><span data-stu-id="d3712-119">Value</span></span>                                                                              | <span data-ttu-id="d3712-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3712-120">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="d3712-121">Filtro de lista de reproducción automática de Microsoft: limita las listas de reproducción automáticas por número, tamaño o duración</span><span class="sxs-lookup"><span data-stu-id="d3712-121">Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration</span></span> | <span data-ttu-id="d3712-122">Limita las listas de reproducción automáticas por número, tamaño o duración.</span><span class="sxs-lookup"><span data-stu-id="d3712-122">Limits auto playlists by count, size, or duration.</span></span> |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="d3712-123">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="d3712-123">Parent/Child Elements</span></span>



| <span data-ttu-id="d3712-124">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="d3712-124">Hierarchy</span></span> | <span data-ttu-id="d3712-125">Elementos</span><span class="sxs-lookup"><span data-stu-id="d3712-125">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="d3712-126">Parent</span><span class="sxs-lookup"><span data-stu-id="d3712-126">Parent</span></span>    | [<span data-ttu-id="d3712-127">smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="d3712-127">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="d3712-128">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="d3712-128">Child</span></span>     | [<span data-ttu-id="d3712-129">Fragment</span><span class="sxs-lookup"><span data-stu-id="d3712-129">fragment</span></span>](fragment-element.md)           |



 

## <a name="remarks"></a><span data-ttu-id="d3712-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3712-130">Remarks</span></span>

<span data-ttu-id="d3712-131">El elemento **Filter** no agrega elementos multimedia a una lista de reproducción; simplemente quita o filtra el contenido seleccionado por el elemento **sourceFilter** .</span><span class="sxs-lookup"><span data-stu-id="d3712-131">The **filter** element does not add any media elements to a playlist; it simply removes or filters out content that was selected by the **sourceFilter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="d3712-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d3712-132">Examples</span></span>


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a><span data-ttu-id="d3712-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3712-133">Requirements</span></span>



| <span data-ttu-id="d3712-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3712-134">Requirement</span></span> | <span data-ttu-id="d3712-135">Value</span><span class="sxs-lookup"><span data-stu-id="d3712-135">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="d3712-136">Versión</span><span class="sxs-lookup"><span data-stu-id="d3712-136">Version</span></span><br/> | <span data-ttu-id="d3712-137">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="d3712-137">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3712-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3712-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3712-139">**Elemento argument**</span><span class="sxs-lookup"><span data-stu-id="d3712-139">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="d3712-140">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="d3712-140">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="d3712-141">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="d3712-141">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="d3712-142">**Elemento sourceFilter**</span><span class="sxs-lookup"><span data-stu-id="d3712-142">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="d3712-143">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d3712-143">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





