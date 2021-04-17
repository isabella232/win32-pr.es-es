---
description: Este filtro desmultiplexa los flujos de transporte y programa MPEG-2 que se entregan en modo de inserciones.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: Demultiplexador MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea71727dc273bd0dc5d65ac49b28385b4898067
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686342"
---
# <a name="mpeg-2-demultiplexer"></a><span data-ttu-id="0c212-103">Demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="0c212-103">MPEG-2 Demultiplexer</span></span>

<span data-ttu-id="0c212-104">Este filtro desmultiplexa los flujos de transporte y programa MPEG-2 que se entregan en modo de inserciones.</span><span class="sxs-lookup"><span data-stu-id="0c212-104">This filter demultiplexes MPEG-2 transport and program streams that are delivered in push-mode.</span></span> <span data-ttu-id="0c212-105">A partir de Windows XP, este filtro también admite secuencias de programa en el modo de extracción (reproducción de archivos).</span><span class="sxs-lookup"><span data-stu-id="0c212-105">Starting in Windows XP, this filter also supports program streams in pull mode (file playback).</span></span> <span data-ttu-id="0c212-106">En plataformas anteriores, use el filtro de [divisor de MPEG-2](mpeg-2-splitter.md) para los flujos de programa en el modo de extracción.</span><span class="sxs-lookup"><span data-stu-id="0c212-106">On earlier platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter for program streams in pull mode.</span></span> <span data-ttu-id="0c212-107">Este filtro se puede usar en cualquier tipo de gráfico de filtros, incluido un gráfico de filtros de TV digital BDA.</span><span class="sxs-lookup"><span data-stu-id="0c212-107">This filter can be used in any type of filter graph, including a BDA digital TV filter graph.</span></span>

> [!Note]  
> <span data-ttu-id="0c212-108">El desmultiplexador MPEG-2 no admite búsquedas con precisión de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="0c212-108">The MPEG-2 Demultiplexer does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c212-109">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="0c212-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="0c212-110">Todos los modos:</span><span class="sxs-lookup"><span data-stu-id="0c212-110">All modes:</span></span><br/>
<ul>
<li><span data-ttu-id="0c212-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c212-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="0c212-112"><strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="0c212-112"><strong>ISpecifyPropertyPages</strong></span></span></li>
</ul>
<span data-ttu-id="0c212-113">Solo modo de inserciones:</span><span class="sxs-lookup"><span data-stu-id="0c212-113">Push mode only:</span></span><br/>
<ul>
<li><span data-ttu-id="0c212-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c212-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="0c212-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c212-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span></span></li>
<li><span data-ttu-id="0c212-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c212-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c212-117">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="0c212-117">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="0c212-118">Tipo principal: MEDIATYPE_STREAM</span><span class="sxs-lookup"><span data-stu-id="0c212-118">Major type: MEDIATYPE_STREAM</span></span><br/> <span data-ttu-id="0c212-119">Subtipo</span><span class="sxs-lookup"><span data-stu-id="0c212-119">Subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="0c212-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="0c212-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="0c212-121">MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="0c212-121">MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="0c212-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="0c212-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="0c212-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span><span class="sxs-lookup"><span data-stu-id="0c212-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span></span></li>
</ul>
<span data-ttu-id="0c212-124">Para obtener más información, consulte <a href="mpeg-2-demultiplexer-media-types.md"><strong>tipos de medios de desmultiplexado MPEG-2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0c212-124">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c212-125">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="0c212-125">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="0c212-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c212-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c212-127">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="0c212-127">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="0c212-128">Los flujos elementales de audio y vídeo deben tener un tipo principal de MEDIATYPE_Audio o MEDIATYPE_Video.</span><span class="sxs-lookup"><span data-stu-id="0c212-128">Audio and video elementary streams must have a major type of MEDIATYPE_Audio or MEDIATYPE_Video.</span></span><br/> <span data-ttu-id="0c212-129">Para obtener más información, consulte <a href="mpeg-2-demultiplexer-media-types.md"><strong>tipos de medios de desmultiplexado MPEG-2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0c212-129">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c212-130">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="0c212-130">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="0c212-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>modo de solo envío: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c212-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>Push mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span></span><br/> <span data-ttu-id="0c212-132">Solo el modo de extracción: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c212-132">Pull mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c212-133">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="0c212-133">Filter CLSID</span></span></td>
<td><span data-ttu-id="0c212-134">CLSID_MPEG2Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="0c212-134">CLSID_MPEG2Demultiplexer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c212-135">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="0c212-135">Property Page CLSID</span></span></td>
<td><span data-ttu-id="0c212-136">Solo está disponible para pruebas.</span><span class="sxs-lookup"><span data-stu-id="0c212-136">Available for testing only.</span></span> <span data-ttu-id="0c212-137">Usar la interfaz <strong>ISpecifyPropertyPages</strong> para tener acceso a las páginas de propiedades</span><span class="sxs-lookup"><span data-stu-id="0c212-137">Use the <strong>ISpecifyPropertyPages</strong> interface to access the property pages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c212-138">Executable</span><span class="sxs-lookup"><span data-stu-id="0c212-138">Executable</span></span></td>
<td><span data-ttu-id="0c212-139">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="0c212-139">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c212-140"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="0c212-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="0c212-141">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="0c212-141">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c212-142"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="0c212-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="0c212-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="0c212-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="0c212-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c212-144">Remarks</span></span>

<span data-ttu-id="0c212-145">Para generar secuencias elementales de audio y vídeo, el Demux debe recibir los flujos PCR y SCR.</span><span class="sxs-lookup"><span data-stu-id="0c212-145">To output audio and video elementary streams, the demux must receive the PCR and SCR streams.</span></span> <span data-ttu-id="0c212-146">En el lado de entrada, esto significa que una secuencia de transporte debe contener las tablas PAT y PMT que definen el PID para el flujo de PCR. los flujos de programa y deben contener al menos un encabezado de paquete.</span><span class="sxs-lookup"><span data-stu-id="0c212-146">On the input side, this means a transport stream must contain the PAT and PMT tables that define the PID for the PCR stream; and program streams must contain at least one pack header.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c212-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c212-147">Requirements</span></span>



| <span data-ttu-id="0c212-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c212-148">Requirement</span></span> | <span data-ttu-id="0c212-149">Value</span><span class="sxs-lookup"><span data-stu-id="0c212-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0c212-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c212-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0c212-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0c212-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0c212-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c212-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0c212-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c212-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c212-154">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="0c212-154">End of server support</span></span><br/>    | <span data-ttu-id="0c212-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c212-155">Windows Server 2003 R2</span></span><br/>                          |



## <a name="see-also"></a><span data-ttu-id="0c212-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c212-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c212-157">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="0c212-157">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="0c212-158">Usar el demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="0c212-158">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




