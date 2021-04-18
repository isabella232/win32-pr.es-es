---
title: Atributo MediaContentTypes
description: El atributo MediaContentTypes especifica el tipo de contenido del elemento.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- MediaContentTypes Media Player de Windows
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8979864151e029abf2731f6f0b4663e078a2c061
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653546"
---
# <a name="mediacontenttypes-attribute"></a><span data-ttu-id="2e5ef-104">Atributo MediaContentTypes</span><span class="sxs-lookup"><span data-stu-id="2e5ef-104">MediaContentTypes Attribute</span></span>

<span data-ttu-id="2e5ef-105">El atributo **MediaContentTypes** especifica el tipo de contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="2e5ef-105">The **MediaContentTypes** attribute specifies the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="2e5ef-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="2e5ef-106">Applies To</span></span>

-   [<span data-ttu-id="2e5ef-107">Reproducción</span><span class="sxs-lookup"><span data-stu-id="2e5ef-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="2e5ef-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e5ef-108">Remarks</span></span>

<span data-ttu-id="2e5ef-109">Este atributo puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="2e5ef-109">This attribute can be one of the following values:</span></span>



| <span data-ttu-id="2e5ef-110">Value</span><span class="sxs-lookup"><span data-stu-id="2e5ef-110">Value</span></span> | <span data-ttu-id="2e5ef-111">Significado</span><span class="sxs-lookup"><span data-stu-id="2e5ef-111">Meaning</span></span>                                |
|-------|----------------------------------------|
| <span data-ttu-id="2e5ef-112">1</span><span class="sxs-lookup"><span data-stu-id="2e5ef-112">1</span></span>     | <span data-ttu-id="2e5ef-113">La lista de reproducción contiene contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="2e5ef-113">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="2e5ef-114">2</span><span class="sxs-lookup"><span data-stu-id="2e5ef-114">2</span></span>     | <span data-ttu-id="2e5ef-115">Que se va a proporcionar.</span><span class="sxs-lookup"><span data-stu-id="2e5ef-115">To be supplied.</span></span>                        |
| <span data-ttu-id="2e5ef-116">3</span><span class="sxs-lookup"><span data-stu-id="2e5ef-116">3</span></span>     | <span data-ttu-id="2e5ef-117">La lista de reproducción contiene contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="2e5ef-117">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="2e5ef-118">4</span><span class="sxs-lookup"><span data-stu-id="2e5ef-118">4</span></span>     | <span data-ttu-id="2e5ef-119">La lista de reproducción contiene contenido de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e5ef-119">The playlist contains video content.</span></span>   |
| <span data-ttu-id="2e5ef-120">5</span><span class="sxs-lookup"><span data-stu-id="2e5ef-120">5</span></span>     | <span data-ttu-id="2e5ef-121">La lista de reproducción contiene el contenido de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2e5ef-121">The playlist contains picture content.</span></span> |
| <span data-ttu-id="2e5ef-122">6</span><span class="sxs-lookup"><span data-stu-id="2e5ef-122">6</span></span>     | <span data-ttu-id="2e5ef-123">La lista de reproducción contiene contenido de TV.</span><span class="sxs-lookup"><span data-stu-id="2e5ef-123">The playlist contains TV content.</span></span>      |



 

<span data-ttu-id="2e5ef-124">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="2e5ef-124">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e5ef-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e5ef-125">Requirements</span></span>



| <span data-ttu-id="2e5ef-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e5ef-126">Requirement</span></span> | <span data-ttu-id="2e5ef-127">Value</span><span class="sxs-lookup"><span data-stu-id="2e5ef-127">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="2e5ef-128">Versión</span><span class="sxs-lookup"><span data-stu-id="2e5ef-128">Version</span></span><br/> | <span data-ttu-id="2e5ef-129">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="2e5ef-129">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e5ef-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e5ef-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e5ef-131">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="2e5ef-131">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





