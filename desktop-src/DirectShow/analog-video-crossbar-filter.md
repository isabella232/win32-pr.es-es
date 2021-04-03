---
description: Filtro de barras de vídeos analógicos
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtro de barras de vídeos analógicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2eb086b85859a3e1e895cd322c68c56916ac19a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997813"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="29280-103">Filtro de barras de vídeos analógicos</span><span class="sxs-lookup"><span data-stu-id="29280-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="29280-104">El filtro de barras de vídeo analógicas representa una cruz de vídeo en un dispositivo de captura de vídeo que admite el Modelo de controlador de Windows (WDM).</span><span class="sxs-lookup"><span data-stu-id="29280-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="29280-105">Este filtro es un filtro de contenedor para las barras cruzadas en los dispositivos de streaming WDM.</span><span class="sxs-lookup"><span data-stu-id="29280-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="29280-106">El nombre descriptivo del filtro se toma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29280-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="29280-107">Cada pin de salida representa una ruta de acceso de hardware para el vídeo analógico de banda.</span><span class="sxs-lookup"><span data-stu-id="29280-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="29280-108">Uno de los pines de entrada procede de un sintonizador de TV (el [filtro de sintonizador de TV](tv-tuner-filter.md)).</span><span class="sxs-lookup"><span data-stu-id="29280-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="29280-109">Otros PIN de entrada admiten secuencias de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="29280-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="29280-110">El filtro admite los subtipos de medios y los formatos que se admiten en las conexiones de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="29280-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="29280-111">No se puede crear directamente este filtro con CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="29280-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="29280-112">La interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) agrega automáticamente este filtro al gráfico según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="29280-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="29280-113">Para obtener más información sobre los filtros de contenedor y los dispositivos de streaming WDM, consulte [Cómo participan los dispositivos de hardware en el gráfico de filtro](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="29280-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



|                                          |                                                                                                |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29280-114">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="29280-114">Filter Interfaces</span></span>                        | <span data-ttu-id="29280-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span><span class="sxs-lookup"><span data-stu-id="29280-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="29280-116">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="29280-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="29280-117">MEDIATYPE \_ AnalogAudio, mediatype \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="29280-117">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="29280-118">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="29280-118">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="29280-119">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="29280-119">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="29280-120">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="29280-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="29280-121">MEDIATYPE \_ AnalogAudio, mediatype \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="29280-121">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="29280-122">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="29280-122">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="29280-123">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="29280-123">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="29280-124">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="29280-124">Filter CLSID</span></span>                             | <span data-ttu-id="29280-125">No aplicable</span><span class="sxs-lookup"><span data-stu-id="29280-125">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="29280-126">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="29280-126">Property Page CLSID</span></span>                      | <span data-ttu-id="29280-127">CLSID \_ CrossbarFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="29280-127">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="29280-128">Executable</span><span class="sxs-lookup"><span data-stu-id="29280-128">Executable</span></span>                               | <span data-ttu-id="29280-129">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="29280-129">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="29280-130">Fundament</span><span class="sxs-lookup"><span data-stu-id="29280-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="29280-131">Dependiente del controlador.</span><span class="sxs-lookup"><span data-stu-id="29280-131">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="29280-132">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="29280-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="29280-133">KSCATEGORY de AM de la \_ \_ Cruz</span><span class="sxs-lookup"><span data-stu-id="29280-133">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="29280-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29280-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29280-135">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="29280-135">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="29280-136">Trabajar con barras cruzadas</span><span class="sxs-lookup"><span data-stu-id="29280-136">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



