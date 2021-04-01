---
description: El descodificador de vídeo MPEG4 parte 2 descodifica secuencias de vídeo codificadas según el estándar MPEG4 parte 2.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: Descodificador de vídeo MPEG-4 parte 2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275837"
---
# <a name="mpeg-4-part-2-video-decoder"></a><span data-ttu-id="6e8f4-103">Descodificador de vídeo MPEG-4 parte 2</span><span class="sxs-lookup"><span data-stu-id="6e8f4-103">MPEG-4 Part 2 Video Decoder</span></span>

<span data-ttu-id="6e8f4-104">El descodificador de vídeo MPEG4 parte 2 descodifica secuencias de vídeo codificadas según el estándar MPEG4 parte 2.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-104">The MPEG4 Part 2 Video decoder decodes video streams that were encoded according to the MPEG4 Part 2 standard.</span></span>

<span data-ttu-id="6e8f4-105">Puede crear una instancia del descodificador de vídeo MPEG4 Part 2 llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-105">You can create an instance of the MPEG4 Part 2 Video decoder by calling **CoCreateInstance**.</span></span> <span data-ttu-id="6e8f4-106">Para crear una instancia del descodificador que se comporta como un objeto multimedia de DirectX (DMO), use el identificador de clase **CLSID \_ CMpeg4sDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-106">To create an instance of the decoder that behaves as a DirectX Media Object (DMO), use the class identifier **CLSID\_CMpeg4sDecMediaObject**.</span></span> <span data-ttu-id="6e8f4-107">Para crear un Istance del descodificador que se comporta como una transformación de Media Foundation (MFT), use el identificador de clase **CLSID \_ CMpeg4sDecMFT**.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-107">To create an istance of the decoder that behaves as a Media Foundation Transform (MFT), use the class identifier **CLSID\_CMpeg4sDecMFT**.</span></span>

## <a name="input-types"></a><span data-ttu-id="6e8f4-108">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="6e8f4-108">Input Types</span></span>

<span data-ttu-id="6e8f4-109">El descodificador de vídeo MPEG4 parte 2 admite los siguientes tipos de medios de entrada.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-109">The MPEG4 Part 2 Video decoder supports the following input media types.</span></span>

-   <span data-ttu-id="6e8f4-110">MEDIASUBTYPE \_ M4S2</span><span class="sxs-lookup"><span data-stu-id="6e8f4-110">MEDIASUBTYPE\_M4S2</span></span>
-   <span data-ttu-id="6e8f4-111">MEDIASUBTYPE \_ m4s2</span><span class="sxs-lookup"><span data-stu-id="6e8f4-111">MEDIASUBTYPE\_m4s2</span></span>
-   <span data-ttu-id="6e8f4-112">MEDIASUBTYPE \_ MP4V</span><span class="sxs-lookup"><span data-stu-id="6e8f4-112">MEDIASUBTYPE\_MP4V</span></span>
-   <span data-ttu-id="6e8f4-113">MEDIASUBTYPE \_ MP4V</span><span class="sxs-lookup"><span data-stu-id="6e8f4-113">MEDIASUBTYPE\_mp4v</span></span>
-   <span data-ttu-id="6e8f4-114">MEDIASUBTYPE \_ MP4 (desusado)</span><span class="sxs-lookup"><span data-stu-id="6e8f4-114">MEDIASUBTYPE\_MP4S (deprecated)</span></span>
-   <span data-ttu-id="6e8f4-115">MEDIASUBTYPE \_ MP4 (desusado)</span><span class="sxs-lookup"><span data-stu-id="6e8f4-115">MEDIASUBTYPE\_mp4s (deprecated)</span></span>

## <a name="output-types"></a><span data-ttu-id="6e8f4-116">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="6e8f4-116">Output Types</span></span>

<span data-ttu-id="6e8f4-117">El descodificador de vídeo MPEG4 parte 2 admite los siguientes subtipos de medios de salida cuando actúa como DMO.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-117">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="6e8f4-118">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="6e8f4-118">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="6e8f4-119">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="6e8f4-119">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="6e8f4-120">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="6e8f4-120">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="6e8f4-121">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="6e8f4-121">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="6e8f4-122">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="6e8f4-122">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="6e8f4-123">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="6e8f4-123">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="6e8f4-124">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="6e8f4-124">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="6e8f4-125">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="6e8f4-125">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="6e8f4-126">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="6e8f4-126">MEDIASUBTYPE\_ RGB565</span></span>
-   <span data-ttu-id="6e8f4-127">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="6e8f4-127">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="6e8f4-128">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="6e8f4-128">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="6e8f4-129">El descodificador de vídeo MPEG4 parte 2 admite los siguientes subtipos de medios de salida cuando actúa como MFT.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-129">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="6e8f4-130">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="6e8f4-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="6e8f4-131">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="6e8f4-131">MEDIASUBTYPE\_YV12</span></span>

## <a name="formats"></a><span data-ttu-id="6e8f4-132">Formatos</span><span class="sxs-lookup"><span data-stu-id="6e8f4-132">Formats</span></span>

<span data-ttu-id="6e8f4-133">El descodificador de vídeo MPEG4 parte 2 acepta los siguientes formatos.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-133">The MPEG4 Part 2 Video decoder accepts the following formats.</span></span>

-   [<span data-ttu-id="6e8f4-134">**VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="6e8f4-134">**VIDEOINFOHEADER**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   <span data-ttu-id="6e8f4-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span><span class="sxs-lookup"><span data-stu-id="6e8f4-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span></span>
-   [<span data-ttu-id="6e8f4-136">**MFVideoInfo**</span><span class="sxs-lookup"><span data-stu-id="6e8f4-136">**MFVideoInfo**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   <span data-ttu-id="6e8f4-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (solo se usa la parte VIH2 del encabezado).</span><span class="sxs-lookup"><span data-stu-id="6e8f4-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (Only the VIH2 portion of the header is used.)</span></span>

## <a name="interfaces-for-the-dmo"></a><span data-ttu-id="6e8f4-138">Interfaces para DMO</span><span class="sxs-lookup"><span data-stu-id="6e8f4-138">Interfaces for the DMO</span></span>

<span data-ttu-id="6e8f4-139">Si crea una instancia del descodificador de vídeo MPEG4 Part 2 como DMO, el descodificador expone las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-139">If you create an instance of the MPEG4 Part 2 Video decoder as a DMO, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="6e8f4-140">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="6e8f4-140">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="6e8f4-141">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6e8f4-141">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)

<span data-ttu-id="6e8f4-142">Puede obtener una interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) llamando a **CoCreateInstance** y puede obtener una interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) llamando a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-142">You can obtain an [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface by calling **CoCreateInstance**, and you can obtain an [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface by calling **QueryInterface**.</span></span>

## <a name="interfaces-for-the-mft"></a><span data-ttu-id="6e8f4-143">Interfaces para MFT</span><span class="sxs-lookup"><span data-stu-id="6e8f4-143">Interfaces for the MFT</span></span>

<span data-ttu-id="6e8f4-144">Si crea una instancia del descodificador de vídeo MPEG2 parte 2 como MFT, el descodificador expone las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-144">If you create an instance of the MPEG2 Part 2 Video decoder as an MFT, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="6e8f4-145">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="6e8f4-145">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="6e8f4-146">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="6e8f4-146">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="6e8f4-147">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="6e8f4-147">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="6e8f4-148">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="6e8f4-148">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="6e8f4-149">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="6e8f4-149">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="6e8f4-150">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="6e8f4-150">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

<span data-ttu-id="6e8f4-151">Puede obtener un puntero a la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) llamando a **CoCreateInstance** y puede obtener un puntero a la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) llamando a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span><span class="sxs-lookup"><span data-stu-id="6e8f4-151">You can obtain a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface by calling **CoCreateInstance**, and you can obtain a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface by calling [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span></span> <span data-ttu-id="6e8f4-152">Puede obtener un puntero a la interfaz [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) o [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) llamando a **QueryInterface** en MFT.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-152">You can obtain a pointer to the [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) or [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) interface by calling **QueryInterface** on the MFT.</span></span> <span data-ttu-id="6e8f4-153">Puede obtener un puntero a la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) o [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) llamando a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) y pasando el servicio de control de **\_ tasa MF \_ \_** del identificador de servicio.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-153">You can obtain a pointer to the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) or [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and passing the service identifier **MF\_RATE\_CONTROL\_SERVICE**.</span></span>

## <a name="profiles-and-levels"></a><span data-ttu-id="6e8f4-154">Perfiles y niveles</span><span class="sxs-lookup"><span data-stu-id="6e8f4-154">Profiles and Levels</span></span>

<span data-ttu-id="6e8f4-155">La especificación MPEG4 define varios perfiles, cada uno de los cuales especifica las herramientas que un codificador puede utilizar para generar una secuencia codificada.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-155">The MPEG4 specification defines several profiles, each of which specifies the tools that an encoder can use to generate an encoded stream.</span></span> <span data-ttu-id="6e8f4-156">El descodificador de vídeo MPEG4 "part2 admite dos de estos perfiles: perfil visual simple y perfil simple avanzado.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-156">The MPEG4 Part2 Video Decoder supports two of those profiles: Simple Visual Profile and Advanced Simple Profile.</span></span> <span data-ttu-id="6e8f4-157">En otras palabras, el descodificador de vídeo MPEG4 parte 2 puede descodificar flujos codificados según el perfil visual simple o el perfil simple avanzado.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-157">In other words, the MPEG4 Part 2 Video decoder can decode streams that were encoded according to either the Simple Visual Profile or the Advanced Simple Profile.</span></span>

<span data-ttu-id="6e8f4-158">El perfil visual simple admite la transmisión básica de vídeo de velocidad de bits baja en modo progresivo.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-158">The Simple Visual Profile supports basic transmission of low bit-rate video in progressive mode.</span></span> <span data-ttu-id="6e8f4-159">Solo admite imágenes intra y de predicción.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-159">It supports only Intra and Prediction pictures.</span></span> <span data-ttu-id="6e8f4-160">También admite el modo de encabezado corto, que es compatible con versiones anteriores del perfil de línea base H. 263.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-160">It also supports the short header mode, which is backward compatible with the H.263 baseline profile.</span></span> <span data-ttu-id="6e8f4-161">A partir de Windows 10, el descodificador de vídeo MPEG-4 parte 2 también admite H. 263v2 (H. 263 +), que admite tamaños de imagen personalizados.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-161">Starting with Windows 10, the MPEG-4 Part 2 Video Decoder also supports H.263v2 (H.263+) which supports custom picture sizes.</span></span>

<span data-ttu-id="6e8f4-162">El perfil simple avanzado es compatible con todas las herramientas del perfil visual simple y, además, admite vídeo entrelazado, fotogramas B, compensación de movimiento de PEL, tablas de cuantificación adicionales y compensación de movimiento global.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-162">The Advanced Simple Profile supports all the tools of the Simple Visual Profile and, in addition, supports interlaced video, B-frames, quarter-pel motion compensation, additional quantization tables, and global motion compensation.</span></span>

<span data-ttu-id="6e8f4-163">La especificación MPEG4 también define varios niveles, cada uno de los cuales especifica restricciones en el flujo de salida generado por un codificador.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-163">The MPEG4 specification also defines several levels, each of which specifies constraints on the output stream generated by an encoder.</span></span>

<span data-ttu-id="6e8f4-164">En la tabla siguiente se muestran los perfiles y niveles, junto con las resoluciones típicas, que admite el descodificador de vídeo MPEG4 Part 2.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-164">The following table shows the profiles and levels, along with typical resolutions, supported by the MPEG4 Part 2 Video decoder.</span></span>



| <span data-ttu-id="6e8f4-165">Perfil</span><span class="sxs-lookup"><span data-stu-id="6e8f4-165">Profile</span></span>         | <span data-ttu-id="6e8f4-166">Nivel</span><span class="sxs-lookup"><span data-stu-id="6e8f4-166">Level</span></span> | <span data-ttu-id="6e8f4-167">Resolución típica</span><span class="sxs-lookup"><span data-stu-id="6e8f4-167">Typical Resolution</span></span> |
|-----------------|-------|--------------------|
| <span data-ttu-id="6e8f4-168">Objetos visuales simples</span><span class="sxs-lookup"><span data-stu-id="6e8f4-168">Simple Visual</span></span>   | <span data-ttu-id="6e8f4-169">0</span><span class="sxs-lookup"><span data-stu-id="6e8f4-169">0</span></span>     | <span data-ttu-id="6e8f4-170">176 x 144</span><span class="sxs-lookup"><span data-stu-id="6e8f4-170">176 x 144</span></span>          |
| <span data-ttu-id="6e8f4-171">Objetos visuales simples</span><span class="sxs-lookup"><span data-stu-id="6e8f4-171">Simple Visual</span></span>   | <span data-ttu-id="6e8f4-172">1</span><span class="sxs-lookup"><span data-stu-id="6e8f4-172">1</span></span>     | <span data-ttu-id="6e8f4-173">176 x 144</span><span class="sxs-lookup"><span data-stu-id="6e8f4-173">176 x 144</span></span>          |
| <span data-ttu-id="6e8f4-174">Objetos visuales simples</span><span class="sxs-lookup"><span data-stu-id="6e8f4-174">Simple Visual</span></span>   | <span data-ttu-id="6e8f4-175">2</span><span class="sxs-lookup"><span data-stu-id="6e8f4-175">2</span></span>     | <span data-ttu-id="6e8f4-176">352 x 288</span><span class="sxs-lookup"><span data-stu-id="6e8f4-176">352 x 288</span></span>          |
| <span data-ttu-id="6e8f4-177">Objetos visuales simples</span><span class="sxs-lookup"><span data-stu-id="6e8f4-177">Simple Visual</span></span>   | <span data-ttu-id="6e8f4-178">3</span><span class="sxs-lookup"><span data-stu-id="6e8f4-178">3</span></span>     | <span data-ttu-id="6e8f4-179">352 x 288</span><span class="sxs-lookup"><span data-stu-id="6e8f4-179">352 x 288</span></span>          |
| <span data-ttu-id="6e8f4-180">SimpleVisual</span><span class="sxs-lookup"><span data-stu-id="6e8f4-180">SimpleVisual</span></span>    | <span data-ttu-id="6e8f4-181">4a</span><span class="sxs-lookup"><span data-stu-id="6e8f4-181">4a</span></span>    | <span data-ttu-id="6e8f4-182">640 x 480</span><span class="sxs-lookup"><span data-stu-id="6e8f4-182">640 x 480</span></span>          |
| <span data-ttu-id="6e8f4-183">Objetos visuales simples</span><span class="sxs-lookup"><span data-stu-id="6e8f4-183">Simple Visual</span></span>   | <span data-ttu-id="6e8f4-184">5</span><span class="sxs-lookup"><span data-stu-id="6e8f4-184">5</span></span>     | <span data-ttu-id="6e8f4-185">720 x 576</span><span class="sxs-lookup"><span data-stu-id="6e8f4-185">720 x 576</span></span>          |
| <span data-ttu-id="6e8f4-186">Avanzado simple</span><span class="sxs-lookup"><span data-stu-id="6e8f4-186">Advanced Simple</span></span> | <span data-ttu-id="6e8f4-187">0</span><span class="sxs-lookup"><span data-stu-id="6e8f4-187">0</span></span>     | <span data-ttu-id="6e8f4-188">176 x 144</span><span class="sxs-lookup"><span data-stu-id="6e8f4-188">176 x 144</span></span>          |
| <span data-ttu-id="6e8f4-189">Avanzado simple</span><span class="sxs-lookup"><span data-stu-id="6e8f4-189">Advanced Simple</span></span> | <span data-ttu-id="6e8f4-190">1</span><span class="sxs-lookup"><span data-stu-id="6e8f4-190">1</span></span>     | <span data-ttu-id="6e8f4-191">176 x 144</span><span class="sxs-lookup"><span data-stu-id="6e8f4-191">176 x 144</span></span>          |
| <span data-ttu-id="6e8f4-192">Avanzado simple</span><span class="sxs-lookup"><span data-stu-id="6e8f4-192">Advanced Simple</span></span> | <span data-ttu-id="6e8f4-193">2</span><span class="sxs-lookup"><span data-stu-id="6e8f4-193">2</span></span>     | <span data-ttu-id="6e8f4-194">352 x 288</span><span class="sxs-lookup"><span data-stu-id="6e8f4-194">352 x 288</span></span>          |
| <span data-ttu-id="6e8f4-195">Avanzado simple</span><span class="sxs-lookup"><span data-stu-id="6e8f4-195">Advanced Simple</span></span> | <span data-ttu-id="6e8f4-196">3</span><span class="sxs-lookup"><span data-stu-id="6e8f4-196">3</span></span>     | <span data-ttu-id="6e8f4-197">352 x 288</span><span class="sxs-lookup"><span data-stu-id="6e8f4-197">352 x 288</span></span>          |
| <span data-ttu-id="6e8f4-198">Avanzado simple</span><span class="sxs-lookup"><span data-stu-id="6e8f4-198">Advanced Simple</span></span> | <span data-ttu-id="6e8f4-199">3b</span><span class="sxs-lookup"><span data-stu-id="6e8f4-199">3b</span></span>    | <span data-ttu-id="6e8f4-200">352 x 288</span><span class="sxs-lookup"><span data-stu-id="6e8f4-200">352 x 288</span></span>          |
| <span data-ttu-id="6e8f4-201">Avanzado simple</span><span class="sxs-lookup"><span data-stu-id="6e8f4-201">Advanced Simple</span></span> | <span data-ttu-id="6e8f4-202">4</span><span class="sxs-lookup"><span data-stu-id="6e8f4-202">4</span></span>     | <span data-ttu-id="6e8f4-203">352 x 756</span><span class="sxs-lookup"><span data-stu-id="6e8f4-203">352 x 756</span></span>          |
| <span data-ttu-id="6e8f4-204">Avanzado simple</span><span class="sxs-lookup"><span data-stu-id="6e8f4-204">Advanced Simple</span></span> | <span data-ttu-id="6e8f4-205">5</span><span class="sxs-lookup"><span data-stu-id="6e8f4-205">5</span></span>     | <span data-ttu-id="6e8f4-206">720 x 576</span><span class="sxs-lookup"><span data-stu-id="6e8f4-206">720 x 576</span></span>          |



 

<span data-ttu-id="6e8f4-207">Para obtener más información acerca de los perfiles y los niveles, consulte la especificación MPEG4 parte 2 (ISO/IEC 14496-2): tecnología de la información: codificación de objetos de audio visual, parte 2: visual.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-207">For more information about profiles and levels, see the MPEG4 Part 2 specification (ISO/IEC 14496-2): Information technology -- Coding of audio-visual objects -- Part 2: Visual.</span></span>

## <a name="decoder-properties"></a><span data-ttu-id="6e8f4-208">Propiedades del descodificador</span><span class="sxs-lookup"><span data-stu-id="6e8f4-208">Decoder Properties</span></span>

<span data-ttu-id="6e8f4-209">Para establecer las propiedades en el descodificador de vídeo MPEG4 parte 2, use la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) o la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="6e8f4-209">To set properties on the MPEG4 Part 2 Video decoder, use the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface or the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="6e8f4-210">El descodificador de vídeo MPEG4 parte 2 admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-210">The MPEG4 Part 2 Video decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6e8f4-211">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6e8f4-211">Property</span></span></th>
<th><span data-ttu-id="6e8f4-212">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e8f4-212">Description</span></span></th>
<th><span data-ttu-id="6e8f4-213">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="6e8f4-213">Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6e8f4-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e8f4-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span></span></td>
<td><span data-ttu-id="6e8f4-215">Especifica el nivel de energía.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-215">Specifies the power level.</span></span><br/> <dl> <span data-ttu-id="6e8f4-216">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-216">Windows 7.</span></span><br />
<span data-ttu-id="6e8f4-217">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-217">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="6e8f4-218">100</span><span class="sxs-lookup"><span data-stu-id="6e8f4-218">100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e8f4-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e8f4-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span></span></td>
<td><span data-ttu-id="6e8f4-220">Especifica el modo de generación de miniaturas.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-220">Specifies the thumbnail generation mode.</span></span><br/> <dl> <span data-ttu-id="6e8f4-221">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-221">Windows 7.</span></span><br />
<span data-ttu-id="6e8f4-222">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-222">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="6e8f4-223"><strong>VARIANT_FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="6e8f4-223"><strong>VARIANT_FALSE</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="6e8f4-224">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e8f4-224">Remarks</span></span>

<span data-ttu-id="6e8f4-225">Los identificadores únicos globales (GUID) para los subtipos multimedia RGB difieren en función de si un descodificador actúa como un DMO o una MFT.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-225">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="6e8f4-226">Los GUID para los subtipos de medios que no son RGB son los mismos, independientemente de si un descodificador actúa como un DMO o una MFT.</span><span class="sxs-lookup"><span data-stu-id="6e8f4-226">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="6e8f4-227">Para obtener información sobre los GUID que representan subtipos de medios, consulte [tipos de medios](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="6e8f4-227">For information about the GUIDs that represent media subtypes, see [Media Types](media-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e8f4-228">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e8f4-228">Requirements</span></span>



| <span data-ttu-id="6e8f4-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e8f4-229">Requirement</span></span> | <span data-ttu-id="6e8f4-230">Value</span><span class="sxs-lookup"><span data-stu-id="6e8f4-230">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8f4-231">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e8f4-231">Minimum supported client</span></span><br/> | <span data-ttu-id="6e8f4-232">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e8f4-232">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6e8f4-233">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e8f4-233">Minimum supported server</span></span><br/> | <span data-ttu-id="6e8f4-234">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e8f4-234">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6e8f4-235">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e8f4-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e8f4-236"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e8f4-236"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="6e8f4-237">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e8f4-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e8f4-238"><dt>MP4SDecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e8f4-238"><dt>MP4SDecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e8f4-239">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e8f4-239">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e8f4-240">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="6e8f4-240">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
