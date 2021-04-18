---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl. h)
description: La transición Mostrar revela la nueva imagen a lo largo de una línea recta que se origina en un lado del marco.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9aa385912cf106955dd33e06824d0b3668fcd97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650065"
---
# <a name="wmt_videoimage_transition_reveal"></a><span data-ttu-id="e54fd-104">transición de imagen de transmisión de \_ imágenes WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="e54fd-104">WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL</span></span>

<span data-ttu-id="e54fd-105">La transición Mostrar revela la nueva imagen a lo largo de una línea recta que se origina en un lado del marco.</span><span class="sxs-lookup"><span data-stu-id="e54fd-105">The reveal transition reveals the new image along a straight line originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="e54fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e54fd-106">Parameters</span></span>

<span data-ttu-id="e54fd-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="e54fd-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e54fd-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e54fd-108">Parameter</span></span></th>
<th><span data-ttu-id="e54fd-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="e54fd-109">Structure member</span></span></th>
<th><span data-ttu-id="e54fd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e54fd-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e54fd-111">Distancia</span><span class="sxs-lookup"><span data-stu-id="e54fd-111">Distance</span></span></td>
<td><span data-ttu-id="e54fd-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="e54fd-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="e54fd-113">Cantidad de la nueva imagen revelada, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e54fd-113">Amount of the new image revealed, in pixels.</span></span> <span data-ttu-id="e54fd-114">Este valor es relativo al lado de origen del marco.</span><span class="sxs-lookup"><span data-stu-id="e54fd-114">This value is relative to the originating side of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e54fd-115">Dirección</span><span class="sxs-lookup"><span data-stu-id="e54fd-115">Direction</span></span></td>
<td><span data-ttu-id="e54fd-116"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="e54fd-116"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="e54fd-117">Dirección de la revelación. Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="e54fd-117">Direction of the revealing.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="e54fd-118">0: mostrar a la derecha; se origina desde el lado izquierdo del marco.</span><span class="sxs-lookup"><span data-stu-id="e54fd-118">0 - Reveal to the right; originate from the left side of the frame.</span></span></li>
<li><span data-ttu-id="e54fd-119">1: mostrar a la izquierda; se origina desde el lado derecho del marco.</span><span class="sxs-lookup"><span data-stu-id="e54fd-119">1 - Reveal to the left; originate from the right side of the frame.</span></span></li>
<li><span data-ttu-id="e54fd-120">2-revelar hacia arriba; se origina desde la parte inferior del marco.</span><span class="sxs-lookup"><span data-stu-id="e54fd-120">2 - Reveal upward; originate from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="e54fd-121">3-revelar hacia abajo; se origina desde la parte superior del marco.</span><span class="sxs-lookup"><span data-stu-id="e54fd-121">3 - Reveal downward; originate from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e54fd-122">Composición</span><span class="sxs-lookup"><span data-stu-id="e54fd-122">Composition</span></span></td>
<td><span data-ttu-id="e54fd-123"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="e54fd-123"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="e54fd-124">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="e54fd-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="e54fd-125">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="e54fd-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="e54fd-126">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="e54fd-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="e54fd-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e54fd-127">Requirements</span></span>



| <span data-ttu-id="e54fd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e54fd-128">Requirement</span></span> | <span data-ttu-id="e54fd-129">Value</span><span class="sxs-lookup"><span data-stu-id="e54fd-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e54fd-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e54fd-130">Header</span></span><br/> | <dl> <span data-ttu-id="e54fd-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e54fd-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e54fd-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e54fd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54fd-133">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="e54fd-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





