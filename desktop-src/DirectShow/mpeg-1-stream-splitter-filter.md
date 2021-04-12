---
description: Filtro de divisor de secuencia MPEG-1
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: Filtro de divisor de secuencia MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152569"
---
# <a name="mpeg-1-stream-splitter-filter"></a><span data-ttu-id="e8625-103">Filtro de divisor de secuencia MPEG-1</span><span class="sxs-lookup"><span data-stu-id="e8625-103">MPEG-1 Stream Splitter Filter</span></span>

<span data-ttu-id="e8625-104">Este filtro divide un flujo del sistema MPEG-1 en sus secuencias de audio y vídeo de componentes.</span><span class="sxs-lookup"><span data-stu-id="e8625-104">This filter splits an MPEG-1 system stream into its component audio and video streams.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8625-105">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="e8625-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="e8625-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8625-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8625-107">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="e8625-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="e8625-108">Tipo principal: MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="e8625-108">Major type: MEDIATYPE_Stream</span></span><br/> <span data-ttu-id="e8625-109">Subtipos</span><span class="sxs-lookup"><span data-stu-id="e8625-109">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="e8625-110">MEDIASUBTYPE_MPEG1System</span><span class="sxs-lookup"><span data-stu-id="e8625-110">MEDIASUBTYPE_MPEG1System</span></span></li>
<li><span data-ttu-id="e8625-111">MEDIASUBTYPE_MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="e8625-111">MEDIASUBTYPE_MPEG1VideoCD</span></span></li>
<li><span data-ttu-id="e8625-112">MEDIASUBTYPE_Audio</span><span class="sxs-lookup"><span data-stu-id="e8625-112">MEDIASUBTYPE_Audio</span></span></li>
<li><span data-ttu-id="e8625-113">MEDIASUBTYPE_Video</span><span class="sxs-lookup"><span data-stu-id="e8625-113">MEDIASUBTYPE_Video</span></span></li>
</ul>
<span data-ttu-id="e8625-114">Consulte <a href="mpeg-1-media-types.md"> <strong>tipos de medios MPEG-1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8625-114">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8625-115">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="e8625-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="e8625-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8625-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8625-117">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="e8625-117">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="e8625-118">Tipo principal: MEDIATYPE_Audio o MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="e8625-118">Major type: MEDIATYPE_Audio or MEDIATYPE_Video</span></span><br/> <span data-ttu-id="e8625-119">Subtipo: MEDIASUBTYPE_MPEG1Payload o MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="e8625-119">Subtype: MEDIASUBTYPE_MPEG1Payload or MEDIASUBTYPE_MPEG1Packet</span></span><br/> <span data-ttu-id="e8625-120">Consulte <a href="mpeg-1-media-types.md"> <strong>tipos de medios MPEG-1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8625-120">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8625-121">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="e8625-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="e8625-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8625-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8625-123">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="e8625-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="e8625-124">CLSID_MPEG1Splitter</span><span class="sxs-lookup"><span data-stu-id="e8625-124">CLSID_MPEG1Splitter</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8625-125">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="e8625-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="e8625-126">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="e8625-126">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8625-127">Executable</span><span class="sxs-lookup"><span data-stu-id="e8625-127">Executable</span></span></td>
<td><span data-ttu-id="e8625-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="e8625-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8625-129"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="e8625-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="e8625-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="e8625-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8625-131"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="e8625-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="e8625-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="e8625-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="e8625-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8625-133">Remarks</span></span>

<span data-ttu-id="e8625-134">Este archivo admite el modo de extracción solo a través de [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ; no admite el modo de extracción.</span><span class="sxs-lookup"><span data-stu-id="e8625-134">This file supports pull mode via [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) only; it does not support push mode.</span></span>

<span data-ttu-id="e8625-135">Dado que el contenido de MPEG-1 no está indexado, la búsqueda puede ser muy aproximada.</span><span class="sxs-lookup"><span data-stu-id="e8625-135">Because MPEG-1 content is not indexed, seeking can be very approximate.</span></span> <span data-ttu-id="e8625-136">Normalmente, es conveniente para una secuencia de sistema MPEG-1 de velocidad de bits fija (que normalmente se genera por el hardware del CD de vídeo).</span><span class="sxs-lookup"><span data-stu-id="e8625-136">It is usually good for a fixed bitrate MPEG-1 system stream (which is usually hardware generated for video CD).</span></span>

<span data-ttu-id="e8625-137">El filtro admite la interfaz [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) para recuperar los metadatos ID3.</span><span class="sxs-lookup"><span data-stu-id="e8625-137">The filter supports the [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) interface for retrieving ID3 metadata.</span></span>

<span data-ttu-id="e8625-138">No todos los ejemplos de MPEG tienen marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e8625-138">Not all MPEG samples have time stamps.</span></span> <span data-ttu-id="e8625-139">La falta de una marca de tiempo en una muestra de MPEG no es un error.</span><span class="sxs-lookup"><span data-stu-id="e8625-139">The lack of a time stamp on an MPEG sample is not an error.</span></span> <span data-ttu-id="e8625-140">En el caso de los desarrolladores de filtros, esto significa que no debe devolver un código de error del método **Receive** del PIN de entrada si se produce un error en [**IMediaSample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) .</span><span class="sxs-lookup"><span data-stu-id="e8625-140">For filter developers, this means that you should not return an error code from your input pin's **Receive** method if [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) fails.</span></span> <span data-ttu-id="e8625-141">Si **Receive** devuelve cualquier valor distinto de S \_ OK, hará que el divisor deje de enviar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="e8625-141">If **Receive** returns any value other than S\_OK, it will cause the splitter to stop sending samples.</span></span>

<span data-ttu-id="e8625-142">Si el archivo contiene una secuencia de vídeo, el divisor de secuencias MPEG-1 admite búsquedas por número de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="e8625-142">If the file contains a video stream, the MPEG-1 Stream Splitter supports seeking by frame number.</span></span> <span data-ttu-id="e8625-143">Para habilitar la búsqueda basada en fotogramas, llame a [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) en el [Administrador de gráficos de filtro](filter-graph-manager.md) con el **\_ \_ marco de formato de hora** de valor.</span><span class="sxs-lookup"><span data-stu-id="e8625-143">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8625-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8625-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8625-145">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="e8625-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




