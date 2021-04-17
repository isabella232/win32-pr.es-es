---
title: Elemento de encabezado
description: El elemento de encabezado contiene metadatos que se aplican a toda la lista de reproducción.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Elemento de encabezado de Windows Media Player
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699760"
---
# <a name="head-element"></a><span data-ttu-id="3edac-104">Elemento de encabezado</span><span class="sxs-lookup"><span data-stu-id="3edac-104">head Element</span></span>

<span data-ttu-id="3edac-105">El elemento de **encabezado** contiene metadatos que se aplican a toda la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="3edac-105">The **head** element contains metadata that applies to the entire playlist.</span></span>

``` syntax
<head>
</head>
```

## <a name="attributes"></a><span data-ttu-id="3edac-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="3edac-106">Attributes</span></span>

<span data-ttu-id="3edac-107">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="3edac-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="3edac-108">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="3edac-108">Parent/Child Elements</span></span>



| <span data-ttu-id="3edac-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="3edac-109">Hierarchy</span></span> | <span data-ttu-id="3edac-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="3edac-110">Elements</span></span>                                                  |
|-----------|-----------------------------------------------------------|
| <span data-ttu-id="3edac-111">Parent</span><span class="sxs-lookup"><span data-stu-id="3edac-111">Parent</span></span>    | [<span data-ttu-id="3edac-112">gestual</span><span class="sxs-lookup"><span data-stu-id="3edac-112">smil</span></span>](smil-element.md)                                  |
| <span data-ttu-id="3edac-113">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="3edac-113">Child</span></span>     | <span data-ttu-id="3edac-114">[título](title-element--wpl.md), [meta](meta-element.md)</span><span class="sxs-lookup"><span data-stu-id="3edac-114">[title](title-element--wpl.md), [meta](meta-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3edac-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3edac-115">Remarks</span></span>

<span data-ttu-id="3edac-116">Normalmente, el elemento de **encabezado** contiene un elemento de **título** y uno o varios elementos **meta** que definen las características globales de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="3edac-116">Typically the **head** element contains a **title** element and one or more **meta** elements that define global characteristics of the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="3edac-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3edac-117">Examples</span></span>


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="3edac-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3edac-118">Requirements</span></span>



| <span data-ttu-id="3edac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3edac-119">Requirement</span></span> | <span data-ttu-id="3edac-120">Value</span><span class="sxs-lookup"><span data-stu-id="3edac-120">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="3edac-121">Versión</span><span class="sxs-lookup"><span data-stu-id="3edac-121">Version</span></span><br/> | <span data-ttu-id="3edac-122">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="3edac-122">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3edac-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3edac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3edac-124">**Elemento meta**</span><span class="sxs-lookup"><span data-stu-id="3edac-124">**meta Element**</span></span>](meta-element.md)
</dt> <dt>

[<span data-ttu-id="3edac-125">**Elemento title (WPL)**</span><span class="sxs-lookup"><span data-stu-id="3edac-125">**title Element (WPL)**</span></span>](title-element--wpl.md)
</dt> <dt>

[<span data-ttu-id="3edac-126">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3edac-126">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





