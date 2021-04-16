---
description: Filtro Smart Tee
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtro Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647e04ef2a24bde43c9d02b7986fd8a645a6b60c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495478"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="3a7e0-103">Filtro Smart Tee</span><span class="sxs-lookup"><span data-stu-id="3a7e0-103">Smart Tee Filter</span></span>

<span data-ttu-id="3a7e0-104">El filtro Smart Tee se usa en gráficos de captura de vídeo para dividir el flujo de vídeo en una secuencia de vista previa y en una secuencia de captura.</span><span class="sxs-lookup"><span data-stu-id="3a7e0-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="3a7e0-105">Esto se hace sin copiar ningún dato adicional.</span><span class="sxs-lookup"><span data-stu-id="3a7e0-105">This is done without any additional data copying.</span></span> <span data-ttu-id="3a7e0-106">Los pin de salida admiten los tipos de medios admitidos en la conexión de bajada.</span><span class="sxs-lookup"><span data-stu-id="3a7e0-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="3a7e0-107">El filtro Smart tee es útil cuando un filtro de captura de vídeo no proporciona PIN independientes para la captura y la vista previa.</span><span class="sxs-lookup"><span data-stu-id="3a7e0-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="3a7e0-108">Los filtros Smart Tee ofrecen datos de vista previa solo si, de lo contrario, no perjudica el rendimiento de la captura.</span><span class="sxs-lookup"><span data-stu-id="3a7e0-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="3a7e0-109">También quita las marcas de tiempo de la secuencia de vista previa.</span><span class="sxs-lookup"><span data-stu-id="3a7e0-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="3a7e0-110">Cuando sea necesario, el generador de gráficos de captura insertará automáticamente el filtro de forma inteligente.</span><span class="sxs-lookup"><span data-stu-id="3a7e0-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="3a7e0-111">Para obtener más información, consulte [combinar captura de vídeo y vista previa](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="3a7e0-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="3a7e0-112">En la ilustración siguiente se muestra un gráfico de captura típico que usa el filtro Smart tee.</span><span class="sxs-lookup"><span data-stu-id="3a7e0-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![usar el filtro Smart Tee](images/smarttee.png)



|                                          |                                                                                                                |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a7e0-114">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="3a7e0-114">Filter Interfaces</span></span>                        | [<span data-ttu-id="3a7e0-115">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="3a7e0-115">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="3a7e0-116">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="3a7e0-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="3a7e0-117">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="3a7e0-117">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="3a7e0-118">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="3a7e0-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="3a7e0-119">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3a7e0-119">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="3a7e0-120">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="3a7e0-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="3a7e0-121">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="3a7e0-121">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="3a7e0-122">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="3a7e0-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="3a7e0-123">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3a7e0-123">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="3a7e0-124">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="3a7e0-124">Filter CLSID</span></span>                             | <span data-ttu-id="3a7e0-125">CLSID \_ SmartTee</span><span class="sxs-lookup"><span data-stu-id="3a7e0-125">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="3a7e0-126">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="3a7e0-126">Property Page CLSID</span></span>                      | <span data-ttu-id="3a7e0-127">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3a7e0-127">No property page.</span></span>                                                                                              |
| <span data-ttu-id="3a7e0-128">Executable</span><span class="sxs-lookup"><span data-stu-id="3a7e0-128">Executable</span></span>                               | <span data-ttu-id="3a7e0-129">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="3a7e0-129">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="3a7e0-130">Fundament</span><span class="sxs-lookup"><span data-stu-id="3a7e0-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="3a7e0-131">MÉRITO \_ \_ no se \_ usa</span><span class="sxs-lookup"><span data-stu-id="3a7e0-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="3a7e0-132">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="3a7e0-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="3a7e0-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3a7e0-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="3a7e0-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a7e0-134">Remarks</span></span>

<span data-ttu-id="3a7e0-135">El PIN de captura es el PIN de salida 0 y el PIN de versión preliminar es el PIN de salida 1.</span><span class="sxs-lookup"><span data-stu-id="3a7e0-135">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a7e0-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a7e0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a7e0-137">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="3a7e0-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



