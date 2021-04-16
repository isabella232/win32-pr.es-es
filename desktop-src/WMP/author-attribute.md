---
title: Atributo Author
description: El atributo Author es el nombre de un intérprete o actor multimedia asociado con el contenido.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Media Player de atributos de autor de Windows
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699890"
---
# <a name="author-attribute"></a><span data-ttu-id="51ef7-104">Atributo Author</span><span class="sxs-lookup"><span data-stu-id="51ef7-104">Author Attribute</span></span>

<span data-ttu-id="51ef7-105">El atributo **Author** es el nombre de un intérprete o actor multimedia asociado con el contenido.</span><span class="sxs-lookup"><span data-stu-id="51ef7-105">The **Author** attribute is the name of a media artist or actor associated with the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="51ef7-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="51ef7-106">Applies To</span></span>

-   [<span data-ttu-id="51ef7-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="51ef7-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="51ef7-108">Listas de reproducción de CD</span><span class="sxs-lookup"><span data-stu-id="51ef7-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="51ef7-109">Pistas de CD</span><span class="sxs-lookup"><span data-stu-id="51ef7-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="51ef7-110">Archivos de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="51ef7-110">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="51ef7-111">DVDs</span><span class="sxs-lookup"><span data-stu-id="51ef7-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="51ef7-112">Media. getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="51ef7-112">Media.getItemInfoByType</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="51ef7-113">Elementos de fotografía</span><span class="sxs-lookup"><span data-stu-id="51ef7-113">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="51ef7-114">Reproducción</span><span class="sxs-lookup"><span data-stu-id="51ef7-114">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="51ef7-115">Elementos de radio</span><span class="sxs-lookup"><span data-stu-id="51ef7-115">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="51ef7-116">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="51ef7-116">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="51ef7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51ef7-117">Remarks</span></span>

<span data-ttu-id="51ef7-118">Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="51ef7-118">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="51ef7-119">Este atributo puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="51ef7-119">This attribute may have multiple values.</span></span> <span data-ttu-id="51ef7-120">Para recuperar todos los valores de un atributo con varios valores, debe utilizar los *medios*. método **getItemInfoByType** , no el *medio*. método **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="51ef7-120">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.**getItemInfo** method.</span></span>

<span data-ttu-id="51ef7-121">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMAuthor.</span><span class="sxs-lookup"><span data-stu-id="51ef7-121">The Windows Media Format SDK constant for this attribute is g\_wszWMAuthor.</span></span>

<span data-ttu-id="51ef7-122">**Actor** y **intérprete** son alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="51ef7-122">**Actor** and **Artist** are aliases for this attribute.</span></span>

<span data-ttu-id="51ef7-123">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="51ef7-123">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="51ef7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51ef7-124">Requirements</span></span>



| <span data-ttu-id="51ef7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="51ef7-125">Requirement</span></span> | <span data-ttu-id="51ef7-126">Value</span><span class="sxs-lookup"><span data-stu-id="51ef7-126">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="51ef7-127">Versión</span><span class="sxs-lookup"><span data-stu-id="51ef7-127">Version</span></span><br/> | <span data-ttu-id="51ef7-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="51ef7-128">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51ef7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="51ef7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ef7-130">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="51ef7-130">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





