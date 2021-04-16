---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl. h)
description: La transición de avance de página transforma la imagen anterior con un efecto de volteo de página, que revela la nueva imagen debajo.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649575"
---
# <a name="wmt_videoimage_transition_page_roll"></a><span data-ttu-id="a93c6-104">\_rollo de página de transición de VIDEOIMAGE WMT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a93c6-104">WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL</span></span>

<span data-ttu-id="a93c6-105">La transición de avance de página transforma la imagen anterior con un efecto de volteo de página, que revela la nueva imagen debajo.</span><span class="sxs-lookup"><span data-stu-id="a93c6-105">The page roll transition transforms the old image with a page-flipping effect, revealing the new image underneath.</span></span>

## <a name="parameters"></a><span data-ttu-id="a93c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a93c6-106">Parameters</span></span>

<span data-ttu-id="a93c6-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="a93c6-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a93c6-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a93c6-108">Parameter</span></span></th>
<th><span data-ttu-id="a93c6-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="a93c6-109">Structure member</span></span></th>
<th><span data-ttu-id="a93c6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a93c6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a93c6-111">Radio</span><span class="sxs-lookup"><span data-stu-id="a93c6-111">Radius</span></span></td>
<td><span data-ttu-id="a93c6-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="a93c6-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="a93c6-113">Radio del efecto de relanzamiento de página.</span><span class="sxs-lookup"><span data-stu-id="a93c6-113">Radius of the roll in the page roll effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a93c6-114">Distancia</span><span class="sxs-lookup"><span data-stu-id="a93c6-114">Distance</span></span></td>
<td><span data-ttu-id="a93c6-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="a93c6-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="a93c6-116">Cantidad de la nueva imagen revelada por el efecto de relanzamiento de página, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a93c6-116">Amount of the new image that is revealed by the page roll effect, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a93c6-117">Dirección</span><span class="sxs-lookup"><span data-stu-id="a93c6-117">Direction</span></span></td>
<td><span data-ttu-id="a93c6-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="a93c6-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="a93c6-119">Esquina o lado del fotograma del vídeo desde el que se origina el lanzamiento de la página. Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="a93c6-119">Corner or side of the video frame, from which the page roll originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="a93c6-120">0: lado izquierdo</span><span class="sxs-lookup"><span data-stu-id="a93c6-120">0 - Left side</span></span></li>
<li><span data-ttu-id="a93c6-121">1-lado derecho</span><span class="sxs-lookup"><span data-stu-id="a93c6-121">1 - Right side</span></span></li>
<li><span data-ttu-id="a93c6-122">2-inferior</span><span class="sxs-lookup"><span data-stu-id="a93c6-122">2 - Bottom</span></span></li>
<li><span data-ttu-id="a93c6-123">3-superior</span><span class="sxs-lookup"><span data-stu-id="a93c6-123">3 - Top</span></span></li>
<li><span data-ttu-id="a93c6-124">4: esquina inferior izquierda</span><span class="sxs-lookup"><span data-stu-id="a93c6-124">4 - Bottom left corner</span></span></li>
<li><span data-ttu-id="a93c6-125">5: esquina inferior derecha</span><span class="sxs-lookup"><span data-stu-id="a93c6-125">5 - Bottom right corner</span></span></li>
<li><span data-ttu-id="a93c6-126">6: esquina superior izquierda</span><span class="sxs-lookup"><span data-stu-id="a93c6-126">6 - Upper left corner</span></span></li>
<li><span data-ttu-id="a93c6-127">7: esquina superior derecha</span><span class="sxs-lookup"><span data-stu-id="a93c6-127">7 - Upper right corner</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a93c6-128">Composición</span><span class="sxs-lookup"><span data-stu-id="a93c6-128">Composition</span></span></td>
<td><span data-ttu-id="a93c6-129"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="a93c6-129"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="a93c6-130">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="a93c6-130">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="a93c6-131">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="a93c6-131">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="a93c6-132">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="a93c6-132">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a93c6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a93c6-133">Requirements</span></span>



| <span data-ttu-id="a93c6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a93c6-134">Requirement</span></span> | <span data-ttu-id="a93c6-135">Value</span><span class="sxs-lookup"><span data-stu-id="a93c6-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a93c6-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a93c6-136">Header</span></span><br/> | <dl> <span data-ttu-id="a93c6-137"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a93c6-137"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a93c6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a93c6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a93c6-139">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="a93c6-139">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





