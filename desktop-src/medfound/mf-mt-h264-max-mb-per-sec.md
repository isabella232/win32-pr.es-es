---
description: Especifica la velocidad de procesamiento máxima de adaptativo macrobloque para una secuencia de vídeo H. 264.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: MF_MT_H264_MAX_MB_PER_SEC atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b53bdbabd9a633464ed388f2309627b69413c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696752"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a><span data-ttu-id="cefd2-103">\_Atributo MF MT \_ H264 \_ Max \_ MB \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="cefd2-103">MF\_MT\_H264\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="cefd2-104">Especifica la velocidad de procesamiento máxima de adaptativo macrobloque para una secuencia de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="cefd2-104">Specifies the maximum macroblock processing rate for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="cefd2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="cefd2-105">Data type</span></span>

<span data-ttu-id="cefd2-106">**\[ UINT32 \]** almacenado como **UINT8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="cefd2-106">**UINT32\[\]** stored as **UINT8\[\]**</span></span>

## <a name="applies-to"></a><span data-ttu-id="cefd2-107">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="cefd2-107">Applies to</span></span>

[<span data-ttu-id="cefd2-108">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="cefd2-108">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="cefd2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cefd2-109">Remarks</span></span>

<span data-ttu-id="cefd2-110">Este atributo se aplica a los tipos de medios para flujos H. 264 transmitidos a través de USB.</span><span class="sxs-lookup"><span data-stu-id="cefd2-110">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="cefd2-111">El valor del atributo es una matriz de valores UINT32, que corresponden a los siguientes campos del descriptor de formato de vídeo UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="cefd2-111">The value of the attribute is an array of UINT32 values, which correspond to the following fields in the UVC 1.5 H.264 video format descriptor.</span></span>

| <span data-ttu-id="cefd2-112">Elemento de matriz</span><span class="sxs-lookup"><span data-stu-id="cefd2-112">Array Element</span></span> | <span data-ttu-id="cefd2-113">Campo descriptor</span><span class="sxs-lookup"><span data-stu-id="cefd2-113">Descriptor Field</span></span>                                           |
|---------------|------------------------------------------------------------|
| <span data-ttu-id="cefd2-114">0</span><span class="sxs-lookup"><span data-stu-id="cefd2-114">0</span></span>             | <span data-ttu-id="cefd2-115">**dwMaxMBperSecOneResolutionNoScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-115">**dwMaxMBperSecOneResolutionNoScalability**</span></span>                |
| <span data-ttu-id="cefd2-116">1</span><span class="sxs-lookup"><span data-stu-id="cefd2-116">1</span></span>             | <span data-ttu-id="cefd2-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span></span>               |
| <span data-ttu-id="cefd2-118">2</span><span class="sxs-lookup"><span data-stu-id="cefd2-118">2</span></span>             | <span data-ttu-id="cefd2-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span></span>             |
| <span data-ttu-id="cefd2-120">3</span><span class="sxs-lookup"><span data-stu-id="cefd2-120">3</span></span>             | <span data-ttu-id="cefd2-121">**dwMaxMBperSecFourResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-121">**dwMaxMBperSecFourResolutionsNoScalability**</span></span>              |
| <span data-ttu-id="cefd2-122">4</span><span class="sxs-lookup"><span data-stu-id="cefd2-122">4</span></span>             | <span data-ttu-id="cefd2-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span></span>          |
| <span data-ttu-id="cefd2-124">5</span><span class="sxs-lookup"><span data-stu-id="cefd2-124">5</span></span>             | <span data-ttu-id="cefd2-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span><span class="sxs-lookup"><span data-stu-id="cefd2-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span></span>        |
| <span data-ttu-id="cefd2-126">6</span><span class="sxs-lookup"><span data-stu-id="cefd2-126">6</span></span>             | <span data-ttu-id="cefd2-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span></span>       |
| <span data-ttu-id="cefd2-128">7</span><span class="sxs-lookup"><span data-stu-id="cefd2-128">7</span></span>             | <span data-ttu-id="cefd2-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span></span>        |
| <span data-ttu-id="cefd2-130">8</span><span class="sxs-lookup"><span data-stu-id="cefd2-130">8</span></span>             | <span data-ttu-id="cefd2-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span></span>   |
| <span data-ttu-id="cefd2-132">9</span><span class="sxs-lookup"><span data-stu-id="cefd2-132">9</span></span>             | <span data-ttu-id="cefd2-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span></span>  |
| <span data-ttu-id="cefd2-134">10</span><span class="sxs-lookup"><span data-stu-id="cefd2-134">10</span></span>            | <span data-ttu-id="cefd2-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span><span class="sxs-lookup"><span data-stu-id="cefd2-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span></span> |
| <span data-ttu-id="cefd2-136">11</span><span class="sxs-lookup"><span data-stu-id="cefd2-136">11</span></span>            | <span data-ttu-id="cefd2-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span></span> |
| <span data-ttu-id="cefd2-138">12</span><span class="sxs-lookup"><span data-stu-id="cefd2-138">12</span></span>            | <span data-ttu-id="cefd2-139">**dwMaxMBperSecOneResolutionFullScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-139">**dwMaxMBperSecOneResolutionFullScalability**</span></span>              |
| <span data-ttu-id="cefd2-140">13</span><span class="sxs-lookup"><span data-stu-id="cefd2-140">13</span></span>            | <span data-ttu-id="cefd2-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span></span>             |
| <span data-ttu-id="cefd2-142">14</span><span class="sxs-lookup"><span data-stu-id="cefd2-142">14</span></span>            | <span data-ttu-id="cefd2-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span></span>           |
| <span data-ttu-id="cefd2-144">15</span><span class="sxs-lookup"><span data-stu-id="cefd2-144">15</span></span>            | <span data-ttu-id="cefd2-145">**dwMaxMBperSecFourResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="cefd2-145">**dwMaxMBperSecFourResolutionsFullScalability**</span></span>            |



 

<span data-ttu-id="cefd2-146">Este atributo también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="cefd2-146">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cefd2-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cefd2-147">Requirements</span></span>



| <span data-ttu-id="cefd2-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="cefd2-148">Requirement</span></span> | <span data-ttu-id="cefd2-149">Value</span><span class="sxs-lookup"><span data-stu-id="cefd2-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cefd2-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cefd2-150">Minimum supported client</span></span><br/> | <span data-ttu-id="cefd2-151">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="cefd2-151">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="cefd2-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cefd2-152">Minimum supported server</span></span><br/> | <span data-ttu-id="cefd2-153">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="cefd2-153">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="cefd2-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cefd2-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="cefd2-155"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cefd2-155"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cefd2-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="cefd2-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cefd2-157">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cefd2-157">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cefd2-158">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="cefd2-158">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




