---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Wmsdkidl. h)
description: La transición de V rellenada revela la nueva imagen en un triángulo que se origina en un lado del marco.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe229657dfd29d3cb9d83a8a4853e2e89a7a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698662"
---
# <a name="wmt_videoimage_transition_filled_v"></a><span data-ttu-id="78a9b-104">\_transición de imagen de vídeo WMT \_ \_ rellenado \_ V</span><span class="sxs-lookup"><span data-stu-id="78a9b-104">WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V</span></span>

<span data-ttu-id="78a9b-105">La transición de V rellenada revela la nueva imagen en un triángulo que se origina en un lado del marco.</span><span class="sxs-lookup"><span data-stu-id="78a9b-105">The filled V transition reveals the new image in a triangle originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="78a9b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78a9b-106">Parameters</span></span>

<span data-ttu-id="78a9b-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="78a9b-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78a9b-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="78a9b-108">Parameter</span></span></th>
<th><span data-ttu-id="78a9b-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="78a9b-109">Structure member</span></span></th>
<th><span data-ttu-id="78a9b-110">Description</span><span class="sxs-lookup"><span data-stu-id="78a9b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="78a9b-111">Ancho</span><span class="sxs-lookup"><span data-stu-id="78a9b-111">Width</span></span></td>
<td><span data-ttu-id="78a9b-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="78a9b-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="78a9b-113">Ancho de la V rellena en píxeles.</span><span class="sxs-lookup"><span data-stu-id="78a9b-113">Width of the filled V in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78a9b-114">Alto</span><span class="sxs-lookup"><span data-stu-id="78a9b-114">Height</span></span></td>
<td><span data-ttu-id="78a9b-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="78a9b-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="78a9b-116">Alto de la V rellena en píxeles.</span><span class="sxs-lookup"><span data-stu-id="78a9b-116">Height of the filled V in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78a9b-117">Dirección</span><span class="sxs-lookup"><span data-stu-id="78a9b-117">Direction</span></span></td>
<td><span data-ttu-id="78a9b-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="78a9b-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="78a9b-119">Dirección desde la que se origina la V rellenada. Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="78a9b-119">Direction from which the filled V originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="78a9b-120">0: escribe desde el lado izquierdo del marco.</span><span class="sxs-lookup"><span data-stu-id="78a9b-120">0 - Enters from the left side of the frame.</span></span></li>
<li><span data-ttu-id="78a9b-121">1: escribe desde el lado derecho del marco.</span><span class="sxs-lookup"><span data-stu-id="78a9b-121">1 - Enters from the right side of the frame.</span></span></li>
<li><span data-ttu-id="78a9b-122">2-escribe desde la parte inferior del marco.</span><span class="sxs-lookup"><span data-stu-id="78a9b-122">2 - Enters from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="78a9b-123">3-escribe desde la parte superior del marco.</span><span class="sxs-lookup"><span data-stu-id="78a9b-123">3 - Enters from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78a9b-124">Composición</span><span class="sxs-lookup"><span data-stu-id="78a9b-124">Composition</span></span></td>
<td><span data-ttu-id="78a9b-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="78a9b-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="78a9b-126">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="78a9b-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="78a9b-127">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="78a9b-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="78a9b-128">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="78a9b-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="78a9b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78a9b-129">Requirements</span></span>



| <span data-ttu-id="78a9b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="78a9b-130">Requirement</span></span> | <span data-ttu-id="78a9b-131">Value</span><span class="sxs-lookup"><span data-stu-id="78a9b-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78a9b-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78a9b-132">Header</span></span><br/> | <dl> <span data-ttu-id="78a9b-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="78a9b-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78a9b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="78a9b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a9b-135">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="78a9b-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





