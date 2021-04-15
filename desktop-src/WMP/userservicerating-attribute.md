---
title: Atributo UserServiceRating
description: El atributo UserServiceRating está reservado para uso futuro.
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- UserServiceRating Media Player de Windows
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690a090aaa9d07ee850caee004242272368129f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708151"
---
# <a name="userservicerating-attribute"></a><span data-ttu-id="dd6db-104">Atributo UserServiceRating</span><span class="sxs-lookup"><span data-stu-id="dd6db-104">UserServiceRating Attribute</span></span>

<span data-ttu-id="dd6db-105">El atributo **UserServiceRating** está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="dd6db-105">The **UserServiceRating** attribute is reserved for future use.</span></span>

## <a name="applies-to"></a><span data-ttu-id="dd6db-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="dd6db-106">Applies To</span></span>

-   [<span data-ttu-id="dd6db-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="dd6db-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="dd6db-108">Reproducción</span><span class="sxs-lookup"><span data-stu-id="dd6db-108">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="dd6db-109">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="dd6db-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="dd6db-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd6db-110">Remarks</span></span>

<span data-ttu-id="dd6db-111">Las clasificaciones de usuario se representan mediante valores enteros, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dd6db-111">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="dd6db-112">Al especificar un valor, use uno de los valores de la columna valor de escritura.</span><span class="sxs-lookup"><span data-stu-id="dd6db-112">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="dd6db-113">Al recuperar valores, puede usar los intervalos de la columna leer valores para determinar el número de estrellas.</span><span class="sxs-lookup"><span data-stu-id="dd6db-113">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="dd6db-114">Rating</span><span class="sxs-lookup"><span data-stu-id="dd6db-114">Rating</span></span>  | <span data-ttu-id="dd6db-115">Escribir valor</span><span class="sxs-lookup"><span data-stu-id="dd6db-115">Writing value</span></span> | <span data-ttu-id="dd6db-116">Leer valores</span><span class="sxs-lookup"><span data-stu-id="dd6db-116">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="dd6db-117">Sin clasificación</span><span class="sxs-lookup"><span data-stu-id="dd6db-117">Unrated</span></span> | <span data-ttu-id="dd6db-118">0</span><span class="sxs-lookup"><span data-stu-id="dd6db-118">0</span></span>             | <span data-ttu-id="dd6db-119">0</span><span class="sxs-lookup"><span data-stu-id="dd6db-119">0</span></span>              |
| <span data-ttu-id="dd6db-120">1 estrella</span><span class="sxs-lookup"><span data-stu-id="dd6db-120">1 star</span></span>  | <span data-ttu-id="dd6db-121">1</span><span class="sxs-lookup"><span data-stu-id="dd6db-121">1</span></span>             | <span data-ttu-id="dd6db-122">De 1 a 12</span><span class="sxs-lookup"><span data-stu-id="dd6db-122">1 to 12</span></span>        |
| <span data-ttu-id="dd6db-123">2 estrellas</span><span class="sxs-lookup"><span data-stu-id="dd6db-123">2 stars</span></span> | <span data-ttu-id="dd6db-124">25</span><span class="sxs-lookup"><span data-stu-id="dd6db-124">25</span></span>            | <span data-ttu-id="dd6db-125">de 13 a 37</span><span class="sxs-lookup"><span data-stu-id="dd6db-125">13 to 37</span></span>       |
| <span data-ttu-id="dd6db-126">3 estrellas</span><span class="sxs-lookup"><span data-stu-id="dd6db-126">3 stars</span></span> | <span data-ttu-id="dd6db-127">50</span><span class="sxs-lookup"><span data-stu-id="dd6db-127">50</span></span>            | <span data-ttu-id="dd6db-128">de 38 a 62</span><span class="sxs-lookup"><span data-stu-id="dd6db-128">38 to 62</span></span>       |
| <span data-ttu-id="dd6db-129">4 estrellas</span><span class="sxs-lookup"><span data-stu-id="dd6db-129">4 stars</span></span> | <span data-ttu-id="dd6db-130">75</span><span class="sxs-lookup"><span data-stu-id="dd6db-130">75</span></span>            | <span data-ttu-id="dd6db-131">de 63 a 86</span><span class="sxs-lookup"><span data-stu-id="dd6db-131">63 to 86</span></span>       |
| <span data-ttu-id="dd6db-132">5 estrellas</span><span class="sxs-lookup"><span data-stu-id="dd6db-132">5 stars</span></span> | <span data-ttu-id="dd6db-133">99</span><span class="sxs-lookup"><span data-stu-id="dd6db-133">99</span></span>            | <span data-ttu-id="dd6db-134">de 87 a 99</span><span class="sxs-lookup"><span data-stu-id="dd6db-134">87 to 99</span></span>       |



 

<span data-ttu-id="dd6db-135">Este atributo solo se almacena en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dd6db-135">This attribute is stored only in the library.</span></span>

<span data-ttu-id="dd6db-136">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="dd6db-136">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd6db-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd6db-137">Requirements</span></span>



| <span data-ttu-id="dd6db-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd6db-138">Requirement</span></span> | <span data-ttu-id="dd6db-139">Value</span><span class="sxs-lookup"><span data-stu-id="dd6db-139">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="dd6db-140">Versión</span><span class="sxs-lookup"><span data-stu-id="dd6db-140">Version</span></span><br/> | <span data-ttu-id="dd6db-141">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="dd6db-141">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd6db-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd6db-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd6db-143">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="dd6db-143">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





