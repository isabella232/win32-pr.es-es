---
description: Filtro de WAVE parser
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filtro de WAVE parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb30465a25ab3a6eef190b5fbecd4a4878c2744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669955"
---
# <a name="wave-parser-filter"></a><span data-ttu-id="78986-103">Filtro de WAVE parser</span><span class="sxs-lookup"><span data-stu-id="78986-103">WAVE Parser Filter</span></span>

<span data-ttu-id="78986-104">El filtro del analizador de onda analiza los datos de audio con formato WAV de los archivos. wav,. au o. AIF.</span><span class="sxs-lookup"><span data-stu-id="78986-104">The WAVE Parser filter parses WAV-format audio data from .wav, .au, or .aif files.</span></span> <span data-ttu-id="78986-105">El filtro de nivel superior debe ser el filtro de [origen de archivo asincrónico](file-source--async--filter.md) , el filtro de [origen de archivo URL](file-source--url--filter.md) o un filtro de origen asincrónico de terceros compatible que contenga datos de audio WAV.</span><span class="sxs-lookup"><span data-stu-id="78986-105">The upstream filter must be the [Async File Source](file-source--async--filter.md) filter, [URL File Source](file-source--url--filter.md) filter, or a compatible third-party asynchronous source filter that contains WAV audio data.</span></span> <span data-ttu-id="78986-106">El flujo de salida es datos de audio, que puede conectarse directamente a un filtro de representación de audio o a un filtro de transformación de audio que intervenga.</span><span class="sxs-lookup"><span data-stu-id="78986-106">The output stream is audio data, which you can connect directly to an audio rendering filter or to an intervening audio transform filter.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="78986-107">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="78986-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="78986-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span><span class="sxs-lookup"><span data-stu-id="78986-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78986-109">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="78986-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="78986-110">Tipo principal: MEDIATYPE_StreamThe siguientes subtipos son válidos:</span><span class="sxs-lookup"><span data-stu-id="78986-110">Major type: MEDIATYPE_StreamThe following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="78986-111">MEDIASUBTYPE_AIFF</span><span class="sxs-lookup"><span data-stu-id="78986-111">MEDIASUBTYPE_AIFF</span></span></li>
<li><span data-ttu-id="78986-112">MEDIASUBTYPE_AU</span><span class="sxs-lookup"><span data-stu-id="78986-112">MEDIASUBTYPE_AU</span></span></li>
<li><span data-ttu-id="78986-113">MEDIASUBTYPE_WAVE</span><span class="sxs-lookup"><span data-stu-id="78986-113">MEDIASUBTYPE_WAVE</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78986-114">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="78986-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="78986-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="78986-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78986-116">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="78986-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="78986-117">Tipo principal: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM u otro tipo de compresión.</span><span class="sxs-lookup"><span data-stu-id="78986-117">Major type: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM or other compression type.</span></span> <span data-ttu-id="78986-118">(Consulte <a href="audio-subtypes.md"><strong>subtipos de audio</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="78986-118">(See <a href="audio-subtypes.md"><strong>Audio Subtypes</strong></a>.)</span></span><br/> <span data-ttu-id="78986-119">Tipo de formato: FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="78986-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78986-120">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="78986-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="78986-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="78986-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78986-122">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="78986-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="78986-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span><span class="sxs-lookup"><span data-stu-id="78986-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78986-124">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="78986-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="78986-125">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="78986-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78986-126">Executable</span><span class="sxs-lookup"><span data-stu-id="78986-126">Executable</span></span></td>
<td><span data-ttu-id="78986-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="78986-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78986-128"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="78986-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="78986-129">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="78986-129">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78986-130"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="78986-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="78986-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="78986-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="78986-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78986-132">Remarks</span></span>

<span data-ttu-id="78986-133">Este filtro admite los siguientes tipos de archivo:</span><span class="sxs-lookup"><span data-stu-id="78986-133">This filter supports the following file types:</span></span>

-   <span data-ttu-id="78986-134">ONDA (. wav)</span><span class="sxs-lookup"><span data-stu-id="78986-134">WAVE (.wav)</span></span>
-   <span data-ttu-id="78986-135">AIFF y AIFF-C (. AIF)</span><span class="sxs-lookup"><span data-stu-id="78986-135">AIFF and AIFF-C (.aif)</span></span>
-   <span data-ttu-id="78986-136">AU (. au)</span><span class="sxs-lookup"><span data-stu-id="78986-136">AU (.au)</span></span>

<span data-ttu-id="78986-137">Sin embargo, tiene las siguientes limitaciones en el formato de audio:</span><span class="sxs-lookup"><span data-stu-id="78986-137">However, it has the following limitations on the audio format:</span></span>

-   <span data-ttu-id="78986-138">El audio debe ser PCM lineal de 8 o 16 bits.</span><span class="sxs-lookup"><span data-stu-id="78986-138">The audio must be 8-bit or 16-bit linear PCM.</span></span>
-   <span data-ttu-id="78986-139">En el caso de los archivos AIFF-C, el audio se debe descomprimir, en el orden de bytes big-endian (tipo de compresión ' NONE ').</span><span class="sxs-lookup"><span data-stu-id="78986-139">For AIFF-C files, the audio must be uncompressed, in big-endian byte order (compression type 'NONE').</span></span>

## <a name="related-topics"></a><span data-ttu-id="78986-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78986-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78986-141">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="78986-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




