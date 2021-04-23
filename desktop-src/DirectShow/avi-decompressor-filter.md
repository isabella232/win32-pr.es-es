---
description: Filtro de descompresión AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtro de descompresión AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ccfeee18a01fa9c8d52ffbf4593b9de5664bb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910103"
---
# <a name="avi-decompressor-filter"></a><span data-ttu-id="b3cd9-103">Filtro de descompresión AVI</span><span class="sxs-lookup"><span data-stu-id="b3cd9-103">AVI Decompressor Filter</span></span>

<span data-ttu-id="b3cd9-104">El filtro de descompresión AVI permite que los códecs del Administrador de compresión de vídeo (VCM) se unan a un gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-104">The AVI Decompressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="b3cd9-105">La aplicación no necesita agregar el filtro al gráfico de filtros; El Administrador de gráficos de filtros lo extrae automáticamente cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-105">The application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span>

<span data-ttu-id="b3cd9-106">Cuando el Administrador de gráficos de filtros está creando un gráfico para representar un archivo AVI, comprueba fourcc en el encabezado AVI del archivo para determinar si la secuencia de vídeo está comprimida.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-106">When the Filter Graph Manager is building a graph to render an AVI file, it checks the FOURCC in the file's AVI header to determine whether the video stream is compressed.</span></span> <span data-ttu-id="b3cd9-107">Si es así, el Administrador de gráficos de filtros agrega el descomprimidor AVI, que busca en el Registro un descomprimidor instalado que pueda controlar el archivo.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-107">If it is, the Filter Graph Manager adds the AVI Decompressor, which then searches the registry for an installed decompressor that can handle the file.</span></span>

> [!Note]  
> <span data-ttu-id="b3cd9-108">Los descomprimores MPEG nunca se implementan como códecs de VCM, sino solo como filtros nativos de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-108">MPEG decompressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 

<span data-ttu-id="b3cd9-109">En su ancla ascendente, el descomprimidor AVI normalmente se conecta al [divisor AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b3cd9-109">On its upstream pin the AVI Decompressor typically connects to the [AVI Splitter](avi-splitter-filter.md).</span></span> <span data-ttu-id="b3cd9-110">En su pin de salida, normalmente se conecta al [representador de](video-renderer-filter.md) vídeo o [al filtro Mux de AVI.](avi-mux-filter.md)</span><span class="sxs-lookup"><span data-stu-id="b3cd9-110">On its output pin it typically connects to the [Video Renderer](video-renderer-filter.md) or the [AVI Mux Filter](avi-mux-filter.md).</span></span>



| <span data-ttu-id="b3cd9-111">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="b3cd9-111">Label</span></span> | <span data-ttu-id="b3cd9-112">Value</span><span class="sxs-lookup"><span data-stu-id="b3cd9-112">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3cd9-113">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="b3cd9-113">Filter Interfaces</span></span>                        | [<span data-ttu-id="b3cd9-114">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="b3cd9-114">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| <span data-ttu-id="b3cd9-115">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="b3cd9-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="b3cd9-116">Tipo principal: MEDIATYPE \_ VideoSubtype: debe corresponder al código FOURCC para el tipo de compresión.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-116">Major type: MEDIATYPE\_VideoSubtype: Must correspond to the FOURCC code for the compression type.</span></span> <span data-ttu-id="b3cd9-117">Para obtener más información, vea [FOURCC Codes](fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b3cd9-117">For more information, see [FOURCC Codes](fourcc-codes.md).</span></span><br/> <span data-ttu-id="b3cd9-118">Tipo de formato: FORMAT \_ VideoInfo</span><span class="sxs-lookup"><span data-stu-id="b3cd9-118">Format type: FORMAT\_VideoInfo</span></span><br/> |
| <span data-ttu-id="b3cd9-119">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="b3cd9-119">Input Pin Interfaces</span></span>                     | <span data-ttu-id="b3cd9-120">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b3cd9-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                             |
| <span data-ttu-id="b3cd9-121">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="b3cd9-121">Output Pin Media Types</span></span>                   | <span data-ttu-id="b3cd9-122">MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfo</span><span class="sxs-lookup"><span data-stu-id="b3cd9-122">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL, FORMAT\_VideoInfo</span></span>                                                                                                                                                            |
| <span data-ttu-id="b3cd9-123">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="b3cd9-123">Output Pin Interfaces</span></span>                    | <span data-ttu-id="b3cd9-124">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b3cd9-124">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                 |
| <span data-ttu-id="b3cd9-125">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="b3cd9-125">Filter CLSID</span></span>                             | <span data-ttu-id="b3cd9-126">CLSID \_ AVIDec</span><span class="sxs-lookup"><span data-stu-id="b3cd9-126">CLSID\_AVIDec</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="b3cd9-127">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="b3cd9-127">Property Page CLSID</span></span>                      | <span data-ttu-id="b3cd9-128">No hay ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-128">No property page.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="b3cd9-129">Executable</span><span class="sxs-lookup"><span data-stu-id="b3cd9-129">Executable</span></span>                               | <span data-ttu-id="b3cd9-130">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="b3cd9-130">quartz.dll</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="b3cd9-131">Mérito</span><span class="sxs-lookup"><span data-stu-id="b3cd9-131">Merit</span></span>](merit.md)                       | <span data-ttu-id="b3cd9-132">PROCEDIMIENTO \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="b3cd9-132">MERIT\_NORMAL</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="b3cd9-133">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="b3cd9-133">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="b3cd9-134">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="b3cd9-134">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="b3cd9-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3cd9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3cd9-136">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="b3cd9-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




