---
description: Filtro de descompresor de AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtro de descompresor de AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b6fcff61dd867c598e793fb5aa8fbff67dc6cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806343"
---
# <a name="avi-decompressor-filter"></a><span data-ttu-id="b4486-103">Filtro de descompresor de AVI</span><span class="sxs-lookup"><span data-stu-id="b4486-103">AVI Decompressor Filter</span></span>

<span data-ttu-id="b4486-104">El filtro de descompresor de AVI permite que los códecs del administrador de compresión de vídeo (VCM) se unan a un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="b4486-104">The AVI Decompressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="b4486-105">No es necesario que la aplicación agregue el filtro al gráfico de filtros. lo extrae automáticamente el administrador de gráficos de filtro cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b4486-105">The application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span>

<span data-ttu-id="b4486-106">Cuando el administrador de gráficos de filtro está compilando un gráfico para representar un archivo AVI, comprueba el FOURCC en el encabezado AVI del archivo para determinar si la secuencia de vídeo está comprimida.</span><span class="sxs-lookup"><span data-stu-id="b4486-106">When the Filter Graph Manager is building a graph to render an AVI file, it checks the FOURCC in the file's AVI header to determine whether the video stream is compressed.</span></span> <span data-ttu-id="b4486-107">Si es así, el administrador de gráficos de filtros agrega el descompresor de AVI, que, a continuación, busca en el registro un descompresor instalado que pueda controlar el archivo.</span><span class="sxs-lookup"><span data-stu-id="b4486-107">If it is, the Filter Graph Manager adds the AVI Decompressor, which then searches the registry for an installed decompressor that can handle the file.</span></span>

> [!Note]  
> <span data-ttu-id="b4486-108">Los descompresores MPEG nunca se implementan como códecs VCM, sino únicamente como filtros de DirectShow nativos.</span><span class="sxs-lookup"><span data-stu-id="b4486-108">MPEG decompressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 

<span data-ttu-id="b4486-109">En su PIN ascendente, el descompresor AVI normalmente se conecta al [divisor de AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b4486-109">On its upstream pin the AVI Decompressor typically connects to the [AVI Splitter](avi-splitter-filter.md).</span></span> <span data-ttu-id="b4486-110">En el PIN de salida, normalmente se conecta al [representador de vídeo](video-renderer-filter.md) o al [filtro de AVI](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b4486-110">On its output pin it typically connects to the [Video Renderer](video-renderer-filter.md) or the [AVI Mux Filter](avi-mux-filter.md).</span></span>



|                                          |                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4486-111">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="b4486-111">Filter Interfaces</span></span>                        | [<span data-ttu-id="b4486-112">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="b4486-112">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| <span data-ttu-id="b4486-113">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="b4486-113">Input Pin Media Types</span></span>                    | <span data-ttu-id="b4486-114">Tipo principal: MEDIATYPE \_ VideoSubtype: debe corresponderse con el código FourCC para el tipo de compresión.</span><span class="sxs-lookup"><span data-stu-id="b4486-114">Major type: MEDIATYPE\_VideoSubtype: Must correspond to the FOURCC code for the compression type.</span></span> <span data-ttu-id="b4486-115">Para obtener más información, consulte [códigos FourCC](fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b4486-115">For more information, see [FOURCC Codes](fourcc-codes.md).</span></span><br/> <span data-ttu-id="b4486-116">Tipo de formato: formato de \_ Videoinfo</span><span class="sxs-lookup"><span data-stu-id="b4486-116">Format type: FORMAT\_VideoInfo</span></span><br/> |
| <span data-ttu-id="b4486-117">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="b4486-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="b4486-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b4486-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                             |
| <span data-ttu-id="b4486-119">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="b4486-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="b4486-120">MEDIATYPE \_ vídeo, MEDIASUBTYPE \_ null, formato de \_ videoinfo</span><span class="sxs-lookup"><span data-stu-id="b4486-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL, FORMAT\_VideoInfo</span></span>                                                                                                                                                            |
| <span data-ttu-id="b4486-121">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="b4486-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="b4486-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b4486-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                 |
| <span data-ttu-id="b4486-123">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="b4486-123">Filter CLSID</span></span>                             | <span data-ttu-id="b4486-124">CLSID \_ AVIDec</span><span class="sxs-lookup"><span data-stu-id="b4486-124">CLSID\_AVIDec</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="b4486-125">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="b4486-125">Property Page CLSID</span></span>                      | <span data-ttu-id="b4486-126">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b4486-126">No property page.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="b4486-127">Executable</span><span class="sxs-lookup"><span data-stu-id="b4486-127">Executable</span></span>                               | <span data-ttu-id="b4486-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="b4486-128">quartz.dll</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="b4486-129">Fundament</span><span class="sxs-lookup"><span data-stu-id="b4486-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="b4486-130">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="b4486-130">MERIT\_NORMAL</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="b4486-131">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="b4486-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="b4486-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="b4486-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="b4486-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4486-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4486-134">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="b4486-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




