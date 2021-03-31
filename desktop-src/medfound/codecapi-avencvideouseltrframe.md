---
description: Especifica que el marco actual está codificado con uno o varios marcos LTR.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: Propiedad CODECAPI_AVEncVideoUseLTRFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252933180e8212c94c3c2b2442397c53d0f9c559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808167"
---
# <a name="codecapi_avencvideouseltrframe-property"></a><span data-ttu-id="69fb0-103">\_Propiedad AVEncVideoUseLTRFrame de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="69fb0-103">CODECAPI\_AVEncVideoUseLTRFrame property</span></span>

<span data-ttu-id="69fb0-104">Especifica que el marco actual está codificado con uno o varios marcos LTR.</span><span class="sxs-lookup"><span data-stu-id="69fb0-104">Specifies that the current frame is encoded using one or multiple LTR frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="69fb0-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="69fb0-105">Data type</span></span>

<span data-ttu-id="69fb0-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="69fb0-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="69fb0-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="69fb0-107">Property GUID</span></span>

<span data-ttu-id="69fb0-108">**CODECAPI \_ AVEncVideoUseLTRFrame**</span><span class="sxs-lookup"><span data-stu-id="69fb0-108">**CODECAPI\_AVEncVideoUseLTRFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="69fb0-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="69fb0-109">Property value</span></span>

<span data-ttu-id="69fb0-110">El valor de este control incluye dos campos, donde cada campo tiene 16 bits.</span><span class="sxs-lookup"><span data-stu-id="69fb0-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69fb0-111">Value</span><span class="sxs-lookup"><span data-stu-id="69fb0-111">Value</span></span></th>
<th><span data-ttu-id="69fb0-112">Significado</span><span class="sxs-lookup"><span data-stu-id="69fb0-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="69fb0-113"><dt><strong>Los primeros bits de campo</strong></dt> <dt>[0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="69fb0-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="69fb0-114">Indica qué Marcos LTR están permitidos para codificar el marco actual.</span><span class="sxs-lookup"><span data-stu-id="69fb0-114">Indicates which LTR frame(s) are allowed for encoding the current frame.</span></span> <br/> <span data-ttu-id="69fb0-115"><strong>Codificadores H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="69fb0-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="69fb0-116">Se trata de un mapa de bits que indica qué marcos de LTR se pueden usar como referencia para este marco.</span><span class="sxs-lookup"><span data-stu-id="69fb0-116">This is a bitmap that indicates which LTR frames can be used as a reference for this frame.</span></span> <span data-ttu-id="69fb0-117">El bit menos significativo corresponde al índice 0 LTR, el segundo bit menos significativo corresponde al índice 1, etc.</span><span class="sxs-lookup"><span data-stu-id="69fb0-117">The least significant bit corresponds to LTR index 0, the second least significant bit corresponds to LTR index 1, etc.</span></span><br/> <span data-ttu-id="69fb0-118">Este valor no debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="69fb0-118">This value shall not be 0.</span></span><br/> <span data-ttu-id="69fb0-119">El índice más alto especificado por este valor no debe ser mayor que el número máximo de Marcos LTR especificado en la propiedad <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> menos uno.</span><span class="sxs-lookup"><span data-stu-id="69fb0-119">The highest index specified by this value shall not be greater than the maximum number of LTR frames specified in the <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> property less one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="69fb0-120"><dt><strong>Los bits del segundo campo</strong></dt> <dt>[16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="69fb0-120"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="69fb0-121">Marca que indica si se requieren limitaciones adicionales para codificar fotogramas posteriores.</span><span class="sxs-lookup"><span data-stu-id="69fb0-121">Flag that indicates whether additional limitations are required for encoding subsequent frames.</span></span> <br/> <span data-ttu-id="69fb0-122"><strong>Codificadores H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="69fb0-122"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="69fb0-123">1 está en el único valor válido para este campo.</span><span class="sxs-lookup"><span data-stu-id="69fb0-123">1 is on the only valid value for this field.</span></span> <span data-ttu-id="69fb0-124">Todos los demás valores no son válidos y se reservan para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="69fb0-124">All other values are invalid and reserved for future use.</span></span><br/> <span data-ttu-id="69fb0-125">Cuando la marca es 1, el codificador debe codificar los fotogramas posteriores en el orden de codificación de acuerdo con las restricciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="69fb0-125">When the flag is 1, the encoder shall encode subsequent frames in encoding order subject to the following constraints:</span></span><br/>
<ul>
<li><span data-ttu-id="69fb0-126">No debe utilizar fotogramas de referencia a corto plazo en el orden de codificación anterior al marco actual o la codificación futura en el orden de codificación.</span><span class="sxs-lookup"><span data-stu-id="69fb0-126">It shall not use short term reference frames in encoding order older than the current frame or future encoding in encoding order.</span></span></li>
<li><span data-ttu-id="69fb0-127">No debe usar marcos LTR no descritos por el control CODECAPI_AVEncVideoUseLTRFrame más reciente.</span><span class="sxs-lookup"><span data-stu-id="69fb0-127">It shall not use LTR frames not described by the most recent CODECAPI_AVEncVideoUseLTRFrame control.</span></span></li>
<li><span data-ttu-id="69fb0-128">Puede usar marcos LTR actualizados después del fotograma actual.</span><span class="sxs-lookup"><span data-stu-id="69fb0-128">It may use LTR frames updated after the current frame.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="69fb0-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69fb0-129">Remarks</span></span>

<span data-ttu-id="69fb0-130">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="69fb0-130">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="69fb0-131">No se debe llamar a esta propiedad si se ha emitido una llamada pendiente para usar un marco LTR mediante la \_ propiedad CODECAPI AVEncVideoUseLTRFrame y el codificador aún no ha generado un fotograma que ha usado LTR.</span><span class="sxs-lookup"><span data-stu-id="69fb0-131">This property should not be called if a pending call to use an LTR frame has been issued using the CODECAPI\_AVEncVideoUseLTRFrame property and the encoder has not yet generated a frame that has used the LTR.</span></span> <span data-ttu-id="69fb0-132">En otras palabras, el codificador no debe poner en cola \_ las solicitudes de CODECAPI AVEncVideoUseLTRFrame.</span><span class="sxs-lookup"><span data-stu-id="69fb0-132">In other words, the encoder should not queue up CODECAPI\_AVEncVideoUseLTRFrame requests.</span></span>

<span data-ttu-id="69fb0-133">Si \_ se envía una solicitud AVEncVideoUseLTRFrame de CODECAPI mientras otra \_ solicitud AVENCVIDEOUSELTRFRAME de CODECAPI está pendiente, se debe quitar la solicitud anterior.</span><span class="sxs-lookup"><span data-stu-id="69fb0-133">If a CODECAPI\_AVEncVideoUseLTRFrame request is submitted while another CODECAPI\_AVEncVideoUseLTRFrame request is still pending, then the older request should be dropped.</span></span>

<span data-ttu-id="69fb0-134">Llamar a CODECAPI \_ AVEncVideoUseLTRFrame en un marco de capa no base es válido y se aplicará al fotograma de capa no base, sin retrasar a un fotograma Base de la capa.</span><span class="sxs-lookup"><span data-stu-id="69fb0-134">Calling CODECAPI\_AVEncVideoUseLTRFrame on a non-base layer frame is valid and shall apply to the non-base layer frame, without delay to a base layer frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="69fb0-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69fb0-135">Requirements</span></span>



| <span data-ttu-id="69fb0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="69fb0-136">Requirement</span></span> | <span data-ttu-id="69fb0-137">Value</span><span class="sxs-lookup"><span data-stu-id="69fb0-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69fb0-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69fb0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="69fb0-139">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="69fb0-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="69fb0-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69fb0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="69fb0-141">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="69fb0-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="69fb0-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69fb0-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="69fb0-143"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="69fb0-143"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69fb0-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="69fb0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69fb0-145">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69fb0-145">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




