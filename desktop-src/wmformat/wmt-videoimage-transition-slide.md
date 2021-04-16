---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl. h)
description: La transición de diapositivas revela la nueva imagen deslizando la imagen antigua fuera del marco.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649791"
---
# <a name="wmt_videoimage_transition_slide"></a><span data-ttu-id="dd0cf-104">diapositiva de transición de \_ imagen WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="dd0cf-104">WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE</span></span>

<span data-ttu-id="dd0cf-105">La transición de diapositivas revela la nueva imagen deslizando la imagen antigua fuera del marco.</span><span class="sxs-lookup"><span data-stu-id="dd0cf-105">The slide transition reveals the new image by sliding the old image out of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd0cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd0cf-106">Parameters</span></span>

<span data-ttu-id="dd0cf-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="dd0cf-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd0cf-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dd0cf-108">Parameter</span></span></th>
<th><span data-ttu-id="dd0cf-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="dd0cf-109">Structure member</span></span></th>
<th><span data-ttu-id="dd0cf-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd0cf-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd0cf-111">Distancia</span><span class="sxs-lookup"><span data-stu-id="dd0cf-111">Distance</span></span></td>
<td><span data-ttu-id="dd0cf-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="dd0cf-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="dd0cf-113">Distancia, en píxeles, que la imagen antigua desliza fuera del marco.</span><span class="sxs-lookup"><span data-stu-id="dd0cf-113">Distance, in pixels, that the old image slides out of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd0cf-114">Dirección</span><span class="sxs-lookup"><span data-stu-id="dd0cf-114">Direction</span></span></td>
<td><span data-ttu-id="dd0cf-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="dd0cf-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="dd0cf-116">Dirección en la que se desplaza la imagen anterior. Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="dd0cf-116">Direction in which the old image slides.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="dd0cf-117">0: diapositiva a la derecha.</span><span class="sxs-lookup"><span data-stu-id="dd0cf-117">0 - Slide to the right.</span></span></li>
<li><span data-ttu-id="dd0cf-118">1: Deslice hacia la izquierda.</span><span class="sxs-lookup"><span data-stu-id="dd0cf-118">1 - Slide to the left.</span></span></li>
<li><span data-ttu-id="dd0cf-119">2-deslizar hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="dd0cf-119">2 - Slide upward.</span></span></li>
<li><span data-ttu-id="dd0cf-120">3-deslizar hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="dd0cf-120">3 - Slide downward.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd0cf-121">Composición</span><span class="sxs-lookup"><span data-stu-id="dd0cf-121">Composition</span></span></td>
<td><span data-ttu-id="dd0cf-122"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="dd0cf-122"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="dd0cf-123">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="dd0cf-123">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="dd0cf-124">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="dd0cf-124">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="dd0cf-125">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="dd0cf-125">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="dd0cf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd0cf-126">Requirements</span></span>



| <span data-ttu-id="dd0cf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd0cf-127">Requirement</span></span> | <span data-ttu-id="dd0cf-128">Value</span><span class="sxs-lookup"><span data-stu-id="dd0cf-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0cf-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd0cf-129">Header</span></span><br/> | <dl> <span data-ttu-id="dd0cf-130"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd0cf-130"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd0cf-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd0cf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd0cf-132">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="dd0cf-132">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





