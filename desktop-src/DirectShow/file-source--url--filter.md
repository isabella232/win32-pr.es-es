---
description: Filtro de origen de archivo (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro de origen de archivo (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152531"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="39d74-103">Filtro de origen de archivo (URL)</span><span class="sxs-lookup"><span data-stu-id="39d74-103">File Source (URL) Filter</span></span>

<span data-ttu-id="39d74-104">El filtro de origen del archivo de la dirección URL es un filtro de origen asíncrono genérico que funciona con cualquier archivo de código fuente que se puede identificar mediante un localizador uniforme de recursos (URL) y cuyo tipo de medio principal es Stream.</span><span class="sxs-lookup"><span data-stu-id="39d74-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="39d74-105">Esto incluye los archivos AVI, MOV, MPEG y WAV.</span><span class="sxs-lookup"><span data-stu-id="39d74-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="39d74-106">Requiere que el filtro de nivel inferior sea un analizador, como el [separador de secuencias MPEG-1](mpeg-1-stream-splitter-filter.md), el [divisor AVI](avi-splitter-filter.md)o el [analizador de películas QuickTime](quicktime-movie-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="39d74-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39d74-107">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="39d74-107">Filter Interfaces</span></span>                        | <span data-ttu-id="39d74-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="39d74-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="39d74-109">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="39d74-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="39d74-110">No aplicable</span><span class="sxs-lookup"><span data-stu-id="39d74-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="39d74-111">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="39d74-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="39d74-112">No aplicable</span><span class="sxs-lookup"><span data-stu-id="39d74-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="39d74-113">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="39d74-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="39d74-114">\_Secuencia MEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="39d74-114">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="39d74-115">El subtipo depende del formato del medio.</span><span class="sxs-lookup"><span data-stu-id="39d74-115">The subtype depends on the media format.</span></span> <span data-ttu-id="39d74-116">(MEDIASUBTYPE \_ ES NULL si el filtro no reconoce el formato).</span><span class="sxs-lookup"><span data-stu-id="39d74-116">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="39d74-117">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="39d74-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="39d74-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="39d74-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="39d74-119">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="39d74-119">Filter CLSID</span></span>                             | <span data-ttu-id="39d74-120">CLSID \_ URLReader</span><span class="sxs-lookup"><span data-stu-id="39d74-120">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="39d74-121">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="39d74-121">Property Page CLSID</span></span>                      | <span data-ttu-id="39d74-122">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="39d74-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="39d74-123">Executable</span><span class="sxs-lookup"><span data-stu-id="39d74-123">Executable</span></span>                               | <span data-ttu-id="39d74-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="39d74-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="39d74-125">Fundament</span><span class="sxs-lookup"><span data-stu-id="39d74-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="39d74-126">MÉRITO \_ improbable</span><span class="sxs-lookup"><span data-stu-id="39d74-126">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="39d74-127">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="39d74-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="39d74-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="39d74-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="39d74-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39d74-129">Remarks</span></span>

<span data-ttu-id="39d74-130">Este filtro usa URLMon y admite páginas de códigos.</span><span class="sxs-lookup"><span data-stu-id="39d74-130">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39d74-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="39d74-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39d74-132">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="39d74-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



