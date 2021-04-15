---
description: Filtro tee de anclaje infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro tee de anclaje infinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a80baf047cdd5559fadaa0f13ea1352d4ed0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423007"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="37a26-103">Filtro tee de anclaje infinito</span><span class="sxs-lookup"><span data-stu-id="37a26-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="37a26-104">Este filtro proporciona ejemplos entregados a su PIN de entrada a un número variable de clavijas de salida.</span><span class="sxs-lookup"><span data-stu-id="37a26-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="37a26-105">Cuando se crea una instancia del filtro, tiene un PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="37a26-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="37a26-106">Cada vez que se conecta un PIN de salida, el filtro crea otro PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="37a26-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="37a26-107">Todos los pin de salida comparten el mismo tipo de medio que el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="37a26-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="37a26-108">También se proporciona una versión de este filtro como ejemplo de SDK.</span><span class="sxs-lookup"><span data-stu-id="37a26-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="37a26-109">Vea [ejemplo de filtro InfTee](inftee-filter-sample.md).</span><span class="sxs-lookup"><span data-stu-id="37a26-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a26-110">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="37a26-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="37a26-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="37a26-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="37a26-112">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="37a26-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="37a26-113">Cualquier tipo de medio</span><span class="sxs-lookup"><span data-stu-id="37a26-113">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="37a26-114">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="37a26-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="37a26-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="37a26-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="37a26-116">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="37a26-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="37a26-117">Cualquier tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="37a26-117">Any media type.</span></span> <span data-ttu-id="37a26-118">El tipo de salida siempre coincide con el tipo de entrada para todos los pin de salida</span><span class="sxs-lookup"><span data-stu-id="37a26-118">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="37a26-119">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="37a26-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="37a26-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="37a26-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="37a26-121">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="37a26-121">Filter CLSID</span></span>                             | <span data-ttu-id="37a26-122">CLSID \_ InfTee</span><span class="sxs-lookup"><span data-stu-id="37a26-122">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="37a26-123">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="37a26-123">Property Page CLSID</span></span>                      | <span data-ttu-id="37a26-124">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="37a26-124">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="37a26-125">Executable</span><span class="sxs-lookup"><span data-stu-id="37a26-125">Executable</span></span>                               | <span data-ttu-id="37a26-126">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="37a26-126">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="37a26-127">Fundament</span><span class="sxs-lookup"><span data-stu-id="37a26-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="37a26-128">MÉRITO \_ \_ no se \_ usa</span><span class="sxs-lookup"><span data-stu-id="37a26-128">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="37a26-129">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="37a26-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="37a26-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="37a26-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="37a26-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37a26-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37a26-132">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="37a26-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



