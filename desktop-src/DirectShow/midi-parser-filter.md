---
description: Filtro del analizador DE MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro del analizador DE MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ce659559852497b8ec55709e77f9510a1deaf2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908433"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="0a6a7-103">Filtro del analizador DE MIDI</span><span class="sxs-lookup"><span data-stu-id="0a6a7-103">MIDI Parser Filter</span></span>

<span data-ttu-id="0a6a7-104">El filtro Analizador DE MIDI lee los datos DE MIDI que se encuentran en . MID y . Archivos MID.</span><span class="sxs-lookup"><span data-stu-id="0a6a7-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="0a6a7-105">El filtro acepta una secuencia de los filtros [Async File Source](file-source--async--filter.md) (Origen de archivo asincrónico) o URL File Source (Origen de archivo [URL)](file-source--url--filter.md) y genera ejemplos de MIDI en [**el representador de MIDI**](midi-renderer-filter.md) para su reproducción.</span><span class="sxs-lookup"><span data-stu-id="0a6a7-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



| <span data-ttu-id="0a6a7-106">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="0a6a7-106">Label</span></span> | <span data-ttu-id="0a6a7-107">Value</span><span class="sxs-lookup"><span data-stu-id="0a6a7-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a6a7-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="0a6a7-108">Filter Interfaces</span></span>                        | <span data-ttu-id="0a6a7-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="0a6a7-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="0a6a7-110">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="0a6a7-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="0a6a7-111">MEDIATYPE \_ Stream, MEDIASUBTYPE \_ Midi</span><span class="sxs-lookup"><span data-stu-id="0a6a7-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="0a6a7-112">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="0a6a7-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="0a6a7-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0a6a7-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="0a6a7-114">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="0a6a7-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="0a6a7-115">MEDIATYPE \_ Midi, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="0a6a7-115">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="0a6a7-116">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="0a6a7-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="0a6a7-117">[**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="0a6a7-117">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="0a6a7-118">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="0a6a7-118">Filter CLSID</span></span>                             | <span data-ttu-id="0a6a7-119">CLSID \_ MIDIParser</span><span class="sxs-lookup"><span data-stu-id="0a6a7-119">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="0a6a7-120">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="0a6a7-120">Property Page CLSID</span></span>                      | <span data-ttu-id="0a6a7-121">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="0a6a7-121">No property page</span></span>                                                                                         |
| <span data-ttu-id="0a6a7-122">Executable</span><span class="sxs-lookup"><span data-stu-id="0a6a7-122">Executable</span></span>                               | <span data-ttu-id="0a6a7-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="0a6a7-123">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="0a6a7-124">Mérito</span><span class="sxs-lookup"><span data-stu-id="0a6a7-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="0a6a7-125">NO ES \_ PROBABLE QUE SE PRODUZCA UN GRAN</span><span class="sxs-lookup"><span data-stu-id="0a6a7-125">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="0a6a7-126">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="0a6a7-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0a6a7-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="0a6a7-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="0a6a7-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a6a7-128">Remarks</span></span>

<span data-ttu-id="0a6a7-129">Para obtener más información, vea [**Representador de MIDI.**](midi-renderer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="0a6a7-129">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a6a7-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a6a7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a6a7-131">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a6a7-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



