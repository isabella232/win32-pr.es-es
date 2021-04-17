---
title: Elemento title (WPL)
description: El elemento title especifica un título para la lista de reproducción.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- Elemento title (WPL) Windows Media Player
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708922"
---
# <a name="title-element-wpl"></a><span data-ttu-id="276c7-104">Elemento title (WPL)</span><span class="sxs-lookup"><span data-stu-id="276c7-104">title Element (WPL)</span></span>

<span data-ttu-id="276c7-105">El elemento **title** especifica un título para la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="276c7-105">The **title** element specifies a title for the playlist.</span></span>

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a><span data-ttu-id="276c7-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="276c7-106">Attributes</span></span>

<span data-ttu-id="276c7-107">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="276c7-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="276c7-108">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="276c7-108">Parent/Child Elements</span></span>



| <span data-ttu-id="276c7-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="276c7-109">Hierarchy</span></span> | <span data-ttu-id="276c7-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="276c7-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="276c7-111">Parent</span><span class="sxs-lookup"><span data-stu-id="276c7-111">Parent</span></span>    | [<span data-ttu-id="276c7-112">head</span><span class="sxs-lookup"><span data-stu-id="276c7-112">head</span></span>](head-element.md) |
| <span data-ttu-id="276c7-113">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="276c7-113">Child</span></span>     | <span data-ttu-id="276c7-114">None</span><span class="sxs-lookup"><span data-stu-id="276c7-114">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="276c7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="276c7-115">Remarks</span></span>

<span data-ttu-id="276c7-116">Al elegir un título para una lista de reproducción de Windows Media (WPL), tenga en cuenta que el contenido de la lista de reproducción puede ser dinámico.</span><span class="sxs-lookup"><span data-stu-id="276c7-116">When choosing a title for a Windows Media Playlist (WPL), consider that the content of the playlist can be dynamic.</span></span> <span data-ttu-id="276c7-117">Un buen enfoque consiste en basar el título en la lógica de los elementos de **argumento** , ya que es lo que define el contenido de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="276c7-117">A good approach is to base the title on the logic in the **argument** elements because this is what defines the content of the playlist.</span></span> <span data-ttu-id="276c7-118">Ejemplos de esto son "mis canciones de rock favoritas de 1966" o "las canciones de baile que no he reproducido recientemente".</span><span class="sxs-lookup"><span data-stu-id="276c7-118">Examples of this are "My Favorite Rock Songs from 1966" or "Dance Songs That I Haven't Played Recently".</span></span>

## <a name="examples"></a><span data-ttu-id="276c7-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="276c7-119">Examples</span></span>


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a><span data-ttu-id="276c7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="276c7-120">Requirements</span></span>



| <span data-ttu-id="276c7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="276c7-121">Requirement</span></span> | <span data-ttu-id="276c7-122">Value</span><span class="sxs-lookup"><span data-stu-id="276c7-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="276c7-123">Versión</span><span class="sxs-lookup"><span data-stu-id="276c7-123">Version</span></span><br/> | <span data-ttu-id="276c7-124">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="276c7-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="276c7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="276c7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276c7-126">**Elemento argument**</span><span class="sxs-lookup"><span data-stu-id="276c7-126">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="276c7-127">**Elemento de encabezado**</span><span class="sxs-lookup"><span data-stu-id="276c7-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="276c7-128">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="276c7-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





