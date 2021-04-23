---
description: Filtro de descodificador de WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro de descodificador de WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908483"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="79019-103">Filtro de descodificador de WST</span><span class="sxs-lookup"><span data-stu-id="79019-103">WST Decoder Filter</span></span>

<span data-ttu-id="79019-104">Este componente se ha quitado de Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="79019-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="79019-105">Está disponible para su uso en los sistemas operativos Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="79019-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="79019-106">A partir de Windows Vista, DirectShow no proporciona un filtro para descodificar El teletexto estándar mundial (WST).</span><span class="sxs-lookup"><span data-stu-id="79019-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="79019-107">El descodificador de WST es un filtro en modo kernel que acepta datos descodificados de Teletext world [](overlay-mixer-filter.md) standard del códec [WST](wst-codec-filter.md) y entrega los mapas de bits al pin 2 en el mezclador de superposición mediante fuentes proporcionadas por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="79019-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="79019-108">En este momento solo se admiten los idiomas europeos occidental; actualmente no se proporcionan fuentes Unicode.</span><span class="sxs-lookup"><span data-stu-id="79019-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="79019-109">Este filtro se puede agregar automáticamente al gráfico llamando a [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)mediante el pin de salida del códec WST.</span><span class="sxs-lookup"><span data-stu-id="79019-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



| <span data-ttu-id="79019-110">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="79019-110">Label</span></span> | <span data-ttu-id="79019-111">Value</span><span class="sxs-lookup"><span data-stu-id="79019-111">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="79019-112">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="79019-112">Filter Interfaces</span></span>                        | <span data-ttu-id="79019-113">ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="79019-113">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="79019-114">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="79019-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="79019-115">MEDIATYPE \_ VBI, MEDIASUBTYPE \_ TELETEXT</span><span class="sxs-lookup"><span data-stu-id="79019-115">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="79019-116">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="79019-116">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="79019-117">**Ipin**</span><span class="sxs-lookup"><span data-stu-id="79019-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="79019-118">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="79019-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="79019-119">VÍDEO \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="79019-119">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="79019-120">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="79019-120">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="79019-121">**Ipin**</span><span class="sxs-lookup"><span data-stu-id="79019-121">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="79019-122">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="79019-122">Filter CLSID</span></span>                             | <span data-ttu-id="79019-123">CLSID \_ WSTDecoder</span><span class="sxs-lookup"><span data-stu-id="79019-123">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="79019-124">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="79019-124">Property Page CLSID</span></span>                      | <span data-ttu-id="79019-125">CLSID \_ WstDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="79019-125">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="79019-126">Executable</span><span class="sxs-lookup"><span data-stu-id="79019-126">Executable</span></span>                               | <span data-ttu-id="79019-127">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="79019-127">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="79019-128">Mérito</span><span class="sxs-lookup"><span data-stu-id="79019-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="79019-129">NORMAL DE LA OPERACIÓN DE \_ NORMALIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="79019-129">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="79019-130">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="79019-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="79019-131">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="79019-131">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="79019-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79019-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79019-133">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="79019-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="79019-134">Visualización del texto teletexto estándar del mundo</span><span class="sxs-lookup"><span data-stu-id="79019-134">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



