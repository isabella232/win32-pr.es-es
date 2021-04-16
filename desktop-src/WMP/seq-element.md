---
title: Seq (elemento)
description: El elemento SEQ contiene elementos que definen una lista de reproducción estática o elementos que definen una lista de reproducción inteligente.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Elemento SEQ Windows Media Player
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649613"
---
# <a name="seq-element"></a><span data-ttu-id="374c3-104">Seq (elemento)</span><span class="sxs-lookup"><span data-stu-id="374c3-104">seq Element</span></span>

<span data-ttu-id="374c3-105">El elemento **Seq** contiene elementos que definen una lista de reproducción estática o elementos que definen una lista de reproducción inteligente.</span><span class="sxs-lookup"><span data-stu-id="374c3-105">The **seq** element contains elements that define a static playlist or elements that define a smart playlist.</span></span>

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a><span data-ttu-id="374c3-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="374c3-106">Attributes</span></span>

<span data-ttu-id="374c3-107">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="374c3-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="374c3-108">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="374c3-108">Parent/Child Elements</span></span>



| <span data-ttu-id="374c3-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="374c3-109">Hierarchy</span></span> | <span data-ttu-id="374c3-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="374c3-110">Elements</span></span>                                                               |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="374c3-111">Parent</span><span class="sxs-lookup"><span data-stu-id="374c3-111">Parent</span></span>    | [<span data-ttu-id="374c3-112">body</span><span class="sxs-lookup"><span data-stu-id="374c3-112">body</span></span>](body-element.md)                                               |
| <span data-ttu-id="374c3-113">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="374c3-113">Child</span></span>     | <span data-ttu-id="374c3-114">[medios](media-element.md), [smartPlaylist](smartplaylist-element.md)</span><span class="sxs-lookup"><span data-stu-id="374c3-114">[media](media-element.md), [smartPlaylist](smartplaylist-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="374c3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="374c3-115">Remarks</span></span>

<span data-ttu-id="374c3-116">Cuando un elemento **Seq** solo contiene elementos **multimedia** que hacen referencia a elementos multimedia específicos, se considera que la lista de reproducción es estática.</span><span class="sxs-lookup"><span data-stu-id="374c3-116">When a **seq** element only contains **media** elements that reference specific media items, the playlist is considered to be static.</span></span> <span data-ttu-id="374c3-117">Cuando un elemento **Seq** contiene un elemento **smartPlaylist** , se considera que es una lista de reproducción "inteligente" dinámica.</span><span class="sxs-lookup"><span data-stu-id="374c3-117">When a **seq** element contains a **smartPlaylist** element, it is considered to be a dynamic "smart" playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="374c3-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="374c3-118">Examples</span></span>


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a><span data-ttu-id="374c3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="374c3-119">Requirements</span></span>



| <span data-ttu-id="374c3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="374c3-120">Requirement</span></span> | <span data-ttu-id="374c3-121">Value</span><span class="sxs-lookup"><span data-stu-id="374c3-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="374c3-122">Versión</span><span class="sxs-lookup"><span data-stu-id="374c3-122">Version</span></span><br/> | <span data-ttu-id="374c3-123">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="374c3-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="374c3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="374c3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="374c3-125">**Elemento BODY**</span><span class="sxs-lookup"><span data-stu-id="374c3-125">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="374c3-126">**Elemento multimedia**</span><span class="sxs-lookup"><span data-stu-id="374c3-126">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="374c3-127">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="374c3-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="374c3-128">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="374c3-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





