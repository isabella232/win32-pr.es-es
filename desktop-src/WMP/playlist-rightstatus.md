---
title: Lista de reproducción. rightStatus
description: El atributo rightStatus especifica o recupera el texto de estado que se muestra en el lado derecho y en la parte inferior del elemento de lista de reproducción.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- Windows Media Player de lista de reproducción. rightStatus
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b382da4ae214c9a830cc64fb1aa0d0edadbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708675"
---
# <a name="playlistrightstatus"></a><span data-ttu-id="72d19-104">Lista de reproducción. rightStatus</span><span class="sxs-lookup"><span data-stu-id="72d19-104">PLAYLIST.rightStatus</span></span>

<span data-ttu-id="72d19-105">El atributo **rightStatus** especifica o recupera el texto de estado que se muestra en el lado derecho y en la parte inferior del elemento de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="72d19-105">The **rightStatus** attribute specifies or retrieves the status text that is displayed on the right side and bottom of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a><span data-ttu-id="72d19-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="72d19-106">Possible Values</span></span>

<span data-ttu-id="72d19-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="72d19-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="72d19-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72d19-108">Remarks</span></span>

<span data-ttu-id="72d19-109">Este atributo puede combinar cualquier texto con palabras clave específicas que muestren la información deseada, como la duración total de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="72d19-109">This attribute can combine any text with specific keywords that will display the desired information, such as the total duration of the playlist.</span></span> <span data-ttu-id="72d19-110">Las palabras clave se incluyen entre símbolos de porcentaje (%) para mantenerlos distintos del texto normal.</span><span class="sxs-lookup"><span data-stu-id="72d19-110">The keywords are surrounded by percentage symbols (%) to keep them distinct from the ordinary text.</span></span>

<span data-ttu-id="72d19-111">Se pueden usar las siguientes palabras clave.</span><span class="sxs-lookup"><span data-stu-id="72d19-111">The following keywords can be used.</span></span>



| <span data-ttu-id="72d19-112">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="72d19-112">Keyword</span></span>               | <span data-ttu-id="72d19-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="72d19-113">Description</span></span>                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d19-114">count</span><span class="sxs-lookup"><span data-stu-id="72d19-114">count</span></span>                 | <span data-ttu-id="72d19-115">Número de elementos de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="72d19-115">Number of items in the playlist.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="72d19-116">tamaño</span><span class="sxs-lookup"><span data-stu-id="72d19-116">size</span></span>                  | <span data-ttu-id="72d19-117">Tamaño total de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="72d19-117">Total size of the playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="72d19-118">duration</span><span class="sxs-lookup"><span data-stu-id="72d19-118">duration</span></span>              | <span data-ttu-id="72d19-119">Duración total de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="72d19-119">Total duration of the playlist.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="72d19-120">*XXXXXX*</span><span class="sxs-lookup"><span data-stu-id="72d19-120">*XXX*</span></span>                 | <span data-ttu-id="72d19-121">Realiza una **getItemInfo** en la lista de reproducción, donde *XXX* es el elemento que se va a recibir.</span><span class="sxs-lookup"><span data-stu-id="72d19-121">Does a **getItemInfo** on the playlist with *XXX* being the item to receive.</span></span>                                                                                                                                 |
| <span data-ttu-id="72d19-122">SelectedSize</span><span class="sxs-lookup"><span data-stu-id="72d19-122">SelectedSize</span></span>          | <span data-ttu-id="72d19-123">Tamaño total de las entradas seleccionadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="72d19-123">Total size of the selected entries in the playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="72d19-124">SelectedCount</span><span class="sxs-lookup"><span data-stu-id="72d19-124">SelectedCount</span></span>         | <span data-ttu-id="72d19-125">Número total de entradas seleccionadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="72d19-125">Total number of selected entries in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="72d19-126">SelectedDuration</span><span class="sxs-lookup"><span data-stu-id="72d19-126">SelectedDuration</span></span>      | <span data-ttu-id="72d19-127">Duración total de las entradas seleccionadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="72d19-127">Total duration of the selected entries in the playlist.</span></span>                                                                                                                                                      |
| <span data-ttu-id="72d19-128">CheckedCount</span><span class="sxs-lookup"><span data-stu-id="72d19-128">CheckedCount</span></span>          | <span data-ttu-id="72d19-129">Número total de pistas comprobadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="72d19-129">Total number of checked tracks in the playlist.</span></span>                                                                                                                                                              |
| <span data-ttu-id="72d19-130">CheckedDuration</span><span class="sxs-lookup"><span data-stu-id="72d19-130">CheckedDuration</span></span>       | <span data-ttu-id="72d19-131">Duración total de las pistas comprobadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="72d19-131">Total duration of the checked tracks in the playlist.</span></span>                                                                                                                                                        |
| <span data-ttu-id="72d19-132">CheckedSize</span><span class="sxs-lookup"><span data-stu-id="72d19-132">CheckedSize</span></span>           | <span data-ttu-id="72d19-133">Tamaño total de las pistas comprobadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="72d19-133">Total size of the checked tracks in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="72d19-134">DurationString</span><span class="sxs-lookup"><span data-stu-id="72d19-134">DurationString</span></span>        | <span data-ttu-id="72d19-135">Muestra el texto que describe la duración como "tiempo total" o "tiempo estimado", en función de si se conocen los valores totales.</span><span class="sxs-lookup"><span data-stu-id="72d19-135">Displays text that describes the duration as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="72d19-136">Este texto va seguido de "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="72d19-136">This text is followed by "%duration%".</span></span>                                       |
| <span data-ttu-id="72d19-137">CheckedDurationString</span><span class="sxs-lookup"><span data-stu-id="72d19-137">CheckedDurationString</span></span> | <span data-ttu-id="72d19-138">Muestra el texto que describe la duración de todos los elementos activados en la lista de reproducción como "tiempo total" o "tiempo estimado", dependiendo de si se conocen los valores totales.</span><span class="sxs-lookup"><span data-stu-id="72d19-138">Displays text that describes the duration for all checked items in the playlist as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="72d19-139">Este texto va seguido de "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="72d19-139">This text is followed by "%duration%".</span></span> |



 

<span data-ttu-id="72d19-140">El valor "tiempo total:% Duration%" para una lista de reproducción que contenga una duración total de siete minutos mostrará "tiempo total: 07:00".</span><span class="sxs-lookup"><span data-stu-id="72d19-140">The value "Total Time: %duration%" for a playlist that contains a total duration of seven minutes will display "Total Time: 07:00".</span></span>

## <a name="requirements"></a><span data-ttu-id="72d19-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72d19-141">Requirements</span></span>



| <span data-ttu-id="72d19-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="72d19-142">Requirement</span></span> | <span data-ttu-id="72d19-143">Value</span><span class="sxs-lookup"><span data-stu-id="72d19-143">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="72d19-144">Versión</span><span class="sxs-lookup"><span data-stu-id="72d19-144">Version</span></span><br/> | <span data-ttu-id="72d19-145">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="72d19-145">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72d19-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="72d19-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d19-147">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="72d19-147">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





