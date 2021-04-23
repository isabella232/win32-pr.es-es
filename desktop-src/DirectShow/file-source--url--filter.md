---
description: Filtro de origen de archivo (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro de origen de archivo (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ddfa7282adbf5117bd2c52465c6eb30efbd69e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909243"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="cbe0b-103">Filtro de origen de archivo (URL)</span><span class="sxs-lookup"><span data-stu-id="cbe0b-103">File Source (URL) Filter</span></span>

<span data-ttu-id="cbe0b-104">El filtro Origen de archivo URL es un filtro de origen asincrónico genérico que funciona con cualquier archivo de origen que se puede identificar mediante un localizador uniforme de recursos (URL) y cuyo tipo principal de medio es stream.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="cbe0b-105">Esto incluye archivos AVI, MOV, MPEG y WAV.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="cbe0b-106">Requiere que el filtro de bajada sea un analizador, como [mpeg-1 stream splitter](mpeg-1-stream-splitter-filter.md), [avi splitter](avi-splitter-filter.md)o [quicktime movie parser](quicktime-movie-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="cbe0b-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



| <span data-ttu-id="cbe0b-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="cbe0b-107">Label</span></span> | <span data-ttu-id="cbe0b-108">Value</span><span class="sxs-lookup"><span data-stu-id="cbe0b-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe0b-109">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="cbe0b-109">Filter Interfaces</span></span>                        | <span data-ttu-id="cbe0b-110">[**IAMOpenProgress,**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="cbe0b-110">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="cbe0b-111">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="cbe0b-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="cbe0b-112">No aplicable</span><span class="sxs-lookup"><span data-stu-id="cbe0b-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="cbe0b-113">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="cbe0b-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="cbe0b-114">No aplicable</span><span class="sxs-lookup"><span data-stu-id="cbe0b-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="cbe0b-115">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="cbe0b-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="cbe0b-116">Secuencia \_ MEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-116">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="cbe0b-117">El subtipo depende del formato multimedia.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-117">The subtype depends on the media format.</span></span> <span data-ttu-id="cbe0b-118">(MEDIASUBTYPE) \_ NULL si el filtro no reconoce el formato).</span><span class="sxs-lookup"><span data-stu-id="cbe0b-118">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="cbe0b-119">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="cbe0b-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="cbe0b-120">[**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="cbe0b-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="cbe0b-121">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="cbe0b-121">Filter CLSID</span></span>                             | <span data-ttu-id="cbe0b-122">CLSID \_ URLReader</span><span class="sxs-lookup"><span data-stu-id="cbe0b-122">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="cbe0b-123">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="cbe0b-123">Property Page CLSID</span></span>                      | <span data-ttu-id="cbe0b-124">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="cbe0b-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="cbe0b-125">Executable</span><span class="sxs-lookup"><span data-stu-id="cbe0b-125">Executable</span></span>                               | <span data-ttu-id="cbe0b-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="cbe0b-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="cbe0b-127">Mérito</span><span class="sxs-lookup"><span data-stu-id="cbe0b-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="cbe0b-128">NO ES \_ PROBABLE QUE SE PRODUZCAN</span><span class="sxs-lookup"><span data-stu-id="cbe0b-128">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="cbe0b-129">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="cbe0b-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="cbe0b-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="cbe0b-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="cbe0b-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cbe0b-131">Remarks</span></span>

<span data-ttu-id="cbe0b-132">Este filtro usa URLMon y admite páginas de códigos.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-132">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbe0b-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cbe0b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbe0b-134">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="cbe0b-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



