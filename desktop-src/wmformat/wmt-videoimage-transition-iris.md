---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl. h)
description: La transición de iris revela la nueva imagen a lo largo de un eje x y un eje y. El efecto visual de esta transición es que la nueva imagen aparece en una cruz de ampliación que llega a todos los lados del marco.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd216c7387f850f317417717c50216dd63449843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649935"
---
# <a name="wmt_videoimage_transition_iris"></a><span data-ttu-id="b4715-105">\_iris de transición de imagen de imágenes WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="b4715-105">WMT\_VIDEOIMAGE\_TRANSITION\_IRIS</span></span>

<span data-ttu-id="b4715-106">La transición de iris revela la nueva imagen a lo largo de un eje x y un eje y.</span><span class="sxs-lookup"><span data-stu-id="b4715-106">The iris transition reveals the new image along an x-axis and a y-axis.</span></span> <span data-ttu-id="b4715-107">El efecto visual de esta transición es que la nueva imagen aparece en una cruz de ampliación que llega a todos los lados del marco.</span><span class="sxs-lookup"><span data-stu-id="b4715-107">The visual effect of this transition is that the new image appears in a widening cross reaching to all sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4715-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4715-108">Parameters</span></span>

<span data-ttu-id="b4715-109">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="b4715-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4715-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b4715-110">Parameter</span></span></th>
<th><span data-ttu-id="b4715-111">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="b4715-111">Structure member</span></span></th>
<th><span data-ttu-id="b4715-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4715-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4715-113">Centrar X</span><span class="sxs-lookup"><span data-stu-id="b4715-113">Center X</span></span></td>
<td><span data-ttu-id="b4715-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="b4715-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="b4715-115">Coordenada X, relativa al fotograma de vídeo, del centro del efecto de iris.</span><span class="sxs-lookup"><span data-stu-id="b4715-115">X-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4715-116">Centrar Y</span><span class="sxs-lookup"><span data-stu-id="b4715-116">Center Y</span></span></td>
<td><span data-ttu-id="b4715-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="b4715-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="b4715-118">Coordenada y, en relación con el fotograma de vídeo, del centro del efecto de iris.</span><span class="sxs-lookup"><span data-stu-id="b4715-118">Y-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4715-119">Ancho</span><span class="sxs-lookup"><span data-stu-id="b4715-119">Width</span></span></td>
<td><span data-ttu-id="b4715-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="b4715-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="b4715-121">Ancho de la línea vertical que revela la nueva imagen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b4715-121">Width of the vertical line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4715-122">Alto</span><span class="sxs-lookup"><span data-stu-id="b4715-122">Height</span></span></td>
<td><span data-ttu-id="b4715-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="b4715-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="b4715-124">Alto de la línea horizontal que revela la nueva imagen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b4715-124">Height of the horizontal line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4715-125">Composición</span><span class="sxs-lookup"><span data-stu-id="b4715-125">Composition</span></span></td>
<td><span data-ttu-id="b4715-126"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="b4715-126"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="b4715-127">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="b4715-127">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="b4715-128">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="b4715-128">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="b4715-129">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="b4715-129">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b4715-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4715-130">Requirements</span></span>



| <span data-ttu-id="b4715-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4715-131">Requirement</span></span> | <span data-ttu-id="b4715-132">Value</span><span class="sxs-lookup"><span data-stu-id="b4715-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4715-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4715-133">Header</span></span><br/> | <dl> <span data-ttu-id="b4715-134"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4715-134"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4715-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4715-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4715-136">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="b4715-136">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





