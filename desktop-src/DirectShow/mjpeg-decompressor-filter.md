---
description: Filtro de descompresor de MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro de descompresor de MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537995"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="bf84f-103">Filtro de descompresor de MJPEG</span><span class="sxs-lookup"><span data-stu-id="bf84f-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="bf84f-104">Este filtro descodifica un flujo de vídeo de Motion JPEG a vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="bf84f-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="bf84f-105">Algunas cámaras de vídeo digital producen una secuencia de vídeo Motion JPEG.</span><span class="sxs-lookup"><span data-stu-id="bf84f-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf84f-106">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="bf84f-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="bf84f-107">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="bf84f-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="bf84f-108">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="bf84f-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="bf84f-109">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="bf84f-109">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="bf84f-110">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="bf84f-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="bf84f-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="bf84f-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="bf84f-112">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="bf84f-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="bf84f-113">\_vídeo de MEDIATYPE, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="bf84f-113">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="bf84f-114">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="bf84f-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="bf84f-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="bf84f-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="bf84f-116">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="bf84f-116">Filter CLSID</span></span>                             | <span data-ttu-id="bf84f-117">CLSID \_ MjpegDec</span><span class="sxs-lookup"><span data-stu-id="bf84f-117">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="bf84f-118">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="bf84f-118">Property Page CLSID</span></span>                      | <span data-ttu-id="bf84f-119">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="bf84f-119">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="bf84f-120">Executable</span><span class="sxs-lookup"><span data-stu-id="bf84f-120">Executable</span></span>                               | <span data-ttu-id="bf84f-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="bf84f-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="bf84f-122">Fundament</span><span class="sxs-lookup"><span data-stu-id="bf84f-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="bf84f-123">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="bf84f-123">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="bf84f-124">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="bf84f-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="bf84f-125">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="bf84f-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="bf84f-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf84f-126">Remarks</span></span>

<span data-ttu-id="bf84f-127">Este filtro es compatible con el vídeo Motion JPEG que usa el código FOURCC "MJPG".</span><span class="sxs-lookup"><span data-stu-id="bf84f-127">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="bf84f-128">No puede descodificar otras variedades de movimiento JPEG.</span><span class="sxs-lookup"><span data-stu-id="bf84f-128">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="bf84f-129">Para ello, deberá usar un filtro de descodificador de terceros.</span><span class="sxs-lookup"><span data-stu-id="bf84f-129">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf84f-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf84f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf84f-131">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="bf84f-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



