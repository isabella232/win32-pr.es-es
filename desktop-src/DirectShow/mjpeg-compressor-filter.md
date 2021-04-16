---
description: Filtro del compresor MJPEG
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro del compresor MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677177"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="b71fd-103">Filtro del compresor MJPEG</span><span class="sxs-lookup"><span data-stu-id="b71fd-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="b71fd-104">Este filtro comprime una secuencia de vídeo sin comprimir, usando la compresión Motion JPEG.</span><span class="sxs-lookup"><span data-stu-id="b71fd-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b71fd-105">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="b71fd-105">Filter Interfaces</span></span>                        | <span data-ttu-id="b71fd-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="b71fd-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="b71fd-107">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="b71fd-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="b71fd-108">\_vídeo de MEDIATYPE, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="b71fd-108">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="b71fd-109">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="b71fd-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="b71fd-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b71fd-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="b71fd-111">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="b71fd-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="b71fd-112">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="b71fd-112">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="b71fd-113">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="b71fd-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="b71fd-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b71fd-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="b71fd-115">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="b71fd-115">Filter CLSID</span></span>                             | <span data-ttu-id="b71fd-116">CLSID \_ MJPGEnc</span><span class="sxs-lookup"><span data-stu-id="b71fd-116">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="b71fd-117">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="b71fd-117">Property Page CLSID</span></span>                      | <span data-ttu-id="b71fd-118">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="b71fd-118">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="b71fd-119">Executable</span><span class="sxs-lookup"><span data-stu-id="b71fd-119">Executable</span></span>                               | <span data-ttu-id="b71fd-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="b71fd-120">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="b71fd-121">Fundament</span><span class="sxs-lookup"><span data-stu-id="b71fd-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="b71fd-122">MÉRITO \_ \_ no se \_ usa</span><span class="sxs-lookup"><span data-stu-id="b71fd-122">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="b71fd-123">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="b71fd-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="b71fd-124">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="b71fd-124">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="b71fd-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b71fd-125">Remarks</span></span>

<span data-ttu-id="b71fd-126">Este filtro codifica mediante el subtipo de medio MEDIASUBTYPE \_ MJPG, que corresponde al código FourCC "MJPG".</span><span class="sxs-lookup"><span data-stu-id="b71fd-126">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b71fd-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b71fd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b71fd-128">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="b71fd-128">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



