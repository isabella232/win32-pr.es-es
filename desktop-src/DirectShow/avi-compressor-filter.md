---
description: Filtro de filtración AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro de filtración AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212ab58eb3800e0ad5531ebc5c50d3b054e7866c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909473"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="9f35e-103">Filtro de filtros AVI</span><span class="sxs-lookup"><span data-stu-id="9f35e-103">AVI Compressor Filter</span></span>

<span data-ttu-id="9f35e-104">El filtro Desenlazador AVI permite que los códecs del Administrador de compresión de vídeo (VCM) se unan a un gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="9f35e-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="9f35e-105">Cada códec aparece como una instancia independiente del filtro.</span><span class="sxs-lookup"><span data-stu-id="9f35e-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="9f35e-106">No se puede crear directamente este filtro con CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="9f35e-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="9f35e-107">En su lugar, debe usar el enumerador de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="9f35e-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="9f35e-108">Para obtener más información, [vea Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="9f35e-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="9f35e-109">El pin de entrada del filtro se conecta a los filtros que emiten datos de vídeo sin comprimir, como los filtros de captura de vídeo o el filtro [divisor AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="9f35e-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="9f35e-110">El pin de salida del filtro normalmente se conecta a un filtro de MUX, como [el filtro Mux de AVI.](avi-mux-filter.md)</span><span class="sxs-lookup"><span data-stu-id="9f35e-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="9f35e-111">Si el códec admite un cuadro de diálogo de configuración vfw de estilo antiguo o el cuadro de diálogo Acerca de , una aplicación puede mostrarlo mediante la [**interfaz IAMVfwCompressDialogs.**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)</span><span class="sxs-lookup"><span data-stu-id="9f35e-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="9f35e-112">Los dispositivos MPEG nunca se implementan como códecs de VCM, sino solo como filtros nativos de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9f35e-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



| <span data-ttu-id="9f35e-113">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="9f35e-113">Label</span></span> | <span data-ttu-id="9f35e-114">Value</span><span class="sxs-lookup"><span data-stu-id="9f35e-114">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f35e-115">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="9f35e-115">Filter Interfaces</span></span>                        | <span data-ttu-id="9f35e-116">[**IAMVfwCompressDialogs,**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)IPersistPropertyBag, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="9f35e-116">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="9f35e-117">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="9f35e-117">Input Pin Media Types</span></span>                    | <span data-ttu-id="9f35e-118">VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="9f35e-118">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="9f35e-119">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="9f35e-119">Input Pin Interfaces</span></span>                     | <span data-ttu-id="9f35e-120">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="9f35e-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="9f35e-121">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="9f35e-121">Output Pin Media Types</span></span>                   | <span data-ttu-id="9f35e-122">VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="9f35e-122">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="9f35e-123">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="9f35e-123">Output Pin Interfaces</span></span>                    | <span data-ttu-id="9f35e-124">[**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="9f35e-124">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="9f35e-125">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="9f35e-125">Filter CLSID</span></span>                             | <span data-ttu-id="9f35e-126">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9f35e-126">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="9f35e-127">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="9f35e-127">Property Page CLSID</span></span>                      | <span data-ttu-id="9f35e-128">No hay ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f35e-128">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="9f35e-129">Executable</span><span class="sxs-lookup"><span data-stu-id="9f35e-129">Executable</span></span>                               | <span data-ttu-id="9f35e-130">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="9f35e-130">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="9f35e-131">Mérito</span><span class="sxs-lookup"><span data-stu-id="9f35e-131">Merit</span></span>](merit.md)                       | <span data-ttu-id="9f35e-132">NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.</span><span class="sxs-lookup"><span data-stu-id="9f35e-132">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="9f35e-133">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="9f35e-133">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="9f35e-134">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="9f35e-134">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="9f35e-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f35e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f35e-136">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="9f35e-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



