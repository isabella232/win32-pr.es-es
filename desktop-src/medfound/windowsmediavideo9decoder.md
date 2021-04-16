---
description: El descodificador de Windows Media Video 9 descodifica las secuencias de vídeo codificadas por el codificador Windows Media Video.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Descodificador de Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718873"
---
# <a name="windows-media-video-9-decoder"></a><span data-ttu-id="eaf64-103">Descodificador de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="eaf64-103">Windows Media Video 9 Decoder</span></span>

<span data-ttu-id="eaf64-104">El descodificador de Windows Media Video 9 descodifica las secuencias de vídeo codificadas por el [**codificador Windows Media Video**](windowsmediavideo9encoder.md).</span><span class="sxs-lookup"><span data-stu-id="eaf64-104">The Windows Media Video 9 decoder decodes video streams that were encoded by the [**Windows Media Video Encoder**](windowsmediavideo9encoder.md).</span></span> <span data-ttu-id="eaf64-105">El codificador y el descodificador admiten las cuatro categorías siguientes de vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="eaf64-105">The encoder and decoder support the following four categories of encoded video.</span></span>

-   <span data-ttu-id="eaf64-106">Perfil sencillo de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="eaf64-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="eaf64-107">Perfil principal de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="eaf64-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="eaf64-108">Perfil avanzado de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="eaf64-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="eaf64-109">Windows Media Video imagen 9,1</span><span class="sxs-lookup"><span data-stu-id="eaf64-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="eaf64-110">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="eaf64-110">Class Identifier</span></span>

<span data-ttu-id="eaf64-111">El identificador de clase (CLSID) del descodificador de Windows Media Video se representa mediante la constante **\_ CWMVDecMediaObject de CLSID**.</span><span class="sxs-lookup"><span data-stu-id="eaf64-111">The class identifier (CLSID) for the Windows Media Video decoder is represented by the constant **CLSID\_CWMVDecMediaObject**.</span></span> <span data-ttu-id="eaf64-112">Puede crear una instancia del descodificador de vídeo llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="eaf64-112">You can create an instance of the video decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="eaf64-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="eaf64-113">Interfaces</span></span>

<span data-ttu-id="eaf64-114">Un objeto de descodificador de vídeo expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto pueda usarse como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="eaf64-114">A video decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="eaf64-115">Un descodificador de vídeo se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="eaf64-115">A video decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="eaf64-116">En la tabla siguiente se muestran las condiciones en las que un descodificador de vídeo se comporta como DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="eaf64-116">The following table shows the conditions under which a video decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="eaf64-117">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="eaf64-117">Operating system</span></span>            | <span data-ttu-id="eaf64-118">Comportamiento del descodificador</span><span class="sxs-lookup"><span data-stu-id="eaf64-118">Decoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf64-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eaf64-119">Windows XP</span></span>                  | <span data-ttu-id="eaf64-120">Un descodificador de vídeo de Windows Media siempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="eaf64-120">A Windows Media video decoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="eaf64-121">Windows Vista y Windows 7</span><span class="sxs-lookup"><span data-stu-id="eaf64-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="eaf64-122">De forma predeterminada, un descodificador de vídeo de Windows Media se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="eaf64-122">By default, a Windows Media video decoder behaves as a DMO.</span></span> <span data-ttu-id="eaf64-123">Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un descodificador de vídeo, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="eaf64-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="eaf64-124">A partir de Windows 7, el descodificador de Windows Media Video implementa la interfaz [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .</span><span class="sxs-lookup"><span data-stu-id="eaf64-124">Beginning with Windows 7, the Windows Media Video decoder implements the [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) interface.</span></span>

## <a name="input-formats"></a><span data-ttu-id="eaf64-125">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="eaf64-125">Input Formats</span></span>

<span data-ttu-id="eaf64-126">En la tabla siguiente se muestran los códigos de cuatro caracteres (FOURCCs) que corresponden a las categorías de entrada codificada admitidas por el descodificador de Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="eaf64-126">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded input that are supported by the Windows Media Video decoder.</span></span>



| <span data-ttu-id="eaf64-127">Category</span><span class="sxs-lookup"><span data-stu-id="eaf64-127">Category</span></span>                               | <span data-ttu-id="eaf64-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="eaf64-128">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="eaf64-129">Perfil sencillo de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="eaf64-129">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="eaf64-130">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="eaf64-130">"WMV3"</span></span>                                   |
| <span data-ttu-id="eaf64-131">Perfil principal de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="eaf64-131">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="eaf64-132">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="eaf64-132">"WMV3"</span></span>                                   |
| <span data-ttu-id="eaf64-133">Perfil avanzado de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="eaf64-133">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="eaf64-134">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="eaf64-134">"WVC1"</span></span>                                   |
| <span data-ttu-id="eaf64-135">Windows Media Video imagen 9,1</span><span class="sxs-lookup"><span data-stu-id="eaf64-135">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="eaf64-136">"WMVP" para 9,1, "WVP2" para la versión 2 de 9,1</span><span class="sxs-lookup"><span data-stu-id="eaf64-136">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="eaf64-137">Formatos de salida</span><span class="sxs-lookup"><span data-stu-id="eaf64-137">Output Formats</span></span>

<span data-ttu-id="eaf64-138">El descodificador de Windows Media Video admite los siguientes subtipos de medios de salida cuando actúa como DMO.</span><span class="sxs-lookup"><span data-stu-id="eaf64-138">The Windows Media Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="eaf64-139">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="eaf64-139">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="eaf64-140">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="eaf64-140">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="eaf64-141">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="eaf64-141">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="eaf64-142">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="eaf64-142">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="eaf64-143">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="eaf64-143">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="eaf64-144">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="eaf64-144">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="eaf64-145">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="eaf64-145">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="eaf64-146">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="eaf64-146">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="eaf64-147">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="eaf64-147">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="eaf64-148">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="eaf64-148">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="eaf64-149">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="eaf64-149">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="eaf64-150">El descodificador de Windows Media Video admite los siguientes subtipos de medios de salida cuando actúa como MFT.</span><span class="sxs-lookup"><span data-stu-id="eaf64-150">The Windows Media Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="eaf64-151">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="eaf64-151">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="eaf64-152">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="eaf64-152">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="eaf64-153">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="eaf64-153">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="eaf64-154">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="eaf64-154">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="eaf64-155">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="eaf64-155">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="eaf64-156">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="eaf64-156">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="eaf64-157">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="eaf64-157">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="eaf64-158">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="eaf64-158">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="eaf64-159">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="eaf64-159">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="eaf64-160">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="eaf64-160">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="eaf64-161">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="eaf64-161">MFVideoFormat\_RGB8</span></span>

## <a name="properties"></a><span data-ttu-id="eaf64-162">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eaf64-162">Properties</span></span>

<span data-ttu-id="eaf64-163">El descodificador de Windows Media Video admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="eaf64-163">The Windows Media Video decoder supports the following properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eaf64-164">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eaf64-164">Property</span></span></th>
<th><span data-ttu-id="eaf64-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="eaf64-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eaf64-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span><span class="sxs-lookup"><span data-stu-id="eaf64-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span></span></td>
<td><span data-ttu-id="eaf64-167">Especifica si el códec descodifica fotogramas de vídeo entrelazados del flujo comprimido como tramas progresivas.</span><span class="sxs-lookup"><span data-stu-id="eaf64-167">Specifies whether the codec decodes interlaced video frames from the compressed stream as progressive frames.</span></span><br/> <dl> <span data-ttu-id="eaf64-168">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="eaf64-168">Windows XP and later.</span></span><br />
<span data-ttu-id="eaf64-169">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="eaf64-169">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="eaf64-170">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eaf64-170">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaf64-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="eaf64-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span></span></td>
<td><span data-ttu-id="eaf64-172">Especifica si el descodificador usará hardware de aceleración de vídeo de DirectX, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="eaf64-172">Specifies whether the decoder will use DirectX video acceleration hardware, if available.</span></span><br/> <dl> <span data-ttu-id="eaf64-173">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="eaf64-173">Windows XP and later.</span></span><br />
<span data-ttu-id="eaf64-174">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="eaf64-174">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="eaf64-175">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="eaf64-175">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eaf64-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span><span class="sxs-lookup"><span data-stu-id="eaf64-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span></span></td>
<td><span data-ttu-id="eaf64-177">Especifica el nivel de energía para el descodificador.</span><span class="sxs-lookup"><span data-stu-id="eaf64-177">Specifies the power level for the decoder.</span></span><br/> <dl> <span data-ttu-id="eaf64-178">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eaf64-178">Windows 7.</span></span><br />
<span data-ttu-id="eaf64-179">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="eaf64-179">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="eaf64-180">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eaf64-180">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaf64-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="eaf64-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span></span></td>
<td><span data-ttu-id="eaf64-182">Especifica si el descodificador debe usar la interpolación de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="eaf64-182">Specifies whether the decoder should use frame interpolation.</span></span><br/> <dl> <span data-ttu-id="eaf64-183">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="eaf64-183">Windows XP and later.</span></span><br />
<span data-ttu-id="eaf64-184">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="eaf64-184">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="eaf64-185">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="eaf64-185">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eaf64-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span><span class="sxs-lookup"><span data-stu-id="eaf64-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span></span></td>
<td><span data-ttu-id="eaf64-187">Especifica si el descodificador admite la interpolación de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="eaf64-187">Specifies whether the decoder supports frame interpolation.</span></span><br/> <dl> <span data-ttu-id="eaf64-188">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="eaf64-188">Windows XP and later.</span></span><br />
<span data-ttu-id="eaf64-189">Perfil simple, perfil principal, perfil avanzado, imagen</span><span class="sxs-lookup"><span data-stu-id="eaf64-189">Simple Profile, Main Profile, Advanced Profile, Image</span></span><br />
<span data-ttu-id="eaf64-190">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eaf64-190">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaf64-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span><span class="sxs-lookup"><span data-stu-id="eaf64-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span></span></td>
<td><span data-ttu-id="eaf64-192">Especifica el número de subprocesos que usará el descodificador.</span><span class="sxs-lookup"><span data-stu-id="eaf64-192">Specifies the number of threads that the decoder will use.</span></span><br/> <dl> <span data-ttu-id="eaf64-193">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="eaf64-193">Windows Vista and later.</span></span><br />
<span data-ttu-id="eaf64-194">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="eaf64-194">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="eaf64-195">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eaf64-195">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eaf64-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span><span class="sxs-lookup"><span data-stu-id="eaf64-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span></span></td>
<td><span data-ttu-id="eaf64-197">Especifica el modo de procesamiento posterior para el descodificador.</span><span class="sxs-lookup"><span data-stu-id="eaf64-197">Specifies the post processing mode for the decoder.</span></span><br/> <dl> <span data-ttu-id="eaf64-198">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="eaf64-198">Windows Vista and later.</span></span><br />
<span data-ttu-id="eaf64-199">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="eaf64-199">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="eaf64-200">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="eaf64-200">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaf64-201"><strong>g_wszWMVCNeedsDrain</strong></span><span class="sxs-lookup"><span data-stu-id="eaf64-201"><strong>g_wszWMVCNeedsDrain</strong></span></span></td>
<td><span data-ttu-id="eaf64-202">Especifica si se debe purgar el descodificador.</span><span class="sxs-lookup"><span data-stu-id="eaf64-202">Specifies whether the decoder should be drained.</span></span><br/> <dl> <span data-ttu-id="eaf64-203">Windows 8</span><span class="sxs-lookup"><span data-stu-id="eaf64-203">Windows 8</span></span><br />
<span data-ttu-id="eaf64-204">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eaf64-204">Read-only.</span></span><br />
</dl> <span data-ttu-id="eaf64-205">El tiempo de ejecución de Windows Media Format usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="eaf64-205">This property is used by the Windows Media Format runtime.</span></span> <span data-ttu-id="eaf64-206">El tipo de propiedad es <strong>VARIANT_BOOL</strong>.</span><span class="sxs-lookup"><span data-stu-id="eaf64-206">The property type is <strong>VARIANT_BOOL</strong>.</span></span> <span data-ttu-id="eaf64-207">Si el valor es <strong>VARIANT_TRUE</strong>, el descodificador se debe purgar después de una discontinuidad.</span><span class="sxs-lookup"><span data-stu-id="eaf64-207">If the value is <strong>VARIANT_TRUE</strong>, the decoder should be drained after a discontinuity.</span></span> <span data-ttu-id="eaf64-208">Para obtener más información acerca de cómo purgar una MFT, vea <a href="basic-mft-processing-model.md">modelo de procesamiento de MFT básico</a>.</span><span class="sxs-lookup"><span data-stu-id="eaf64-208">For more information about draining an MFT, see <a href="basic-mft-processing-model.md">Basic MFT Processing Model</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eaf64-209">Para consultar esta propiedad, use la interfaz <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="eaf64-209">To query this property, use the <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> interface.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="eaf64-210">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eaf64-210">Remarks</span></span>

<span data-ttu-id="eaf64-211">La resolución máxima permitida por el descodificador de Windows Media Video 9 es 4096x4096.</span><span class="sxs-lookup"><span data-stu-id="eaf64-211">The maximum resolution allowed by the Windows Media Video 9 decoder is 4096x4096.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf64-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaf64-212">Requirements</span></span>



| <span data-ttu-id="eaf64-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaf64-213">Requirement</span></span> | <span data-ttu-id="eaf64-214">Value</span><span class="sxs-lookup"><span data-stu-id="eaf64-214">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf64-215">Remoto</span><span class="sxs-lookup"><span data-stu-id="eaf64-215">Client</span></span><br/> | <span data-ttu-id="eaf64-216">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="eaf64-216">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="eaf64-217">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eaf64-217">Header</span></span><br/> | <dl> <span data-ttu-id="eaf64-218"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaf64-218"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="eaf64-219">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eaf64-219">DLL</span></span><br/>    | <dl> <span data-ttu-id="eaf64-220"><dt>Wmvdecod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaf64-220"><dt>Wmvdecod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf64-221">Vea también</span><span class="sxs-lookup"><span data-stu-id="eaf64-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf64-222">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="eaf64-222">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="eaf64-223">Implementación de códecs</span><span class="sxs-lookup"><span data-stu-id="eaf64-223">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
