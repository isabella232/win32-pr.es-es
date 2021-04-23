---
description: Filtro de descompresión M FILTER
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro de descompresión M FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910023"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="cfe51-103">Filtro de descompresión M FILTER</span><span class="sxs-lookup"><span data-stu-id="cfe51-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="cfe51-104">Este filtro descodifica una secuencia de vídeo del movimiento JPEG al vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="cfe51-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="cfe51-105">Algunas cámaras de vídeo digitales generan una secuencia de vídeo JPEG de movimiento.</span><span class="sxs-lookup"><span data-stu-id="cfe51-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



| <span data-ttu-id="cfe51-106">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="cfe51-106">Label</span></span> | <span data-ttu-id="cfe51-107">Value</span><span class="sxs-lookup"><span data-stu-id="cfe51-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe51-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="cfe51-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="cfe51-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="cfe51-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="cfe51-110">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="cfe51-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="cfe51-111">MEDIATYPE \_ Video, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="cfe51-111">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="cfe51-112">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="cfe51-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="cfe51-113">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="cfe51-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="cfe51-114">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="cfe51-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="cfe51-115">MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="cfe51-115">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="cfe51-116">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="cfe51-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="cfe51-117">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="cfe51-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="cfe51-118">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="cfe51-118">Filter CLSID</span></span>                             | <span data-ttu-id="cfe51-119">CLSID \_ MshuegDec</span><span class="sxs-lookup"><span data-stu-id="cfe51-119">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="cfe51-120">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="cfe51-120">Property Page CLSID</span></span>                      | <span data-ttu-id="cfe51-121">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="cfe51-121">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="cfe51-122">Executable</span><span class="sxs-lookup"><span data-stu-id="cfe51-122">Executable</span></span>                               | <span data-ttu-id="cfe51-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="cfe51-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="cfe51-124">Mérito</span><span class="sxs-lookup"><span data-stu-id="cfe51-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="cfe51-125">NORMAL DE LA OPERACIÓN DE \_ NORMALIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="cfe51-125">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="cfe51-126">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="cfe51-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="cfe51-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="cfe51-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="cfe51-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cfe51-128">Remarks</span></span>

<span data-ttu-id="cfe51-129">Este filtro es compatible con el vídeo JPEG de movimiento que usa el código FOURCC "MJPG".</span><span class="sxs-lookup"><span data-stu-id="cfe51-129">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="cfe51-130">No puede descodificar otras variedades de JPEG de movimiento.</span><span class="sxs-lookup"><span data-stu-id="cfe51-130">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="cfe51-131">Para ello, deberá usar un filtro de descodificador de terceros.</span><span class="sxs-lookup"><span data-stu-id="cfe51-131">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfe51-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cfe51-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfe51-133">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="cfe51-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



