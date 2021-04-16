---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl. h)
description: La transición de bajorrelieve revela la nueva imagen en un rectángulo que se origina en una esquina del fotograma.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd41887fafaae2756e2dafe3d57d4f1a86edf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649691"
---
# <a name="wmt_videoimage_transition_inset"></a><span data-ttu-id="23bf8-104">\_bajorrelieve de transición de imagen de videoimágenes WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="23bf8-104">WMT\_VIDEOIMAGE\_TRANSITION\_INSET</span></span>

<span data-ttu-id="23bf8-105">La transición de bajorrelieve revela la nueva imagen en un rectángulo que se origina en una esquina del fotograma.</span><span class="sxs-lookup"><span data-stu-id="23bf8-105">The inset transition reveals the new image in a rectangle originating from one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="23bf8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23bf8-106">Parameters</span></span>

<span data-ttu-id="23bf8-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="23bf8-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23bf8-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="23bf8-108">Parameter</span></span></th>
<th><span data-ttu-id="23bf8-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="23bf8-109">Structure member</span></span></th>
<th><span data-ttu-id="23bf8-110">Description</span><span class="sxs-lookup"><span data-stu-id="23bf8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="23bf8-111">Ancho</span><span class="sxs-lookup"><span data-stu-id="23bf8-111">Width</span></span></td>
<td><span data-ttu-id="23bf8-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="23bf8-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="23bf8-113">Ancho del bajorrelieve en píxeles.</span><span class="sxs-lookup"><span data-stu-id="23bf8-113">Width of the inset in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23bf8-114">Alto</span><span class="sxs-lookup"><span data-stu-id="23bf8-114">Height</span></span></td>
<td><span data-ttu-id="23bf8-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="23bf8-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="23bf8-116">Alto del bajorrelieve en píxeles.</span><span class="sxs-lookup"><span data-stu-id="23bf8-116">Height of the inset in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23bf8-117">Dirección</span><span class="sxs-lookup"><span data-stu-id="23bf8-117">Direction</span></span></td>
<td><span data-ttu-id="23bf8-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="23bf8-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="23bf8-119">Esquina desde la que se origina el bajorrelieve. Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="23bf8-119">Corner from which the inset originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="23bf8-120">0: inferior izquierda</span><span class="sxs-lookup"><span data-stu-id="23bf8-120">0 - Lower left</span></span></li>
<li><span data-ttu-id="23bf8-121">1-inferior derecha</span><span class="sxs-lookup"><span data-stu-id="23bf8-121">1 - Lower right</span></span></li>
<li><span data-ttu-id="23bf8-122">2: parte superior izquierda</span><span class="sxs-lookup"><span data-stu-id="23bf8-122">2 - Upper left</span></span></li>
<li><span data-ttu-id="23bf8-123">3-superior derecha</span><span class="sxs-lookup"><span data-stu-id="23bf8-123">3 - Upper right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23bf8-124">Composición</span><span class="sxs-lookup"><span data-stu-id="23bf8-124">Composition</span></span></td>
<td><span data-ttu-id="23bf8-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="23bf8-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="23bf8-126">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="23bf8-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="23bf8-127">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="23bf8-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="23bf8-128">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="23bf8-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="23bf8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23bf8-129">Requirements</span></span>



| <span data-ttu-id="23bf8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="23bf8-130">Requirement</span></span> | <span data-ttu-id="23bf8-131">Value</span><span class="sxs-lookup"><span data-stu-id="23bf8-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23bf8-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23bf8-132">Header</span></span><br/> | <dl> <span data-ttu-id="23bf8-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="23bf8-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23bf8-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="23bf8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23bf8-135">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="23bf8-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





