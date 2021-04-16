---
description: Cambia el tamaño de una secuencia de vídeo.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: Tamaño DSP de vídeo (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696672"
---
# <a name="video-resizer-dsp"></a><span data-ttu-id="6aac2-103">Vídeo de tamaño DSP</span><span class="sxs-lookup"><span data-stu-id="6aac2-103">Video Resizer DSP</span></span>

<span data-ttu-id="6aac2-104">Cambia el tamaño de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6aac2-104">Resizes a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="6aac2-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="6aac2-105">CLSID</span></span>

<span data-ttu-id="6aac2-106">CLSID \_ CResizerDMO</span><span class="sxs-lookup"><span data-stu-id="6aac2-106">CLSID\_CResizerDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="6aac2-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="6aac2-107">Interfaces</span></span>

-   [<span data-ttu-id="6aac2-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="6aac2-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="6aac2-109">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="6aac2-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="6aac2-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="6aac2-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="6aac2-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="6aac2-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="6aac2-112">**IWMResizerProps**</span><span class="sxs-lookup"><span data-stu-id="6aac2-112">**IWMResizerProps**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a><span data-ttu-id="6aac2-113">Formatos</span><span class="sxs-lookup"><span data-stu-id="6aac2-113">Formats</span></span>

<span data-ttu-id="6aac2-114">El DSP de tamaño de vídeo admite los siguientes subtipos de medios de entrada/salida cuando actúa como un objeto multimedia de DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="6aac2-114">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="6aac2-115">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="6aac2-115">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="6aac2-116">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="6aac2-116">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="6aac2-117">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="6aac2-117">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="6aac2-118">MEDIASUBTYPE \_ i420</span><span class="sxs-lookup"><span data-stu-id="6aac2-118">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="6aac2-119">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="6aac2-119">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="6aac2-120">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="6aac2-120">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="6aac2-121">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="6aac2-121">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="6aac2-122">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="6aac2-122">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="6aac2-123">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="6aac2-123">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="6aac2-124">MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="6aac2-124">MEDIASUBTYPE\_AYUV</span></span>
-   <span data-ttu-id="6aac2-125">MEDIASUBTYPE \_ V216</span><span class="sxs-lookup"><span data-stu-id="6aac2-125">MEDIASUBTYPE\_V216</span></span>
-   <span data-ttu-id="6aac2-126">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="6aac2-126">MEDIASUBTYPE\_YV12</span></span>

<span data-ttu-id="6aac2-127">El DSP de tamaño de vídeo admite los siguientes subtipos de medios de entrada/salida cuando actúa como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="6aac2-127">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="6aac2-128">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="6aac2-128">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="6aac2-129">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="6aac2-129">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="6aac2-130">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="6aac2-130">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="6aac2-131">MFVideoFormat \_ i420</span><span class="sxs-lookup"><span data-stu-id="6aac2-131">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="6aac2-132">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="6aac2-132">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="6aac2-133">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="6aac2-133">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="6aac2-134">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="6aac2-134">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="6aac2-135">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="6aac2-135">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="6aac2-136">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="6aac2-136">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="6aac2-137">MFVideoFormat \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="6aac2-137">MFVideoFormat\_AYUV</span></span>
-   <span data-ttu-id="6aac2-138">MFVideoFormat \_ V216</span><span class="sxs-lookup"><span data-stu-id="6aac2-138">MFVideoFormat\_V216</span></span>
-   <span data-ttu-id="6aac2-139">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="6aac2-139">MFVideoFormat\_YV12</span></span>

## <a name="properties"></a><span data-ttu-id="6aac2-140">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6aac2-140">Properties</span></span>

-   [<span data-ttu-id="6aac2-141">MFPKEY \_ cambiar el tamaño de \_ src \_ left</span><span class="sxs-lookup"><span data-stu-id="6aac2-141">MFPKEY\_RESIZE\_SRC\_LEFT</span></span>](mfpkey-resize-src-left.md)
-   [<span data-ttu-id="6aac2-142">MFPKEY \_ cambiar tamaño \_ src \_ superior</span><span class="sxs-lookup"><span data-stu-id="6aac2-142">MFPKEY\_RESIZE\_SRC\_TOP</span></span>](mfpkey-resize-src-top.md)
-   [<span data-ttu-id="6aac2-143">MFPKEY \_ cambiar el tamaño de \_ src \_</span><span class="sxs-lookup"><span data-stu-id="6aac2-143">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span>](mfpkey-resize-src-width.md)
-   [<span data-ttu-id="6aac2-144">MFPKEY \_ cambiar el tamaño de \_ src \_</span><span class="sxs-lookup"><span data-stu-id="6aac2-144">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span>](mfpkey-resize-src-height.md)
-   [<span data-ttu-id="6aac2-145">MFPKEY \_ cambio de tamaño de DST a la \_ \_ izquierda</span><span class="sxs-lookup"><span data-stu-id="6aac2-145">MFPKEY\_RESIZE\_DST\_LEFT</span></span>](mfpkey-resize-dst-left.md)
-   [<span data-ttu-id="6aac2-146">MFPKEY \_ cambiar el tamaño de \_ DST \_ superior</span><span class="sxs-lookup"><span data-stu-id="6aac2-146">MFPKEY\_RESIZE\_DST\_TOP</span></span>](mfpkey-resize-dst-top.md)
-   [<span data-ttu-id="6aac2-147">MFPKEY \_ cambiar el \_ ancho de DST \_</span><span class="sxs-lookup"><span data-stu-id="6aac2-147">MFPKEY\_RESIZE\_DST\_WIDTH</span></span>](mfpkey-resize-dst-width.md)
-   [<span data-ttu-id="6aac2-148">MFPKEY \_ cambiar el tamaño de \_ DST \_</span><span class="sxs-lookup"><span data-stu-id="6aac2-148">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span>](mfpkey-resize-dst-height.md)
-   [<span data-ttu-id="6aac2-149">MFPKEY \_ cambiar el tamaño de la \_ calidad</span><span class="sxs-lookup"><span data-stu-id="6aac2-149">MFPKEY\_RESIZE\_QUALITY</span></span>](mfpkey-resize-quality.md)
-   [<span data-ttu-id="6aac2-150">MFPKEY \_ cambiar el tamaño del \_ entrelazado</span><span class="sxs-lookup"><span data-stu-id="6aac2-150">MFPKEY\_RESIZE\_INTERLACE</span></span>](mfpkey-resize-interlace.md)
-   [<span data-ttu-id="6aac2-151">MFPKEY \_ cambiar el tamaño de \_ GEOMAPX</span><span class="sxs-lookup"><span data-stu-id="6aac2-151">MFPKEY\_RESIZE\_GEOMAPX</span></span>](mfpkey-resize-geomapx.md)
-   [<span data-ttu-id="6aac2-152">MFPKEY \_ cambiar el tamaño de \_ GEOMAPY</span><span class="sxs-lookup"><span data-stu-id="6aac2-152">MFPKEY\_RESIZE\_GEOMAPY</span></span>](mfpkey-resize-geomapy.md)
-   [<span data-ttu-id="6aac2-153">MFPKEY \_ cambiar el tamaño de \_ GEOMAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="6aac2-153">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span>](mfpkey-resize-geomapwidth.md)
-   [<span data-ttu-id="6aac2-154">MFPKEY \_ cambiar el tamaño de \_ GEOMAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="6aac2-154">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span>](mfpkey-resize-geomapheight.md)
-   [<span data-ttu-id="6aac2-155">MFPKEY \_ cambiar el tamaño de \_ MINAPX</span><span class="sxs-lookup"><span data-stu-id="6aac2-155">MFPKEY\_RESIZE\_MINAPX</span></span>](mfpkey-resize-minapx.md)
-   [<span data-ttu-id="6aac2-156">MFPKEY \_ cambiar el tamaño de \_ MINAPY</span><span class="sxs-lookup"><span data-stu-id="6aac2-156">MFPKEY\_RESIZE\_MINAPY</span></span>](mfpkey-resize-minapy.md)
-   [<span data-ttu-id="6aac2-157">MFPKEY \_ cambiar el tamaño de \_ MINAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="6aac2-157">MFPKEY\_RESIZE\_MINAPWIDTH</span></span>](mfpkey-resize-minapwidth.md)
-   [<span data-ttu-id="6aac2-158">MFPKEY \_ cambiar el tamaño de \_ MINAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="6aac2-158">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span>](mfpkey-resize-minapheight.md)
-   [<span data-ttu-id="6aac2-159">MFPKEY \_ cambiar el tamaño de \_ PANSCANAPX</span><span class="sxs-lookup"><span data-stu-id="6aac2-159">MFPKEY\_RESIZE\_PANSCANAPX</span></span>](mfpkey-resize-panscanapx.md)
-   [<span data-ttu-id="6aac2-160">MFPKEY \_ cambiar el tamaño de \_ PANSCANAPY</span><span class="sxs-lookup"><span data-stu-id="6aac2-160">MFPKEY\_RESIZE\_PANSCANAPY</span></span>](mfpkey-resize-panscanapy.md)
-   [<span data-ttu-id="6aac2-161">MFPKEY \_ cambiar el tamaño de \_ PANSCANAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="6aac2-161">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span>](mfpkey-resize-panscanapwidth.md)
-   [<span data-ttu-id="6aac2-162">MFPKEY \_ cambiar el tamaño de \_ PANSCANAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="6aac2-162">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span>](mfpkey-resize-panscanapheight.md)
-   [<span data-ttu-id="6aac2-163">MFPKEY \_ PIXELASPECTRATIO</span><span class="sxs-lookup"><span data-stu-id="6aac2-163">MFPKEY\_PIXELASPECTRATIO</span></span>](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a><span data-ttu-id="6aac2-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6aac2-164">Remarks</span></span>

<span data-ttu-id="6aac2-165">El ajuste de vídeo DSP se implementa como un objeto COM que puede actuar como DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="6aac2-165">The Video Resizer DSP is implemented as a COM object that can act as a DMO or an MFT.</span></span> <span data-ttu-id="6aac2-166">El objeto tiene un identificador de clase único (CLSID) independientemente de si actúa como un DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="6aac2-166">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="6aac2-167">Para obtener información sobre cuándo un DSP actúa como DMO o MFT, consulte [procesadores de señal digital](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="6aac2-167">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="6aac2-168">Los identificadores únicos globales (GUID) para los subtipos multimedia RGB difieren en función de si un DSP actúa como DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="6aac2-168">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="6aac2-169">Los GUID para los subtipos de medios que no son RGB son los mismos, independientemente de si un DSP actúa como DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="6aac2-169">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="6aac2-170">Para obtener información sobre los GUID que representan subtipos de medios, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="6aac2-170">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="6aac2-171">Este DSP puede realizar el recorte y el escalado en la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6aac2-171">This DSP can perform both cropping and scaling on the video image.</span></span> <span data-ttu-id="6aac2-172">El formato del tipo de salida debe coincidir con el formato del tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="6aac2-172">The format of the output type must match the format of the input type.</span></span> <span data-ttu-id="6aac2-173">El DSP no realiza conversiones de espacio de color.</span><span class="sxs-lookup"><span data-stu-id="6aac2-173">The DSP does not perform color-space conversions.</span></span>

<span data-ttu-id="6aac2-174">Antes de establecer el tipo de salida, puede definir cualquiera de las siguientes regiones mediante las propiedades que se muestran en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="6aac2-174">Before setting the output type, you can define any of the following regions by using the properties listed in this table.</span></span>



| <span data-ttu-id="6aac2-175">Region</span><span class="sxs-lookup"><span data-stu-id="6aac2-175">Region</span></span>                   | <span data-ttu-id="6aac2-176">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6aac2-176">Properties</span></span>                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aac2-177">Rectángulo de origen</span><span class="sxs-lookup"><span data-stu-id="6aac2-177">Source rectangle</span></span>         | <span data-ttu-id="6aac2-178">MFPKEY \_ cambiar el tamaño de \_ src \_ left</span><span class="sxs-lookup"><span data-stu-id="6aac2-178">MFPKEY\_RESIZE\_SRC\_LEFT</span></span><br/> <span data-ttu-id="6aac2-179">MFPKEY \_ cambiar tamaño \_ src \_ superior</span><span class="sxs-lookup"><span data-stu-id="6aac2-179">MFPKEY\_RESIZE\_SRC\_TOP</span></span><br/> <span data-ttu-id="6aac2-180">MFPKEY \_ cambiar el tamaño de \_ src \_</span><span class="sxs-lookup"><span data-stu-id="6aac2-180">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span><br/> <span data-ttu-id="6aac2-181">MFPKEY \_ cambiar el tamaño de \_ src \_</span><span class="sxs-lookup"><span data-stu-id="6aac2-181">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="6aac2-182">Rectángulo de destino</span><span class="sxs-lookup"><span data-stu-id="6aac2-182">Destination rectangle</span></span>    | <span data-ttu-id="6aac2-183">MFPKEY \_ cambio de tamaño de DST a la \_ \_ izquierda</span><span class="sxs-lookup"><span data-stu-id="6aac2-183">MFPKEY\_RESIZE\_DST\_LEFT</span></span><br/> <span data-ttu-id="6aac2-184">MFPKEY \_ cambiar el tamaño de \_ DST \_ superior</span><span class="sxs-lookup"><span data-stu-id="6aac2-184">MFPKEY\_RESIZE\_DST\_TOP</span></span><br/> <span data-ttu-id="6aac2-185">MFPKEY \_ cambiar el \_ ancho de DST \_</span><span class="sxs-lookup"><span data-stu-id="6aac2-185">MFPKEY\_RESIZE\_DST\_WIDTH</span></span><br/> <span data-ttu-id="6aac2-186">MFPKEY \_ cambiar el tamaño de \_ DST \_</span><span class="sxs-lookup"><span data-stu-id="6aac2-186">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="6aac2-187">Abertura geométrica</span><span class="sxs-lookup"><span data-stu-id="6aac2-187">Geometric aperture</span></span>       | <span data-ttu-id="6aac2-188">MFPKEY \_ cambiar el tamaño de \_ GEOMAPX</span><span class="sxs-lookup"><span data-stu-id="6aac2-188">MFPKEY\_RESIZE\_GEOMAPX</span></span><br/> <span data-ttu-id="6aac2-189">MFPKEY \_ cambiar el tamaño de \_ GEOMAPY</span><span class="sxs-lookup"><span data-stu-id="6aac2-189">MFPKEY\_RESIZE\_GEOMAPY</span></span><br/> <span data-ttu-id="6aac2-190">MFPKEY \_ cambiar el tamaño de \_ GEOMAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="6aac2-190">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span><br/> <span data-ttu-id="6aac2-191">MFPKEY \_ cambiar el tamaño de \_ GEOMAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="6aac2-191">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span><br/>             |
| <span data-ttu-id="6aac2-192">Apertura de pantalla mínima</span><span class="sxs-lookup"><span data-stu-id="6aac2-192">Minimum display aperture</span></span> | <span data-ttu-id="6aac2-193">MFPKEY \_ cambiar el tamaño de \_ MINAPX</span><span class="sxs-lookup"><span data-stu-id="6aac2-193">MFPKEY\_RESIZE\_MINAPX</span></span><br/> <span data-ttu-id="6aac2-194">MFPKEY \_ cambiar el tamaño de \_ MINAPY</span><span class="sxs-lookup"><span data-stu-id="6aac2-194">MFPKEY\_RESIZE\_MINAPY</span></span><br/> <span data-ttu-id="6aac2-195">MFPKEY \_ cambiar el tamaño de \_ MINAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="6aac2-195">MFPKEY\_RESIZE\_MINAPWIDTH</span></span><br/> <span data-ttu-id="6aac2-196">MFPKEY \_ cambiar el tamaño de \_ MINAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="6aac2-196">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span><br/>                 |
| <span data-ttu-id="6aac2-197">Región de Pan/Scan</span><span class="sxs-lookup"><span data-stu-id="6aac2-197">Pan/scan region</span></span>          | <span data-ttu-id="6aac2-198">MFPKEY \_ cambiar el tamaño de \_ PANSCANAPX</span><span class="sxs-lookup"><span data-stu-id="6aac2-198">MFPKEY\_RESIZE\_PANSCANAPX</span></span><br/> <span data-ttu-id="6aac2-199">MFPKEY \_ cambiar el tamaño de \_ PANSCANAPY</span><span class="sxs-lookup"><span data-stu-id="6aac2-199">MFPKEY\_RESIZE\_PANSCANAPY</span></span><br/> <span data-ttu-id="6aac2-200">MFPKEY \_ cambiar el tamaño de \_ PANSCANAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="6aac2-200">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span><br/> <span data-ttu-id="6aac2-201">MFPKEY \_ cambiar el tamaño de \_ PANSCANAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="6aac2-201">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span><br/> |



 

<span data-ttu-id="6aac2-202">En cada caso, debe establecer todas las propiedades asociadas para que la configuración surta efecto.</span><span class="sxs-lookup"><span data-stu-id="6aac2-202">In each case, you must set all of the associated properties for the setting to take effect.</span></span>

<span data-ttu-id="6aac2-203">El DSP copia la parte de la imagen de origen definida por el rectángulo de origen y lo estira o comprime en el rectángulo de destino en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="6aac2-203">The DSP copies the portion of the source image defined by source rectangle, and stretches or compresses it onto the destination rectangle on the output buffer.</span></span> <span data-ttu-id="6aac2-204">No es necesario que los rectángulos de origen y de destino tengan el mismo tamaño.</span><span class="sxs-lookup"><span data-stu-id="6aac2-204">The source and destination rectangles do not need to be the same size.</span></span> <span data-ttu-id="6aac2-205">El tamaño del marco en el tipo de medio de salida debe ser lo suficientemente grande como para contener el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="6aac2-205">The frame size in the output media type must be large enough to hold the destination rectangle.</span></span>

<span data-ttu-id="6aac2-206">La abertura geométrica, la abertura de pantalla mínima y la región de Pan/Scan no afectan al modo en que el DSP cambia el tamaño del vídeo.</span><span class="sxs-lookup"><span data-stu-id="6aac2-206">The geometric aperture, minimum display aperture, and pan/scan region do not affect how the DSP resizes the video.</span></span> <span data-ttu-id="6aac2-207">Sin embargo, podrían afectar al modo en que el componente de nivel inferior interpreta el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6aac2-207">However, they might affect how the downstream component interprets the video frame.</span></span> <span data-ttu-id="6aac2-208">En concreto, el representador de vídeo mejorado (EVR) usa estos valores al calcular la relación de aspecto de la imagen y el área de presentación.</span><span class="sxs-lookup"><span data-stu-id="6aac2-208">In particular, the enhanced video renderer (EVR) uses these values when it calculates the picture aspect ratio and the display area.</span></span>

<span data-ttu-id="6aac2-209">Si usa Media Foundation tipos de medios, puede establecer la abertura geométrica, la abertura de pantalla mínima y las regiones de Pan/Scan directamente en el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="6aac2-209">If you are using Media Foundation media types, you can set the geometric aperture, minimum display aperture, and pan/scan regions directly in the output media type.</span></span> <span data-ttu-id="6aac2-210">De lo contrario, si usa tipos de medios DMO, establézcalo mediante las propiedades.</span><span class="sxs-lookup"><span data-stu-id="6aac2-210">Otherwise, if you are using DMO media types, set them using the properties.</span></span>

<span data-ttu-id="6aac2-211">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="6aac2-211">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="6aac2-212">**\_ \_ apertura geométrica de MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="6aac2-212">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
-   [<span data-ttu-id="6aac2-213">**\_ \_ apertura mínima de \_ pantalla MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="6aac2-213">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="6aac2-214">**\_apertura de \_ \_ análisis panorámico MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="6aac2-214">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a><span data-ttu-id="6aac2-215">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6aac2-215">Requirements</span></span>



| <span data-ttu-id="6aac2-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aac2-216">Requirement</span></span> | <span data-ttu-id="6aac2-217">Value</span><span class="sxs-lookup"><span data-stu-id="6aac2-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6aac2-218">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6aac2-218">Minimum supported client</span></span><br/> | <span data-ttu-id="6aac2-219">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6aac2-219">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6aac2-220">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6aac2-220">Minimum supported server</span></span><br/> | <span data-ttu-id="6aac2-221">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6aac2-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6aac2-222">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6aac2-222">Header</span></span><br/>                   | <dl> <span data-ttu-id="6aac2-223"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aac2-223"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="6aac2-224">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6aac2-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aac2-225"><dt>Vidreszr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6aac2-225"><dt>Vidreszr.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6aac2-226">Vea también</span><span class="sxs-lookup"><span data-stu-id="6aac2-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aac2-227">Procesadores de señal digital</span><span class="sxs-lookup"><span data-stu-id="6aac2-227">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
