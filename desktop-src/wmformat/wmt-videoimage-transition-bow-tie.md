---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl. h)
description: La transición de lazo revela la nueva imagen en un conjunto de triángulos en lados opuestos del marco.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd4d426c335a30853085a2501206ccd6e7efc7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678953"
---
# <a name="wmt_videoimage_transition_bow_tie"></a><span data-ttu-id="cec5b-104">\_ \_ vinculación de lazo de transición de imagen WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="cec5b-104">WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE</span></span>

<span data-ttu-id="cec5b-105">La transición de lazo revela la nueva imagen en un conjunto de triángulos en lados opuestos del marco.</span><span class="sxs-lookup"><span data-stu-id="cec5b-105">The bow tie transition reveals the new image in a set of triangles on opposite sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="cec5b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cec5b-106">Parameters</span></span>

<span data-ttu-id="cec5b-107">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="cec5b-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cec5b-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="cec5b-108">Parameter</span></span></th>
<th><span data-ttu-id="cec5b-109">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="cec5b-109">Structure member</span></span></th>
<th><span data-ttu-id="cec5b-110">Description</span><span class="sxs-lookup"><span data-stu-id="cec5b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cec5b-111">Ancho</span><span class="sxs-lookup"><span data-stu-id="cec5b-111">Width</span></span></td>
<td><span data-ttu-id="cec5b-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="cec5b-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="cec5b-113">Ancho de cada lado triangular del empate.</span><span class="sxs-lookup"><span data-stu-id="cec5b-113">Width of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cec5b-114">Alto</span><span class="sxs-lookup"><span data-stu-id="cec5b-114">Height</span></span></td>
<td><span data-ttu-id="cec5b-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="cec5b-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="cec5b-116">Alto de cada lado triangular del empate.</span><span class="sxs-lookup"><span data-stu-id="cec5b-116">Height of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cec5b-117">Dirección</span><span class="sxs-lookup"><span data-stu-id="cec5b-117">Direction</span></span></td>
<td><span data-ttu-id="cec5b-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="cec5b-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="cec5b-119">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="cec5b-119">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="cec5b-120">0: especifica el efecto de empate horizontal, en el que los triángulos entran en los lados derecho e izquierdo del marco.</span><span class="sxs-lookup"><span data-stu-id="cec5b-120">0 - Specifies horizontal bow tie effect, in which the triangles enter from the right and left sides of the frame.</span></span></li>
<li><span data-ttu-id="cec5b-121">1: especifica el efecto de empate vertical, en el que los triángulos entran en la parte superior e inferior del marco.</span><span class="sxs-lookup"><span data-stu-id="cec5b-121">1 - Specifies vertical bow tie effect, in which the triangles enter from the top and bottom of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cec5b-122">Composición</span><span class="sxs-lookup"><span data-stu-id="cec5b-122">Composition</span></span></td>
<td><span data-ttu-id="cec5b-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="cec5b-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="cec5b-124">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="cec5b-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="cec5b-125">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="cec5b-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="cec5b-126">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="cec5b-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="cec5b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cec5b-127">Requirements</span></span>



| <span data-ttu-id="cec5b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cec5b-128">Requirement</span></span> | <span data-ttu-id="cec5b-129">Value</span><span class="sxs-lookup"><span data-stu-id="cec5b-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cec5b-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cec5b-130">Header</span></span><br/> | <dl> <span data-ttu-id="cec5b-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cec5b-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec5b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="cec5b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec5b-133">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="cec5b-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





