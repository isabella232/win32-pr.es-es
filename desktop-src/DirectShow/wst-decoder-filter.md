---
description: Filtro de descodificador de elemento WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro de descodificador de elemento WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f2d20873ff9a5e7c009c4a84f7a23c273d6590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908357"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="4c54c-103">Filtro de descodificador de elemento WST</span><span class="sxs-lookup"><span data-stu-id="4c54c-103">WST Decoder Filter</span></span>

<span data-ttu-id="4c54c-104">Este componente se ha quitado de Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c54c-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="4c54c-105">Está disponible para su uso en los sistemas operativos Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4c54c-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="4c54c-106">A partir de Windows Vista, DirectShow no proporciona un filtro para descodificar el teletexto del estándar mundial (elemento WST).</span><span class="sxs-lookup"><span data-stu-id="4c54c-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="4c54c-107">El descodificador de elemento WST es un filtro de modo kernel que acepta datos de teletexto del mundo descodificados del [códec elemento WST](wst-codec-filter.md) y entrega los mapas de bits al pin 2 del [mezclador de superposición](overlay-mixer-filter.md) con las fuentes proporcionadas por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4c54c-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="4c54c-108">En este momento solo se admiten idiomas de Europa occidental; no se proporcionan fuentes Unicode actualmente.</span><span class="sxs-lookup"><span data-stu-id="4c54c-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="4c54c-109">Este filtro se puede Agregar al gráfico automáticamente mediante una llamada a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), mediante el PIN de salida del códec elemento WST.</span><span class="sxs-lookup"><span data-stu-id="4c54c-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



|                                          |                                                               |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4c54c-110">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="4c54c-110">Filter Interfaces</span></span>                        | <span data-ttu-id="4c54c-111">ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="4c54c-111">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="4c54c-112">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="4c54c-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="4c54c-113">MEDIATYPE \_ VBI, MEDIASUBTYPE \_ teletexto</span><span class="sxs-lookup"><span data-stu-id="4c54c-113">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="4c54c-114">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="4c54c-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="4c54c-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="4c54c-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="4c54c-116">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="4c54c-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="4c54c-117">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="4c54c-117">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="4c54c-118">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="4c54c-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="4c54c-119">**IPin**</span><span class="sxs-lookup"><span data-stu-id="4c54c-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="4c54c-120">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="4c54c-120">Filter CLSID</span></span>                             | <span data-ttu-id="4c54c-121">CLSID \_ WSTDecoder</span><span class="sxs-lookup"><span data-stu-id="4c54c-121">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="4c54c-122">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="4c54c-122">Property Page CLSID</span></span>                      | <span data-ttu-id="4c54c-123">CLSID \_ WstDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="4c54c-123">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="4c54c-124">Executable</span><span class="sxs-lookup"><span data-stu-id="4c54c-124">Executable</span></span>                               | <span data-ttu-id="4c54c-125">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="4c54c-125">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="4c54c-126">Fundament</span><span class="sxs-lookup"><span data-stu-id="4c54c-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="4c54c-127">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="4c54c-127">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="4c54c-128">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="4c54c-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="4c54c-129">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="4c54c-129">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="4c54c-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c54c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c54c-131">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4c54c-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="4c54c-132">Ver teletexto estándar del mundo</span><span class="sxs-lookup"><span data-stu-id="4c54c-132">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



