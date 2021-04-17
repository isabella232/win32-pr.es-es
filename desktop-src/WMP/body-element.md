---
title: Elemento BODY
description: El elemento BODY contiene los elementos que definen el contenido de una lista de reproducción.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Elemento de cuerpo Media Player de Windows
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700005"
---
# <a name="body-element"></a><span data-ttu-id="1d7ce-104">Elemento BODY</span><span class="sxs-lookup"><span data-stu-id="1d7ce-104">body Element</span></span>

<span data-ttu-id="1d7ce-105">El elemento **Body** contiene los elementos que definen el contenido de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="1d7ce-105">The **body** element contains the elements that define the contents of a playlist.</span></span>

``` syntax
<body>
</body>
```

## <a name="attributes"></a><span data-ttu-id="1d7ce-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="1d7ce-106">Attributes</span></span>

<span data-ttu-id="1d7ce-107">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="1d7ce-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="1d7ce-108">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="1d7ce-108">Parent/Child Elements</span></span>



| <span data-ttu-id="1d7ce-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="1d7ce-109">Hierarchy</span></span> | <span data-ttu-id="1d7ce-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="1d7ce-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="1d7ce-111">Parent</span><span class="sxs-lookup"><span data-stu-id="1d7ce-111">Parent</span></span>    | [<span data-ttu-id="1d7ce-112">gestual</span><span class="sxs-lookup"><span data-stu-id="1d7ce-112">smil</span></span>](smil-element.md) |
| <span data-ttu-id="1d7ce-113">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="1d7ce-113">Child</span></span>     | [<span data-ttu-id="1d7ce-114">Próx</span><span class="sxs-lookup"><span data-stu-id="1d7ce-114">seq</span></span>](seq-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="1d7ce-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d7ce-115">Remarks</span></span>

<span data-ttu-id="1d7ce-116">El contenido de una lista de reproducción se organiza dentro de un elemento **Seq** incluido en el elemento **Body** .</span><span class="sxs-lookup"><span data-stu-id="1d7ce-116">The contents of a playlist are organized within a **seq** element that is contained within the **body** element.</span></span> <span data-ttu-id="1d7ce-117">Normalmente, hay un elemento **Seq** que define un conjunto estático de elementos multimedia y contiene elementos **multimedia** , o bien uno que define un conjunto dinámico de elementos multimedia y contiene un elemento **smartPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="1d7ce-117">Typically there is either one **seq** element that defines a static set of media items and contains **media** elements, or there is one that defines a dynamic set of media items and contains a **smartPlaylist** element.</span></span>

## <a name="examples"></a><span data-ttu-id="1d7ce-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1d7ce-118">Examples</span></span>


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a><span data-ttu-id="1d7ce-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d7ce-119">Requirements</span></span>



| <span data-ttu-id="1d7ce-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d7ce-120">Requirement</span></span> | <span data-ttu-id="1d7ce-121">Value</span><span class="sxs-lookup"><span data-stu-id="1d7ce-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="1d7ce-122">Versión</span><span class="sxs-lookup"><span data-stu-id="1d7ce-122">Version</span></span><br/> | <span data-ttu-id="1d7ce-123">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="1d7ce-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d7ce-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d7ce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d7ce-125">**Elemento multimedia**</span><span class="sxs-lookup"><span data-stu-id="1d7ce-125">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="1d7ce-126">**Seq (elemento)**</span><span class="sxs-lookup"><span data-stu-id="1d7ce-126">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="1d7ce-127">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="1d7ce-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="1d7ce-128">**Elemento SMIL**</span><span class="sxs-lookup"><span data-stu-id="1d7ce-128">**smil Element**</span></span>](smil-element.md)
</dt> <dt>

[<span data-ttu-id="1d7ce-129">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1d7ce-129">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





