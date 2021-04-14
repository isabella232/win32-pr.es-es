---
description: Convierte un flujo de vídeo entre formatos de color.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Convertidor de colores DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496834"
---
# <a name="color-converter-dsp"></a><span data-ttu-id="9327c-103">DSP de convertidor de colores</span><span class="sxs-lookup"><span data-stu-id="9327c-103">Color Converter DSP</span></span>

<span data-ttu-id="9327c-104">Convierte un flujo de vídeo entre formatos de color.</span><span class="sxs-lookup"><span data-stu-id="9327c-104">Converts a video stream between color formats.</span></span>

## <a name="clsid"></a><span data-ttu-id="9327c-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="9327c-105">CLSID</span></span>

<span data-ttu-id="9327c-106">CLSID \_ CColorConvertDMO</span><span class="sxs-lookup"><span data-stu-id="9327c-106">CLSID\_CColorConvertDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="9327c-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="9327c-107">Interfaces</span></span>

-   [<span data-ttu-id="9327c-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="9327c-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="9327c-109">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="9327c-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="9327c-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="9327c-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="9327c-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="9327c-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="9327c-112">IWMColorConvProps</span><span class="sxs-lookup"><span data-stu-id="9327c-112">IWMColorConvProps</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a><span data-ttu-id="9327c-113">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="9327c-113">Input Formats</span></span>

-   <span data-ttu-id="9327c-114">RGB 24</span><span class="sxs-lookup"><span data-stu-id="9327c-114">RGB 24</span></span>
-   <span data-ttu-id="9327c-115">RGB 32</span><span class="sxs-lookup"><span data-stu-id="9327c-115">RGB 32</span></span>
-   <span data-ttu-id="9327c-116">RGB 555</span><span class="sxs-lookup"><span data-stu-id="9327c-116">RGB 555</span></span>
-   <span data-ttu-id="9327c-117">RGB 565</span><span class="sxs-lookup"><span data-stu-id="9327c-117">RGB 565</span></span>
-   <span data-ttu-id="9327c-118">RGB 8</span><span class="sxs-lookup"><span data-stu-id="9327c-118">RGB 8</span></span>
-   <span data-ttu-id="9327c-119">AYUV</span><span class="sxs-lookup"><span data-stu-id="9327c-119">AYUV</span></span>
-   <span data-ttu-id="9327c-120">I420</span><span class="sxs-lookup"><span data-stu-id="9327c-120">I420</span></span>
-   <span data-ttu-id="9327c-121">IYUV</span><span class="sxs-lookup"><span data-stu-id="9327c-121">IYUV</span></span>
-   <span data-ttu-id="9327c-122">NV11</span><span class="sxs-lookup"><span data-stu-id="9327c-122">NV11</span></span>
-   <span data-ttu-id="9327c-123">NV12</span><span class="sxs-lookup"><span data-stu-id="9327c-123">NV12</span></span>
-   <span data-ttu-id="9327c-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="9327c-124">UYVY</span></span>
-   <span data-ttu-id="9327c-125">V216</span><span class="sxs-lookup"><span data-stu-id="9327c-125">V216</span></span>
-   <span data-ttu-id="9327c-126">V410</span><span class="sxs-lookup"><span data-stu-id="9327c-126">V410</span></span>
-   <span data-ttu-id="9327c-127">Y41P</span><span class="sxs-lookup"><span data-stu-id="9327c-127">Y41P</span></span>
-   <span data-ttu-id="9327c-128">Y41T</span><span class="sxs-lookup"><span data-stu-id="9327c-128">Y41T</span></span>
-   <span data-ttu-id="9327c-129">Y42T</span><span class="sxs-lookup"><span data-stu-id="9327c-129">Y42T</span></span>
-   <span data-ttu-id="9327c-130">YUY2</span><span class="sxs-lookup"><span data-stu-id="9327c-130">YUY2</span></span>
-   <span data-ttu-id="9327c-131">YV12</span><span class="sxs-lookup"><span data-stu-id="9327c-131">YV12</span></span>
-   <span data-ttu-id="9327c-132">YVU9</span><span class="sxs-lookup"><span data-stu-id="9327c-132">YVU9</span></span>
-   <span data-ttu-id="9327c-133">YVYU</span><span class="sxs-lookup"><span data-stu-id="9327c-133">YVYU</span></span>

## <a name="output-formats"></a><span data-ttu-id="9327c-134">Formatos de salida</span><span class="sxs-lookup"><span data-stu-id="9327c-134">Output Formats</span></span>

-   <span data-ttu-id="9327c-135">RGB 24</span><span class="sxs-lookup"><span data-stu-id="9327c-135">RGB 24</span></span>
-   <span data-ttu-id="9327c-136">RGB 32</span><span class="sxs-lookup"><span data-stu-id="9327c-136">RGB 32</span></span>
-   <span data-ttu-id="9327c-137">RGB 555</span><span class="sxs-lookup"><span data-stu-id="9327c-137">RGB 555</span></span>
-   <span data-ttu-id="9327c-138">RGB 565</span><span class="sxs-lookup"><span data-stu-id="9327c-138">RGB 565</span></span>
-   <span data-ttu-id="9327c-139">RGB 8</span><span class="sxs-lookup"><span data-stu-id="9327c-139">RGB 8</span></span>
-   <span data-ttu-id="9327c-140">AYUV</span><span class="sxs-lookup"><span data-stu-id="9327c-140">AYUV</span></span>
-   <span data-ttu-id="9327c-141">I420</span><span class="sxs-lookup"><span data-stu-id="9327c-141">I420</span></span>
-   <span data-ttu-id="9327c-142">IYUV</span><span class="sxs-lookup"><span data-stu-id="9327c-142">IYUV</span></span>
-   <span data-ttu-id="9327c-143">NV11</span><span class="sxs-lookup"><span data-stu-id="9327c-143">NV11</span></span>
-   <span data-ttu-id="9327c-144">NV12</span><span class="sxs-lookup"><span data-stu-id="9327c-144">NV12</span></span>
-   <span data-ttu-id="9327c-145">UYVY</span><span class="sxs-lookup"><span data-stu-id="9327c-145">UYVY</span></span>
-   <span data-ttu-id="9327c-146">V216</span><span class="sxs-lookup"><span data-stu-id="9327c-146">V216</span></span>
-   <span data-ttu-id="9327c-147">V410</span><span class="sxs-lookup"><span data-stu-id="9327c-147">V410</span></span>
-   <span data-ttu-id="9327c-148">YUY2</span><span class="sxs-lookup"><span data-stu-id="9327c-148">YUY2</span></span>
-   <span data-ttu-id="9327c-149">YV12</span><span class="sxs-lookup"><span data-stu-id="9327c-149">YV12</span></span>
-   <span data-ttu-id="9327c-150">YVYU</span><span class="sxs-lookup"><span data-stu-id="9327c-150">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="9327c-151">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9327c-151">Properties</span></span>

-   [<span data-ttu-id="9327c-152">MFPKEY \_ COLORCONV \_ SRCLEFT</span><span class="sxs-lookup"><span data-stu-id="9327c-152">MFPKEY\_COLORCONV\_SRCLEFT</span></span>](mfpkey-colorconv-srcleft.md)
-   [<span data-ttu-id="9327c-153">MFPKEY \_ COLORCONV \_ SRCTOP</span><span class="sxs-lookup"><span data-stu-id="9327c-153">MFPKEY\_COLORCONV\_SRCTOP</span></span>](mfpkey-colorconv-srctop.md)
-   [<span data-ttu-id="9327c-154">MFPKEY \_ COLORCONV \_ DSTLEFT</span><span class="sxs-lookup"><span data-stu-id="9327c-154">MFPKEY\_COLORCONV\_DSTLEFT</span></span>](mfpkey-colorconv-dstleft.md)
-   [<span data-ttu-id="9327c-155">MFPKEY \_ COLORCONV \_ DSTTOP</span><span class="sxs-lookup"><span data-stu-id="9327c-155">MFPKEY\_COLORCONV\_DSTTOP</span></span>](mfpkey-colorconv-dsttop.md)
-   [<span data-ttu-id="9327c-156">MFPKEY \_ ancho de COLORCONV \_</span><span class="sxs-lookup"><span data-stu-id="9327c-156">MFPKEY\_COLORCONV\_WIDTH</span></span>](mfpkey-colorconv-width.md)
-   [<span data-ttu-id="9327c-157">alto de MFPKEY \_ COLORCONV \_</span><span class="sxs-lookup"><span data-stu-id="9327c-157">MFPKEY\_COLORCONV\_HEIGHT</span></span>](mfpkey-colorconv-height.md)
-   [<span data-ttu-id="9327c-158">\_modo COLORCONV de MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="9327c-158">MFPKEY\_COLORCONV\_MODE</span></span>](mfpkey-colorconv-mode.md)

## <a name="remarks"></a><span data-ttu-id="9327c-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9327c-159">Remarks</span></span>

<span data-ttu-id="9327c-160">El DSP del convertidor de colores se implementa como un objeto COM que puede actuar como un objeto DirectXMedia (DMO) o una transformación Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="9327c-160">The Color Converter DSP is implemented as a COM object that can act as a DirectXMedia Object (DMO) or a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="9327c-161">El objeto tiene un identificador de clase único (CLSID) independientemente de si actúa como un DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="9327c-161">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="9327c-162">Para obtener información sobre cuándo un DSP actúa como DMO o MFT, consulte [procesadores de señal digital](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="9327c-162">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="9327c-163">Los identificadores únicos globales (GUID) para los subtipos multimedia RGB difieren en función de si un DSP actúa como DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="9327c-163">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="9327c-164">Los GUID para los subtipos de medios que no son RGB son los mismos, independientemente de si un DSP actúa como DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="9327c-164">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="9327c-165">Para obtener información sobre los GUID que representan subtipos de medios, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="9327c-165">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="9327c-166">De forma predeterminada, este DSP copia toda la imagen de origen en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="9327c-166">By default, this DSP copies the entire source image to the output buffer.</span></span> <span data-ttu-id="9327c-167">Opcionalmente, puede especificar los rectángulos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="9327c-167">Optionally, you can specify source and destination rectangles.</span></span> <span data-ttu-id="9327c-168">El DSP copia la parte de la imagen de origen definida por el rectángulo de origen y la escribe en el rectángulo de destino en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="9327c-168">The DSP copies the portion of the source image defined by source rectangle, and writes it into the destination rectangle on the output buffer.</span></span> <span data-ttu-id="9327c-169">El DSP no realiza ningún ajuste de escala; los rectángulos de origen y de destino deben tener el mismo tamaño.</span><span class="sxs-lookup"><span data-stu-id="9327c-169">The DSP does not perform any scaling; the source and destination rectangles must be the same size.</span></span> <span data-ttu-id="9327c-170">Los rectángulos de origen y de destino no pueden superar los límites del fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9327c-170">The source and destination rectangles cannot exceed the boundaries of the video frame.</span></span>

<span data-ttu-id="9327c-171">Todas las propiedades excepto el [**\_ \_ modo MFPKEY COLORCONV**](mfpkey-colorconv-mode.md) se deben establecer en un grupo.</span><span class="sxs-lookup"><span data-stu-id="9327c-171">All of the properties except [**MFPKEY\_COLORCONV\_MODE**](mfpkey-colorconv-mode.md) must be set in a group.</span></span> <span data-ttu-id="9327c-172">Si establece cualquiera de estas propiedades, debe establecer todas las demás.</span><span class="sxs-lookup"><span data-stu-id="9327c-172">If you set any of these properties, you must set all of the others.</span></span> <span data-ttu-id="9327c-173">De lo contrario, los rectángulos de origen y de destino podrían no ser válidos, en cuyo caso los métodos [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) y [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) devolverán **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="9327c-173">Otherwise, the source and destination rectangles might be invalid, in which case both the [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) and [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) methods will return **E\_INVALIDARG**.</span></span>

<span data-ttu-id="9327c-174">El convertidor de colores no admite todas las combinaciones de formato de entrada y de salida.</span><span class="sxs-lookup"><span data-stu-id="9327c-174">The color converter does not support every combination of input format and output format.</span></span> <span data-ttu-id="9327c-175">Normalmente, debe establecer el formato multimedia que conoce, ya sea de entrada o de salida, y, a continuación, enumerar los formatos disponibles en la secuencia opuesta.</span><span class="sxs-lookup"><span data-stu-id="9327c-175">Usually, you should set the media format that you know, either input or output, and then enumerate the available formats on the opposite stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="9327c-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9327c-176">Requirements</span></span>



| <span data-ttu-id="9327c-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="9327c-177">Requirement</span></span> | <span data-ttu-id="9327c-178">Value</span><span class="sxs-lookup"><span data-stu-id="9327c-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9327c-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9327c-179">Minimum supported client</span></span><br/> | <span data-ttu-id="9327c-180">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9327c-180">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9327c-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9327c-181">Minimum supported server</span></span><br/> | <span data-ttu-id="9327c-182">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9327c-182">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9327c-183">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9327c-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="9327c-184"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9327c-184"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="9327c-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9327c-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9327c-186"><dt>Colorcnv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9327c-186"><dt>Colorcnv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9327c-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="9327c-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9327c-188">Procesadores de señal digital</span><span class="sxs-lookup"><span data-stu-id="9327c-188">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
