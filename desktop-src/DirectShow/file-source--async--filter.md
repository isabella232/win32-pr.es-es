---
description: Filtro de origen de archivo (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtro de origen de archivo (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494987"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="12e9b-103">Filtro de origen de archivo (Async)</span><span class="sxs-lookup"><span data-stu-id="12e9b-103">File Source (Async) Filter</span></span>

<span data-ttu-id="12e9b-104">El filtro de origen de archivo asincrónico se abre y Lee los archivos locales de muchos formatos de datos diferentes y pasa los datos a un filtro de analizador.</span><span class="sxs-lookup"><span data-stu-id="12e9b-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="12e9b-105">Para descargar archivos multimedia de la web a través de HTTP, use el filtro de [origen de archivo (URL)](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="12e9b-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="12e9b-106">Para leer archivos ASF, use el filtro de [lector ASF de WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="12e9b-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e9b-107">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="12e9b-107">Filter Interfaces</span></span>                        | <span data-ttu-id="12e9b-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="12e9b-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="12e9b-109">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="12e9b-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="12e9b-110">No aplicable</span><span class="sxs-lookup"><span data-stu-id="12e9b-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="12e9b-111">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="12e9b-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="12e9b-112">No aplicable</span><span class="sxs-lookup"><span data-stu-id="12e9b-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="12e9b-113">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="12e9b-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="12e9b-114">**MEDIATYPE \_ Flujo**.</span><span class="sxs-lookup"><span data-stu-id="12e9b-114">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="12e9b-115">El subtipo depende del formato del medio.</span><span class="sxs-lookup"><span data-stu-id="12e9b-115">The subtype depends on the media format.</span></span> <span data-ttu-id="12e9b-116">(**MEDIASUBTYPE \_ null** si el filtro no reconoce el formato).</span><span class="sxs-lookup"><span data-stu-id="12e9b-116">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="12e9b-117">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="12e9b-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="12e9b-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="12e9b-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="12e9b-119">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="12e9b-119">Filter CLSID</span></span>                             | <span data-ttu-id="12e9b-120">**CLSID \_ AsyncReader**</span><span class="sxs-lookup"><span data-stu-id="12e9b-120">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="12e9b-121">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="12e9b-121">Property Page CLSID</span></span>                      | <span data-ttu-id="12e9b-122">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="12e9b-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="12e9b-123">Executable</span><span class="sxs-lookup"><span data-stu-id="12e9b-123">Executable</span></span>                               | <span data-ttu-id="12e9b-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="12e9b-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="12e9b-125">Fundament</span><span class="sxs-lookup"><span data-stu-id="12e9b-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="12e9b-126">**MÉRITO \_ improbable**</span><span class="sxs-lookup"><span data-stu-id="12e9b-126">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="12e9b-127">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="12e9b-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="12e9b-128">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="12e9b-128">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="12e9b-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12e9b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12e9b-130">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="12e9b-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



