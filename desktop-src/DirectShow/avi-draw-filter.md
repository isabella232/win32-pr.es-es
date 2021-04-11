---
description: Filtro de dibujo AVI
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: Filtro de dibujo AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6d6b318b7a1f7e762fc0806186114fb9256f5c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152056"
---
# <a name="avi-draw-filter"></a><span data-ttu-id="1da53-103">Filtro de dibujo AVI</span><span class="sxs-lookup"><span data-stu-id="1da53-103">AVI Draw Filter</span></span>

<span data-ttu-id="1da53-104">El filtro de extracción AVI se extrae automáticamente en un gráfico de reproducción en lugar del [descompresor AVI](avi-decompressor-filter.md) cuando el vídeo se envía a un monitor de televisión NTSC externo.</span><span class="sxs-lookup"><span data-stu-id="1da53-104">The AVI Draw filter is pulled automatically into a playback graph instead of the [AVI Decompressor](avi-decompressor-filter.md) when video is being output to an external NTSC television monitor.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1da53-105">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="1da53-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="1da53-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="1da53-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1da53-107">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="1da53-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="1da53-108">Tipo principal: MEDIATYPE_VideoSubtypes:</span><span class="sxs-lookup"><span data-stu-id="1da53-108">Major Type: MEDIATYPE_VideoSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="1da53-109">MEDIASUBTYPE_MJPG</span><span class="sxs-lookup"><span data-stu-id="1da53-109">MEDIASUBTYPE_MJPG</span></span></li>
<li><span data-ttu-id="1da53-110">MEDIASUBTYPE_TVMJ</span><span class="sxs-lookup"><span data-stu-id="1da53-110">MEDIASUBTYPE_TVMJ</span></span></li>
<li><span data-ttu-id="1da53-111">MEDIASUBTYPE_WAKE</span><span class="sxs-lookup"><span data-stu-id="1da53-111">MEDIASUBTYPE_WAKE</span></span></li>
<li><span data-ttu-id="1da53-112">MEDIASUBTYPE_CFCC</span><span class="sxs-lookup"><span data-stu-id="1da53-112">MEDIASUBTYPE_CFCC</span></span></li>
<li><span data-ttu-id="1da53-113">MEDIASUBTYPE_IJPG</span><span class="sxs-lookup"><span data-stu-id="1da53-113">MEDIASUBTYPE_IJPG</span></span></li>
<li><span data-ttu-id="1da53-114">MEDIASUBTYPE_Plum</span><span class="sxs-lookup"><span data-stu-id="1da53-114">MEDIASUBTYPE_Plum</span></span></li>
<li><span data-ttu-id="1da53-115">MEDIASUBTYPE_DVCS</span><span class="sxs-lookup"><span data-stu-id="1da53-115">MEDIASUBTYPE_DVCS</span></span></li>
<li><span data-ttu-id="1da53-116">MEDIASUBTYPE_DVSD</span><span class="sxs-lookup"><span data-stu-id="1da53-116">MEDIASUBTYPE_DVSD</span></span></li>
<li><span data-ttu-id="1da53-117">MEDIASUBTYPE_MDVF</span><span class="sxs-lookup"><span data-stu-id="1da53-117">MEDIASUBTYPE_MDVF</span></span></li>
<li><span data-ttu-id="1da53-118">Tipo de formato: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="1da53-118">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1da53-119">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="1da53-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="1da53-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1da53-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1da53-121">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="1da53-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="1da53-122">MEDIATYPE_Video, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="1da53-122">MEDIATYPE_Video, MEDIASUBTYPE_NULL</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1da53-123">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="1da53-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="1da53-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1da53-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1da53-125">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="1da53-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="1da53-126">CLSID_AVIDraw</span><span class="sxs-lookup"><span data-stu-id="1da53-126">CLSID_AVIDraw</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1da53-127">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="1da53-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="1da53-128">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="1da53-128">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1da53-129">Executable</span><span class="sxs-lookup"><span data-stu-id="1da53-129">Executable</span></span></td>
<td><span data-ttu-id="1da53-130">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1da53-130">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1da53-131"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="1da53-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="1da53-132">MERIT_NORMAL + 100</span><span class="sxs-lookup"><span data-stu-id="1da53-132">MERIT_NORMAL + 100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1da53-133"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="1da53-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="1da53-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="1da53-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1da53-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1da53-135">Remarks</span></span>

<span data-ttu-id="1da53-136">Puesto que el filtro de dibujo AVI y el [filtro de captura VFW](vfw-capture-filter.md) se conectan al mismo hardware, no pueden estar en el mismo gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="1da53-136">Since the AVI Draw filter and the [VFW Capture Filter](vfw-capture-filter.md) both connect to the same hardware, they cannot be in the same filter graph.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1da53-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1da53-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1da53-138">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="1da53-138">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




