---
description: El codificador de Windows Media Video 9 codifica las secuencias de vídeo.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Codificador de Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36ee5823c585d60ee74e75f99e8ec9b4d91f5cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721605"
---
# <a name="windows-media-video-9-encoder"></a><span data-ttu-id="85ee5-103">Codificador de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="85ee5-103">Windows Media Video 9 Encoder</span></span>

<span data-ttu-id="85ee5-104">El codificador de Windows Media Video 9 codifica las secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="85ee5-104">The Windows Media Video 9 encoder encodes video streams.</span></span> <span data-ttu-id="85ee5-105">El codificador admite las cuatro categorías de salida codificadas siguientes.</span><span class="sxs-lookup"><span data-stu-id="85ee5-105">The encoder supports the following four categories of encoded output.</span></span>

-   <span data-ttu-id="85ee5-106">Perfil sencillo de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="85ee5-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="85ee5-107">Perfil principal de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="85ee5-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="85ee5-108">Perfil avanzado de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="85ee5-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="85ee5-109">Windows Media Video imagen 9,1</span><span class="sxs-lookup"><span data-stu-id="85ee5-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="85ee5-110">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="85ee5-110">Class Identifier</span></span>

<span data-ttu-id="85ee5-111">El identificador de clase (CLSID) del codificador Windows Media Video se representa mediante la constante CWMV9EncMediaObject de **CLSID \_**.</span><span class="sxs-lookup"><span data-stu-id="85ee5-111">The class identifier (CLSID) for the Windows Media Video encoder is represented by the constant **CLSID\_CWMV9EncMediaObject**.</span></span> <span data-ttu-id="85ee5-112">Puede crear una instancia del codificador de vídeo llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="85ee5-112">You can create an instance of the video encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="85ee5-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="85ee5-113">Interfaces</span></span>

<span data-ttu-id="85ee5-114">Un objeto de codificador de vídeo expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto pueda usarse como un objeto multimedia de DirectX (DMO) y expone la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="85ee5-114">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="85ee5-115">Un codificador de vídeo se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="85ee5-115">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="85ee5-116">En la tabla siguiente se muestran las condiciones en las que un codificador de vídeo se comporta como un DMO o una MFT.</span><span class="sxs-lookup"><span data-stu-id="85ee5-116">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="85ee5-117">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="85ee5-117">Operating system</span></span>            | <span data-ttu-id="85ee5-118">Comportamiento del codificador</span><span class="sxs-lookup"><span data-stu-id="85ee5-118">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85ee5-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="85ee5-119">Windows XP</span></span>                  | <span data-ttu-id="85ee5-120">Un codificador de vídeo de Windows Media siempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="85ee5-120">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="85ee5-121">Windows Vista y Windows 7</span><span class="sxs-lookup"><span data-stu-id="85ee5-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="85ee5-122">De forma predeterminada, un codificador de vídeo de Windows Media se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="85ee5-122">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="85ee5-123">Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un codificador de vídeo, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="85ee5-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="85ee5-124">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="85ee5-124">Input Formats</span></span>

<span data-ttu-id="85ee5-125">El codificador Windows Media Video admite los siguientes subtipos de medios de entrada cuando actúa como DMO.</span><span class="sxs-lookup"><span data-stu-id="85ee5-125">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="85ee5-126">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="85ee5-126">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="85ee5-127">MEDIASUBTYPE \_ i420</span><span class="sxs-lookup"><span data-stu-id="85ee5-127">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="85ee5-128">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="85ee5-128">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="85ee5-129">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="85ee5-129">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="85ee5-130">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="85ee5-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="85ee5-131">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="85ee5-131">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="85ee5-132">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="85ee5-132">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="85ee5-133">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="85ee5-133">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="85ee5-134">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="85ee5-134">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="85ee5-135">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="85ee5-135">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="85ee5-136">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="85ee5-136">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="85ee5-137">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="85ee5-137">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="85ee5-138">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="85ee5-138">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="85ee5-139">fotomovimiento MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="85ee5-139">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="85ee5-140">El codificador Windows Media Video admite los siguientes subtipos de medios de entrada cuando actúa como MFT.</span><span class="sxs-lookup"><span data-stu-id="85ee5-140">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="85ee5-141">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="85ee5-141">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="85ee5-142">MFVideoFormat \_ i420</span><span class="sxs-lookup"><span data-stu-id="85ee5-142">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="85ee5-143">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="85ee5-143">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="85ee5-144">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="85ee5-144">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="85ee5-145">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="85ee5-145">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="85ee5-146">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="85ee5-146">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="85ee5-147">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="85ee5-147">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="85ee5-148">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="85ee5-148">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="85ee5-149">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="85ee5-149">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="85ee5-150">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="85ee5-150">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="85ee5-151">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="85ee5-151">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="85ee5-152">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="85ee5-152">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="85ee5-153">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="85ee5-153">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="85ee5-154">fotomovimiento MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="85ee5-154">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="85ee5-155">Formatos de salida</span><span class="sxs-lookup"><span data-stu-id="85ee5-155">Output Formats</span></span>

<span data-ttu-id="85ee5-156">En la tabla siguiente se muestran los códigos de cuatro caracteres (FOURCCs) que corresponden a las categorías de salida codificada.</span><span class="sxs-lookup"><span data-stu-id="85ee5-156">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded output.</span></span>



| <span data-ttu-id="85ee5-157">Category</span><span class="sxs-lookup"><span data-stu-id="85ee5-157">Category</span></span>                               | <span data-ttu-id="85ee5-158">FOURCC</span><span class="sxs-lookup"><span data-stu-id="85ee5-158">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="85ee5-159">Perfil sencillo de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="85ee5-159">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="85ee5-160">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="85ee5-160">"WMV3"</span></span>                                   |
| <span data-ttu-id="85ee5-161">Perfil principal de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="85ee5-161">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="85ee5-162">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="85ee5-162">"WMV3"</span></span>                                   |
| <span data-ttu-id="85ee5-163">Perfil avanzado de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="85ee5-163">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="85ee5-164">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="85ee5-164">"WVC1"</span></span>                                   |
| <span data-ttu-id="85ee5-165">Windows Media Video imagen 9,1</span><span class="sxs-lookup"><span data-stu-id="85ee5-165">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="85ee5-166">"WMVP" para 9,1, "WVP2" para la versión 2 de 9,1</span><span class="sxs-lookup"><span data-stu-id="85ee5-166">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

<span data-ttu-id="85ee5-167">Para distinguir entre el perfil simple y el perfil principal, establezca la propiedad [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="85ee5-167">To distinguish between Simple Profile and Main Profile, set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property.</span></span>

## <a name="properties"></a><span data-ttu-id="85ee5-168">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85ee5-168">Properties</span></span>

<span data-ttu-id="85ee5-169">El codificador de Windows Media Video 9 admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="85ee5-169">The Windows Media Video 9 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="85ee5-170">Propiedad</span><span class="sxs-lookup"><span data-stu-id="85ee5-170">Property</span></span></th>
<th><span data-ttu-id="85ee5-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="85ee5-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85ee5-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-173">Especifica la sobrecarga, en bytes por paquete, necesaria para el contenedor que se usa para almacenar el contenido comprimido.</span><span class="sxs-lookup"><span data-stu-id="85ee5-173">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="85ee5-174">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-174">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-175">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-175">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-176">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-178">Especifica la velocidad media de fotogramas del contenido de vídeo, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="85ee5-178">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="85ee5-179">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-179">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-180">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-180">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-181">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-183">Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida con la velocidad de bits media (especificada por <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="85ee5-183">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="85ee5-184">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-184">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-185">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-185">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-186">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="85ee5-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-188">Especifica el incremento diferencial entre el cuantificador de imágenes del marco de anclaje y el cuantificador de imágenes del fotograma B.</span><span class="sxs-lookup"><span data-stu-id="85ee5-188">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span><br/> <dl> <span data-ttu-id="85ee5-189">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-189">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-190">Perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-190">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-191">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-191">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-193">Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida en la velocidad de bits máxima (especificada por <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="85ee5-193">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="85ee5-194">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-194">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-195">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-195">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-196">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="85ee5-196">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-198">Especifica si la secuencia de bits de vídeo codificada contiene un valor de llenado de búfer con cada fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="85ee5-198">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="85ee5-199">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-199">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-200">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-200">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-201">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-201">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-203">Especifica el patrón de codificación que se va a utilizar al principio de un grupo de imágenes.</span><span class="sxs-lookup"><span data-stu-id="85ee5-203">Specifies the encoding pattern to use at the beginning of a group of pictures.</span></span><br/> <dl> <span data-ttu-id="85ee5-204">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="85ee5-205">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-205">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-206">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-206">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-208">Especifica el número de fotogramas de vídeo codificados por el códec.</span><span class="sxs-lookup"><span data-stu-id="85ee5-208">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="85ee5-209">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-209">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-210">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-210">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-211">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-213">Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.</span><span class="sxs-lookup"><span data-stu-id="85ee5-213">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="85ee5-214">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-214">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-215">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-215">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-216">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-216">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-218">Esta propiedad se sustituye por <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="85ee5-218">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-220">Especifica la complejidad del algoritmo del codificador.</span><span class="sxs-lookup"><span data-stu-id="85ee5-220">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="85ee5-221">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-221">Windows Vista and later.</span></span><br />
<span data-ttu-id="85ee5-222">Perfil simple, perfil principal.</span><span class="sxs-lookup"><span data-stu-id="85ee5-222">Simple Profile, Main Profile.</span></span> <span data-ttu-id="85ee5-223">Perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-223">Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-224">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-224">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-226">Especifica el tipo de optimización que se va a usar para el códec de perfil avanzado de Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="85ee5-226">Specifies the type of optimization to use for the Windows Media Video 9 Advanced Profile codec.</span></span><br/> <dl> <span data-ttu-id="85ee5-227">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-227">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-228">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-228">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-229">Escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-229">Write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-231">Especifica una representación numérica del equilibrio entre la suavidad de movimiento y la calidad de la imagen en la salida del códec.</span><span class="sxs-lookup"><span data-stu-id="85ee5-231">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="85ee5-232">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-232">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-233">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-233">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-234">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-234">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-236">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="85ee5-236">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-238">Especifica la plantilla de conformidad del dispositivo a la que se ajusta el contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-238">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="85ee5-239">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-239">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-240">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-240">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-241">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-241">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-243">Especifica la plantilla de conformidad del dispositivo que desea usar para la codificación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="85ee5-243">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="85ee5-244">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-244">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-245">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-245">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-246">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-246">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-248">Especifica el método utilizado para codificar la información del vector de movimiento.</span><span class="sxs-lookup"><span data-stu-id="85ee5-248">Specifies the method used to encode the motion vector information.</span></span><br/> <dl> <span data-ttu-id="85ee5-249">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-249">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-250">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-250">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-251">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-251">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-253">Especifica si el códec usará el filtro de ruido al codificar.</span><span class="sxs-lookup"><span data-stu-id="85ee5-253">Specifies whether the codec will use the noise filter when encoding.</span></span><br/> <dl> <span data-ttu-id="85ee5-254">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-254">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-255">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-255">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-256">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-256">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-258">Especifica el nivel de calidad deseado para la codificación de velocidad de bits variable (VBR) basada en la calidad (1-paso).</span><span class="sxs-lookup"><span data-stu-id="85ee5-258">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="85ee5-259">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="85ee5-260">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-260">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-261">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-261">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-263">Especifica el número de fotogramas de vídeo que se han quitado durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="85ee5-263">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="85ee5-264">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-264">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-265">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-265">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-266">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-266">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-268">Especifica el final de una fase de codificación.</span><span class="sxs-lookup"><span data-stu-id="85ee5-268">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="85ee5-269">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-269">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-270">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-270">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-271">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-271">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-273">Especifica un alto de marco intermedio para el vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-273">Specifies an intermediate frame height for encoded video.</span></span><br/> <dl> <span data-ttu-id="85ee5-274">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-274">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-275">Perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-275">Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-276">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-278">Especifica un ancho de marco intermedio para el vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-278">Specifies an intermediate frame width for encoded video.</span></span><br/> <dl> <span data-ttu-id="85ee5-279">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-279">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-280">Perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-280">Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-281">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-283">Especifica si el códec debe utilizar el filtrado medio durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="85ee5-283">Specifies whether the codec should use median filtering during encoding.</span></span><br/> <dl> <span data-ttu-id="85ee5-284">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-284">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-285">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-285">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-286">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-286">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-288">Especifica el FOURCC que identifica el codificador que se desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="85ee5-288">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="85ee5-289">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-289">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-290">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-290">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-291">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-291">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-293">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="85ee5-293">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-295">Especifica si el codificador puede quitar fotogramas.</span><span class="sxs-lookup"><span data-stu-id="85ee5-295">Specifies whether the encoder is allowed to drop frames.</span></span><br/> <dl> <span data-ttu-id="85ee5-296">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-296">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-297">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-297">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-298">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-298">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-300">Especifica si la salida del códec se entrelazará.</span><span class="sxs-lookup"><span data-stu-id="85ee5-300">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="85ee5-301">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-301">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-302">Perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-302">Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-303">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-303">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-305">Especifica el tiempo máximo, en milisegundos, entre los fotogramas clave de la salida del códec.</span><span class="sxs-lookup"><span data-stu-id="85ee5-305">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="85ee5-306">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-306">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-307">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-307">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-308">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-308">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-310">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="85ee5-310">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-312">Especifica el número de fotogramas después del fotograma actual que el códec evaluará antes de codificar el fotograma actual.</span><span class="sxs-lookup"><span data-stu-id="85ee5-312">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span><br/> <dl> <span data-ttu-id="85ee5-313">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-313">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-314">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-314">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-315">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-315">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-317">Especifica si el códec debe utilizar el filtro de desbloqueo en bucle durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="85ee5-317">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span><br/> <dl> <span data-ttu-id="85ee5-318">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-318">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-319">Perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-319">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-320">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-320">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-322">Especifica el método de costo que usa el códec para determinar qué modo de adaptativo macrobloque debe usar.</span><span class="sxs-lookup"><span data-stu-id="85ee5-322">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span><br/> <dl> <span data-ttu-id="85ee5-323">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-323">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-324">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-324">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-325">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-325">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-327">Especifica el método que se va a utilizar para la coincidencia de movimiento.</span><span class="sxs-lookup"><span data-stu-id="85ee5-327">Specifies the method to use for motion matching.</span></span><br/> <dl> <span data-ttu-id="85ee5-328">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-328">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-329">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-329">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-330">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-330">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-332">Especifica los tipos de información de vídeo que se usan en las operaciones de búsqueda de movimiento.</span><span class="sxs-lookup"><span data-stu-id="85ee5-332">Specifies the types of video information that are used in motion search operations.</span></span><br/> <dl> <span data-ttu-id="85ee5-333">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-333">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-334">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-334">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-335">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-335">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-337">Especifica el intervalo usado en las búsquedas de movimiento.</span><span class="sxs-lookup"><span data-stu-id="85ee5-337">Specifies the range used in motion searches.</span></span><br/> <dl> <span data-ttu-id="85ee5-338">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-338">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-339">Perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-339">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-340">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-340">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-342">Especifica si el códec debe intentar detectar bordes de fotogramas ruidosos y quitarlos.</span><span class="sxs-lookup"><span data-stu-id="85ee5-342">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span><br/> <dl> <span data-ttu-id="85ee5-343">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-343">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-344">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-344">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-345">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-345">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-347">Especifica el número de fotogramas predictivos bidireccionales (fotogramas B).</span><span class="sxs-lookup"><span data-stu-id="85ee5-347">Specifies the number of bidirectional predictive frames (B-frames).</span></span><br/> <dl> <span data-ttu-id="85ee5-348">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-348">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-349">Perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-349">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-350">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-350">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-352">Especifica el número de subprocesos que el códec usará para la codificación.</span><span class="sxs-lookup"><span data-stu-id="85ee5-352">Specifies the number of threads that the codec will use for encoding.</span></span><br/> <dl> <span data-ttu-id="85ee5-353">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-353">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-354">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-354">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-355">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-355">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-357">Especifica el número máximo de pasos admitidos por el códec.</span><span class="sxs-lookup"><span data-stu-id="85ee5-357">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="85ee5-358">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-358">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-359">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-359">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-360">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-360">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-362">Especifica el número de pasos que el códec usará para codificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="85ee5-362">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="85ee5-363">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-363">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-364">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-364">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-365">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="85ee5-365">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-367">Especifica si el códec debe utilizar la optimización perceptual conservadora al codificar.</span><span class="sxs-lookup"><span data-stu-id="85ee5-367">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span><br/> <dl> <span data-ttu-id="85ee5-368">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-368">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-369">Perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-369">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-370">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-370">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-372">Especifica si el codificador genera entradas de fotogramas ficticias en el flujo de bits para los fotogramas duplicados.</span><span class="sxs-lookup"><span data-stu-id="85ee5-372">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="85ee5-373">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-373">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-374">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-374">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-375">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-375">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-377">Especifica QP.</span><span class="sxs-lookup"><span data-stu-id="85ee5-377">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="85ee5-378">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-378">Windows Vista and later.</span></span><br />
<span data-ttu-id="85ee5-379">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-379">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-380">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-380">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-382">Especifica el grado en el que el códec debe reducir el intervalo de color efectivo del vídeo.</span><span class="sxs-lookup"><span data-stu-id="85ee5-382">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span><br/> <dl> <span data-ttu-id="85ee5-383">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-383">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-384">Perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-384">Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-385">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-385">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-387">Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="85ee5-387">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="85ee5-388">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-388">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-389">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-389">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-390">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="85ee5-390">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-392">Especifica si el codificador utiliza la búsqueda MV de subpíxeles basada en RD.</span><span class="sxs-lookup"><span data-stu-id="85ee5-392">Specifies whether the encoder uses RD-based sub-pixel MV search.</span></span> <br/> <dl> <span data-ttu-id="85ee5-393">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-393">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-394">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-394">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-395">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-395">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-397">Para la recodificación del segmento, especifica el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="85ee5-397">For segment re-encoding, specifies the buffer size.</span></span><br/> <dl> <span data-ttu-id="85ee5-398">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-398">Windows Vista and later.</span></span><br />
<span data-ttu-id="85ee5-399">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-399">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-400">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-400">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-402">Para la recodificación de segmentos, especifica la duración del segmento que se va a volver a codificar.</span><span class="sxs-lookup"><span data-stu-id="85ee5-402">For segment re-encoding, specifies the duration of the segment to be re-encoded.</span></span><br/> <dl> <span data-ttu-id="85ee5-403">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-403">Windows Vista and later.</span></span><br />
<span data-ttu-id="85ee5-404">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-404">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-405">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-405">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-407">Para la recodificación del segmento, especifica el cuantificador del marco antes del segmento inicial.</span><span class="sxs-lookup"><span data-stu-id="85ee5-407">For segment re-encoding, specifies the quantizer of the frame prior to the starting segment.</span></span><br/> <dl> <span data-ttu-id="85ee5-408">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-408">Windows Vista and later.</span></span><br />
<span data-ttu-id="85ee5-409">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-409">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-410">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-410">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-412">Para la recodificación de segmentos, especifica el llenado del búfer de inicio.</span><span class="sxs-lookup"><span data-stu-id="85ee5-412">For segment re-encoding, specifies the starting buffer fullness.</span></span><br/> <dl> <span data-ttu-id="85ee5-413">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-413">Windows Vista and later.</span></span><br />
<span data-ttu-id="85ee5-414">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-414">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-415">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-415">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-417">Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la velocidad de bits variable (VBR) limitada de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="85ee5-417">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="85ee5-418">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-418">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-419">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-419">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-420">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="85ee5-420">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-422">Especifica el número de fotogramas de vídeo pasados al codificador durante el proceso de codificación.</span><span class="sxs-lookup"><span data-stu-id="85ee5-422">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="85ee5-423">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-423">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-424">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-424">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-425">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-425">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-427">Especifica si el códec usará la codificación de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="85ee5-427">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="85ee5-428">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-428">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-429">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-429">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-430">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="85ee5-430">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-432">Especifica el nivel de calidad real de la codificación de velocidad de bits variable (VBR) basada en la calidad (1-paso).</span><span class="sxs-lookup"><span data-stu-id="85ee5-432">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="85ee5-433">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-433">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-434">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-434">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-435">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-435">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-437">Especifica si el códec usará la optimización del escalado de vídeo.</span><span class="sxs-lookup"><span data-stu-id="85ee5-437">Specifies whether the codec will use video scaling optimization.</span></span><br/> <dl> <span data-ttu-id="85ee5-438">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-438">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-439">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-439">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-440">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-440">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-442">Especifica la cantidad de contenido, en milisegundos, que puede caber en el búfer del modelo.</span><span class="sxs-lookup"><span data-stu-id="85ee5-442">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="85ee5-443">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-443">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-444">Perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-444">Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-445">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-445">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-447">Para la recodificación de segmentos, especifica los datos privados del códec del archivo que se va a codificar de nuevo.</span><span class="sxs-lookup"><span data-stu-id="85ee5-447">For segment re-encoding, specifies the codec private data of the file that is being re-encoded.</span></span><br/> <dl> <span data-ttu-id="85ee5-448">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-448">Windows Vista and later.</span></span><br />
<span data-ttu-id="85ee5-449">Perfil simple, perfil principal, perfil avanzado, imagen.</span><span class="sxs-lookup"><span data-stu-id="85ee5-449">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="85ee5-450">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-450">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85ee5-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-452">Especifica el tipo de lógica que el códec usará para detectar vídeo de origen entrelazado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-452">Specifies the type of logic that the codec will use to detect interlaced source video.</span></span><br/> <dl> <span data-ttu-id="85ee5-453">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-453">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-454">Perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-454">Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-455">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="85ee5-455">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85ee5-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="85ee5-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="85ee5-457">Especifica el número de fotogramas de vídeo que se omitieron porque eran duplicados de fotogramas anteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-457">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="85ee5-458">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85ee5-458">Windows XP and later.</span></span><br />
<span data-ttu-id="85ee5-459">Perfil simple, perfil principal, perfil avanzado.</span><span class="sxs-lookup"><span data-stu-id="85ee5-459">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="85ee5-460">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ee5-460">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="85ee5-461">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85ee5-461">Requirements</span></span>



| <span data-ttu-id="85ee5-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="85ee5-462">Requirement</span></span> | <span data-ttu-id="85ee5-463">Value</span><span class="sxs-lookup"><span data-stu-id="85ee5-463">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85ee5-464">Remoto</span><span class="sxs-lookup"><span data-stu-id="85ee5-464">Client</span></span><br/> | <span data-ttu-id="85ee5-465">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="85ee5-465">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="85ee5-466">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85ee5-466">Header</span></span><br/> | <dl> <span data-ttu-id="85ee5-467"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="85ee5-467"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="85ee5-468">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85ee5-468">DLL</span></span><br/>    | <dl> <span data-ttu-id="85ee5-469"><dt>Wmvencod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85ee5-469"><dt>Wmvencod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85ee5-470">Vea también</span><span class="sxs-lookup"><span data-stu-id="85ee5-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ee5-471">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="85ee5-471">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="85ee5-472">Implementación de códecs</span><span class="sxs-lookup"><span data-stu-id="85ee5-472">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
