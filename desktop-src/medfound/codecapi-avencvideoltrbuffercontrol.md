---
description: Especifica el número máximo de marcos de referencia a largo plazo (LTR) controlados por la aplicación.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: Propiedad CODECAPI_AVEncVideoLTRBufferControl (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539627"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a><span data-ttu-id="917ca-103">\_Propiedad AVEncVideoLTRBufferControl de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="917ca-103">CODECAPI\_AVEncVideoLTRBufferControl property</span></span>

<span data-ttu-id="917ca-104">Especifica el número máximo de marcos de referencia a largo plazo (LTR) controlados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="917ca-104">Specifies the maximum number of Long Term Reference (LTR) frames controlled by application.</span></span>

## <a name="data-type"></a><span data-ttu-id="917ca-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="917ca-105">Data type</span></span>

<span data-ttu-id="917ca-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="917ca-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="917ca-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="917ca-107">Property GUID</span></span>

<span data-ttu-id="917ca-108">**CODECAPI \_ AVEncVideoLTRBufferControl**</span><span class="sxs-lookup"><span data-stu-id="917ca-108">**CODECAPI\_AVEncVideoLTRBufferControl**</span></span>

## <a name="property-value"></a><span data-ttu-id="917ca-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="917ca-109">Property value</span></span>

<span data-ttu-id="917ca-110">El valor de este control incluye dos campos, donde cada campo tiene 16 bits.</span><span class="sxs-lookup"><span data-stu-id="917ca-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="917ca-111">Value</span><span class="sxs-lookup"><span data-stu-id="917ca-111">Value</span></span></th>
<th><span data-ttu-id="917ca-112">Significado</span><span class="sxs-lookup"><span data-stu-id="917ca-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="917ca-113"><dt><strong>Los primeros bits de campo</strong></dt> <dt>[0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="917ca-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="917ca-114">El número de Marcos LTR controlados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="917ca-114">The number of LTR frames controlled by the application.</span></span><br/> <span data-ttu-id="917ca-115"><strong>Codificadores H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="917ca-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="917ca-116">Suponiendo que el valor es N y N es un valor distinto de cero, en cada fotograma de IDR el codificador debe marcar automáticamente los fotogramas que siguen al fotograma IDR (incluido el fotograma de IDR) como marcos LTR, siempre y cuando se apliquen las 3 siguientes:</span><span class="sxs-lookup"><span data-stu-id="917ca-116">Assuming the value is N and N is non-zero value, at each IDR frame the encoder must automatically mark the frames following the IDR frame (and including the IDR frame) as LTR frames as long as all 3 of the following apply:</span></span>
<ul>
<li><span data-ttu-id="917ca-117">El marco no se ha establecido para que se marque como marco de referencia a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="917ca-117">The frame is not already set to be marked as a long term reference frame.</span></span></li>
<li><span data-ttu-id="917ca-118">El marco es un marco de nivel base.</span><span class="sxs-lookup"><span data-stu-id="917ca-118">The frame is a base layer frame.</span></span> <span data-ttu-id="917ca-119">Por ejemplo, el elemento de sintaxis <strong>temporal_id</strong> igual a 0.</span><span class="sxs-lookup"><span data-stu-id="917ca-119">For example, syntax element <strong>temporal_id</strong> equal to 0.</span></span></li>
<li><span data-ttu-id="917ca-120">El número de fotogramas marcados actualmente como LTR es menor que N.</span><span class="sxs-lookup"><span data-stu-id="917ca-120">The number of frames currently marked as LTR is less than N.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="917ca-121"><dt><strong>Los bits del segundo campo</strong></dt> <dt>[16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="917ca-121"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="917ca-122">El modo de confianza de control LTR.</span><span class="sxs-lookup"><span data-stu-id="917ca-122">The trust mode of LTR control.</span></span><br/> <span data-ttu-id="917ca-123"><strong>Codificadores H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="917ca-123"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="917ca-124">1 (confiar hasta) significa que el codificador puede usar un marco LTR a menos que la aplicación lo invalide explícitamente a través del control <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> .</span><span class="sxs-lookup"><span data-stu-id="917ca-124">1 (Trust Until) means the encoder may use an LTR frame unless the app explicitly invalidates it through the <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> control.</span></span> <br/> <span data-ttu-id="917ca-125">Otros valores no son válidos y se reservan para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="917ca-125">Other values are invalid and reserved for future use.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="917ca-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="917ca-126">Remarks</span></span>

<span data-ttu-id="917ca-127">Se trata de una API estática.</span><span class="sxs-lookup"><span data-stu-id="917ca-127">This is a static API.</span></span>

<span data-ttu-id="917ca-128">El valor predeterminado debe ser 0</span><span class="sxs-lookup"><span data-stu-id="917ca-128">Default value shall be 0</span></span>

## <a name="requirements"></a><span data-ttu-id="917ca-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="917ca-129">Requirements</span></span>



| <span data-ttu-id="917ca-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="917ca-130">Requirement</span></span> | <span data-ttu-id="917ca-131">Value</span><span class="sxs-lookup"><span data-stu-id="917ca-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="917ca-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="917ca-132">Minimum supported client</span></span><br/> | <span data-ttu-id="917ca-133">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="917ca-133">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="917ca-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="917ca-134">Minimum supported server</span></span><br/> | <span data-ttu-id="917ca-135">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="917ca-135">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="917ca-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="917ca-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="917ca-137"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="917ca-137"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="917ca-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="917ca-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917ca-139">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="917ca-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




