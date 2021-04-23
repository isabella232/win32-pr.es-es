---
description: Filtro de tuner de TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro de tuner de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f1fa68d7fc2723839882dd232e630dbe128634
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909033"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="f95bb-103">Filtro de tuner de TV</span><span class="sxs-lookup"><span data-stu-id="f95bb-103">TV Tuner Filter</span></span>

<span data-ttu-id="f95bb-104">El filtro de tv tuner selecciona un canal de difusión o cable análogo que se va a ver.</span><span class="sxs-lookup"><span data-stu-id="f95bb-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="f95bb-105">El flujo de salida único es una ruta de acceso de hardware para vídeo de banda base análoga.</span><span class="sxs-lookup"><span data-stu-id="f95bb-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="f95bb-106">Esta salida debe conectarse al filtro de barra cruzada de vídeo análogo.</span><span class="sxs-lookup"><span data-stu-id="f95bb-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="f95bb-107">Las clavijas de entrada incluyen una entrada para el cable y una entrada de la antena.</span><span class="sxs-lookup"><span data-stu-id="f95bb-107">The input pins include an input for cable and an antenna input.</span></span>



| <span data-ttu-id="f95bb-108">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="f95bb-108">Label</span></span> | <span data-ttu-id="f95bb-109">Value</span><span class="sxs-lookup"><span data-stu-id="f95bb-109">Value</span></span> |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f95bb-110">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="f95bb-110">Filter Interfaces</span></span>                        | <span data-ttu-id="f95bb-111">[**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMTVTuner,**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) **ISpecifyPropertyPages,** **IPersistPropertyBag,** **IKsObject,** [**IKsPropertySet**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="f95bb-111">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="f95bb-112">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="f95bb-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="f95bb-113">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="f95bb-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="f95bb-114">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="f95bb-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="f95bb-115">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="f95bb-115">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="f95bb-116">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="f95bb-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="f95bb-117">Vídeo: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SUBTYPE \_ NONE Audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="f95bb-117">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="f95bb-118">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="f95bb-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="f95bb-119">**Ipin**</span><span class="sxs-lookup"><span data-stu-id="f95bb-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="f95bb-120">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="f95bb-120">Filter CLSID</span></span>                             | <span data-ttu-id="f95bb-121">CLSID \_ TVTunerFilter</span><span class="sxs-lookup"><span data-stu-id="f95bb-121">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="f95bb-122">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="f95bb-122">Property Page CLSID</span></span>                      | <span data-ttu-id="f95bb-123">CLSID \_ TVTunerFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="f95bb-123">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="f95bb-124">Executable</span><span class="sxs-lookup"><span data-stu-id="f95bb-124">Executable</span></span>                               | <span data-ttu-id="f95bb-125">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="f95bb-125">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="f95bb-126">Mérito</span><span class="sxs-lookup"><span data-stu-id="f95bb-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="f95bb-127">NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.</span><span class="sxs-lookup"><span data-stu-id="f95bb-127">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="f95bb-128">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="f95bb-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f95bb-129">AM \_ KSCATEGORY \_ TVTUNER</span><span class="sxs-lookup"><span data-stu-id="f95bb-129">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="f95bb-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f95bb-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f95bb-131">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="f95bb-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



