---
title: Atributo UserRating
description: El atributo UserRating es la clasificación especificada por el usuario en la biblioteca.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- UserRating Media Player de Windows
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a25dd7b4e55195deaecf5228b9ad5bad9195c2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708152"
---
# <a name="userrating-attribute"></a><span data-ttu-id="444bd-104">Atributo UserRating</span><span class="sxs-lookup"><span data-stu-id="444bd-104">UserRating Attribute</span></span>

<span data-ttu-id="444bd-105">El atributo **UserRating** es la clasificación especificada por el usuario en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="444bd-105">The **UserRating** attribute is the rating specified by the user in the library.</span></span>

## <a name="applies-to"></a><span data-ttu-id="444bd-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="444bd-106">Applies To</span></span>

-   [<span data-ttu-id="444bd-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="444bd-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="444bd-108">Otros elementos</span><span class="sxs-lookup"><span data-stu-id="444bd-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="444bd-109">Elementos de fotografía</span><span class="sxs-lookup"><span data-stu-id="444bd-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="444bd-110">Reproducción</span><span class="sxs-lookup"><span data-stu-id="444bd-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="444bd-111">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="444bd-111">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="444bd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="444bd-112">Remarks</span></span>

<span data-ttu-id="444bd-113">Las clasificaciones de usuario se representan mediante valores enteros, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="444bd-113">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="444bd-114">Al especificar un valor, use uno de los valores de la columna valor de escritura.</span><span class="sxs-lookup"><span data-stu-id="444bd-114">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="444bd-115">Al recuperar valores, puede usar los intervalos de la columna leer valores para determinar el número de estrellas.</span><span class="sxs-lookup"><span data-stu-id="444bd-115">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="444bd-116">Rating</span><span class="sxs-lookup"><span data-stu-id="444bd-116">Rating</span></span>  | <span data-ttu-id="444bd-117">Escribir valor</span><span class="sxs-lookup"><span data-stu-id="444bd-117">Writing value</span></span> | <span data-ttu-id="444bd-118">Leer valores</span><span class="sxs-lookup"><span data-stu-id="444bd-118">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="444bd-119">Sin clasificación</span><span class="sxs-lookup"><span data-stu-id="444bd-119">Unrated</span></span> | <span data-ttu-id="444bd-120">0</span><span class="sxs-lookup"><span data-stu-id="444bd-120">0</span></span>             | <span data-ttu-id="444bd-121">0</span><span class="sxs-lookup"><span data-stu-id="444bd-121">0</span></span>              |
| <span data-ttu-id="444bd-122">1 estrella</span><span class="sxs-lookup"><span data-stu-id="444bd-122">1 star</span></span>  | <span data-ttu-id="444bd-123">1</span><span class="sxs-lookup"><span data-stu-id="444bd-123">1</span></span>             | <span data-ttu-id="444bd-124">De 1 a 12</span><span class="sxs-lookup"><span data-stu-id="444bd-124">1 to 12</span></span>        |
| <span data-ttu-id="444bd-125">2 estrellas</span><span class="sxs-lookup"><span data-stu-id="444bd-125">2 stars</span></span> | <span data-ttu-id="444bd-126">25</span><span class="sxs-lookup"><span data-stu-id="444bd-126">25</span></span>            | <span data-ttu-id="444bd-127">de 13 a 37</span><span class="sxs-lookup"><span data-stu-id="444bd-127">13 to 37</span></span>       |
| <span data-ttu-id="444bd-128">3 estrellas</span><span class="sxs-lookup"><span data-stu-id="444bd-128">3 stars</span></span> | <span data-ttu-id="444bd-129">50</span><span class="sxs-lookup"><span data-stu-id="444bd-129">50</span></span>            | <span data-ttu-id="444bd-130">de 38 a 62</span><span class="sxs-lookup"><span data-stu-id="444bd-130">38 to 62</span></span>       |
| <span data-ttu-id="444bd-131">4 estrellas</span><span class="sxs-lookup"><span data-stu-id="444bd-131">4 stars</span></span> | <span data-ttu-id="444bd-132">75</span><span class="sxs-lookup"><span data-stu-id="444bd-132">75</span></span>            | <span data-ttu-id="444bd-133">de 63 a 86</span><span class="sxs-lookup"><span data-stu-id="444bd-133">63 to 86</span></span>       |
| <span data-ttu-id="444bd-134">5 estrellas</span><span class="sxs-lookup"><span data-stu-id="444bd-134">5 stars</span></span> | <span data-ttu-id="444bd-135">99</span><span class="sxs-lookup"><span data-stu-id="444bd-135">99</span></span>            | <span data-ttu-id="444bd-136">de 87 a 99</span><span class="sxs-lookup"><span data-stu-id="444bd-136">87 to 99</span></span>       |



 

<span data-ttu-id="444bd-137">Este atributo solo se almacena en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="444bd-137">This attribute is stored only in the library.</span></span>

<span data-ttu-id="444bd-138">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="444bd-138">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="444bd-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="444bd-139">Requirements</span></span>



| <span data-ttu-id="444bd-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="444bd-140">Requirement</span></span> | <span data-ttu-id="444bd-141">Value</span><span class="sxs-lookup"><span data-stu-id="444bd-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="444bd-142">Versión</span><span class="sxs-lookup"><span data-stu-id="444bd-142">Version</span></span><br/> | <span data-ttu-id="444bd-143">Windows Media Player 9 series o posterior (el elemento de fotografía solo se admite en Windows Media Player 10 o posterior)</span><span class="sxs-lookup"><span data-stu-id="444bd-143">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="444bd-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="444bd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="444bd-145">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="444bd-145">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





