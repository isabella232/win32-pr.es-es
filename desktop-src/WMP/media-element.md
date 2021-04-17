---
title: Elemento multimedia
description: El elemento multimedia especifica uno de los elementos multimedia de una lista de reproducción.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Elemento multimedia Windows Media Player
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653301"
---
# <a name="media-element"></a><span data-ttu-id="f72a2-104">Elemento multimedia</span><span class="sxs-lookup"><span data-stu-id="f72a2-104">media Element</span></span>

<span data-ttu-id="f72a2-105">El elemento **multimedia** especifica uno de los elementos multimedia de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="f72a2-105">The **media** element specifies one of the media items in a playlist.</span></span>

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a><span data-ttu-id="f72a2-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="f72a2-106">Attributes</span></span>



| <span data-ttu-id="f72a2-107">Término</span><span class="sxs-lookup"><span data-stu-id="f72a2-107">Term</span></span>                                                                                                                       | <span data-ttu-id="f72a2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f72a2-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f72a2-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="f72a2-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (required)</span></span> <br/> | <span data-ttu-id="f72a2-110">Dirección URL de un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="f72a2-110">The URL of a media item.</span></span><br/>                                                              |
| <span data-ttu-id="f72a2-111"><span id="cid"></span><span id="CID"></span>**Cid**</span><span class="sxs-lookup"><span data-stu-id="f72a2-111"><span id="cid"></span><span id="CID"></span>**cid**</span></span><br/>                                                             | <span data-ttu-id="f72a2-112">IDENTIFICADOR de contenido que es único para este elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="f72a2-112">The content ID that is unique to this media item.</span></span><br/>                                     |
| <span data-ttu-id="f72a2-113"><span id="tid"></span><span id="TID"></span>**TID**</span><span class="sxs-lookup"><span data-stu-id="f72a2-113"><span id="tid"></span><span id="TID"></span>**tid**</span></span><br/>                                                             | <span data-ttu-id="f72a2-114">El identificador de seguimiento que se puede usar para realizar el seguimiento del objeto del sistema de archivos para este elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="f72a2-114">The tracking ID that can be used to track the File System Object for this media item.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="f72a2-115">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="f72a2-115">Parent/Child Elements</span></span>



| <span data-ttu-id="f72a2-116">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="f72a2-116">Hierarchy</span></span> | <span data-ttu-id="f72a2-117">Elementos</span><span class="sxs-lookup"><span data-stu-id="f72a2-117">Elements</span></span>               |
|-----------|------------------------|
| <span data-ttu-id="f72a2-118">Parent</span><span class="sxs-lookup"><span data-stu-id="f72a2-118">Parent</span></span>    | [<span data-ttu-id="f72a2-119">Próx</span><span class="sxs-lookup"><span data-stu-id="f72a2-119">seq</span></span>](seq-element.md) |
| <span data-ttu-id="f72a2-120">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="f72a2-120">Child</span></span>     | <span data-ttu-id="f72a2-121">None</span><span class="sxs-lookup"><span data-stu-id="f72a2-121">None</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="f72a2-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f72a2-122">Remarks</span></span>

<span data-ttu-id="f72a2-123">El atributo **CID** (el ID. de contenido) lo rellena la Media Player de Windows como una manera de identificar de forma única un elemento de contenido multimedia aunque se hayan cambiado sus atributos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="f72a2-123">The **cid** attribute (the content ID) is populated by the Windows Media Player as a way to uniquely identify a piece of media content even if its metadata attributes have been changed.</span></span> <span data-ttu-id="f72a2-124">Esto permite el uso compartido de listas de reproducción en todos los equipos, ya que el contenido se puede identificar en otro equipo, y la ruta de acceso a ella puede ser "reparada automáticamente" por la lista de reproducción de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f72a2-124">This allows the sharing of playlists across computers, because the content can be identified on another computer, and the path to it can be "auto-repaired" by the Windows Media Playlist.</span></span> <span data-ttu-id="f72a2-125">El atributo **TID** (el ID. de seguimiento) usa el sistema de archivos de Windows para reparar automáticamente la ruta de acceso al medio si se cambia el nombre o la ubicación del archivo.</span><span class="sxs-lookup"><span data-stu-id="f72a2-125">The **tid** attribute (the tracking ID) uses the Windows file system to auto-repair the path to the media if the name or location of the file is changed.</span></span>

## <a name="examples"></a><span data-ttu-id="f72a2-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f72a2-126">Examples</span></span>


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a><span data-ttu-id="f72a2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f72a2-127">Requirements</span></span>



| <span data-ttu-id="f72a2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f72a2-128">Requirement</span></span> | <span data-ttu-id="f72a2-129">Value</span><span class="sxs-lookup"><span data-stu-id="f72a2-129">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="f72a2-130">Versión</span><span class="sxs-lookup"><span data-stu-id="f72a2-130">Version</span></span><br/> | <span data-ttu-id="f72a2-131">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="f72a2-131">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f72a2-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f72a2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72a2-133">**Seq (elemento)**</span><span class="sxs-lookup"><span data-stu-id="f72a2-133">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="f72a2-134">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f72a2-134">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





