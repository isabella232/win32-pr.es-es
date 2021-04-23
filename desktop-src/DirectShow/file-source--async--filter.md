---
description: Filtro de origen de archivo (asincrónico)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtro de origen de archivo (asincrónico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909703"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="82d1b-103">Filtro de origen de archivo (asincrónico)</span><span class="sxs-lookup"><span data-stu-id="82d1b-103">File Source (Async) Filter</span></span>

<span data-ttu-id="82d1b-104">El filtro Async File Source (Origen de archivo asincrónico) se abre y lee archivos locales de muchos formatos de datos diferentes y pasa los datos a un filtro de analizador.</span><span class="sxs-lookup"><span data-stu-id="82d1b-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="82d1b-105">Para descargar archivos multimedia desde la web a través de HTTP, use el filtro [Origen de archivo (URL).](file-source--url--filter.md)</span><span class="sxs-lookup"><span data-stu-id="82d1b-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="82d1b-106">Para leer archivos ASF, use el filtro [WM ASF Reader.](wm-asf-reader-filter.md)</span><span class="sxs-lookup"><span data-stu-id="82d1b-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



| <span data-ttu-id="82d1b-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="82d1b-107">Label</span></span> | <span data-ttu-id="82d1b-108">Value</span><span class="sxs-lookup"><span data-stu-id="82d1b-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d1b-109">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="82d1b-109">Filter Interfaces</span></span>                        | <span data-ttu-id="82d1b-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="82d1b-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="82d1b-111">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="82d1b-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="82d1b-112">No aplicable</span><span class="sxs-lookup"><span data-stu-id="82d1b-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="82d1b-113">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="82d1b-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="82d1b-114">No aplicable</span><span class="sxs-lookup"><span data-stu-id="82d1b-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="82d1b-115">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="82d1b-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="82d1b-116">**MEDIATYPE \_ Transmitir**.</span><span class="sxs-lookup"><span data-stu-id="82d1b-116">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="82d1b-117">El subtipo depende del formato multimedia.</span><span class="sxs-lookup"><span data-stu-id="82d1b-117">The subtype depends on the media format.</span></span> <span data-ttu-id="82d1b-118">**(MEDIASUBTYPE \_ NULL** si el filtro no reconoce el formato).</span><span class="sxs-lookup"><span data-stu-id="82d1b-118">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="82d1b-119">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="82d1b-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="82d1b-120">[**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="82d1b-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="82d1b-121">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="82d1b-121">Filter CLSID</span></span>                             | <span data-ttu-id="82d1b-122">**CLSID \_ AsyncReader**</span><span class="sxs-lookup"><span data-stu-id="82d1b-122">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="82d1b-123">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="82d1b-123">Property Page CLSID</span></span>                      | <span data-ttu-id="82d1b-124">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="82d1b-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="82d1b-125">Executable</span><span class="sxs-lookup"><span data-stu-id="82d1b-125">Executable</span></span>                               | <span data-ttu-id="82d1b-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="82d1b-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="82d1b-127">Mérito</span><span class="sxs-lookup"><span data-stu-id="82d1b-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="82d1b-128">**NO PROBABLE \_ QUE SE PRODUZCAN LOS CASO**</span><span class="sxs-lookup"><span data-stu-id="82d1b-128">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="82d1b-129">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="82d1b-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="82d1b-130">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="82d1b-130">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="82d1b-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82d1b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82d1b-132">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="82d1b-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



