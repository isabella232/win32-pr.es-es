---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl. h)
description: La transición diagonal revela la nueva imagen a lo largo de una línea diagonal que se origina en una esquina del fotograma.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690151"
---
# <a name="wmt_videoimage_transition_diagonal"></a><span data-ttu-id="40765-104">DIAGONAL de transición de imagen de videotransmisión WMT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="40765-104">WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL</span></span>

<span data-ttu-id="40765-105">La transición diagonal revela la nueva imagen a lo largo de una línea diagonal que se origina en una esquina del fotograma.</span><span class="sxs-lookup"><span data-stu-id="40765-105">The diagonal transition reveals the new image along a diagonal line originating in one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="40765-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40765-106">Parameters</span></span>

<span data-ttu-id="40765-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="40765-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40765-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="40765-108">Parameter</span></span></th>
<th><span data-ttu-id="40765-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="40765-109">Structure member</span></span></th>
<th><span data-ttu-id="40765-110">Description</span><span class="sxs-lookup"><span data-stu-id="40765-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40765-111">Ancho</span><span class="sxs-lookup"><span data-stu-id="40765-111">Width</span></span></td>
<td><span data-ttu-id="40765-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="40765-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="40765-113">Ancho de la sección diagonal en píxeles.</span><span class="sxs-lookup"><span data-stu-id="40765-113">Width of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40765-114">Alto</span><span class="sxs-lookup"><span data-stu-id="40765-114">Height</span></span></td>
<td><span data-ttu-id="40765-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="40765-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="40765-116">Alto de la sección diagonal en píxeles.</span><span class="sxs-lookup"><span data-stu-id="40765-116">Height of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40765-117">Dirección</span><span class="sxs-lookup"><span data-stu-id="40765-117">Direction</span></span></td>
<td><span data-ttu-id="40765-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="40765-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="40765-119">Determina la esquina desde la que se origina la transición. Establezca en uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="40765-119">Determines the corner from which the transition originates.Set to one of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="40765-120">0: parte superior derecha</span><span class="sxs-lookup"><span data-stu-id="40765-120">0 - Upper right</span></span></li>
<li><span data-ttu-id="40765-121">1: parte superior izquierda</span><span class="sxs-lookup"><span data-stu-id="40765-121">1 - Upper left</span></span></li>
<li><span data-ttu-id="40765-122">2-inferior derecha</span><span class="sxs-lookup"><span data-stu-id="40765-122">2 - Lower right</span></span></li>
<li><span data-ttu-id="40765-123">3-inferior izquierda</span><span class="sxs-lookup"><span data-stu-id="40765-123">3 - Lower left</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40765-124">Composición</span><span class="sxs-lookup"><span data-stu-id="40765-124">Composition</span></span></td>
<td><span data-ttu-id="40765-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="40765-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="40765-126">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="40765-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="40765-127">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="40765-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="40765-128">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="40765-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="40765-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40765-129">Requirements</span></span>



| <span data-ttu-id="40765-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="40765-130">Requirement</span></span> | <span data-ttu-id="40765-131">Value</span><span class="sxs-lookup"><span data-stu-id="40765-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40765-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40765-132">Header</span></span><br/> | <dl> <span data-ttu-id="40765-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="40765-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40765-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="40765-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40765-135">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="40765-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





