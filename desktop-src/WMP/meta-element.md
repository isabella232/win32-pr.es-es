---
title: Elemento meta
description: El elemento meta especifica metadatos que se aplican a toda la lista de reproducción.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Media Player del elemento meta de Windows
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653544"
---
# <a name="meta-element"></a><span data-ttu-id="26d84-104">Elemento meta</span><span class="sxs-lookup"><span data-stu-id="26d84-104">meta Element</span></span>

<span data-ttu-id="26d84-105">El elemento **meta** especifica metadatos que se aplican a toda la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="26d84-105">The **meta** element specifies metadata that applies to the entire playlist.</span></span>

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a><span data-ttu-id="26d84-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="26d84-106">Attributes</span></span>



| <span data-ttu-id="26d84-107">Término</span><span class="sxs-lookup"><span data-stu-id="26d84-107">Term</span></span>                                                                       | <span data-ttu-id="26d84-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="26d84-108">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26d84-109"><span id="name"></span><span id="NAME"></span>**Name**</span><span class="sxs-lookup"><span data-stu-id="26d84-109"><span id="name"></span><span id="NAME"></span>**name**</span></span><br/>          | <span data-ttu-id="26d84-110">Nombre de un elemento de metadatos.</span><span class="sxs-lookup"><span data-stu-id="26d84-110">The name of an item of metadata.</span></span><br/>                                                                                       |
| <span data-ttu-id="26d84-111"><span id="content"></span><span id="CONTENT"></span>**Content**</span><span class="sxs-lookup"><span data-stu-id="26d84-111"><span id="content"></span><span id="CONTENT"></span>**content**</span></span><br/> | <span data-ttu-id="26d84-112">Valor de un elemento de metadatos.</span><span class="sxs-lookup"><span data-stu-id="26d84-112">The value of an item of metadata.</span></span> <span data-ttu-id="26d84-113">Por ejemplo, si el atributo de nombre es "género", el atributo de contenido podría ser "Rock".</span><span class="sxs-lookup"><span data-stu-id="26d84-113">For example, if the name attribute is "Genre" the content attribute could be "Rock".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="26d84-114">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="26d84-114">Parent/Child Elements</span></span>



| <span data-ttu-id="26d84-115">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="26d84-115">Hierarchy</span></span> | <span data-ttu-id="26d84-116">Elementos</span><span class="sxs-lookup"><span data-stu-id="26d84-116">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="26d84-117">Parent</span><span class="sxs-lookup"><span data-stu-id="26d84-117">Parent</span></span>    | [<span data-ttu-id="26d84-118">head</span><span class="sxs-lookup"><span data-stu-id="26d84-118">head</span></span>](head-element.md) |
| <span data-ttu-id="26d84-119">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="26d84-119">Child</span></span>     | <span data-ttu-id="26d84-120">None</span><span class="sxs-lookup"><span data-stu-id="26d84-120">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="26d84-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26d84-121">Remarks</span></span>

<span data-ttu-id="26d84-122">El creador de una lista de reproducción de Windows Media puede establecer el atributo de nombre de un elemento meta en cualquier cadena.</span><span class="sxs-lookup"><span data-stu-id="26d84-122">The creator of a Windows Media Playlist can set the name attribute of a meta element to any string.</span></span> <span data-ttu-id="26d84-123">La lista siguiente muestra algunos atributos de nombre típicos que se encuentran en las listas de reproducción de Windows Media creadas por Windows Media Player y otros componentes de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="26d84-123">The following list shows some typical name attributes that are found in Windows Media Playlists created by Windows Media Player and other Microsoft components.</span></span>

-   <span data-ttu-id="26d84-124">Autor</span><span class="sxs-lookup"><span data-stu-id="26d84-124">Author</span></span>
-   <span data-ttu-id="26d84-125">Category</span><span class="sxs-lookup"><span data-stu-id="26d84-125">Category</span></span>
-   <span data-ttu-id="26d84-126">Género</span><span class="sxs-lookup"><span data-stu-id="26d84-126">Genre</span></span>
-   <span data-ttu-id="26d84-127">UserName</span><span class="sxs-lookup"><span data-stu-id="26d84-127">UserName</span></span>
-   <span data-ttu-id="26d84-128">UserRating</span><span class="sxs-lookup"><span data-stu-id="26d84-128">UserRating</span></span>
-   <span data-ttu-id="26d84-129">Generator</span><span class="sxs-lookup"><span data-stu-id="26d84-129">Generator</span></span>

## <a name="examples"></a><span data-ttu-id="26d84-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="26d84-130">Examples</span></span>


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="26d84-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26d84-131">Requirements</span></span>



| <span data-ttu-id="26d84-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d84-132">Requirement</span></span> | <span data-ttu-id="26d84-133">Value</span><span class="sxs-lookup"><span data-stu-id="26d84-133">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="26d84-134">Versión</span><span class="sxs-lookup"><span data-stu-id="26d84-134">Version</span></span><br/> | <span data-ttu-id="26d84-135">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="26d84-135">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26d84-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="26d84-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d84-137">**Elemento de encabezado**</span><span class="sxs-lookup"><span data-stu-id="26d84-137">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="26d84-138">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="26d84-138">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





