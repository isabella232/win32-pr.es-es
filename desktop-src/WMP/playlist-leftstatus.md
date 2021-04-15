---
title: Lista de reproducción. leftStatus
description: El atributo leftStatus especifica o recupera el texto de estado que se muestra en el lado izquierdo y en la parte inferior del elemento de lista de reproducción.
ms.assetid: c83f4fd1-d0e6-4822-9208-8e968c409a78
keywords:
- Windows Media Player de lista de reproducción. leftStatus
topic_type:
- apiref
api_name:
- PLAYLIST.leftStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33d4c3d235a7bba67219378063cb9811601e68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708814"
---
# <a name="playlistleftstatus"></a><span data-ttu-id="67c85-104">Lista de reproducción. leftStatus</span><span class="sxs-lookup"><span data-stu-id="67c85-104">PLAYLIST.leftStatus</span></span>

<span data-ttu-id="67c85-105">El atributo **leftStatus** especifica o recupera el texto de estado que se muestra en el lado izquierdo y en la parte inferior del elemento de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="67c85-105">The **leftStatus** attribute specifies or retrieves the status text that is displayed on the left side and bottom of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.leftStatus
```

## <a name="possible-values"></a><span data-ttu-id="67c85-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="67c85-106">Possible Values</span></span>

<span data-ttu-id="67c85-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="67c85-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="67c85-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67c85-108">Remarks</span></span>

<span data-ttu-id="67c85-109">Este atributo puede combinar cualquier texto con palabras clave específicas que muestren la información deseada, como la duración total de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="67c85-109">This attribute can combine any text with specific keywords that will display the desired information, such as the total duration of the playlist.</span></span> <span data-ttu-id="67c85-110">Las palabras clave se incluyen entre símbolos de porcentaje (%) para mantenerlos distintos del texto normal.</span><span class="sxs-lookup"><span data-stu-id="67c85-110">The keywords are surrounded by percentage symbols (%) to keep them distinct from the ordinary text.</span></span>

<span data-ttu-id="67c85-111">Se pueden usar las siguientes palabras clave.</span><span class="sxs-lookup"><span data-stu-id="67c85-111">The following keywords can be used.</span></span>



| <span data-ttu-id="67c85-112">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="67c85-112">Keyword</span></span>               | <span data-ttu-id="67c85-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="67c85-113">Description</span></span>                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c85-114">count</span><span class="sxs-lookup"><span data-stu-id="67c85-114">count</span></span>                 | <span data-ttu-id="67c85-115">Número de elementos de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="67c85-115">Number of items in the playlist.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="67c85-116">tamaño</span><span class="sxs-lookup"><span data-stu-id="67c85-116">size</span></span>                  | <span data-ttu-id="67c85-117">Tamaño total de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="67c85-117">Total size of the playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="67c85-118">duration</span><span class="sxs-lookup"><span data-stu-id="67c85-118">duration</span></span>              | <span data-ttu-id="67c85-119">Duración total de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="67c85-119">Total duration of the playlist.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="67c85-120">*XXXXXX*</span><span class="sxs-lookup"><span data-stu-id="67c85-120">*XXX*</span></span>                 | <span data-ttu-id="67c85-121">Realiza una **getItemInfo** en la lista de reproducción, donde *XXX* es el elemento que se va a recibir.</span><span class="sxs-lookup"><span data-stu-id="67c85-121">Does a **getItemInfo** on the playlist with *XXX* being the item to receive.</span></span>                                                                                                                                 |
| <span data-ttu-id="67c85-122">SelectedSize</span><span class="sxs-lookup"><span data-stu-id="67c85-122">SelectedSize</span></span>          | <span data-ttu-id="67c85-123">Tamaño total de las entradas seleccionadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="67c85-123">Total size of the selected entries in the playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="67c85-124">SelectedCount</span><span class="sxs-lookup"><span data-stu-id="67c85-124">SelectedCount</span></span>         | <span data-ttu-id="67c85-125">Número total de entradas seleccionadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="67c85-125">Total number of selected entries in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="67c85-126">SelectedDuration</span><span class="sxs-lookup"><span data-stu-id="67c85-126">SelectedDuration</span></span>      | <span data-ttu-id="67c85-127">Duración total de las entradas seleccionadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="67c85-127">Total duration of the selected entries in the playlist.</span></span>                                                                                                                                                      |
| <span data-ttu-id="67c85-128">CheckedCount</span><span class="sxs-lookup"><span data-stu-id="67c85-128">CheckedCount</span></span>          | <span data-ttu-id="67c85-129">Número total de pistas comprobadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="67c85-129">Total number of checked tracks in the playlist.</span></span>                                                                                                                                                              |
| <span data-ttu-id="67c85-130">CheckedDuration</span><span class="sxs-lookup"><span data-stu-id="67c85-130">CheckedDuration</span></span>       | <span data-ttu-id="67c85-131">Duración total de las pistas comprobadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="67c85-131">Total duration of the checked tracks in the playlist.</span></span>                                                                                                                                                        |
| <span data-ttu-id="67c85-132">CheckedSize</span><span class="sxs-lookup"><span data-stu-id="67c85-132">CheckedSize</span></span>           | <span data-ttu-id="67c85-133">Tamaño total de las pistas comprobadas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="67c85-133">Total size of the checked tracks in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="67c85-134">DurationString</span><span class="sxs-lookup"><span data-stu-id="67c85-134">DurationString</span></span>        | <span data-ttu-id="67c85-135">Muestra el texto que describe la duración como "tiempo total" o "tiempo estimado", en función de si se conocen los valores totales.</span><span class="sxs-lookup"><span data-stu-id="67c85-135">Displays text that describes the duration as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="67c85-136">Este texto va seguido de "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="67c85-136">This text is followed by "%duration%".</span></span>                                       |
| <span data-ttu-id="67c85-137">CheckedDurationString</span><span class="sxs-lookup"><span data-stu-id="67c85-137">CheckedDurationString</span></span> | <span data-ttu-id="67c85-138">Muestra el texto que describe la duración de todos los elementos activados en la lista de reproducción como "tiempo total" o "tiempo estimado", dependiendo de si se conocen los valores totales.</span><span class="sxs-lookup"><span data-stu-id="67c85-138">Displays text that describes the duration for all checked items in the playlist as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="67c85-139">Este texto va seguido de "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="67c85-139">This text is followed by "%duration%".</span></span> |



 

<span data-ttu-id="67c85-140">El valor "tiempo total:% Duration%" para una lista de reproducción que contenga una duración total de siete minutos mostrará "tiempo total: 07:00".</span><span class="sxs-lookup"><span data-stu-id="67c85-140">The value "Total Time: %duration%" for a playlist that contains a total duration of seven minutes will display "Total Time: 07:00".</span></span>

## <a name="requirements"></a><span data-ttu-id="67c85-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67c85-141">Requirements</span></span>



| <span data-ttu-id="67c85-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="67c85-142">Requirement</span></span> | <span data-ttu-id="67c85-143">Value</span><span class="sxs-lookup"><span data-stu-id="67c85-143">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="67c85-144">Versión</span><span class="sxs-lookup"><span data-stu-id="67c85-144">Version</span></span><br/> | <span data-ttu-id="67c85-145">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="67c85-145">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67c85-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="67c85-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c85-147">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="67c85-147">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





