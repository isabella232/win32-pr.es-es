---
title: WMT_VIDEOIMAGE_TRANSITION_CIRCLE (Wmsdkidl. h)
description: La transición circular revela la nueva imagen en un círculo.
ms.assetid: ba3bcf46-1254-4aad-a958-0f9ddb2f40dc
keywords:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ccf3a8eff2ca5a5069fa01c4e61bc0735808fd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700376"
---
# <a name="wmt_videoimage_transition_circle"></a><span data-ttu-id="5aa2a-104">Círculo de transición de \_ imagen WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="5aa2a-104">WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE</span></span>

<span data-ttu-id="5aa2a-105">La transición circular revela la nueva imagen en un círculo.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-105">The circle transition reveals the new image in a circle.</span></span>

## <a name="parameters"></a><span data-ttu-id="5aa2a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aa2a-106">Parameters</span></span>

<span data-ttu-id="5aa2a-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5aa2a-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5aa2a-108">Parameter</span></span></th>
<th><span data-ttu-id="5aa2a-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="5aa2a-109">Structure member</span></span></th>
<th><span data-ttu-id="5aa2a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aa2a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5aa2a-111">Centrar X</span><span class="sxs-lookup"><span data-stu-id="5aa2a-111">Center X</span></span></td>
<td><span data-ttu-id="5aa2a-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="5aa2a-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="5aa2a-113">Coordenada X, relativa al fotograma del vídeo, del centro del círculo.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-113">X-coordinate, relative to the video frame, of the center of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5aa2a-114">Centrar Y</span><span class="sxs-lookup"><span data-stu-id="5aa2a-114">Center Y</span></span></td>
<td><span data-ttu-id="5aa2a-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="5aa2a-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="5aa2a-116">Coordenada y, en relación con el fotograma de vídeo, del centro del círculo.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-116">Y-coordinate, relative to the video frame, of center of the circle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5aa2a-117">Radio</span><span class="sxs-lookup"><span data-stu-id="5aa2a-117">Radius</span></span></td>
<td><span data-ttu-id="5aa2a-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="5aa2a-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="5aa2a-119">Radio, en píxeles, del círculo.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-119">Radius, in pixels, of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5aa2a-120">Composición</span><span class="sxs-lookup"><span data-stu-id="5aa2a-120">Composition</span></span></td>
<td><span data-ttu-id="5aa2a-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="5aa2a-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="5aa2a-122">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="5aa2a-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="5aa2a-123">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="5aa2a-124">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="5aa2a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aa2a-125">Requirements</span></span>



| <span data-ttu-id="5aa2a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aa2a-126">Requirement</span></span> | <span data-ttu-id="5aa2a-127">Value</span><span class="sxs-lookup"><span data-stu-id="5aa2a-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa2a-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5aa2a-128">Header</span></span><br/> | <dl> <span data-ttu-id="5aa2a-129"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aa2a-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aa2a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aa2a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa2a-131">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="5aa2a-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





