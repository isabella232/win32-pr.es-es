---
description: Asignador de superficie de VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Asignador de superficie de VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909013"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="a5032-103">Asignador de superficie de VBI</span><span class="sxs-lookup"><span data-stu-id="a5032-103">VBI Surface Allocator</span></span>

<span data-ttu-id="a5032-104">El asignador de superficie de VBI controla la asignación de búferes de VBI en gráficos de televisión análogos con escenarios de captura de puertos de vídeo de hardware.</span><span class="sxs-lookup"><span data-stu-id="a5032-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="a5032-105">Con dispositivos como el descodificador Bt829, el búfer de fotogramas puede contener varios búferes de captura de VBI a los que se accede a través de un mecanismo propietario basado en hardware conocido genéricamente como puerto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a5032-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="a5032-106">El filtro Asignador de superficie de VBI se conecta de bajada desde el filtro de captura y no tiene ningún pin de salida.</span><span class="sxs-lookup"><span data-stu-id="a5032-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="a5032-107">El filtro funciona estrechamente con el mezclador de superposición [(a](overlay-mixer-filter.md) través de DirectDraw) para realizar operaciones coordinadas en el puerto de vídeo de hardware, utilizando la misma memoria de búfer de fotograma SVGA limitada.</span><span class="sxs-lookup"><span data-stu-id="a5032-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



| <span data-ttu-id="a5032-108">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="a5032-108">Label</span></span> | <span data-ttu-id="a5032-109">Value</span><span class="sxs-lookup"><span data-stu-id="a5032-109">Value</span></span> |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a5032-110">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="a5032-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="a5032-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a5032-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="a5032-112">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="a5032-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="a5032-113">VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ VPVBI</span><span class="sxs-lookup"><span data-stu-id="a5032-113">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="a5032-114">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="a5032-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="a5032-115">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="a5032-115">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="a5032-116">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="a5032-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="a5032-117">MEDIATYPE \_ NULL, MEDIASUBTYPE \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="a5032-117">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="a5032-118">(Nunca se ha conectado nada al pin de salida).</span><span class="sxs-lookup"><span data-stu-id="a5032-118">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="a5032-119">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="a5032-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="a5032-120">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a5032-120">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="a5032-121">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="a5032-121">Filter CLSID</span></span>                             | <span data-ttu-id="a5032-122">CLSID \_ VBISurfaces</span><span class="sxs-lookup"><span data-stu-id="a5032-122">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="a5032-123">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="a5032-123">Property Page CLSID</span></span>                      | <span data-ttu-id="a5032-124">No hay ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="a5032-124">No property page.</span></span>                                                                   |
| <span data-ttu-id="a5032-125">Executable</span><span class="sxs-lookup"><span data-stu-id="a5032-125">Executable</span></span>                               | <span data-ttu-id="a5032-126">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="a5032-126">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="a5032-127">Mérito</span><span class="sxs-lookup"><span data-stu-id="a5032-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="a5032-128">PROCEDIMIENTO \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="a5032-128">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="a5032-129">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="a5032-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a5032-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="a5032-130">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="a5032-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5032-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5032-132">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="a5032-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



