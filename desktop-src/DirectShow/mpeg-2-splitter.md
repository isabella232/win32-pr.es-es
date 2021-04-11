---
description: Separador MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Separador MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274765"
---
# <a name="mpeg-2-splitter"></a><span data-ttu-id="5e501-103">Separador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="5e501-103">MPEG-2 Splitter</span></span>

<span data-ttu-id="5e501-104">A partir de Microsoft® Windows® XP, el filtro de divisores MPEG-2 está en desuso.</span><span class="sxs-lookup"><span data-stu-id="5e501-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="5e501-105">En su lugar, use el [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="5e501-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

<span data-ttu-id="5e501-106">En plataformas anteriores, use el divisor MPEG-2 para secuencias de programas MPEG-2 entregadas en modo de extracción que contienen al menos uno de los siguientes tipos de secuencias: vídeo MPEG-2; Audio MPEG-2; La codificación de audio AC3 tal y como se define para el vídeo de DVD; o PCM audio codificado tal y como se define para el vídeo en DVD.</span><span class="sxs-lookup"><span data-stu-id="5e501-106">On earlier platforms, use the MPEG-2 Splitter for MPEG-2 program streams delivered in pull mode that contain at least one of the following stream types: MPEG-2 video; MPEG-2 audio; AC3 audio encoded as defined for DVD video; or PCM audio encoded as defined for DVD video.</span></span> <span data-ttu-id="5e501-107">Este filtro analiza los flujos, crea un PIN de salida para cada flujo y envía los paquetes de audio o vídeo comprimidos MPEG a un filtro de descodificador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="5e501-107">This filter parses the streams, creates an output pin for each stream, and outputs the compressed MPEG audio or video packets to an MPEG-2 decoder filter.</span></span>

<span data-ttu-id="5e501-108">En el caso de los flujos de programa y transporte entregados en modo de inserciones, use el [demultiplexador MPEG-2](mpeg-2-demultiplexer.md)en todas las plataformas.</span><span class="sxs-lookup"><span data-stu-id="5e501-108">For program and transport streams delivered in push-mode, use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md), on all platforms.</span></span>

> [!Note]  
> <span data-ttu-id="5e501-109">El separador MPEG-2 no admite búsquedas con precisión de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="5e501-109">The MPEG-2 Splitter does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e501-110">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="5e501-110">Filter Interfaces</span></span></td>
<td><span data-ttu-id="5e501-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e501-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e501-112">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="5e501-112">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="5e501-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="5e501-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="5e501-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span><span class="sxs-lookup"><span data-stu-id="5e501-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span></span></li>
<li><span data-ttu-id="5e501-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="5e501-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e501-116">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="5e501-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="5e501-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e501-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e501-118">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="5e501-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="5e501-119">Depende del tipo de flujo.</span><span class="sxs-lookup"><span data-stu-id="5e501-119">Depends on the stream type.</span></span> <span data-ttu-id="5e501-120">Consulte <a href="mpeg-2-splitter-media-types.md">tipos de medios de divisor MPEG-2</a></span><span class="sxs-lookup"><span data-stu-id="5e501-120">See <a href="mpeg-2-splitter-media-types.md">MPEG-2 Splitter Media Types</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e501-121">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="5e501-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="5e501-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e501-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e501-123">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="5e501-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="5e501-124">CLSID_MMSPLITTER</span><span class="sxs-lookup"><span data-stu-id="5e501-124">CLSID_MMSPLITTER</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e501-125">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="5e501-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="5e501-126">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5e501-126">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e501-127">Executable</span><span class="sxs-lookup"><span data-stu-id="5e501-127">Executable</span></span></td>
<td><span data-ttu-id="5e501-128">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="5e501-128">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e501-129"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="5e501-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="5e501-130">MERIT_NORMAL + 1</span><span class="sxs-lookup"><span data-stu-id="5e501-130">MERIT_NORMAL + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e501-131"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="5e501-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="5e501-132">CLSID_AudioInputDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="5e501-132">CLSID_AudioInputDeviceCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5e501-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e501-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e501-134">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="5e501-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="5e501-135">Usar el divisor MPEG-2</span><span class="sxs-lookup"><span data-stu-id="5e501-135">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



