---
description: Filtro de analizador de películas QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtro de analizador de películas QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a046e143487a1455aeeb125910bbf4452b4f947
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359989"
---
# <a name="quicktime-movie-parser-filter"></a><span data-ttu-id="68ba2-103">Filtro de analizador de películas QuickTime</span><span class="sxs-lookup"><span data-stu-id="68ba2-103">QuickTime Movie Parser Filter</span></span>

<span data-ttu-id="68ba2-104">Este componente se ha quitado de Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="68ba2-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="68ba2-105">Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="68ba2-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="68ba2-106">El filtro del analizador de películas de QuickTime divide los datos de Apple® QuickTime® en secuencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="68ba2-106">The QuickTime Movie Parser filter splits Apple® QuickTime® data into audio and video streams.</span></span> <span data-ttu-id="68ba2-107">Admite QuickTime 2,0 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="68ba2-107">It supports QuickTime 2.0 and earlier.</span></span> <span data-ttu-id="68ba2-108">El PIN de entrada se conecta a un filtro de origen como el filtro de [origen de archivo asincrónico](file-source--async--filter.md) o el filtro de origen de archivo de la [dirección URL](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="68ba2-108">The input pin connects to a source filter such as the [Async File Source](file-source--async--filter.md) filter or the [URL File Source](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="68ba2-109">El analizador utiliza el filtro de descompresor [AVI](avi-decompressor-filter.md) o [descompresor QT](qt-decompressor-filter.md) para descomprimir archivos QuickTime.</span><span class="sxs-lookup"><span data-stu-id="68ba2-109">The Parser uses the [AVI Decompressor](avi-decompressor-filter.md) or [QT Decompressor](qt-decompressor-filter.md) filter to decompress QuickTime files.</span></span> <span data-ttu-id="68ba2-110">El filtro crea un PIN de salida para el flujo de vídeo y un PIN de salida para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="68ba2-110">The filter creates one output pin for the video stream and one output pin for the audio stream.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68ba2-111">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="68ba2-111">Filter Interfaces</span></span></td>
<td><span data-ttu-id="68ba2-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="68ba2-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68ba2-113">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="68ba2-113">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="68ba2-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span><span class="sxs-lookup"><span data-stu-id="68ba2-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68ba2-115">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="68ba2-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="68ba2-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="68ba2-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68ba2-117">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="68ba2-117">Output Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="68ba2-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="68ba2-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></li>
<li><span data-ttu-id="68ba2-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="68ba2-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68ba2-120">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="68ba2-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="68ba2-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="68ba2-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68ba2-122">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="68ba2-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="68ba2-123">CLSID_QuickTimeParser</span><span class="sxs-lookup"><span data-stu-id="68ba2-123">CLSID_QuickTimeParser</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68ba2-124">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="68ba2-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="68ba2-125">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="68ba2-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68ba2-126">Executable</span><span class="sxs-lookup"><span data-stu-id="68ba2-126">Executable</span></span></td>
<td><span data-ttu-id="68ba2-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="68ba2-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68ba2-128"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="68ba2-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="68ba2-129">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="68ba2-129">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68ba2-130"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="68ba2-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="68ba2-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="68ba2-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="68ba2-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68ba2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68ba2-133">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="68ba2-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



