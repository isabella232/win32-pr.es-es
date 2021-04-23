---
description: Filtro de ditherer de color VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtro de ditherer de color VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908683"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="26bc9-103">Filtro de ditherer de color VGA 16</span><span class="sxs-lookup"><span data-stu-id="26bc9-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="26bc9-104">El filtro Vga 16 Color Ditherer convierte un tipo de color RGB en una pantalla de color de 4 bits para que se puedan mostrar secuencias de vídeo AVI y MPEG en monitores de 16 colores anteriores.</span><span class="sxs-lookup"><span data-stu-id="26bc9-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="26bc9-105">Este filtro se inserta en el gráfico entre un filtro de descompresión y un filtro de representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="26bc9-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



| <span data-ttu-id="26bc9-106">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="26bc9-106">Label</span></span> | <span data-ttu-id="26bc9-107">Value</span><span class="sxs-lookup"><span data-stu-id="26bc9-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26bc9-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="26bc9-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="26bc9-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="26bc9-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="26bc9-110">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="26bc9-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="26bc9-111">VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="26bc9-111">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="26bc9-112">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="26bc9-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="26bc9-113">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="26bc9-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="26bc9-114">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="26bc9-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="26bc9-115">VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="26bc9-115">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="26bc9-116">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="26bc9-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="26bc9-117">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="26bc9-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="26bc9-118">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="26bc9-118">Filter CLSID</span></span>                             | <span data-ttu-id="26bc9-119">CLSID \_ Dither</span><span class="sxs-lookup"><span data-stu-id="26bc9-119">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="26bc9-120">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="26bc9-120">Property Page CLSID</span></span>                      | <span data-ttu-id="26bc9-121">No hay ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="26bc9-121">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="26bc9-122">Executable</span><span class="sxs-lookup"><span data-stu-id="26bc9-122">Executable</span></span>                               | <span data-ttu-id="26bc9-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="26bc9-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="26bc9-124">Mérito</span><span class="sxs-lookup"><span data-stu-id="26bc9-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="26bc9-125">NO ES \_ PROBABLE QUE SE PRODUZCAN</span><span class="sxs-lookup"><span data-stu-id="26bc9-125">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="26bc9-126">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="26bc9-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="26bc9-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="26bc9-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="26bc9-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26bc9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26bc9-129">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="26bc9-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



