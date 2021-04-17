---
description: Filtro contenedor ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro contenedor ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686413"
---
# <a name="acm-wrapper-filter"></a><span data-ttu-id="3d7d4-103">Filtro contenedor ACM</span><span class="sxs-lookup"><span data-stu-id="3d7d4-103">ACM Wrapper Filter</span></span>

<span data-ttu-id="3d7d4-104">El filtro contenedor ACM permite a los códecs del administrador de compresión de audio (ACM) unirse a un gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-104">The ACM Wrapper filter enables Audio Compression Manager (ACM) codecs to join a filter graph.</span></span> <span data-ttu-id="3d7d4-105">Puede actuar como un filtro de descompresión o como un filtro de compresión.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-105">It can act either as a decompression filter or as a compression filter.</span></span>

<span data-ttu-id="3d7d4-106">Como filtro de descompresión, el contenedor ACM aparece en la categoría "filtros de DirectShow" (CLSID \_ LegacyAmFilterCategory) y tiene un mérito de mérito \_ normal.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-106">As a decompression filter, the ACM Wrapper appears in the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory) and has a merit of MERIT\_NORMAL.</span></span> <span data-ttu-id="3d7d4-107">El tipo de medio de conexión en el PIN de entrada determina qué códec usa el filtro.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-107">The connection media type on the input pin determines which codec the filter uses.</span></span> <span data-ttu-id="3d7d4-108">Normalmente, la aplicación no necesita agregar el filtro al gráfico de filtro; lo extrae automáticamente el administrador de gráficos de filtro cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-108">Typically, the application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span> <span data-ttu-id="3d7d4-109">La descompresión solo es para audio PCM.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-109">Decompression is only to PCM audio.</span></span>

<span data-ttu-id="3d7d4-110">Como filtro de compresión, el contenedor ACM aparece en la categoría "compresores de audio" (CLSID \_ AudioCompressorCategory) y tiene un mérito de mérito \_ \_ no \_ utilizado.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-110">As a compression filter, the ACM Wrapper appears in the "Audio Compressors" category (CLSID\_AudioCompressorCategory) and has a merit of MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="3d7d4-111">Cada códec aparece como una instancia independiente.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-111">Each codec appears as a separate instance.</span></span> <span data-ttu-id="3d7d4-112">Para la compresión, no se puede crear directamente el filtro con CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-112">For compression, you cannot directly create the filter with CoCreateInstance.</span></span> <span data-ttu-id="3d7d4-113">En su lugar, debe usar el enumerador de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-113">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="3d7d4-114">Para obtener más información, vea [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="3d7d4-114">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d7d4-115">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="3d7d4-115">Filter interfaces</span></span></td>
<td><span data-ttu-id="3d7d4-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3d7d4-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d7d4-117">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="3d7d4-117">Input pin media types</span></span></td>
<td><span data-ttu-id="3d7d4-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="3d7d4-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d7d4-119">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="3d7d4-119">Input pin interfaces</span></span></td>
<td><span data-ttu-id="3d7d4-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d7d4-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d7d4-121">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="3d7d4-121">Output pin media types</span></span></td>
<td><span data-ttu-id="3d7d4-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM FORMAT_WaveFormatEx. es posible cualquier combinación de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3d7d4-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Any combination of the following are possible:</span></span><br/>
<ul>
<li><span data-ttu-id="3d7d4-123">Muestras por segundo (kHz): 44,1, 22,05, 11,025 o 8,0.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-123">Samples per second (kHz): 44.1, 22.05, 11.025, or 8.0.</span></span></li>
<li><span data-ttu-id="3d7d4-124">Canales: estéreo o mono.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-124">Channels: Stereo or mono.</span></span></li>
<li><span data-ttu-id="3d7d4-125">Bits por muestra: 8 o 16.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-125">Bits per sample: 8 or 16.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d7d4-126">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="3d7d4-126">Output pin interfaces</span></span></td>
<td><span data-ttu-id="3d7d4-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d7d4-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d7d4-128">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="3d7d4-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="3d7d4-129">CLSID_ACMWrapper</span><span class="sxs-lookup"><span data-stu-id="3d7d4-129">CLSID_ACMWrapper</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d7d4-130">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="3d7d4-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="3d7d4-131">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3d7d4-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d7d4-132">Executable</span><span class="sxs-lookup"><span data-stu-id="3d7d4-132">Executable</span></span></td>
<td><span data-ttu-id="3d7d4-133">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="3d7d4-133">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d7d4-134"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="3d7d4-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="3d7d4-135">MERIT_NORMAL o MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="3d7d4-135">MERIT_NORMAL or MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d7d4-136"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="3d7d4-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="3d7d4-137">CLSID_LegacyAmFilterCategory o CLSID_AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="3d7d4-137">CLSID_LegacyAmFilterCategory or CLSID_AudioCompressorCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3d7d4-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d7d4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d7d4-139">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d7d4-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




