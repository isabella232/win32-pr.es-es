---
description: Filtro de barra cruzada de vídeo análogo
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtro de barra cruzada de vídeo análogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909603"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="4b9ac-103">Filtro de barra cruzada de vídeo análogo</span><span class="sxs-lookup"><span data-stu-id="4b9ac-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="4b9ac-104">El filtro Analog Video Crossbar representa una barra cruzada de vídeo en un dispositivo de captura de vídeo que admite Modelo de controlador de Windows (WDM).</span><span class="sxs-lookup"><span data-stu-id="4b9ac-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="4b9ac-105">Este filtro es un filtro contenedor para barras cruzadas en dispositivos de streaming WDM.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="4b9ac-106">El nombre descriptivo del filtro se toma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="4b9ac-107">Cada pin de salida representa una ruta de acceso de hardware para vídeo de banda base análoga.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="4b9ac-108">Una de las clavijas de entrada procede de un afinador de TV (el [filtro de tuner de TV).](tv-tuner-filter.md)</span><span class="sxs-lookup"><span data-stu-id="4b9ac-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="4b9ac-109">Otras patillas de entrada admiten secuencias de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="4b9ac-110">El filtro admite los subtipos de medios y los formatos que se admiten en las conexiones de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="4b9ac-111">No se puede crear directamente este filtro con CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="4b9ac-112">La [**interfaz ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) agrega automáticamente este filtro al gráfico según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="4b9ac-113">Para obtener más información sobre los filtros de contenedor y los dispositivos de streaming de WDM, vea [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="4b9ac-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



| <span data-ttu-id="4b9ac-114">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="4b9ac-114">Label</span></span> | <span data-ttu-id="4b9ac-115">Value</span><span class="sxs-lookup"><span data-stu-id="4b9ac-115">Value</span></span> |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9ac-116">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="4b9ac-116">Filter Interfaces</span></span>                        | <span data-ttu-id="4b9ac-117">[**IAMCrossbar,**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span><span class="sxs-lookup"><span data-stu-id="4b9ac-117">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="4b9ac-118">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="4b9ac-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="4b9ac-119">MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="4b9ac-119">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="4b9ac-120">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="4b9ac-120">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="4b9ac-121">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="4b9ac-121">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="4b9ac-122">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="4b9ac-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="4b9ac-123">MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="4b9ac-123">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="4b9ac-124">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="4b9ac-124">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="4b9ac-125">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="4b9ac-125">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="4b9ac-126">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="4b9ac-126">Filter CLSID</span></span>                             | <span data-ttu-id="4b9ac-127">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4b9ac-127">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="4b9ac-128">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="4b9ac-128">Property Page CLSID</span></span>                      | <span data-ttu-id="4b9ac-129">CLSID \_ CrossbarFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="4b9ac-129">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="4b9ac-130">Executable</span><span class="sxs-lookup"><span data-stu-id="4b9ac-130">Executable</span></span>                               | <span data-ttu-id="4b9ac-131">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="4b9ac-131">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="4b9ac-132">Mérito</span><span class="sxs-lookup"><span data-stu-id="4b9ac-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="4b9ac-133">Dependiente del controlador.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-133">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="4b9ac-134">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="4b9ac-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="4b9ac-135">BARRA \_ CRUZADA DE AM KSCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="4b9ac-135">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="4b9ac-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4b9ac-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b9ac-137">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4b9ac-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="4b9ac-138">Trabajar con barras cruzadas</span><span class="sxs-lookup"><span data-stu-id="4b9ac-138">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



