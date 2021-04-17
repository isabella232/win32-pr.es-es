---
description: Usar el divisor MPEG-2
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Usar el divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667850"
---
# <a name="using-the-mpeg-2-splitter"></a><span data-ttu-id="7831c-103">Usar el divisor MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7831c-103">Using the MPEG-2 Splitter</span></span>

> [!Note]  
> <span data-ttu-id="7831c-104">A partir de Microsoft® Windows® XP, el filtro de divisores MPEG-2 está en desuso.</span><span class="sxs-lookup"><span data-stu-id="7831c-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="7831c-105">En su lugar, use el [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="7831c-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

 

<span data-ttu-id="7831c-106">El filtro de divisor de MPEG-2 admite la reproducción en modo de extracción de secuencias de programas MPEG-2 que contienen al menos uno de los siguientes tipos de secuencias.</span><span class="sxs-lookup"><span data-stu-id="7831c-106">The MPEG-2 Splitter filter supports pull-mode playback of MPEG-2 program streams that contain at least one of the following stream types.</span></span>

-   <span data-ttu-id="7831c-107">Vídeo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7831c-107">MPEG-2 video</span></span>
-   <span data-ttu-id="7831c-108">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7831c-108">MPEG-2 audio</span></span>
-   <span data-ttu-id="7831c-109">Audio Dolby AC-3 codificado tal y como se define para DVD-Video</span><span class="sxs-lookup"><span data-stu-id="7831c-109">Dolby AC-3 audio encoded as defined for DVD-Video</span></span>
-   <span data-ttu-id="7831c-110">LPCM (código de pulso lineal modulado) codificado de audio como definido para DVD-Video</span><span class="sxs-lookup"><span data-stu-id="7831c-110">LPCM (Linear Pulse Code Modulated) audio encoded as defined for DVD-Video</span></span>

<span data-ttu-id="7831c-111">Para obtener una lista de los tipos de medios que admite el separador MPEG-2, consulte [tipos de medios de divisor MPEG-2](mpeg-2-splitter-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="7831c-111">For a list of media types that the MPEG-2 Splitter supports, see [MPEG-2 Splitter Media Types](mpeg-2-splitter-media-types.md).</span></span>

<span data-ttu-id="7831c-112">El divisor MPEG-2 no analiza las secuencias de transporte.</span><span class="sxs-lookup"><span data-stu-id="7831c-112">The MPEG-2 Splitter does not parse transport streams.</span></span> <span data-ttu-id="7831c-113">Use el filtro de desmultiplexador MPEG-2 para las secuencias de transporte (solo en modo de extracción).</span><span class="sxs-lookup"><span data-stu-id="7831c-113">Use the MPEG-2 Demultiplexer filter for transport streams (push mode only).</span></span>

<span data-ttu-id="7831c-114">**Marcas de tiempo**</span><span class="sxs-lookup"><span data-stu-id="7831c-114">**Time Stamps**</span></span>

<span data-ttu-id="7831c-115">Al reproducir secuencias de programas MPEG-2, el filtro de divisor de MPEG-2 trata la primera referencia de reloj del sistema que encuentra como el origen de la hora de cualquier flujo.</span><span class="sxs-lookup"><span data-stu-id="7831c-115">When playing back MPEG-2 program streams, the MPEG-2 Splitter filter treats the first system clock reference it encounters as the time origin of any stream.</span></span> <span data-ttu-id="7831c-116">Esto difiere del [separador de secuencias MPEG-1](mpeg-1-stream-splitter-filter.md), que usa marcas de tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="7831c-116">This differs from the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), which uses presentation time stamps.</span></span> <span data-ttu-id="7831c-117">El método [**IAMParse:: GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) devuelve el tiempo de reloj del sistema de secuencias (posiblemente estimado) para los datos que ha procesado.</span><span class="sxs-lookup"><span data-stu-id="7831c-117">The [**IAMParse::GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) method returns the (possibly estimated) stream system clock time for the data it has processed.</span></span>

<span data-ttu-id="7831c-118">Si el filtro de separador MPEG-2 encuentra un ejemplo de entrada con el conjunto de propiedades discontinuidad (la propiedad discontinuidad se puede establecer mediante [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) o [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), omite los datos hasta que encuentra el primer paquete de los datos y ajusta sus marcas de tiempo para que la referencia de reloj del sistema (SCR) de ese paquete se considere idéntica al tiempo de SCR antes de la discontinuidad.</span><span class="sxs-lookup"><span data-stu-id="7831c-118">If the MPEG-2 splitter filter encounters an input sample with the discontinuity property set (the discontinuity property can be set by using [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) or [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), it skips data until it finds the first pack in the data and adjusts its time stamps so that the system clock reference (SCR) for that pack is considered identical to the SCR time before the discontinuity.</span></span> <span data-ttu-id="7831c-119">Si el reloj de SCR aparece para saltar hacia atrás o para avanzar por más de un segundo, (en línea con la especificación de secuencia de programa MPEG-2), también se trata como una discontinuidad del reloj y la discrepancia del reloj aparente se resta de las marcas de tiempo que se pasan a los filtros de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="7831c-119">If the SCR clock appears either to jump backward or to jump forward by more than a second, then (in line with the MPEG-2 program stream specification), this is also treated as a clock discontinuity and the apparent clock discrepancy is subtracted from the time stamps passed to downstream filters.</span></span>

<span data-ttu-id="7831c-120">**Selección de flujo**</span><span class="sxs-lookup"><span data-stu-id="7831c-120">**Stream Selection**</span></span>

<span data-ttu-id="7831c-121">Cuando se reproduce la secuencia de programa MPEG-2, se eligen la primera secuencia de vídeo y la primera secuencia de audio que se ha encontrado al atravesar el flujo de programa.</span><span class="sxs-lookup"><span data-stu-id="7831c-121">When playing back the MPEG-2 program stream, the first video stream and first audio stream found traversing the program stream are chosen.</span></span> <span data-ttu-id="7831c-122">Se admite un máximo de un audio y un PIN de salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7831c-122">Up to one audio and one video output pin are supported.</span></span> <span data-ttu-id="7831c-123">A través de la interfaz [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) , se pueden seleccionar diferentes flujos del mismo tipo hasta el número especificado por el límite de audio en el encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="7831c-123">Through the [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) interface, different streams of the same type can be selected up to the number specified by the audio limit in the system header.</span></span> <span data-ttu-id="7831c-124">En el caso de audio MPEG-2, se supone que las secuencias forman un intervalo contiguo a partir de la secuencia 0xC0.</span><span class="sxs-lookup"><span data-stu-id="7831c-124">For MPEG-2 audio, it is currently assumed the streams form a contiguous range starting at stream 0xC0.</span></span>

<span data-ttu-id="7831c-125">**Interfaces admitidas**</span><span class="sxs-lookup"><span data-stu-id="7831c-125">**Supported Interfaces**</span></span>

<span data-ttu-id="7831c-126">El filtro de divisor de MPEG-2 admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="7831c-126">The MPEG-2 splitter filter supports the following interfaces.</span></span>

-   <span data-ttu-id="7831c-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span><span class="sxs-lookup"><span data-stu-id="7831c-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span></span> <span data-ttu-id="7831c-128">Solo flujo de programa MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="7831c-128">MPEG-2 program stream only.</span></span>
-   <span data-ttu-id="7831c-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span><span class="sxs-lookup"><span data-stu-id="7831c-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span></span> <span data-ttu-id="7831c-130">Solo flujo de programa MPEG-2, solo secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="7831c-130">MPEG-2 program stream only, audio streams only.</span></span>
-   <span data-ttu-id="7831c-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span><span class="sxs-lookup"><span data-stu-id="7831c-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span></span> <span data-ttu-id="7831c-132">Incluye el modo de búsqueda de bytes.</span><span class="sxs-lookup"><span data-stu-id="7831c-132">Includes byte mode seeking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7831c-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7831c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7831c-134">Compatibilidad con MPEG-2 en DirectShow</span><span class="sxs-lookup"><span data-stu-id="7831c-134">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



