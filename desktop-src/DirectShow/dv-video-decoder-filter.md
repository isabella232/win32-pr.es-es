---
description: Filtro de descodificador de vídeo DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Filtro de descodificador de vídeo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6baab43d4a369cb16d92974a0e6e469c914961bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536501"
---
# <a name="dv-video-decoder-filter"></a><span data-ttu-id="45c29-103">Filtro de descodificador de vídeo DV</span><span class="sxs-lookup"><span data-stu-id="45c29-103">DV Video Decoder Filter</span></span>

<span data-ttu-id="45c29-104">Este filtro descodifica una secuencia de vídeo digital (DV) en vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="45c29-104">This filter decodes a digital video (DV) stream into uncompressed video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45c29-105">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="45c29-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="45c29-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="45c29-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45c29-107">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="45c29-107">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="45c29-108">MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="45c29-108">MEDIATYPE_Video</span></span></li>
<li><span data-ttu-id="45c29-109">MEDIASUBTYPE_dvsd</span><span class="sxs-lookup"><span data-stu-id="45c29-109">MEDIASUBTYPE_dvsd</span></span></li>
<li><span data-ttu-id="45c29-110">FORMAT_VideoInfo, FORMAT_DvInfo</span><span class="sxs-lookup"><span data-stu-id="45c29-110">FORMAT_VideoInfo, FORMAT_DvInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45c29-111">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="45c29-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="45c29-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="45c29-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45c29-113">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="45c29-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="45c29-114"><strong>Tipo principal</strong>:<strong>subtipos</strong>de MEDIATYPE_Video:</span><span class="sxs-lookup"><span data-stu-id="45c29-114"><strong>Major type</strong>: MEDIATYPE_Video<strong>Subtypes</strong>:</span></span><br/>
<ul>
<li><span data-ttu-id="45c29-115">MEDIASUBTYPE_YUY2</span><span class="sxs-lookup"><span data-stu-id="45c29-115">MEDIASUBTYPE_YUY2</span></span></li>
<li><span data-ttu-id="45c29-116">MEDIASUBTYPE_UYVY</span><span class="sxs-lookup"><span data-stu-id="45c29-116">MEDIASUBTYPE_UYVY</span></span></li>
<li><span data-ttu-id="45c29-117">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="45c29-117">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="45c29-118">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="45c29-118">MEDIASUBTYPE_RGB32</span></span></li>
<li><span data-ttu-id="45c29-119">MEDIASUBTYPE_ARGB32</span><span class="sxs-lookup"><span data-stu-id="45c29-119">MEDIASUBTYPE_ARGB32</span></span></li>
<li><span data-ttu-id="45c29-120">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="45c29-120">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="45c29-121">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="45c29-121">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="45c29-122">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="45c29-122">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="45c29-123">MEDIASUBTYPE_Y41P</span><span class="sxs-lookup"><span data-stu-id="45c29-123">MEDIASUBTYPE_Y41P</span></span></li>
</ul><span data-ttu-id="45c29-124">
<strong>Tipos de formato</strong>:</span><span class="sxs-lookup"><span data-stu-id="45c29-124">
<strong>Format types</strong>:</span></span><br/> <span data-ttu-id="45c29-125">Format_VideoInfo, Format_VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="45c29-125">Format_VideoInfo, Format_VideoInfo2</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45c29-126">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="45c29-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="45c29-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="45c29-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45c29-128">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="45c29-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="45c29-129">CLSID_DVVideoCodec</span><span class="sxs-lookup"><span data-stu-id="45c29-129">CLSID_DVVideoCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45c29-130">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="45c29-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="45c29-131">CLSID_DVDecPropertiesPage</span><span class="sxs-lookup"><span data-stu-id="45c29-131">CLSID_DVDecPropertiesPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45c29-132">Executable</span><span class="sxs-lookup"><span data-stu-id="45c29-132">Executable</span></span></td>
<td><span data-ttu-id="45c29-133">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="45c29-133">qdv.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45c29-134"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="45c29-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="45c29-135">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="45c29-135">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45c29-136"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="45c29-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="45c29-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="45c29-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="45c29-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45c29-138">Remarks</span></span>

<span data-ttu-id="45c29-139">Use la interfaz [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) para establecer la resolución de descodificación en Full, Half size, Quarter size o un tamaño de un octavo.</span><span class="sxs-lookup"><span data-stu-id="45c29-139">Use the [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) interface to set the decoding resolution to full, half size, quarter size, or one-eighth size.</span></span>

<span data-ttu-id="45c29-140">**Entrelazado**: las versiones anteriores del descodificador siempre desentrelazan el vídeo.</span><span class="sxs-lookup"><span data-stu-id="45c29-140">**Interlacing**: Earlier versions of the decoder always deinterlace the video.</span></span> <span data-ttu-id="45c29-141">A partir de DirectX 9,0, el descodificador de vídeo DV puede conservar el entrelazado.</span><span class="sxs-lookup"><span data-stu-id="45c29-141">As of DirectX 9.0, the DV Video Decoder can preserve the interlacing.</span></span> <span data-ttu-id="45c29-142">Esto permite que el vídeo entrelazado esté desentrelazado por el procesador de mezcla de vídeo (VMR), para mejorar la calidad de representación.</span><span class="sxs-lookup"><span data-stu-id="45c29-142">This enables the interlaced video to be deinterlaced by the Video Mixing Renderer (VMR), for improved rendering quality.</span></span> <span data-ttu-id="45c29-143">Para usar esta característica, el filtro de nivel inferior debe admitir formatos de [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , indicados por ese formato \_ de valor VideoInfo2 en el miembro **formatType** de la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="45c29-143">To use this feature, the downstream filter must support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, indicated by that value Format\_VideoInfo2 in the **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="45c29-144">En la salida de la resolución completa, las marcas de desentrelazado (**dwInterlace**) de la estructura **VIDEOINFOHEADER2** se establecen en `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` , que indica campos entrelazados.</span><span class="sxs-lookup"><span data-stu-id="45c29-144">At full resolution output, the deinterlacing flags (**dwInterlace**) in the **VIDEOINFOHEADER2** structure are set to `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave`, indicating interlaced fields.</span></span> <span data-ttu-id="45c29-145">A media resolución o inferior, **dwInterlace** se establece en cero, lo que indica fotogramas progresivos.</span><span class="sxs-lookup"><span data-stu-id="45c29-145">At half resolution or lower, **dwInterlace** is set to zero, indicating progressive frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45c29-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45c29-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45c29-147">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="45c29-147">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="45c29-148">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="45c29-148">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




