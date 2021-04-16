---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl. h)
description: La transición de la rueda revela la nueva imagen al girar cuatro líneas alrededor de un punto de pivote común, como los radios de una rueda.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f39d3355cfce3397c379bf7edafaae77ccfafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650207"
---
# <a name="wmt_videoimage_transition_wheel"></a><span data-ttu-id="9fe66-104">\_rueda de transición de VIDEOIMAGE WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="9fe66-104">WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL</span></span>

<span data-ttu-id="9fe66-105">La transición de la rueda revela la nueva imagen al girar cuatro líneas alrededor de un punto de pivote común, como los radios de una rueda.</span><span class="sxs-lookup"><span data-stu-id="9fe66-105">The wheel transition reveals the new image by rotating four lines around a common pivot point, like the spokes of a wheel.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fe66-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fe66-106">Parameters</span></span>

<span data-ttu-id="9fe66-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="9fe66-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9fe66-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9fe66-108">Parameter</span></span></th>
<th><span data-ttu-id="9fe66-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="9fe66-109">Structure member</span></span></th>
<th><span data-ttu-id="9fe66-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fe66-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9fe66-111">Centrar X</span><span class="sxs-lookup"><span data-stu-id="9fe66-111">Center X</span></span></td>
<td><span data-ttu-id="9fe66-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="9fe66-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="9fe66-113">Coordenada X, relativa al fotograma de vídeo, del centro del efecto de la rueda.</span><span class="sxs-lookup"><span data-stu-id="9fe66-113">X-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9fe66-114">Centrar Y</span><span class="sxs-lookup"><span data-stu-id="9fe66-114">Center Y</span></span></td>
<td><span data-ttu-id="9fe66-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="9fe66-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="9fe66-116">Coordenada y, en relación con el fotograma de vídeo, del centro del efecto de la rueda.</span><span class="sxs-lookup"><span data-stu-id="9fe66-116">Y-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9fe66-117">Ángulo</span><span class="sxs-lookup"><span data-stu-id="9fe66-117">Angle</span></span></td>
<td><span data-ttu-id="9fe66-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="9fe66-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="9fe66-119">Ángulo de giro, en grados, de los radios del efecto de la rueda.</span><span class="sxs-lookup"><span data-stu-id="9fe66-119">Angle of rotation, in degrees, of the spokes of the wheel effect.</span></span> <span data-ttu-id="9fe66-120">Un valor de 0,0 indica la imagen antigua sin que se revele ninguna de las imágenes nuevas.</span><span class="sxs-lookup"><span data-stu-id="9fe66-120">A value of 0.0 indicates the old image without any of the new image revealed.</span></span> <span data-ttu-id="9fe66-121">Un valor de 90,0 indica que la nueva imagen se ha revelado por completo. El movimiento de 0,0 a 90,0 aparece como rotación en el sentido de las agujas del reloj de los radios.</span><span class="sxs-lookup"><span data-stu-id="9fe66-121">A value of 90.0 indicates the new image fully revealed.Movement from 0.0 to 90.0 appears as clockwise rotation of the spokes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9fe66-122">Composición</span><span class="sxs-lookup"><span data-stu-id="9fe66-122">Composition</span></span></td>
<td><span data-ttu-id="9fe66-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="9fe66-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="9fe66-124">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="9fe66-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="9fe66-125">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="9fe66-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="9fe66-126">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="9fe66-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9fe66-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fe66-127">Requirements</span></span>



| <span data-ttu-id="9fe66-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fe66-128">Requirement</span></span> | <span data-ttu-id="9fe66-129">Value</span><span class="sxs-lookup"><span data-stu-id="9fe66-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe66-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fe66-130">Header</span></span><br/> | <dl> <span data-ttu-id="9fe66-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fe66-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fe66-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fe66-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe66-133">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="9fe66-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





