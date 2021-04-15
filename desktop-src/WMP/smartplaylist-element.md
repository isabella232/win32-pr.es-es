---
title: Elemento smartPlaylist
description: El elemento smartPlaylist contiene la parte definida dinámicamente de una lista de reproducción.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- Elemento smartPlaylist Media Player Windows
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 511294af2de4343cb7f63db4312d530aadf57da6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709124"
---
# <a name="smartplaylist-element"></a><span data-ttu-id="0237c-104">Elemento smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="0237c-104">smartPlaylist Element</span></span>

<span data-ttu-id="0237c-105">El elemento **smartPlaylist** contiene la parte definida dinámicamente de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="0237c-105">The **smartPlaylist** element contains the dynamically defined portion of a playlist.</span></span>

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a><span data-ttu-id="0237c-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="0237c-106">Attributes</span></span>



| <span data-ttu-id="0237c-107">Término</span><span class="sxs-lookup"><span data-stu-id="0237c-107">Term</span></span>                                                                                                                                   | <span data-ttu-id="0237c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0237c-108">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0237c-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**versión** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="0237c-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**version** (required)</span></span> <br/> | <span data-ttu-id="0237c-110">Número decimal que representa el número de versión del esquema de lista de reproducción inteligente.</span><span class="sxs-lookup"><span data-stu-id="0237c-110">The decimal number representing the version number of the smart playlist schema.</span></span> <span data-ttu-id="0237c-111">Establezca en 1.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="0237c-111">Set to 1.0.0.0.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="0237c-112">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="0237c-112">Parent/Child Elements</span></span>



| <span data-ttu-id="0237c-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="0237c-113">Hierarchy</span></span> | <span data-ttu-id="0237c-114">Elementos</span><span class="sxs-lookup"><span data-stu-id="0237c-114">Elements</span></span>                                                       |
|-----------|----------------------------------------------------------------|
| <span data-ttu-id="0237c-115">Parent</span><span class="sxs-lookup"><span data-stu-id="0237c-115">Parent</span></span>    | [<span data-ttu-id="0237c-116">Próx</span><span class="sxs-lookup"><span data-stu-id="0237c-116">seq</span></span>](seq-element.md)                                         |
| <span data-ttu-id="0237c-117">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="0237c-117">Child</span></span>     | <span data-ttu-id="0237c-118">[querySet](queryset-element.md), [filtro](filter-element.md)</span><span class="sxs-lookup"><span data-stu-id="0237c-118">[querySet](queryset-element.md), [filter](filter-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0237c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0237c-119">Remarks</span></span>

<span data-ttu-id="0237c-120">Un elemento **smartPlaylist** normalmente contiene un elemento **querySet** y también puede contener un elemento **Filter** .</span><span class="sxs-lookup"><span data-stu-id="0237c-120">A **smartPlaylist** element typically contains a **querySet** element and can also contain a **filter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="0237c-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0237c-121">Examples</span></span>


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
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
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
```



## <a name="requirements"></a><span data-ttu-id="0237c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0237c-122">Requirements</span></span>



| <span data-ttu-id="0237c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0237c-123">Requirement</span></span> | <span data-ttu-id="0237c-124">Value</span><span class="sxs-lookup"><span data-stu-id="0237c-124">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="0237c-125">Versión</span><span class="sxs-lookup"><span data-stu-id="0237c-125">Version</span></span><br/> | <span data-ttu-id="0237c-126">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="0237c-126">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0237c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0237c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0237c-128">**Elemento argument**</span><span class="sxs-lookup"><span data-stu-id="0237c-128">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="0237c-129">**Elemento Filter**</span><span class="sxs-lookup"><span data-stu-id="0237c-129">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="0237c-130">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="0237c-130">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="0237c-131">**Elemento querySet**</span><span class="sxs-lookup"><span data-stu-id="0237c-131">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="0237c-132">**Seq (elemento)**</span><span class="sxs-lookup"><span data-stu-id="0237c-132">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="0237c-133">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0237c-133">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





