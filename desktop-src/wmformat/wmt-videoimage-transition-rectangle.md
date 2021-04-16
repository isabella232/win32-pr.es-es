---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Wmsdkidl. h)
description: La transición de rectángulo revela la nueva imagen en un rectángulo dentro del marco.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdcc5e5b074a07cee13a9af7f7a0f8c0f629de0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709066"
---
# <a name="wmt_videoimage_transition_rectangle"></a><span data-ttu-id="6af4e-104">\_rectángulo de transición de imagen de videoimágenes WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="6af4e-104">WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE</span></span>

<span data-ttu-id="6af4e-105">La transición de rectángulo revela la nueva imagen en un rectángulo dentro del marco.</span><span class="sxs-lookup"><span data-stu-id="6af4e-105">The rectangle transition reveals the new image in a rectangle within the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="6af4e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6af4e-106">Parameters</span></span>

<span data-ttu-id="6af4e-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="6af4e-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6af4e-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6af4e-108">Parameter</span></span></th>
<th><span data-ttu-id="6af4e-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="6af4e-109">Structure member</span></span></th>
<th><span data-ttu-id="6af4e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6af4e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6af4e-111">Centrar X</span><span class="sxs-lookup"><span data-stu-id="6af4e-111">Center X</span></span></td>
<td><span data-ttu-id="6af4e-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="6af4e-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="6af4e-113">Coordenada X, relativa al fotograma de vídeo, del centro del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="6af4e-113">X-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6af4e-114">Centrar Y</span><span class="sxs-lookup"><span data-stu-id="6af4e-114">Center Y</span></span></td>
<td><span data-ttu-id="6af4e-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="6af4e-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="6af4e-116">Coordenada y, en relación con el fotograma de vídeo, del centro del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="6af4e-116">Y-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6af4e-117">Ancho</span><span class="sxs-lookup"><span data-stu-id="6af4e-117">Width</span></span></td>
<td><span data-ttu-id="6af4e-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="6af4e-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="6af4e-119">Ancho del rectángulo en píxeles.</span><span class="sxs-lookup"><span data-stu-id="6af4e-119">Width of the rectangle in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6af4e-120">Alto</span><span class="sxs-lookup"><span data-stu-id="6af4e-120">Height</span></span></td>
<td><span data-ttu-id="6af4e-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="6af4e-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="6af4e-122">Alto del rectángulo en píxeles.</span><span class="sxs-lookup"><span data-stu-id="6af4e-122">Height of the rectangle in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6af4e-123">Composición</span><span class="sxs-lookup"><span data-stu-id="6af4e-123">Composition</span></span></td>
<td><span data-ttu-id="6af4e-124"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="6af4e-124"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="6af4e-125">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="6af4e-125">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="6af4e-126">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="6af4e-126">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="6af4e-127">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="6af4e-127">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="6af4e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6af4e-128">Requirements</span></span>



| <span data-ttu-id="6af4e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6af4e-129">Requirement</span></span> | <span data-ttu-id="6af4e-130">Value</span><span class="sxs-lookup"><span data-stu-id="6af4e-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6af4e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6af4e-131">Header</span></span><br/> | <dl> <span data-ttu-id="6af4e-132"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6af4e-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6af4e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6af4e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af4e-134">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="6af4e-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





