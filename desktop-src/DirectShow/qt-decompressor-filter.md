---
description: Filtro de descompresor de QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Filtro de descompresor de QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e586eb9d65ee00509f4a434f3283bd762d535b26
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494860"
---
# <a name="qt-decompressor-filter"></a><span data-ttu-id="ed93d-103">Filtro de descompresor de QT</span><span class="sxs-lookup"><span data-stu-id="ed93d-103">QT Decompressor Filter</span></span>

<span data-ttu-id="ed93d-104">Este componente se ha quitado de Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="ed93d-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="ed93d-105">Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ed93d-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="ed93d-106">El filtro de descompresor de QT descomprime el vídeo de Apple® QuickTime® 2,0.</span><span class="sxs-lookup"><span data-stu-id="ed93d-106">The QT Decompressor filter decompresses Apple® QuickTime® 2.0 video.</span></span> <span data-ttu-id="ed93d-107">Este formato se usa normalmente en archivos QuickTime más antiguos.</span><span class="sxs-lookup"><span data-stu-id="ed93d-107">This format is typically used in older QuickTime files.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed93d-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="ed93d-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="ed93d-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed93d-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed93d-110">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="ed93d-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="ed93d-111">MEDIATYPE_Video, FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="ed93d-111">MEDIATYPE_Video, FORMAT_VideoInfo</span></span><br/> <span data-ttu-id="ed93d-112">Los siguientes subtipos son válidos:</span><span class="sxs-lookup"><span data-stu-id="ed93d-112">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="ed93d-113">MEDIASUBTYPE_QTRpza</span><span class="sxs-lookup"><span data-stu-id="ed93d-113">MEDIASUBTYPE_QTRpza</span></span></li>
<li><span data-ttu-id="ed93d-114">MEDIASUBTYPE_QTSmc</span><span class="sxs-lookup"><span data-stu-id="ed93d-114">MEDIASUBTYPE_QTSmc</span></span></li>
<li><span data-ttu-id="ed93d-115">MEDIASUBTYPE_QTRle</span><span class="sxs-lookup"><span data-stu-id="ed93d-115">MEDIASUBTYPE_QTRle</span></span></li>
<li><span data-ttu-id="ed93d-116">MEDIASUBTYPE_QTJpeg</span><span class="sxs-lookup"><span data-stu-id="ed93d-116">MEDIASUBTYPE_QTJpeg</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed93d-117">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="ed93d-117">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="ed93d-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed93d-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed93d-119">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="ed93d-119">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="ed93d-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="ed93d-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed93d-121">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="ed93d-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="ed93d-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed93d-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed93d-123">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="ed93d-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="ed93d-124">CLSID_QTDec</span><span class="sxs-lookup"><span data-stu-id="ed93d-124">CLSID_QTDec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed93d-125">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="ed93d-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="ed93d-126">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ed93d-126">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed93d-127">Executable</span><span class="sxs-lookup"><span data-stu-id="ed93d-127">Executable</span></span></td>
<td><span data-ttu-id="ed93d-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="ed93d-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed93d-129"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="ed93d-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="ed93d-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="ed93d-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed93d-131"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="ed93d-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="ed93d-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="ed93d-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ed93d-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed93d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed93d-134">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="ed93d-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




