---
description: Filtro del navegador de DVD
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Filtro del navegador de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53bb1c6f46e3dd846ffccda32fece2c2f04c8992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495143"
---
# <a name="dvd-navigator-filter"></a><span data-ttu-id="26dd9-103">Filtro del navegador de DVD</span><span class="sxs-lookup"><span data-stu-id="26dd9-103">DVD Navigator Filter</span></span>

<span data-ttu-id="26dd9-104">El filtro del navegador de DVD es el filtro de origen de un gráfico de filtros de reproducción DVD-Video.</span><span class="sxs-lookup"><span data-stu-id="26dd9-104">The DVD Navigator filter is the source filter for a DVD-Video playback filter graph.</span></span> <span data-ttu-id="26dd9-105">Abre todos los archivos necesarios en un volumen de DVD-Video, navega por los archivos linear DVD-Video. VOB y analiza la secuencia de programa MPEG-2 resultante, dividiendo el flujo en tres terminales de salida (vídeo, audio, subimagen).</span><span class="sxs-lookup"><span data-stu-id="26dd9-105">It opens all necessary files in a DVD-Video volume, navigates through the linear DVD-Video .vob files, and parses the resulting MPEG-2 program stream, splitting the stream into three (video, audio, subpicture) output pins.</span></span>

<span data-ttu-id="26dd9-106">El filtro de navegador de DVD también implementa las interfaces [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) y [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) que permiten a una aplicación de reproducción de DVD controlar DVD-Video reproducción.</span><span class="sxs-lookup"><span data-stu-id="26dd9-106">The DVD Navigator filter also implements the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interfaces that enable a DVD playback application to control DVD-Video playback.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26dd9-107">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="26dd9-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="26dd9-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26dd9-109">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="26dd9-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="26dd9-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="26dd9-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26dd9-111">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="26dd9-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="26dd9-112">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="26dd9-112">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26dd9-113">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="26dd9-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="26dd9-114">Tipos base:</span><span class="sxs-lookup"><span data-stu-id="26dd9-114">Base types:</span></span><br/>
<ul>
<li><span data-ttu-id="26dd9-115">Vídeo: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-115">Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="26dd9-116">Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-116">Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="26dd9-117">Subimagen: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-117">Subpicture: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="26dd9-118">Tipos extendidos:</span><span class="sxs-lookup"><span data-stu-id="26dd9-118">Extended types:</span></span><br/> <span data-ttu-id="26dd9-119">Vídeo:</span><span class="sxs-lookup"><span data-stu-id="26dd9-119">Video:</span></span><br/>
<ul>
<li><span data-ttu-id="26dd9-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="26dd9-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="26dd9-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
</ul>
<span data-ttu-id="26dd9-123">Audio:</span><span class="sxs-lookup"><span data-stu-id="26dd9-123">Audio:</span></span><br/>
<ul>
<li><span data-ttu-id="26dd9-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="26dd9-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="26dd9-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
</ul>
<span data-ttu-id="26dd9-127">Subimagen:</span><span class="sxs-lookup"><span data-stu-id="26dd9-127">Subpicture:</span></span><br/>
<ul>
<li><span data-ttu-id="26dd9-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="26dd9-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="26dd9-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="26dd9-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="26dd9-131">Para habilitar los tipos extendidos, llame a <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2:: SetOption</strong></a> y establezca el valor de</span><span class="sxs-lookup"><span data-stu-id="26dd9-131">To enable the extended types, call <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2::SetOption</strong></a> and set the</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26dd9-132">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="26dd9-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="26dd9-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="26dd9-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26dd9-134">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="26dd9-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="26dd9-135">CLSID_DVDNavigator</span><span class="sxs-lookup"><span data-stu-id="26dd9-135">CLSID_DVDNavigator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26dd9-136">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="26dd9-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="26dd9-137">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="26dd9-137">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26dd9-138">Executable</span><span class="sxs-lookup"><span data-stu-id="26dd9-138">Executable</span></span></td>
<td><span data-ttu-id="26dd9-139">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="26dd9-139">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26dd9-140"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="26dd9-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="26dd9-141">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="26dd9-141">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26dd9-142"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="26dd9-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="26dd9-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="26dd9-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="26dd9-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26dd9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26dd9-145">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="26dd9-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="26dd9-146">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="26dd9-146">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




