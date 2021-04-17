---
title: Atributo UserEffectiveRating
description: El atributo UserEffectiveRating es la clasificación calculada por Windows Media Player en función de la frecuencia de reproducción del elemento.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- UserEffectiveRating Media Player de Windows
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94abda9f8237c169845683263081566957a10b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718701"
---
# <a name="usereffectiverating-attribute"></a><span data-ttu-id="f33c7-104">Atributo UserEffectiveRating</span><span class="sxs-lookup"><span data-stu-id="f33c7-104">UserEffectiveRating Attribute</span></span>

<span data-ttu-id="f33c7-105">El atributo **UserEffectiveRating** es la clasificación calculada por Windows Media Player en función de la frecuencia de reproducción del elemento.</span><span class="sxs-lookup"><span data-stu-id="f33c7-105">The **UserEffectiveRating** attribute is the rating computed by Windows Media Player based on how often the item has been played.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f33c7-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="f33c7-106">Applies To</span></span>

-   [<span data-ttu-id="f33c7-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="f33c7-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="f33c7-108">Otros elementos</span><span class="sxs-lookup"><span data-stu-id="f33c7-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="f33c7-109">Reproducción</span><span class="sxs-lookup"><span data-stu-id="f33c7-109">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="f33c7-110">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="f33c7-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="f33c7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f33c7-111">Remarks</span></span>

<span data-ttu-id="f33c7-112">Las clasificaciones de usuario se representan mediante valores enteros, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f33c7-112">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="f33c7-113">Al especificar un valor, use uno de los valores de la columna valor de escritura.</span><span class="sxs-lookup"><span data-stu-id="f33c7-113">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="f33c7-114">Al recuperar valores, puede usar los intervalos de la columna leer valores para determinar el número de estrellas.</span><span class="sxs-lookup"><span data-stu-id="f33c7-114">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="f33c7-115">Rating</span><span class="sxs-lookup"><span data-stu-id="f33c7-115">Rating</span></span>  | <span data-ttu-id="f33c7-116">Escribir valor</span><span class="sxs-lookup"><span data-stu-id="f33c7-116">Writing value</span></span> | <span data-ttu-id="f33c7-117">Leer valores</span><span class="sxs-lookup"><span data-stu-id="f33c7-117">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="f33c7-118">Sin clasificación</span><span class="sxs-lookup"><span data-stu-id="f33c7-118">Unrated</span></span> | <span data-ttu-id="f33c7-119">0</span><span class="sxs-lookup"><span data-stu-id="f33c7-119">0</span></span>             | <span data-ttu-id="f33c7-120">0</span><span class="sxs-lookup"><span data-stu-id="f33c7-120">0</span></span>              |
| <span data-ttu-id="f33c7-121">1 estrella</span><span class="sxs-lookup"><span data-stu-id="f33c7-121">1 star</span></span>  | <span data-ttu-id="f33c7-122">1</span><span class="sxs-lookup"><span data-stu-id="f33c7-122">1</span></span>             | <span data-ttu-id="f33c7-123">De 1 a 12</span><span class="sxs-lookup"><span data-stu-id="f33c7-123">1 to 12</span></span>        |
| <span data-ttu-id="f33c7-124">2 estrellas</span><span class="sxs-lookup"><span data-stu-id="f33c7-124">2 stars</span></span> | <span data-ttu-id="f33c7-125">25</span><span class="sxs-lookup"><span data-stu-id="f33c7-125">25</span></span>            | <span data-ttu-id="f33c7-126">de 13 a 37</span><span class="sxs-lookup"><span data-stu-id="f33c7-126">13 to 37</span></span>       |
| <span data-ttu-id="f33c7-127">3 estrellas</span><span class="sxs-lookup"><span data-stu-id="f33c7-127">3 stars</span></span> | <span data-ttu-id="f33c7-128">50</span><span class="sxs-lookup"><span data-stu-id="f33c7-128">50</span></span>            | <span data-ttu-id="f33c7-129">de 38 a 62</span><span class="sxs-lookup"><span data-stu-id="f33c7-129">38 to 62</span></span>       |
| <span data-ttu-id="f33c7-130">4 estrellas</span><span class="sxs-lookup"><span data-stu-id="f33c7-130">4 stars</span></span> | <span data-ttu-id="f33c7-131">75</span><span class="sxs-lookup"><span data-stu-id="f33c7-131">75</span></span>            | <span data-ttu-id="f33c7-132">de 63 a 86</span><span class="sxs-lookup"><span data-stu-id="f33c7-132">63 to 86</span></span>       |
| <span data-ttu-id="f33c7-133">5 estrellas</span><span class="sxs-lookup"><span data-stu-id="f33c7-133">5 stars</span></span> | <span data-ttu-id="f33c7-134">99</span><span class="sxs-lookup"><span data-stu-id="f33c7-134">99</span></span>            | <span data-ttu-id="f33c7-135">de 87 a 99</span><span class="sxs-lookup"><span data-stu-id="f33c7-135">87 to 99</span></span>       |



 

<span data-ttu-id="f33c7-136">Este atributo solo se almacena en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f33c7-136">This attribute is stored only in the library.</span></span>

<span data-ttu-id="f33c7-137">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f33c7-137">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f33c7-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f33c7-138">Requirements</span></span>



| <span data-ttu-id="f33c7-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f33c7-139">Requirement</span></span> | <span data-ttu-id="f33c7-140">Value</span><span class="sxs-lookup"><span data-stu-id="f33c7-140">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="f33c7-141">Versión</span><span class="sxs-lookup"><span data-stu-id="f33c7-141">Version</span></span><br/> | <span data-ttu-id="f33c7-142">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="f33c7-142">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f33c7-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="f33c7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33c7-144">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="f33c7-144">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





