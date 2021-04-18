---
description: El codificador de pantalla de Windows Media Video 9 está optimizado para codificar capturas de pantalla secuenciales desde monitores de equipos.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Codificador de pantalla de Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709104"
---
# <a name="windows-media-video-9-screen-encoder"></a><span data-ttu-id="d34c1-103">Codificador de pantalla de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="d34c1-103">Windows Media Video 9 Screen Encoder</span></span>

<span data-ttu-id="d34c1-104">El codificador de pantalla de Windows Media Video 9 está optimizado para codificar capturas de pantalla secuenciales desde monitores de equipos.</span><span class="sxs-lookup"><span data-stu-id="d34c1-104">The Windows Media Video 9 Screen encoder is optimized for encoding sequential screen shots from computer monitors.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="d34c1-105">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="d34c1-105">Class Identifier</span></span>

<span data-ttu-id="d34c1-106">El identificador de clase (CLSID) del codificador de pantalla de Windows Media Video 9 se representa mediante la constante **\_ CMSSCEncMediaObject2 de CLSID**.</span><span class="sxs-lookup"><span data-stu-id="d34c1-106">The class identifier (CLSID) for the Windows Media Video 9 Screen encoder is represented by the constant **CLSID\_CMSSCEncMediaObject2**.</span></span> <span data-ttu-id="d34c1-107">Puede crear una instancia del codificador llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="d34c1-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="d34c1-108">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="d34c1-108">Input Types</span></span>

<span data-ttu-id="d34c1-109">El codificador de pantalla de la versión 9 admite los siguientes tipos de entrada cuando se usa como un objeto multimedia de DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="d34c1-109">The following input types are supported by the Version 9 Screen encoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="d34c1-110">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="d34c1-110">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="d34c1-111">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d34c1-111">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="d34c1-112">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="d34c1-112">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="d34c1-113">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d34c1-113">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="d34c1-114">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d34c1-114">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="d34c1-115">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d34c1-115">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="d34c1-116">El codificador de pantalla de la versión 9 admite los siguientes tipos de entrada cuando se usa como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="d34c1-116">The following input types are supported by the Version 9 Screen encoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="d34c1-117">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="d34c1-117">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="d34c1-118">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d34c1-118">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="d34c1-119">MFVideoFormat \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="d34c1-119">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="d34c1-120">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d34c1-120">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="d34c1-121">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d34c1-121">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="d34c1-122">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d34c1-122">MFVideoFormat\_RGB8</span></span>

## <a name="output-types"></a><span data-ttu-id="d34c1-123">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="d34c1-123">Output Types</span></span>

<span data-ttu-id="d34c1-124">El código de cuatro caracteres (FOURCC) para el contenido codificado en pantalla de la versión 9 de Windows Media Video es "MSS2".</span><span class="sxs-lookup"><span data-stu-id="d34c1-124">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="d34c1-125">El codificador de pantalla de la versión 9 admite los siguientes tipos de salida.</span><span class="sxs-lookup"><span data-stu-id="d34c1-125">The following output types are supported by the Version 9 Screen encoder.</span></span>

-   <span data-ttu-id="d34c1-126">MEDIASUBTYPE \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="d34c1-126">MEDIASUBTYPE\_MSS2</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="d34c1-127">Propiedades del codificador</span><span class="sxs-lookup"><span data-stu-id="d34c1-127">Encoder Properties</span></span>

<span data-ttu-id="d34c1-128">El codificador de pantalla de Windows Media Video 9 admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d34c1-128">The Windows Media Video 9 Screen encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d34c1-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d34c1-129">Property</span></span></th>
<th><span data-ttu-id="d34c1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d34c1-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d34c1-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span></span></td>
<td><span data-ttu-id="d34c1-132">Especifica la sobrecarga, en bytes por paquete, necesaria para el contenedor que se usa para almacenar el contenido comprimido.</span><span class="sxs-lookup"><span data-stu-id="d34c1-132">Specifies the overhead, in bytes per packet, required for the container that is used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="d34c1-133">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-133">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-134">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-134">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span></span></td>
<td><span data-ttu-id="d34c1-136">Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida con la velocidad de bits media (especificada por <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span><span class="sxs-lookup"><span data-stu-id="d34c1-136">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span></span><br/> <dl> <span data-ttu-id="d34c1-137">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-137">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d34c1-138">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d34c1-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span></span></td>
<td><span data-ttu-id="d34c1-140">Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida en la velocidad de bits máxima (especificada por <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span><span class="sxs-lookup"><span data-stu-id="d34c1-140">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span></span><br/> <dl> <span data-ttu-id="d34c1-141">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-141">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-142">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d34c1-142">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span></span></td>
<td><span data-ttu-id="d34c1-144">Especifica si la secuencia de bits de vídeo codificada contiene un valor de llenado de búfer con cada fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="d34c1-144">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="d34c1-145">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-145">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-146">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-146">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d34c1-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span></span></td>
<td><span data-ttu-id="d34c1-148">Especifica el número de fotogramas de vídeo codificados por el códec.</span><span class="sxs-lookup"><span data-stu-id="d34c1-148">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="d34c1-149">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-149">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-150">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-150">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span></span></td>
<td><span data-ttu-id="d34c1-152">Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.</span><span class="sxs-lookup"><span data-stu-id="d34c1-152">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="d34c1-153">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-153">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-154">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-154">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d34c1-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span></span></td>
<td><span data-ttu-id="d34c1-156">Esta propiedad se sustituye por <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span><span class="sxs-lookup"><span data-stu-id="d34c1-156">This property is superseded by <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span></span></td>
<td><span data-ttu-id="d34c1-158">Especifica la complejidad del algoritmo del codificador.</span><span class="sxs-lookup"><span data-stu-id="d34c1-158">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="d34c1-159">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="d34c1-160">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-160">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d34c1-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span></span></td>
<td><span data-ttu-id="d34c1-162">Especifica una representación numérica del equilibrio entre la suavidad de movimiento y la calidad de la imagen en la salida del códec.</span><span class="sxs-lookup"><span data-stu-id="d34c1-162">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="d34c1-163">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-163">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-164">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-164">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span></span></td>
<td><span data-ttu-id="d34c1-166">Especifica el número de fotogramas de vídeo que se han quitado durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="d34c1-166">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="d34c1-167">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-167">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-168">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-168">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d34c1-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span></span></td>
<td><span data-ttu-id="d34c1-170">Especifica el final de una fase de codificación.</span><span class="sxs-lookup"><span data-stu-id="d34c1-170">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="d34c1-171">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-171">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-172">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-172">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span></span></td>
<td><span data-ttu-id="d34c1-174">Especifica el FOURCC que identifica el codificador que se desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="d34c1-174">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="d34c1-175">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-175">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-176">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d34c1-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span></span></td>
<td><span data-ttu-id="d34c1-178">Especifica el tiempo máximo, en milisegundos, entre los fotogramas clave de la salida del códec.</span><span class="sxs-lookup"><span data-stu-id="d34c1-178">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="d34c1-179">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-179">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-180">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-180">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span></span></td>
<td><span data-ttu-id="d34c1-182">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d34c1-182">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d34c1-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span></span></td>
<td><span data-ttu-id="d34c1-184">Especifica el número máximo de pasos admitidos por el códec.</span><span class="sxs-lookup"><span data-stu-id="d34c1-184">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="d34c1-185">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-185">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-186">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-186">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span></span></td>
<td><span data-ttu-id="d34c1-188">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-188">Windows XP and later.</span></span> <span data-ttu-id="d34c1-189">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d34c1-189">Read/write.</span></span><br/> <span data-ttu-id="d34c1-190">Especifica el número de pasos que el códec usará para codificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="d34c1-190">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="d34c1-191">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-191">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-192">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d34c1-192">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d34c1-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span></span></td>
<td><span data-ttu-id="d34c1-194">Especifica QP.</span><span class="sxs-lookup"><span data-stu-id="d34c1-194">Specifies QP.</span></span> <span data-ttu-id="d34c1-195">Los valores posibles son de 1,0 a 31,0.</span><span class="sxs-lookup"><span data-stu-id="d34c1-195">Possible values are 1.0 through 31.0.</span></span><br/> <dl> <span data-ttu-id="d34c1-196">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-196">Windows Vista and later.</span></span><br />
<span data-ttu-id="d34c1-197">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-197">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span></span></td>
<td><span data-ttu-id="d34c1-199">Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="d34c1-199">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d34c1-200">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-200">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-201">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d34c1-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d34c1-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span></span></td>
<td><span data-ttu-id="d34c1-203">Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de dos pasos restringidos.</span><span class="sxs-lookup"><span data-stu-id="d34c1-203">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d34c1-204">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-204">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-205">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d34c1-205">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span></span></td>
<td><span data-ttu-id="d34c1-207">Especifica el número de fotogramas de vídeo pasados al codificador durante el proceso de codificación.</span><span class="sxs-lookup"><span data-stu-id="d34c1-207">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="d34c1-208">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-208">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-209">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-209">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d34c1-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span></span></td>
<td><span data-ttu-id="d34c1-211">Especifica si el códec usará la codificación de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="d34c1-211">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d34c1-212">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-212">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-213">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d34c1-213">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span></span></td>
<td><span data-ttu-id="d34c1-215">Especifica el nivel de calidad real de la codificación de velocidad de bits variable (VBR) basada en la calidad (1-paso).</span><span class="sxs-lookup"><span data-stu-id="d34c1-215">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d34c1-216">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-216">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-217">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-217">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d34c1-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span></span></td>
<td><span data-ttu-id="d34c1-219">La cantidad de contenido, en milisegundos, que puede caber en el búfer del modelo.</span><span class="sxs-lookup"><span data-stu-id="d34c1-219">The amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="d34c1-220">Windows XP y versiones posteriores,</span><span class="sxs-lookup"><span data-stu-id="d34c1-220">Windows XP and later,</span></span><br />
<span data-ttu-id="d34c1-221">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-221">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d34c1-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="d34c1-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span></span></td>
<td><span data-ttu-id="d34c1-223">Especifica el número de fotogramas de vídeo que se omitieron porque eran duplicados de fotogramas anteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-223">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="d34c1-224">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d34c1-224">Windows XP and later.</span></span><br />
<span data-ttu-id="d34c1-225">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d34c1-225">Read-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="d34c1-226">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d34c1-226">Remarks</span></span>

<span data-ttu-id="d34c1-227">Un objeto de codificador de pantalla expone la interfaz **IMediaObject** para que el objeto pueda usarse como un objeto multimedia de DirectX (DMO) y expone la interfaz **IMFTransform** para que el objeto se pueda usar como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="d34c1-227">A screen encoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="d34c1-228">Un codificador de pantalla se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d34c1-228">A screen encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="d34c1-229">En la tabla siguiente se muestran las condiciones en las que un codificador de pantalla se comporta como un DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="d34c1-229">The following table shows the conditions under which a screen encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="d34c1-230">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d34c1-230">Operating system</span></span>            | <span data-ttu-id="d34c1-231">Comportamiento del codificador</span><span class="sxs-lookup"><span data-stu-id="d34c1-231">Encoder behavior</span></span>                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d34c1-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d34c1-232">Windows XP</span></span>                  | <span data-ttu-id="d34c1-233">Un codificador de pantalla de Windows Media siempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="d34c1-233">A Windows Media Screen encoder always behaves as a DMO.</span></span>                                                                                             |
| <span data-ttu-id="d34c1-234">Windows Vista y Windows 7</span><span class="sxs-lookup"><span data-stu-id="d34c1-234">Windows Vista and Windows 7</span></span> | <span data-ttu-id="d34c1-235">De forma predeterminada, un codificador de pantalla de Windows Media se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="d34c1-235">By default, a Windows Media Screen encoder behaves as a DMO.</span></span> <span data-ttu-id="d34c1-236">Si obtiene una interfaz **IMFTransform** en un codificador de pantalla, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="d34c1-236">If you obtain an **IMFTransform** interface on a screen encoder, it behaves as an MFT.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d34c1-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d34c1-237">Requirements</span></span>



| <span data-ttu-id="d34c1-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="d34c1-238">Requirement</span></span> | <span data-ttu-id="d34c1-239">Value</span><span class="sxs-lookup"><span data-stu-id="d34c1-239">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d34c1-240">Remoto</span><span class="sxs-lookup"><span data-stu-id="d34c1-240">Client</span></span><br/> | <span data-ttu-id="d34c1-241">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="d34c1-241">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="d34c1-242">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d34c1-242">Header</span></span><br/> | <dl> <span data-ttu-id="d34c1-243"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d34c1-243"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="d34c1-244">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d34c1-244">DLL</span></span><br/>    | <dl> <span data-ttu-id="d34c1-245"><dt>Wmvsencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d34c1-245"><dt>Wmvsencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d34c1-246">Vea también</span><span class="sxs-lookup"><span data-stu-id="d34c1-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34c1-247">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="d34c1-247">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="d34c1-248">Implementación de códecs</span><span class="sxs-lookup"><span data-stu-id="d34c1-248">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="d34c1-249">Usar el códec de pantalla de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="d34c1-249">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="d34c1-250">Descodificador de pantalla de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="d34c1-250">Windows Media Video 9 Screen Decoder</span></span>](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




