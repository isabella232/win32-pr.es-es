---
description: Filtro de disexistente de color VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtro de disexistente de color VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082945"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="62dd9-103">Filtro de disexistente de color VGA 16</span><span class="sxs-lookup"><span data-stu-id="62dd9-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="62dd9-104">El filtro de separador de color VGA 16 convierte un tipo de color RGB en una pantalla de color de 4 bits para que las secuencias de vídeo AVI y MPEG se puedan mostrar en monitores de 16 colores más antiguos.</span><span class="sxs-lookup"><span data-stu-id="62dd9-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="62dd9-105">Este filtro se inserta en el gráfico entre un filtro de descompresor y un filtro de representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="62dd9-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62dd9-106">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="62dd9-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="62dd9-107">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="62dd9-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="62dd9-108">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="62dd9-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="62dd9-109">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="62dd9-109">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="62dd9-110">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="62dd9-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="62dd9-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="62dd9-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="62dd9-112">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="62dd9-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="62dd9-113">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="62dd9-113">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="62dd9-114">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="62dd9-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="62dd9-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="62dd9-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="62dd9-116">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="62dd9-116">Filter CLSID</span></span>                             | <span data-ttu-id="62dd9-117">\_Interpolación de CLSID</span><span class="sxs-lookup"><span data-stu-id="62dd9-117">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="62dd9-118">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="62dd9-118">Property Page CLSID</span></span>                      | <span data-ttu-id="62dd9-119">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="62dd9-119">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="62dd9-120">Executable</span><span class="sxs-lookup"><span data-stu-id="62dd9-120">Executable</span></span>                               | <span data-ttu-id="62dd9-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="62dd9-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="62dd9-122">Fundament</span><span class="sxs-lookup"><span data-stu-id="62dd9-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="62dd9-123">MÉRITO \_ improbable</span><span class="sxs-lookup"><span data-stu-id="62dd9-123">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="62dd9-124">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="62dd9-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="62dd9-125">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="62dd9-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="62dd9-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62dd9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62dd9-127">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="62dd9-127">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



