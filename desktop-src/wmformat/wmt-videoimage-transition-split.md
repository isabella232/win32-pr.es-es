---
title: WMT_VIDEOIMAGE_TRANSITION_SPLIT (Wmsdkidl. h)
description: La transición dividida revela la nueva imagen dividiendo la imagen anterior. La división aparece a lo largo de una línea recta horizontal o vertical que comienza dentro del marco.
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df253c730b85c4bef8cf18d05ed98fcbd78f35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649790"
---
# <a name="wmt_videoimage_transition_split"></a><span data-ttu-id="229b7-105">División de transición de imagen de videotransmisión WMT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="229b7-105">WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT</span></span>

<span data-ttu-id="229b7-106">La transición dividida revela la nueva imagen dividiendo la imagen anterior.</span><span class="sxs-lookup"><span data-stu-id="229b7-106">The split transition reveals the new image by splitting the old image.</span></span> <span data-ttu-id="229b7-107">La división aparece a lo largo de una línea recta horizontal o vertical que comienza dentro del marco.</span><span class="sxs-lookup"><span data-stu-id="229b7-107">The split appears along a straight horizontal or vertical line starting inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="229b7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="229b7-108">Parameters</span></span>

<span data-ttu-id="229b7-109">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="229b7-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="229b7-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="229b7-110">Parameter</span></span></th>
<th><span data-ttu-id="229b7-111">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="229b7-111">Structure member</span></span></th>
<th><span data-ttu-id="229b7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="229b7-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="229b7-113">Centrar X</span><span class="sxs-lookup"><span data-stu-id="229b7-113">Center X</span></span></td>
<td><span data-ttu-id="229b7-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="229b7-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="229b7-115">Coordenada X, relativa al fotograma de vídeo, de la línea de origen de la división.</span><span class="sxs-lookup"><span data-stu-id="229b7-115">X-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="229b7-116">Centrar Y</span><span class="sxs-lookup"><span data-stu-id="229b7-116">Center Y</span></span></td>
<td><span data-ttu-id="229b7-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="229b7-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="229b7-118">Coordenada y, en relación con el fotograma de vídeo, de la línea de origen de la división.</span><span class="sxs-lookup"><span data-stu-id="229b7-118">Y-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="229b7-119">Distancia</span><span class="sxs-lookup"><span data-stu-id="229b7-119">Distance</span></span></td>
<td><span data-ttu-id="229b7-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="229b7-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="229b7-121">Ancho de la división en píxeles.</span><span class="sxs-lookup"><span data-stu-id="229b7-121">Width of the split in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="229b7-122">Dirección</span><span class="sxs-lookup"><span data-stu-id="229b7-122">Direction</span></span></td>
<td><span data-ttu-id="229b7-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="229b7-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="229b7-124">Orientación de la división. Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="229b7-124">Orientation of the split.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="229b7-125">0: se divide a lo largo de una línea horizontal.</span><span class="sxs-lookup"><span data-stu-id="229b7-125">0 - Splits along a horizontal line.</span></span></li>
<li><span data-ttu-id="229b7-126">1: divide a lo largo de una línea vertical.</span><span class="sxs-lookup"><span data-stu-id="229b7-126">1 - Splits along a vertical line.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="229b7-127">Composición</span><span class="sxs-lookup"><span data-stu-id="229b7-127">Composition</span></span></td>
<td><span data-ttu-id="229b7-128"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="229b7-128"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="229b7-129">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="229b7-129">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="229b7-130">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="229b7-130">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="229b7-131">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="229b7-131">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="229b7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="229b7-132">Requirements</span></span>



| <span data-ttu-id="229b7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="229b7-133">Requirement</span></span> | <span data-ttu-id="229b7-134">Value</span><span class="sxs-lookup"><span data-stu-id="229b7-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="229b7-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="229b7-135">Header</span></span><br/> | <dl> <span data-ttu-id="229b7-136"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="229b7-136"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="229b7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="229b7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229b7-138">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="229b7-138">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





