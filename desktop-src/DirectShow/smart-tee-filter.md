---
description: Filtro de teo inteligente
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtro de teo inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c52077066f69e50fbb5218012a402a8d556c15c1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909303"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="81af8-103">Filtro de teo inteligente</span><span class="sxs-lookup"><span data-stu-id="81af8-103">Smart Tee Filter</span></span>

<span data-ttu-id="81af8-104">El filtro Smart Tee se usa en gráficos de captura de vídeo para dividir la secuencia de vídeo en una secuencia de vista previa y una secuencia de captura.</span><span class="sxs-lookup"><span data-stu-id="81af8-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="81af8-105">Esto se hace sin copiar datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="81af8-105">This is done without any additional data copying.</span></span> <span data-ttu-id="81af8-106">Las clavijas de salida admiten cualquier tipo de medio que se admita en la conexión de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="81af8-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="81af8-107">El filtro Smart Tee es útil cuando un filtro de captura de vídeo no proporciona pasadores independientes para la captura y vista previa.</span><span class="sxs-lookup"><span data-stu-id="81af8-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="81af8-108">El filtro Smart Tee ofrece datos de vista previa solo si esto no afecta al rendimiento de la captura.</span><span class="sxs-lookup"><span data-stu-id="81af8-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="81af8-109">También quita las marcas de tiempo de la secuencia de vista previa.</span><span class="sxs-lookup"><span data-stu-id="81af8-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="81af8-110">El generador de gráficos de captura inserta automáticamente el filtro Smart Tee cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="81af8-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="81af8-111">Para obtener más información, vea [Combinar captura de vídeo y versión preliminar.](combining-video-capture-and-preview.md)</span><span class="sxs-lookup"><span data-stu-id="81af8-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="81af8-112">En la ilustración siguiente se muestra un gráfico de captura típico que usa el filtro Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="81af8-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![usar el filtro de tee inteligente](images/smarttee.png)



| <span data-ttu-id="81af8-114">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="81af8-114">Label</span></span> | <span data-ttu-id="81af8-115">Value</span><span class="sxs-lookup"><span data-stu-id="81af8-115">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81af8-116">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="81af8-116">Filter Interfaces</span></span>                        | [<span data-ttu-id="81af8-117">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="81af8-117">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="81af8-118">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="81af8-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="81af8-119">VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="81af8-119">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="81af8-120">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="81af8-120">Input Pin Interfaces</span></span>                     | <span data-ttu-id="81af8-121">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="81af8-121">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="81af8-122">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="81af8-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="81af8-123">VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="81af8-123">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="81af8-124">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="81af8-124">Output Pin Interfaces</span></span>                    | <span data-ttu-id="81af8-125">[**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="81af8-125">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="81af8-126">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="81af8-126">Filter CLSID</span></span>                             | <span data-ttu-id="81af8-127">CLSID \_ SmartTee</span><span class="sxs-lookup"><span data-stu-id="81af8-127">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="81af8-128">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="81af8-128">Property Page CLSID</span></span>                      | <span data-ttu-id="81af8-129">No hay ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="81af8-129">No property page.</span></span>                                                                                              |
| <span data-ttu-id="81af8-130">Executable</span><span class="sxs-lookup"><span data-stu-id="81af8-130">Executable</span></span>                               | <span data-ttu-id="81af8-131">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="81af8-131">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="81af8-132">Mérito</span><span class="sxs-lookup"><span data-stu-id="81af8-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="81af8-133">NO USE EL VALOR DE NO \_ \_ \_ USE.</span><span class="sxs-lookup"><span data-stu-id="81af8-133">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="81af8-134">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="81af8-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="81af8-135">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="81af8-135">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="81af8-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81af8-136">Remarks</span></span>

<span data-ttu-id="81af8-137">El pin de captura es el pin de salida 0 y el pin de vista previa es el pin de salida 1.</span><span class="sxs-lookup"><span data-stu-id="81af8-137">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81af8-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81af8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81af8-139">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="81af8-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



