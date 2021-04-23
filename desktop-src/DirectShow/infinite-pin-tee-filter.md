---
description: Filtro de tee de pin infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro de tee de pin infinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3433a0c2f5fe55fa59c42ed6e02d34f6e2cf0e6d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909233"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="8a1d2-103">Filtro de tee de pin infinito</span><span class="sxs-lookup"><span data-stu-id="8a1d2-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="8a1d2-104">Este filtro entrega ejemplos entregados a su pin de entrada a un número variable de pines de salida.</span><span class="sxs-lookup"><span data-stu-id="8a1d2-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="8a1d2-105">Cuando se crea una instancia del filtro, tiene un pin de salida.</span><span class="sxs-lookup"><span data-stu-id="8a1d2-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="8a1d2-106">Cada vez que se conecta un pin de salida, el filtro crea otro pin de salida.</span><span class="sxs-lookup"><span data-stu-id="8a1d2-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="8a1d2-107">Todos los pines de salida comparten el mismo tipo de medio que el pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="8a1d2-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="8a1d2-108">También se proporciona una versión de este filtro como ejemplo de SDK.</span><span class="sxs-lookup"><span data-stu-id="8a1d2-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="8a1d2-109">Vea [InfTee Filter Sample](inftee-filter-sample.md).</span><span class="sxs-lookup"><span data-stu-id="8a1d2-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



| <span data-ttu-id="8a1d2-110">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="8a1d2-110">Label</span></span> | <span data-ttu-id="8a1d2-111">Value</span><span class="sxs-lookup"><span data-stu-id="8a1d2-111">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1d2-112">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="8a1d2-112">Filter Interfaces</span></span>                        | [<span data-ttu-id="8a1d2-113">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="8a1d2-113">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="8a1d2-114">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="8a1d2-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="8a1d2-115">Cualquier tipo de medio</span><span class="sxs-lookup"><span data-stu-id="8a1d2-115">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="8a1d2-116">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="8a1d2-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="8a1d2-117">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8a1d2-117">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="8a1d2-118">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="8a1d2-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="8a1d2-119">Cualquier tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8a1d2-119">Any media type.</span></span> <span data-ttu-id="8a1d2-120">El tipo de salida siempre coincide con el tipo de entrada, para todos los pines de salida</span><span class="sxs-lookup"><span data-stu-id="8a1d2-120">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="8a1d2-121">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="8a1d2-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="8a1d2-122">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8a1d2-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="8a1d2-123">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="8a1d2-123">Filter CLSID</span></span>                             | <span data-ttu-id="8a1d2-124">CLSID \_ InfTee</span><span class="sxs-lookup"><span data-stu-id="8a1d2-124">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="8a1d2-125">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="8a1d2-125">Property Page CLSID</span></span>                      | <span data-ttu-id="8a1d2-126">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="8a1d2-126">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="8a1d2-127">Executable</span><span class="sxs-lookup"><span data-stu-id="8a1d2-127">Executable</span></span>                               | <span data-ttu-id="8a1d2-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="8a1d2-128">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="8a1d2-129">Mérito</span><span class="sxs-lookup"><span data-stu-id="8a1d2-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="8a1d2-130">NO USE EL VALOR DE NO \_ \_ \_ USE.</span><span class="sxs-lookup"><span data-stu-id="8a1d2-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="8a1d2-131">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="8a1d2-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="8a1d2-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="8a1d2-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="8a1d2-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a1d2-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a1d2-134">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="8a1d2-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



