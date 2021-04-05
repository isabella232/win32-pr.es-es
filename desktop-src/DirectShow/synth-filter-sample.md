---
description: Ejemplo de filtro de sintetizador
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Ejemplo de filtro de sintetizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913137"
---
# <a name="synth-filter-sample"></a><span data-ttu-id="3868f-103">Ejemplo de filtro de sintetizador</span><span class="sxs-lookup"><span data-stu-id="3868f-103">Synth Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="3868f-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="3868f-104">Description</span></span>

<span data-ttu-id="3868f-105">El filtro de sintetizador es un filtro de origen que genera perfiles de onda de audio.</span><span class="sxs-lookup"><span data-stu-id="3868f-105">The Synth filter is a source filter that generates audio waveforms.</span></span>

<span data-ttu-id="3868f-106">Este filtro muestra la creación de gráficos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="3868f-106">This filter illustrates dynamic graph building.</span></span> <span data-ttu-id="3868f-107">Puede cambiar entre audio PCM sin comprimir y \_ formato MS ADPCM (modulación de código de Delta de Microsoft adaptable) comprimido.</span><span class="sxs-lookup"><span data-stu-id="3868f-107">It can switch between uncompressed PCM audio and compressed MS\_ADPCM (Microsoft Adaptive Delta Pulse Code Modulation) format.</span></span>

<span data-ttu-id="3868f-108">Este filtro aparece en GraphEdit como "filtro de sintetizador de audio".</span><span class="sxs-lookup"><span data-stu-id="3868f-108">This filter appears in GraphEdit as "Audio Synthesizer Filter."</span></span>

<span data-ttu-id="3868f-109">Para obtener más información sobre la creación de gráficos dinámicos, vea [creación de gráficos dinámicos](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="3868f-109">For more information about dynamic graph building, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="usage"></a><span data-ttu-id="3868f-110">Uso</span><span class="sxs-lookup"><span data-stu-id="3868f-110">Usage</span></span>

<span data-ttu-id="3868f-111">El filtro de sintetizador permite al usuario establecer la forma de onda, la frecuencia, el número de canales y otras propiedades a través de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3868f-111">The Synth filter enables the user to set the waveform, frequency, number of channels, and other properties through the property page.</span></span> <span data-ttu-id="3868f-112">Para establecer el extremo superior o inferior del intervalo de frecuencia de barrido, mantenga presionada la tecla Mayús mientras ajusta el control deslizante de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="3868f-112">To set either the upper or lower endpoint of the swept frequency range, hold down SHIFT while adjusting the frequency slider.</span></span> <span data-ttu-id="3868f-113">El filtro también admite una interfaz personalizada, ISynth2, para establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3868f-113">The filter also supports a custom interface, ISynth2, for setting these properties.</span></span>

<span data-ttu-id="3868f-114">Para demostrar la característica de creación de gráficos dinámicos, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3868f-114">To demonstrate the dynamic graph building feature, do the following:</span></span>

1.  <span data-ttu-id="3868f-115">Cree el filtro y regístrelo con la utilidad regsvr32.</span><span class="sxs-lookup"><span data-stu-id="3868f-115">Build the filter and register it with the Regsvr32 utility.</span></span>
2.  <span data-ttu-id="3868f-116">Inicie GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="3868f-116">Launch GraphEdit.</span></span>
3.  <span data-ttu-id="3868f-117">Inserte el filtro de sintetizador de audio.</span><span class="sxs-lookup"><span data-stu-id="3868f-117">Insert the Audio Synthesizer filter.</span></span> <span data-ttu-id="3868f-118">Aparece en la categoría filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3868f-118">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="3868f-119">Representar el PIN de salida del filtro.</span><span class="sxs-lookup"><span data-stu-id="3868f-119">Render the filter's output pin.</span></span>
5.  <span data-ttu-id="3868f-120">Haga clic en el botón **reproducir** .</span><span class="sxs-lookup"><span data-stu-id="3868f-120">Click the **Play** button.</span></span>
6.  <span data-ttu-id="3868f-121">Abra la página de propiedades del filtro.</span><span class="sxs-lookup"><span data-stu-id="3868f-121">Open the filter's property page.</span></span>
7.  <span data-ttu-id="3868f-122">En el área formato de salida, seleccione PCM o Microsoft ADPCM.</span><span class="sxs-lookup"><span data-stu-id="3868f-122">In the Output Format area, select PCM or Microsoft ADPCM.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="3868f-123">Notas de programación</span><span class="sxs-lookup"><span data-stu-id="3868f-123">Programming Notes</span></span>

<span data-ttu-id="3868f-124">Este ejemplo contiene los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="3868f-124">This sample contains the following files:</span></span>

-   <span data-ttu-id="3868f-125">Dynsrc. h, dynsrc. cpp: contiene dos clases base para filtros de origen que admiten la creación de gráficos dinámicos, CDynamicSource y CDynamicSourceStream.</span><span class="sxs-lookup"><span data-stu-id="3868f-125">Dynsrc.h, Dynsrc.cpp: Contains two base classes for source filters that support dynamic graph building, CDynamicSource and CDynamicSourceStream.</span></span>
-   <span data-ttu-id="3868f-126">ISynth. h: declara la interfaz ISynth2 personalizada para establecer las propiedades del filtro.</span><span class="sxs-lookup"><span data-stu-id="3868f-126">ISynth.h: Declares the custom ISynth2 interface for setting properties on the filter.</span></span>
-   <span data-ttu-id="3868f-127">Resource. h: contiene constantes de recursos.</span><span class="sxs-lookup"><span data-stu-id="3868f-127">Resource.h: Contains resource constants.</span></span>
-   <span data-ttu-id="3868f-128">Sint. def: exporta las funciones DLL que necesita la biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="3868f-128">Synth.def: Exports the DLL functions needed by the COM library.</span></span>
-   <span data-ttu-id="3868f-129">Sint. h, Sint. cpp: contiene la clase CAudioSynth, que genera los datos de audio y la clase CSynthFilter, que implementa el filtro.</span><span class="sxs-lookup"><span data-stu-id="3868f-129">Synth.h, Synth.cpp: Contains the CAudioSynth class, which generates the audio data, and the CSynthFilter class, which implements the filter.</span></span>
-   <span data-ttu-id="3868f-130">Sintetizador. RC: contiene los recursos utilizados por el filtro.</span><span class="sxs-lookup"><span data-stu-id="3868f-130">Synth.rc: Contains resources used by the filter.</span></span>
-   <span data-ttu-id="3868f-131">Synthprp. h, Synthprp. cpp: implementa la página de propiedades del filtro.</span><span class="sxs-lookup"><span data-stu-id="3868f-131">Synthprp.h, Synthprp.cpp: Implements the filter's property page.</span></span>

<span data-ttu-id="3868f-132">La clase CDynamicSource se adapta de la clase base [**CSource**](csource.md) .</span><span class="sxs-lookup"><span data-stu-id="3868f-132">The CDynamicSource class is adapted from the [**CSource**](csource.md) base class.</span></span> <span data-ttu-id="3868f-133">Usa uno o varios PIN de salida derivados de la clase CDynamicSourceStream.</span><span class="sxs-lookup"><span data-stu-id="3868f-133">It uses one or more output pins derived from the CDynamicSourceStream class.</span></span> <span data-ttu-id="3868f-134">La clase CDynamicSourceStream se adapta de la clase [**CSourceStream**](csourcestream.md) , pero se deriva de la clase [**CDynamicOutputPin**](cdynamicoutputpin.md) en lugar de la clase [**CBaseOutputPin**](cbaseoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="3868f-134">The CDynamicSourceStream class is adapted from the [**CSourceStream**](csourcestream.md) class, but derives from the [**CDynamicOutputPin**](cdynamicoutputpin.md) class rather than the [**CBaseOutputPin**](cbaseoutputpin.md) class.</span></span>

<span data-ttu-id="3868f-135">La clase CDynamicSource tiene los siguientes métodos no encontrados en [**CSource**](csource.md):</span><span class="sxs-lookup"><span data-stu-id="3868f-135">The CDynamicSource class has the following methods not found in [**CSource**](csource.md):</span></span>

-   <span data-ttu-id="3868f-136">STOP: señala el evento STOP ([**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) y cierra el subproceso de trabajo para todos los PIN no conectados.</span><span class="sxs-lookup"><span data-stu-id="3868f-136">Stop: Signals the stop event ([**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md)), and shuts down the worker thread for all unconnected pins.</span></span> <span data-ttu-id="3868f-137">En un PIN conectado, el método inactivo del PIN cerrará el subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="3868f-137">On a connected pin, the pin's Inactive method will shut down the worker thread.</span></span>
-   <span data-ttu-id="3868f-138">Pausar: restablece el evento de detención.</span><span class="sxs-lookup"><span data-stu-id="3868f-138">Pause: Resets the stop event.</span></span>
-   <span data-ttu-id="3868f-139">JoinFilterGraph: llama al método [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) en cada pin.</span><span class="sxs-lookup"><span data-stu-id="3868f-139">JoinFilterGraph: Calls the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method on each pin.</span></span>

<span data-ttu-id="3868f-140">La clase CDynamicSourceStream tiene los siguientes métodos no encontrados en [**CSourceStream**](csourcestream.md):</span><span class="sxs-lookup"><span data-stu-id="3868f-140">The CDynamicSourceStream class has the following methods not found in [**CSourceStream**](csourcestream.md):</span></span>

-   <span data-ttu-id="3868f-141">DestroySourceThread: cierra el subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="3868f-141">DestroySourceThread: Shuts down the worker thread.</span></span>
-   <span data-ttu-id="3868f-142">FatalError: indica un error al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="3868f-142">FatalError: Signals an error to the filter graph manager.</span></span>
-   <span data-ttu-id="3868f-143">OutputPinNeedsToBeReconnected: indica que el PIN de salida debe volver a conectarse.</span><span class="sxs-lookup"><span data-stu-id="3868f-143">OutputPinNeedsToBeReconnected: Signals that the output pin should be reconnected.</span></span> <span data-ttu-id="3868f-144">Cuando se llama a este método, el subproceso de trabajo llama al método [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) para volver a conectar el PIN.</span><span class="sxs-lookup"><span data-stu-id="3868f-144">When this method is called, the worker thread calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to reconnect the pin.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="3868f-145">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="3868f-145">Downloading the Sample</span></span>

<span data-ttu-id="3868f-146">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3868f-146">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="3868f-147">Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ \] raíz de SDK* de filtros de DirectShow de \\ \\ multimedia \\ \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="3868f-147">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Synth.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3868f-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3868f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3868f-149">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="3868f-149">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



