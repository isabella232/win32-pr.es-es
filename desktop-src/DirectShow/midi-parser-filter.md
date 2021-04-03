---
description: Filtro de analizador MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro de analizador MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b741b2c82eda224a24ffee8a56f8977cbb510f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997657"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="6535b-103">Filtro de analizador MIDI</span><span class="sxs-lookup"><span data-stu-id="6535b-103">MIDI Parser Filter</span></span>

<span data-ttu-id="6535b-104">El filtro del analizador MIDI Lee los datos MIDI que se encuentran en. MID y. Archivos RMI.</span><span class="sxs-lookup"><span data-stu-id="6535b-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="6535b-105">El filtro acepta un flujo desde el [origen de archivo asincrónico](file-source--async--filter.md) o los filtros de origen de archivo de la [dirección URL](file-source--url--filter.md) , y envía muestras MIDI al [**representador MIDI**](midi-renderer-filter.md) para su reproducción.</span><span class="sxs-lookup"><span data-stu-id="6535b-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6535b-106">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="6535b-106">Filter Interfaces</span></span>                        | <span data-ttu-id="6535b-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="6535b-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="6535b-108">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="6535b-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="6535b-109">\_Secuencia de MEDIATYPE, MEDIASUBTYPE \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="6535b-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="6535b-110">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="6535b-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="6535b-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="6535b-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="6535b-112">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="6535b-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="6535b-113">MEDIATYPE \_ MIDI, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="6535b-113">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="6535b-114">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="6535b-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="6535b-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="6535b-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="6535b-116">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="6535b-116">Filter CLSID</span></span>                             | <span data-ttu-id="6535b-117">CLSID \_ MIDIParser</span><span class="sxs-lookup"><span data-stu-id="6535b-117">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="6535b-118">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="6535b-118">Property Page CLSID</span></span>                      | <span data-ttu-id="6535b-119">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="6535b-119">No property page</span></span>                                                                                         |
| <span data-ttu-id="6535b-120">Executable</span><span class="sxs-lookup"><span data-stu-id="6535b-120">Executable</span></span>                               | <span data-ttu-id="6535b-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="6535b-121">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="6535b-122">Fundament</span><span class="sxs-lookup"><span data-stu-id="6535b-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="6535b-123">MÉRITO \_ improbable</span><span class="sxs-lookup"><span data-stu-id="6535b-123">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="6535b-124">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="6535b-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="6535b-125">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="6535b-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="6535b-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6535b-126">Remarks</span></span>

<span data-ttu-id="6535b-127">Para obtener más información, vea [**representador MIDI**](midi-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="6535b-127">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6535b-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6535b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6535b-129">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="6535b-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



