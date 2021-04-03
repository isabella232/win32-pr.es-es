---
description: Filtro de compresor AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro de compresor AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ef342d1ea740503d9fc1e9e9b898aadc3801
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906317"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="2bab8-103">Filtro de compresor AVI</span><span class="sxs-lookup"><span data-stu-id="2bab8-103">AVI Compressor Filter</span></span>

<span data-ttu-id="2bab8-104">El filtro del compresor AVI permite que los códecs del administrador de compresión de vídeo (VCM) se unan a un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="2bab8-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="2bab8-105">Cada códec aparece como una instancia independiente del filtro.</span><span class="sxs-lookup"><span data-stu-id="2bab8-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="2bab8-106">No se puede crear directamente este filtro con CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="2bab8-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="2bab8-107">En su lugar, debe usar el enumerador de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="2bab8-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="2bab8-108">Para obtener más información, vea [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="2bab8-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="2bab8-109">El PIN de entrada del filtro se conecta a los filtros que generan datos de vídeo sin comprimir, como filtros de captura de vídeo o el [filtro de divisor de AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2bab8-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="2bab8-110">El PIN de salida del filtro se conecta normalmente a un filtro MUX, como el [filtro de AVI](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2bab8-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="2bab8-111">Si el códec es compatible con un cuadro de diálogo de configuración de VFW de estilo antiguo o con el cuadro de diálogo acerca de, una aplicación puede mostrarlo mediante la interfaz [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .</span><span class="sxs-lookup"><span data-stu-id="2bab8-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="2bab8-112">Los compresores MPEG nunca se implementan como códecs VCM, sino únicamente como filtros de DirectShow nativos.</span><span class="sxs-lookup"><span data-stu-id="2bab8-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bab8-113">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="2bab8-113">Filter Interfaces</span></span>                        | <span data-ttu-id="2bab8-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="2bab8-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="2bab8-115">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="2bab8-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="2bab8-116">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="2bab8-116">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="2bab8-117">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="2bab8-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="2bab8-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="2bab8-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="2bab8-119">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="2bab8-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="2bab8-120">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="2bab8-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="2bab8-121">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="2bab8-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="2bab8-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="2bab8-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="2bab8-123">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="2bab8-123">Filter CLSID</span></span>                             | <span data-ttu-id="2bab8-124">No aplicable</span><span class="sxs-lookup"><span data-stu-id="2bab8-124">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="2bab8-125">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="2bab8-125">Property Page CLSID</span></span>                      | <span data-ttu-id="2bab8-126">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="2bab8-126">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="2bab8-127">Executable</span><span class="sxs-lookup"><span data-stu-id="2bab8-127">Executable</span></span>                               | <span data-ttu-id="2bab8-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="2bab8-128">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2bab8-129">Fundament</span><span class="sxs-lookup"><span data-stu-id="2bab8-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="2bab8-130">MÉRITO \_ \_ no se \_ usa</span><span class="sxs-lookup"><span data-stu-id="2bab8-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="2bab8-131">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="2bab8-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="2bab8-132">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="2bab8-132">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="2bab8-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2bab8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bab8-134">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="2bab8-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



