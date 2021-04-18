---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (Wmsdkidl. h)
description: La transición de estrella revela la nueva imagen en una estrella de cinco puntas dentro del marco.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af064682c4488153823164433bd432a9080336fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708818"
---
# <a name="wmt_videoimage_transition_star"></a><span data-ttu-id="46d56-104">estrella de transición de \_ imágenes WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="46d56-104">WMT\_VIDEOIMAGE\_TRANSITION\_STAR</span></span>

<span data-ttu-id="46d56-105">La transición de estrella revela la nueva imagen en una estrella de cinco puntas dentro del marco.</span><span class="sxs-lookup"><span data-stu-id="46d56-105">The star transition reveals the new image in a five-pointed star inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="46d56-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46d56-106">Parameters</span></span>

<span data-ttu-id="46d56-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="46d56-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46d56-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="46d56-108">Parameter</span></span></th>
<th><span data-ttu-id="46d56-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="46d56-109">Structure member</span></span></th>
<th><span data-ttu-id="46d56-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="46d56-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d56-111">Centrar X</span><span class="sxs-lookup"><span data-stu-id="46d56-111">Center X</span></span></td>
<td><span data-ttu-id="46d56-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="46d56-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="46d56-113">Coordenada X, relativa al fotograma de vídeo, del centro de la estrella.</span><span class="sxs-lookup"><span data-stu-id="46d56-113">X-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d56-114">Centrar Y</span><span class="sxs-lookup"><span data-stu-id="46d56-114">Center Y</span></span></td>
<td><span data-ttu-id="46d56-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="46d56-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="46d56-116">Coordenada y, en relación con el fotograma de vídeo, del centro de la estrella.</span><span class="sxs-lookup"><span data-stu-id="46d56-116">Y-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46d56-117">Radio</span><span class="sxs-lookup"><span data-stu-id="46d56-117">Radius</span></span></td>
<td><span data-ttu-id="46d56-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="46d56-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="46d56-119">Radio, en píxeles, del círculo definido por los puntos de la estrella.</span><span class="sxs-lookup"><span data-stu-id="46d56-119">Radius, in pixels, of the circle defined by the points of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d56-120">Composición</span><span class="sxs-lookup"><span data-stu-id="46d56-120">Composition</span></span></td>
<td><span data-ttu-id="46d56-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="46d56-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="46d56-122">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="46d56-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="46d56-123">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="46d56-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="46d56-124">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="46d56-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="46d56-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46d56-125">Requirements</span></span>



| <span data-ttu-id="46d56-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="46d56-126">Requirement</span></span> | <span data-ttu-id="46d56-127">Value</span><span class="sxs-lookup"><span data-stu-id="46d56-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46d56-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46d56-128">Header</span></span><br/> | <dl> <span data-ttu-id="46d56-129"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46d56-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d56-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="46d56-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d56-131">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="46d56-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





