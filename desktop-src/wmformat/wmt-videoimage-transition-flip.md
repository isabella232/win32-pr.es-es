---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl. h)
description: La transición de volteo gira la imagen anterior en un eje y a través del centro del marco. La nueva imagen se revela como la parte posterior de la imagen anterior.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc92ad1dfffd945b89293dd9207289aa47645d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650188"
---
# <a name="wmt_videoimage_transition_flip"></a><span data-ttu-id="4235f-105">\_volteo de transición de imagen de videoimágenes WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="4235f-105">WMT\_VIDEOIMAGE\_TRANSITION\_FLIP</span></span>

<span data-ttu-id="4235f-106">La transición de volteo gira la imagen anterior en un eje y a través del centro del marco.</span><span class="sxs-lookup"><span data-stu-id="4235f-106">The flip transition rotates the old image on a y-axis through the center of the frame.</span></span> <span data-ttu-id="4235f-107">La nueva imagen se revela como la parte posterior de la imagen anterior.</span><span class="sxs-lookup"><span data-stu-id="4235f-107">The new image is revealed as the back of the old image.</span></span>

## <a name="parameters"></a><span data-ttu-id="4235f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4235f-108">Parameters</span></span>

<span data-ttu-id="4235f-109">En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.</span><span class="sxs-lookup"><span data-stu-id="4235f-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4235f-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4235f-110">Parameter</span></span></th>
<th><span data-ttu-id="4235f-111">Miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="4235f-111">Structure member</span></span></th>
<th><span data-ttu-id="4235f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4235f-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4235f-113">Ángulo</span><span class="sxs-lookup"><span data-stu-id="4235f-113">Angle</span></span></td>
<td><span data-ttu-id="4235f-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="4235f-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="4235f-115">Ángulo de rotación, de 0,0 a 180,0 grados.</span><span class="sxs-lookup"><span data-stu-id="4235f-115">Angle of the rotation, from 0.0 to 180.0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4235f-116">Composición</span><span class="sxs-lookup"><span data-stu-id="4235f-116">Composition</span></span></td>
<td><span data-ttu-id="4235f-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="4235f-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="4235f-118">Establezca en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="4235f-118">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="4235f-119">0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="4235f-119">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="4235f-120">1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</span><span class="sxs-lookup"><span data-stu-id="4235f-120">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="4235f-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4235f-121">Remarks</span></span>

<span data-ttu-id="4235f-122">Puede visualizar el efecto de esta transición como si ambas imágenes fueran fotografías físicas Unidas juntas hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="4235f-122">You can visualize the effect of this transition as if both images were physical photographs glued together back-to-back.</span></span> <span data-ttu-id="4235f-123">La transición tiene el mismo efecto que contener dos fotografías de este tipo en el centro del borde inferior y girarlas 180 grados.</span><span class="sxs-lookup"><span data-stu-id="4235f-123">The transition has the same effect as holding two such photographs at the center of the bottom edge and rotating them 180 degrees.</span></span>

## <a name="requirements"></a><span data-ttu-id="4235f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4235f-124">Requirements</span></span>



| <span data-ttu-id="4235f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4235f-125">Requirement</span></span> | <span data-ttu-id="4235f-126">Value</span><span class="sxs-lookup"><span data-stu-id="4235f-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4235f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4235f-127">Header</span></span><br/> | <dl> <span data-ttu-id="4235f-128"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4235f-128"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4235f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4235f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4235f-130">**Transiciones de imagen de vídeo**</span><span class="sxs-lookup"><span data-stu-id="4235f-130">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





