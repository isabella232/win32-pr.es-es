---
description: El codificador Windows Media Video 7/8 implementa versiones anteriores del codificador Windows Media Video.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Codificador Windows Media Video 7/8 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700272"
---
# <a name="windows-media-video-78-encoder"></a><span data-ttu-id="d486d-103">Codificador Windows Media Video 7/8</span><span class="sxs-lookup"><span data-stu-id="d486d-103">Windows Media Video 7/8 Encoder</span></span>

<span data-ttu-id="d486d-104">El codificador Windows Media Video 7/8 implementa versiones anteriores del codificador Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="d486d-104">The Windows Media Video 7/8 encoder implements previous versions of the Windows Media Video encoder.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="d486d-105">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="d486d-105">Class Identifier</span></span>

<span data-ttu-id="d486d-106">El identificador de clase (CLSID) del codificador Windows Media Video 7/8 es **CLSID \_ CWMVXEncMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="d486d-106">The class identifier (CLSID) for the Windows Media Video 7/8 encoder is **CLSID\_CWMVXEncMediaObject**.</span></span> <span data-ttu-id="d486d-107">Puede crear una instancia del codificador llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="d486d-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="d486d-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="d486d-108">Interfaces</span></span>

<span data-ttu-id="d486d-109">Un objeto de codificador de vídeo expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto pueda usarse como un objeto multimedia de DirectX (DMO) y expone la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="d486d-109">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="d486d-110">Un codificador de vídeo se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d486d-110">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="d486d-111">En la tabla siguiente se muestran las condiciones en las que un codificador de vídeo se comporta como un DMO o una MFT.</span><span class="sxs-lookup"><span data-stu-id="d486d-111">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="d486d-112">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d486d-112">Operating system</span></span>            | <span data-ttu-id="d486d-113">Comportamiento del codificador</span><span class="sxs-lookup"><span data-stu-id="d486d-113">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d486d-114">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d486d-114">Windows XP</span></span>                  | <span data-ttu-id="d486d-115">Un codificador de vídeo de Windows Media siempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="d486d-115">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="d486d-116">Windows Vista y Windows 7</span><span class="sxs-lookup"><span data-stu-id="d486d-116">Windows Vista and Windows 7</span></span> | <span data-ttu-id="d486d-117">De forma predeterminada, un codificador de vídeo de Windows Media se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="d486d-117">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="d486d-118">Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un codificador de vídeo, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="d486d-118">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="d486d-119">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="d486d-119">Input Formats</span></span>

<span data-ttu-id="d486d-120">El codificador Windows Media Video admite los siguientes subtipos de medios de entrada cuando actúa como DMO.</span><span class="sxs-lookup"><span data-stu-id="d486d-120">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="d486d-121">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="d486d-121">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="d486d-122">MEDIASUBTYPE \_ i420</span><span class="sxs-lookup"><span data-stu-id="d486d-122">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="d486d-123">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="d486d-123">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="d486d-124">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="d486d-124">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="d486d-125">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="d486d-125">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="d486d-126">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="d486d-126">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="d486d-127">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="d486d-127">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="d486d-128">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="d486d-128">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="d486d-129">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d486d-129">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="d486d-130">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="d486d-130">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="d486d-131">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d486d-131">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="d486d-132">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d486d-132">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="d486d-133">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d486d-133">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="d486d-134">fotomovimiento MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="d486d-134">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="d486d-135">El codificador Windows Media Video admite los siguientes subtipos de medios de entrada cuando actúa como MFT.</span><span class="sxs-lookup"><span data-stu-id="d486d-135">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="d486d-136">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="d486d-136">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="d486d-137">MFVideoFormat \_ i420</span><span class="sxs-lookup"><span data-stu-id="d486d-137">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="d486d-138">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="d486d-138">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="d486d-139">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="d486d-139">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="d486d-140">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="d486d-140">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="d486d-141">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="d486d-141">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="d486d-142">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="d486d-142">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="d486d-143">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="d486d-143">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="d486d-144">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d486d-144">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="d486d-145">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="d486d-145">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="d486d-146">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d486d-146">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="d486d-147">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d486d-147">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="d486d-148">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d486d-148">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="d486d-149">fotomovimiento MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="d486d-149">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="d486d-150">Formatos de salida</span><span class="sxs-lookup"><span data-stu-id="d486d-150">Output Formats</span></span>

<span data-ttu-id="d486d-151">En la tabla siguiente se muestran los códigos de cuatro caracteres (FOURCCs) para los tipos de salida admitidos por el codificador Windows Media Video 7/8.</span><span class="sxs-lookup"><span data-stu-id="d486d-151">The following table shows the four-character codes (FOURCCs) for the output types supported by the Windows Media Video 7/8 encoder.</span></span>



| <span data-ttu-id="d486d-152">Category</span><span class="sxs-lookup"><span data-stu-id="d486d-152">Category</span></span>              | <span data-ttu-id="d486d-153">FOURCC</span><span class="sxs-lookup"><span data-stu-id="d486d-153">FOURCC</span></span> |
|-----------------------|--------|
| <span data-ttu-id="d486d-154">Windows Media Video 7</span><span class="sxs-lookup"><span data-stu-id="d486d-154">Windows Media Video 7</span></span> | <span data-ttu-id="d486d-155">"WMV1"</span><span class="sxs-lookup"><span data-stu-id="d486d-155">"WMV1"</span></span> |
| <span data-ttu-id="d486d-156">Windows Media Video 8</span><span class="sxs-lookup"><span data-stu-id="d486d-156">Windows Media Video 8</span></span> | <span data-ttu-id="d486d-157">"WMV2"</span><span class="sxs-lookup"><span data-stu-id="d486d-157">"WMV2"</span></span> |



 

## <a name="properties"></a><span data-ttu-id="d486d-158">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d486d-158">Properties</span></span>

<span data-ttu-id="d486d-159">El codificador Windows Media Video 7/8 admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d486d-159">The Windows Media Video 7/8 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d486d-160">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d486d-160">Property</span></span></th>
<th><span data-ttu-id="d486d-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="d486d-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d486d-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="d486d-163">Especifica la sobrecarga, en bytes por paquete, necesaria para el contenedor que se usa para almacenar el contenido comprimido.</span><span class="sxs-lookup"><span data-stu-id="d486d-163">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="d486d-164">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-164">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-165">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-165">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="d486d-167">Especifica la velocidad media de fotogramas del contenido de vídeo, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="d486d-167">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="d486d-168">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-168">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-169">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d486d-169">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="d486d-171">Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida con la velocidad de bits media (especificada por <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="d486d-171">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="d486d-172">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-172">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-173">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d486d-173">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="d486d-175">Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida en la velocidad de bits máxima (especificada por <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="d486d-175">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="d486d-176">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-176">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-177">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d486d-177">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="d486d-179">Especifica si la secuencia de bits de vídeo codificada contiene un valor de llenado de búfer con cada fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="d486d-179">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="d486d-180">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-180">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-181">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d486d-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d486d-183">Especifica el número de fotogramas de vídeo codificados por el códec.</span><span class="sxs-lookup"><span data-stu-id="d486d-183">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="d486d-184">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-184">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-185">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d486d-185">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d486d-187">Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.</span><span class="sxs-lookup"><span data-stu-id="d486d-187">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="d486d-188">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-188">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-189">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d486d-189">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="d486d-191">Esta propiedad se sustituye por <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d486d-191">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="d486d-193">Especifica la complejidad del algoritmo del codificador.</span><span class="sxs-lookup"><span data-stu-id="d486d-193">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="d486d-194">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-194">Windows Vista and later.</span></span><br />
<span data-ttu-id="d486d-195">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-195">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="d486d-197">Especifica una representación numérica del equilibrio entre la suavidad de movimiento y la calidad de la imagen en la salida del códec.</span><span class="sxs-lookup"><span data-stu-id="d486d-197">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="d486d-198">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-198">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-199">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-199">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="d486d-201">Especifica la plantilla de conformidad del dispositivo a la que se ajusta el contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="d486d-201">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="d486d-202">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-202">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-203">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d486d-203">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="d486d-205">Especifica la plantilla de conformidad del dispositivo que desea usar para la codificación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d486d-205">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="d486d-206">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-206">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-207">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-207">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d486d-209">Especifica el número de fotogramas de vídeo que se han quitado durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="d486d-209">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="d486d-210">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-210">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-211">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d486d-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="d486d-213">Especifica el final de una fase de codificación.</span><span class="sxs-lookup"><span data-stu-id="d486d-213">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="d486d-214">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-214">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-215">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-215">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="d486d-217">Especifica el FOURCC que identifica el codificador que se desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="d486d-217">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="d486d-218">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-218">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-219">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-219">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="d486d-221">Especifica si la salida del códec se entrelazará.</span><span class="sxs-lookup"><span data-stu-id="d486d-221">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="d486d-222">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-222">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-223">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-223">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="d486d-225">Especifica el tiempo máximo, en milisegundos, entre los fotogramas clave de la salida del códec.</span><span class="sxs-lookup"><span data-stu-id="d486d-225">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="d486d-226">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-226">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-227">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-227">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="d486d-229">Especifica el número máximo de pasos admitidos por el códec.</span><span class="sxs-lookup"><span data-stu-id="d486d-229">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="d486d-230">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-230">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-231">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d486d-231">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="d486d-233">Especifica el número de pasos que el códec usará para codificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="d486d-233">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="d486d-234">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-234">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-235">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d486d-235">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d486d-237">Especifica si el codificador genera entradas de fotogramas ficticias en el flujo de bits para los fotogramas duplicados.</span><span class="sxs-lookup"><span data-stu-id="d486d-237">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="d486d-238">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-238">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-239">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-239">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="d486d-241">Especifica QP.</span><span class="sxs-lookup"><span data-stu-id="d486d-241">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="d486d-242">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-242">Windows Vista and later.</span></span><br />
<span data-ttu-id="d486d-243">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-243">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="d486d-245">Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="d486d-245">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d486d-246">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-246">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-247">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d486d-247">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="d486d-249">Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la velocidad de bits variable (VBR) limitada de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="d486d-249">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="d486d-250">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-250">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-251">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d486d-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d486d-253">Especifica el número de fotogramas de vídeo pasados al codificador durante el proceso de codificación.</span><span class="sxs-lookup"><span data-stu-id="d486d-253">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="d486d-254">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-254">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-255">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d486d-255">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="d486d-257">Especifica si el códec usará la codificación de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="d486d-257">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d486d-258">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-258">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-259">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d486d-259">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="d486d-261">Especifica el nivel de calidad real de la codificación de velocidad de bits variable (VBR) basada en la calidad (1-paso).</span><span class="sxs-lookup"><span data-stu-id="d486d-261">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d486d-262">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-262">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-263">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-263">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d486d-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="d486d-265">Especifica la cantidad de contenido, en milisegundos, que puede caber en el búfer del modelo.</span><span class="sxs-lookup"><span data-stu-id="d486d-265">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="d486d-266">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-266">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-267">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d486d-267">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d486d-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d486d-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="d486d-269">Especifica el número de fotogramas de vídeo que se omitieron porque eran duplicados de fotogramas anteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-269">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="d486d-270">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d486d-270">Windows XP and later.</span></span><br />
<span data-ttu-id="d486d-271">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d486d-271">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d486d-272">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d486d-272">Requirements</span></span>



| <span data-ttu-id="d486d-273">Requisito</span><span class="sxs-lookup"><span data-stu-id="d486d-273">Requirement</span></span> | <span data-ttu-id="d486d-274">Value</span><span class="sxs-lookup"><span data-stu-id="d486d-274">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d486d-275">Remoto</span><span class="sxs-lookup"><span data-stu-id="d486d-275">Client</span></span><br/> | <span data-ttu-id="d486d-276">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="d486d-276">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="d486d-277">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d486d-277">Header</span></span><br/> | <dl> <span data-ttu-id="d486d-278"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d486d-278"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="d486d-279">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d486d-279">DLL</span></span><br/>    | <dl> <span data-ttu-id="d486d-280"><dt>Wmvxencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d486d-280"><dt>Wmvxencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d486d-281">Vea también</span><span class="sxs-lookup"><span data-stu-id="d486d-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d486d-282">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="d486d-282">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="d486d-283">Implementación de códecs</span><span class="sxs-lookup"><span data-stu-id="d486d-283">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="d486d-284">GUID de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="d486d-284">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 
