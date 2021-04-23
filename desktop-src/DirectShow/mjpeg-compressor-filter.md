---
description: Filtro de filtro de filtro M FILTER
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro de filtro de filtro M FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02928df4d09b50c0ac152aed99ed87dc6362fb70
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910013"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="1b713-103">Filtro de filtro de filtro M FILTER</span><span class="sxs-lookup"><span data-stu-id="1b713-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="1b713-104">Este filtro comprime una secuencia de vídeo sin comprimir mediante la compresión JPEG de movimiento.</span><span class="sxs-lookup"><span data-stu-id="1b713-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



| <span data-ttu-id="1b713-105">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="1b713-105">Label</span></span> | <span data-ttu-id="1b713-106">Value</span><span class="sxs-lookup"><span data-stu-id="1b713-106">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b713-107">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="1b713-107">Filter Interfaces</span></span>                        | <span data-ttu-id="1b713-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="1b713-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="1b713-109">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="1b713-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="1b713-110">MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="1b713-110">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="1b713-111">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="1b713-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="1b713-112">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1b713-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="1b713-113">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="1b713-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="1b713-114">MEDIATYPE \_ Video, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="1b713-114">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="1b713-115">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="1b713-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="1b713-116">[**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1b713-116">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="1b713-117">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="1b713-117">Filter CLSID</span></span>                             | <span data-ttu-id="1b713-118">CLSID \_ MJPGEnc</span><span class="sxs-lookup"><span data-stu-id="1b713-118">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="1b713-119">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="1b713-119">Property Page CLSID</span></span>                      | <span data-ttu-id="1b713-120">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="1b713-120">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="1b713-121">Executable</span><span class="sxs-lookup"><span data-stu-id="1b713-121">Executable</span></span>                               | <span data-ttu-id="1b713-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1b713-122">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="1b713-123">Mérito</span><span class="sxs-lookup"><span data-stu-id="1b713-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="1b713-124">NO USE EL VALOR DE NO \_ \_ \_ USE.</span><span class="sxs-lookup"><span data-stu-id="1b713-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="1b713-125">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="1b713-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1b713-126">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="1b713-126">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="1b713-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b713-127">Remarks</span></span>

<span data-ttu-id="1b713-128">Este filtro codifica mediante el subtipo multimedia MEDIASUBTYPE MJPG, que corresponde al código \_ FOURCC "MJPG".</span><span class="sxs-lookup"><span data-stu-id="1b713-128">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b713-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b713-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b713-130">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="1b713-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



