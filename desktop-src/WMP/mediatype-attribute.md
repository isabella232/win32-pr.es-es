---
title: MediaType (atributo)
description: El atributo MediaType es el tipo de contenido del elemento.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- Atributo MediaType Media Player Windows
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653545"
---
# <a name="mediatype-attribute"></a><span data-ttu-id="679eb-104">MediaType (atributo)</span><span class="sxs-lookup"><span data-stu-id="679eb-104">MediaType Attribute</span></span>

<span data-ttu-id="679eb-105">El atributo **mediatype** es el tipo de contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="679eb-105">The **MediaType** attribute is the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="679eb-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="679eb-106">Applies To</span></span>

-   [<span data-ttu-id="679eb-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="679eb-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="679eb-108">Otros elementos</span><span class="sxs-lookup"><span data-stu-id="679eb-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="679eb-109">Elementos de fotografía</span><span class="sxs-lookup"><span data-stu-id="679eb-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="679eb-110">Reproducción</span><span class="sxs-lookup"><span data-stu-id="679eb-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="679eb-111">Elementos de radio</span><span class="sxs-lookup"><span data-stu-id="679eb-111">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="679eb-112">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="679eb-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="679eb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="679eb-113">Remarks</span></span>

<span data-ttu-id="679eb-114">Este atributo solo se almacena en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="679eb-114">This attribute is stored only in the library.</span></span>

<span data-ttu-id="679eb-115">Este atributo tiene uno de los valores siguientes: "audio", "otro", "foto", "lista de reproducción", "radio" o "vídeo".</span><span class="sxs-lookup"><span data-stu-id="679eb-115">This attribute has one of the following values: "audio", "other", "photo", "playlist", "radio", or "video".</span></span> <span data-ttu-id="679eb-116">Use este atributo con el *MediaCollection*. método **getByAttribute** para recuperar una lista de reproducción que contenga todos los elementos de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="679eb-116">Use this attribute with the *MediaCollection*.**getByAttribute** method to retrieve a playlist containing all of the items of a particular type.</span></span>

<span data-ttu-id="679eb-117">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="679eb-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="679eb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="679eb-118">Requirements</span></span>



| <span data-ttu-id="679eb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="679eb-119">Requirement</span></span> | <span data-ttu-id="679eb-120">Value</span><span class="sxs-lookup"><span data-stu-id="679eb-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="679eb-121">Versión</span><span class="sxs-lookup"><span data-stu-id="679eb-121">Version</span></span><br/> | <span data-ttu-id="679eb-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="679eb-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="679eb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="679eb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="679eb-124">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="679eb-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="679eb-125">**MediaCollection.getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="679eb-125">**MediaCollection.getByAttribute**</span></span>](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





