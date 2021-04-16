---
description: Filtro de descodificador de vídeo MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Filtro de descodificador de vídeo MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7f48e441226dee33ef949219e8008e15c9d711
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686290"
---
# <a name="mpeg-1-video-decoder-filter"></a><span data-ttu-id="2cba7-103">Filtro de descodificador de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="2cba7-103">MPEG-1 Video Decoder Filter</span></span>

<span data-ttu-id="2cba7-104">Descodifica vídeo MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="2cba7-104">Decodes MPEG-1 video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2cba7-105">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="2cba7-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="2cba7-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cba7-107">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="2cba7-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="2cba7-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="2cba7-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span></span><br/> <span data-ttu-id="2cba7-109">Los siguientes subtipos son válidos:</span><span class="sxs-lookup"><span data-stu-id="2cba7-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="2cba7-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span></span></li>
<li><span data-ttu-id="2cba7-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2cba7-112">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="2cba7-112">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="2cba7-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"> <strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="2cba7-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cba7-114">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="2cba7-114">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="2cba7-115">Tipo principal: <strong>MEDIATYPE_Video</strong>,</span><span class="sxs-lookup"><span data-stu-id="2cba7-115">Major type: <strong>MEDIATYPE_Video</strong>,</span></span><br/> <span data-ttu-id="2cba7-116">Tipo de formato: <strong>FORMAT_VideoInfo</strong> o <strong>FORMAT_VideoInfo2</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-116">Format type: <strong>FORMAT_VideoInfo</strong> or <strong>FORMAT_VideoInfo2</strong></span></span><br/> <span data-ttu-id="2cba7-117">Subtipos</span><span class="sxs-lookup"><span data-stu-id="2cba7-117">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="2cba7-118"><strong>MEDIASUBTYPE_RGB24</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-118"><strong>MEDIASUBTYPE_RGB24</strong></span></span></li>
<li><span data-ttu-id="2cba7-119"><strong>MEDIASUBTYPE_RGB32</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-119"><strong>MEDIASUBTYPE_RGB32</strong></span></span></li>
<li><span data-ttu-id="2cba7-120"><strong>MEDIASUBTYPE_RGB8</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-120"><strong>MEDIASUBTYPE_RGB8</strong></span></span></li>
<li><span data-ttu-id="2cba7-121"><strong>MEDIASUBTYPE_RGB555</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-121"><strong>MEDIASUBTYPE_RGB555</strong></span></span></li>
<li><span data-ttu-id="2cba7-122"><strong>MEDIASUBTYPE_RGB565</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-122"><strong>MEDIASUBTYPE_RGB565</strong></span></span></li>
<li><span data-ttu-id="2cba7-123"><strong>MEDIASUBTYPE_UYVY</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-123"><strong>MEDIASUBTYPE_UYVY</strong></span></span></li>
<li><span data-ttu-id="2cba7-124"><strong>MEDIASUBTYPE_Y41P</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-124"><strong>MEDIASUBTYPE_Y41P</strong></span></span></li>
<li><span data-ttu-id="2cba7-125"><strong>MEDIASUBTYPE_YUY2</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-125"><strong>MEDIASUBTYPE_YUY2</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2cba7-126">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="2cba7-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="2cba7-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2cba7-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cba7-128">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="2cba7-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="2cba7-129"><strong>CLSID_CMpegVideoCodec</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-129"><strong>CLSID_CMpegVideoCodec</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2cba7-130">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="2cba7-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="2cba7-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span><span class="sxs-lookup"><span data-stu-id="2cba7-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cba7-132">Executable</span><span class="sxs-lookup"><span data-stu-id="2cba7-132">Executable</span></span></td>
<td><span data-ttu-id="2cba7-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="2cba7-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2cba7-134"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="2cba7-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="2cba7-135">0x40000001</span><span class="sxs-lookup"><span data-stu-id="2cba7-135">0x40000001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cba7-136"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="2cba7-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="2cba7-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="2cba7-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="2cba7-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2cba7-138">Remarks</span></span>

<span data-ttu-id="2cba7-139">Este filtro puede descodificar en una superficie DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="2cba7-139">This filter can decode into a DirectDraw Surface.</span></span> <span data-ttu-id="2cba7-140">El filtro usa MMX si el equipo es compatible con MMX.</span><span class="sxs-lookup"><span data-stu-id="2cba7-140">The filter uses MMX if the machine supports MMX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cba7-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cba7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cba7-142">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="2cba7-142">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




