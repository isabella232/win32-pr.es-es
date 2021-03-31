---
description: Filtro de sintonizador de TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro de sintonizador de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dd03b965275f5e9b9405b027c8e66a7fb0f157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361310"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="46a2e-103">Filtro de sintonizador de TV</span><span class="sxs-lookup"><span data-stu-id="46a2e-103">TV Tuner Filter</span></span>

<span data-ttu-id="46a2e-104">El filtro sintonizador de TV selecciona un canal de difusión o cable analógico que se va a ver.</span><span class="sxs-lookup"><span data-stu-id="46a2e-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="46a2e-105">El flujo de salida único es una ruta de acceso de hardware para el vídeo analógico de banda.</span><span class="sxs-lookup"><span data-stu-id="46a2e-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="46a2e-106">Esta salida debe conectarse al filtro de barras de vídeo analógicas.</span><span class="sxs-lookup"><span data-stu-id="46a2e-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="46a2e-107">Los pines de entrada incluyen una entrada de cable y una entrada de antena.</span><span class="sxs-lookup"><span data-stu-id="46a2e-107">The input pins include an input for cable and an antenna input.</span></span>



|                                          |                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a2e-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="46a2e-108">Filter Interfaces</span></span>                        | <span data-ttu-id="46a2e-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="46a2e-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="46a2e-110">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="46a2e-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="46a2e-111">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="46a2e-111">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="46a2e-112">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="46a2e-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="46a2e-113">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="46a2e-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="46a2e-114">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="46a2e-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="46a2e-115">Vídeo: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SubType \_ None audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="46a2e-115">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="46a2e-116">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="46a2e-116">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="46a2e-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="46a2e-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="46a2e-118">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="46a2e-118">Filter CLSID</span></span>                             | <span data-ttu-id="46a2e-119">CLSID \_ TVTunerFilter</span><span class="sxs-lookup"><span data-stu-id="46a2e-119">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="46a2e-120">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="46a2e-120">Property Page CLSID</span></span>                      | <span data-ttu-id="46a2e-121">CLSID \_ TVTunerFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="46a2e-121">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="46a2e-122">Executable</span><span class="sxs-lookup"><span data-stu-id="46a2e-122">Executable</span></span>                               | <span data-ttu-id="46a2e-123">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="46a2e-123">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="46a2e-124">Fundament</span><span class="sxs-lookup"><span data-stu-id="46a2e-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="46a2e-125">MÉRITO \_ \_ no se \_ usa</span><span class="sxs-lookup"><span data-stu-id="46a2e-125">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="46a2e-126">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="46a2e-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="46a2e-127">\_TVTUNER KSCATEGORY \_ AM</span><span class="sxs-lookup"><span data-stu-id="46a2e-127">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="46a2e-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="46a2e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46a2e-129">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="46a2e-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



