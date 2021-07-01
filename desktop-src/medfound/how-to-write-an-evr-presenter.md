---
description: En este artículo se describe cómo escribir un presentador personalizado para el representador de vídeo mejorado (EVR).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Cómo escribir un presentador de EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505ba7ec225ac5f1316ad4343a4e1058ff0b6cb8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118780"
---
# <a name="how-to-write-an-evr-presenter"></a><span data-ttu-id="edad7-103">Cómo escribir un presentador de EVR</span><span class="sxs-lookup"><span data-stu-id="edad7-103">How to Write an EVR Presenter</span></span>

<span data-ttu-id="edad7-104">En este artículo se describe cómo escribir un presentador personalizado para el representador de vídeo mejorado (EVR).</span><span class="sxs-lookup"><span data-stu-id="edad7-104">This article describes how to write a custom presenter for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="edad7-105">Se puede usar un presentador personalizado con DirectShow y Media Foundation; las interfaces y el modelo de objetos son los mismos para ambas tecnologías, aunque la secuencia exacta de operaciones puede variar.</span><span class="sxs-lookup"><span data-stu-id="edad7-105">A custom presenter can be used with both DirectShow and Media Foundation; the interfaces and object model are the same for both technologies, although the exact sequence of operations might vary.</span></span>

<span data-ttu-id="edad7-106">El código de ejemplo de este tema se adapta del ejemplo [EVRPresenter](evrpresenter-sample.md), que se proporciona en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="edad7-106">The example code in this topic is adapted from the [EVRPresenter Sample](evrpresenter-sample.md), which is provided in the Windows SDK.</span></span>

<span data-ttu-id="edad7-107">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="edad7-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="edad7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="edad7-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="edad7-109">Modelo de objetos del presentador</span><span class="sxs-lookup"><span data-stu-id="edad7-109">Presenter Object Model</span></span>](#presenter-object-model)
    -   [<span data-ttu-id="edad7-110">Data Flow dentro de la EVR</span><span class="sxs-lookup"><span data-stu-id="edad7-110">Data Flow Inside the EVR</span></span>](#data-flow-inside-the-evr)
    -   [<span data-ttu-id="edad7-111">Estados del presentador</span><span class="sxs-lookup"><span data-stu-id="edad7-111">Presenter States</span></span>](#presenter-states)
    -   [<span data-ttu-id="edad7-112">Interfaces de presentador</span><span class="sxs-lookup"><span data-stu-id="edad7-112">Presenter Interfaces</span></span>](#presenter-interfaces)
    -   [<span data-ttu-id="edad7-113">Implementación de IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="edad7-113">Implementing IMFVideoDeviceID</span></span>](#implementing-imfvideodeviceid)
    -   [<span data-ttu-id="edad7-114">Implementación de IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="edad7-114">Implementing IMFTopologyServiceLookupClient</span></span>](#implementing-imftopologyservicelookupclient)
    -   [<span data-ttu-id="edad7-115">Implementación de IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="edad7-115">Implementing IMFVideoPresenter</span></span>](#implementing-imfvideopresenter)
    -   [<span data-ttu-id="edad7-116">Implementación de IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="edad7-116">Implementing IMFClockStateSink</span></span>](#implementing-imfclockstatesink)
    -   [<span data-ttu-id="edad7-117">Implementación de IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="edad7-117">Implementing IMFRateSupport</span></span>](#implementing-imfratesupport)
    -   [<span data-ttu-id="edad7-118">Envío de eventos al EVR</span><span class="sxs-lookup"><span data-stu-id="edad7-118">Sending Events to the EVR</span></span>](#sending-events-to-the-evr)
-   [<span data-ttu-id="edad7-119">Formatos de negociación</span><span class="sxs-lookup"><span data-stu-id="edad7-119">Negotiating Formats</span></span>](#negotiating-formats)
-   [<span data-ttu-id="edad7-120">Administración del dispositivo Direct3D</span><span class="sxs-lookup"><span data-stu-id="edad7-120">Managing the Direct3D Device</span></span>](#managing-the-direct3d-device)
    -   [<span data-ttu-id="edad7-121">Asignación de superficies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="edad7-121">Allocating Direct3D Surfaces</span></span>](#allocating-direct3d-surfaces)
    -   [<span data-ttu-id="edad7-122">Ejemplos de seguimiento</span><span class="sxs-lookup"><span data-stu-id="edad7-122">Tracking Samples</span></span>](#tracking-samples)
-   [<span data-ttu-id="edad7-123">Salida de procesamiento</span><span class="sxs-lookup"><span data-stu-id="edad7-123">Processing Output</span></span>](#processing-output)
    -   [<span data-ttu-id="edad7-124">Volver a dibujar fotogramas</span><span class="sxs-lookup"><span data-stu-id="edad7-124">Repainting Frames</span></span>](#repainting-frames)
    -   [<span data-ttu-id="edad7-125">Ejemplos de programación</span><span class="sxs-lookup"><span data-stu-id="edad7-125">Scheduling Samples</span></span>](#scheduling-samples)
    -   [<span data-ttu-id="edad7-126">Presentación de ejemplos</span><span class="sxs-lookup"><span data-stu-id="edad7-126">Presenting Samples</span></span>](#presenting-samples)
    -   [<span data-ttu-id="edad7-127">Rectángulos de origen y destino</span><span class="sxs-lookup"><span data-stu-id="edad7-127">Source and Destination Rectangles</span></span>](#source-and-destination-rectangles)
    -   [<span data-ttu-id="edad7-128">Fin de la secuencia</span><span class="sxs-lookup"><span data-stu-id="edad7-128">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="edad7-129">Ejecución paso a paso de fotogramas</span><span class="sxs-lookup"><span data-stu-id="edad7-129">Frame Stepping</span></span>](#frame-stepping)
    -   [<span data-ttu-id="edad7-130">Implementación de la ejecución paso a paso de fotogramas</span><span class="sxs-lookup"><span data-stu-id="edad7-130">Implementing Frame Stepping</span></span>](#implementing-frame-stepping)
-   [<span data-ttu-id="edad7-131">Establecimiento del presentador en la EVR</span><span class="sxs-lookup"><span data-stu-id="edad7-131">Setting the Presenter on the EVR</span></span>](#setting-the-presenter-on-the-evr)
    -   [<span data-ttu-id="edad7-132">Establecimiento del presentador en DirectShow</span><span class="sxs-lookup"><span data-stu-id="edad7-132">Setting the Presenter in DirectShow</span></span>](#setting-the-presenter-in-directshow)
    -   [<span data-ttu-id="edad7-133">Establecimiento del presentador en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="edad7-133">Setting the Presenter in Media Foundation</span></span>](#setting-the-presenter-in-media-foundation)
-   [<span data-ttu-id="edad7-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edad7-134">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="edad7-135">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="edad7-135">Prerequisites</span></span>

<span data-ttu-id="edad7-136">Antes de escribir un presentador personalizado, debe estar familiarizado con las siguientes tecnologías:</span><span class="sxs-lookup"><span data-stu-id="edad7-136">Before writing a custom presenter, you should be familiar with the following technologies:</span></span>

-   <span data-ttu-id="edad7-137">Representador de vídeo mejorado.</span><span class="sxs-lookup"><span data-stu-id="edad7-137">The enhanced video renderer.</span></span> <span data-ttu-id="edad7-138">Consulte [Representador de vídeo mejorado.](enhanced-video-renderer.md)</span><span class="sxs-lookup"><span data-stu-id="edad7-138">See [Enhanced Video Renderer](enhanced-video-renderer.md).</span></span>
-   <span data-ttu-id="edad7-139">Gráficos de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="edad7-139">Direct3D graphics.</span></span> <span data-ttu-id="edad7-140">No es necesario comprender los gráficos 3D para escribir un presentador, pero debe saber cómo crear un dispositivo Direct3D y administrar las superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="edad7-140">You don't need to understand 3-D graphics to write a presenter, but you must know how to create a Direct3D device and manage Direct3D surfaces.</span></span> <span data-ttu-id="edad7-141">Si no está familiarizado con Direct3D, lea las secciones "Dispositivos Direct3D" y "Recursos de Direct3D" en la documentación del SDK de gráficos de DirectX.</span><span class="sxs-lookup"><span data-stu-id="edad7-141">If you aren't familiar with Direct3D, read the sections "Direct3D Devices" and "Direct3D Resources" in the DirectX Graphics SDK documentation.</span></span>
-   <span data-ttu-id="edad7-142">DirectShow filtra gráficos o la canalización Media Foundation, en función de la tecnología que la aplicación usará para representar vídeo.</span><span class="sxs-lookup"><span data-stu-id="edad7-142">DirectShow filter graphs or the Media Foundation pipeline, depending on which technology your application will use to render video.</span></span>
-   <span data-ttu-id="edad7-143">[Media Foundation transforma](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="edad7-143">[Media Foundation Transforms](media-foundation-transforms.md).</span></span> <span data-ttu-id="edad7-144">El mezclador EVR es una Media Foundation y el presentador llama a métodos directamente en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-144">The EVR mixer is a Media Foundation transform, and the presenter calls methods directly on the mixer.</span></span>
-   <span data-ttu-id="edad7-145">Implementar objetos COM.</span><span class="sxs-lookup"><span data-stu-id="edad7-145">Implementing COM objects.</span></span> <span data-ttu-id="edad7-146">El presentador es un objeto COM en proceso y sin subprocesos.</span><span class="sxs-lookup"><span data-stu-id="edad7-146">The presenter is an in-process, free-threaded COM object.</span></span>

## <a name="presenter-object-model"></a><span data-ttu-id="edad7-147">Modelo de objetos del presentador</span><span class="sxs-lookup"><span data-stu-id="edad7-147">Presenter Object Model</span></span>

<span data-ttu-id="edad7-148">Esta sección contiene información general sobre el modelo de objetos del presentador y las interfaces.</span><span class="sxs-lookup"><span data-stu-id="edad7-148">This section contains an overview the presenter object model and interfaces.</span></span>

### <a name="data-flow-inside-the-evr"></a><span data-ttu-id="edad7-149">Data Flow dentro de la EVR</span><span class="sxs-lookup"><span data-stu-id="edad7-149">Data Flow Inside the EVR</span></span>

<span data-ttu-id="edad7-150">La EVR usa dos componentes de complemento para representar vídeo: el *mezclador* y *el presentador*.</span><span class="sxs-lookup"><span data-stu-id="edad7-150">The EVR uses two plug-in components to render video: the *mixer* and the *presenter*.</span></span> <span data-ttu-id="edad7-151">El mezclador combina las secuencias de vídeo y desenlaza el vídeo si es necesario.</span><span class="sxs-lookup"><span data-stu-id="edad7-151">The mixer blends the video streams and deinterlaces the video if needed.</span></span> <span data-ttu-id="edad7-152">El presentador dibuja *(o* presenta) el vídeo en la pantalla y programa cuando se dibuja cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="edad7-152">The presenter draws (or *presents*) the video onto the display and schedules when each frame is drawn.</span></span> <span data-ttu-id="edad7-153">Las aplicaciones pueden reemplazar cualquiera de estos objetos por una implementación personalizada.</span><span class="sxs-lookup"><span data-stu-id="edad7-153">Applications can replace either of these objects with a custom implementation.</span></span>

<span data-ttu-id="edad7-154">El EVR tiene uno o varios flujos de entrada y el mezclador tiene un número correspondiente de flujos de entrada.</span><span class="sxs-lookup"><span data-stu-id="edad7-154">The EVR has one or more input streams, and the mixer has a corresponding number of input streams.</span></span> <span data-ttu-id="edad7-155">El flujo 0 siempre es la *secuencia de referencia.*</span><span class="sxs-lookup"><span data-stu-id="edad7-155">Stream 0 is always the *reference stream*.</span></span> <span data-ttu-id="edad7-156">Las demás secuencias son *substreams*, que el mezclador combina alfa en la secuencia de referencia.</span><span class="sxs-lookup"><span data-stu-id="edad7-156">The other streams are *substreams*, which the mixer alpha-blends onto the reference stream.</span></span> <span data-ttu-id="edad7-157">La secuencia de referencia determina la velocidad de fotogramas maestra para el vídeo compuesto.</span><span class="sxs-lookup"><span data-stu-id="edad7-157">The reference stream determines the master frame-rate for the composited video.</span></span> <span data-ttu-id="edad7-158">Para cada fotograma de referencia, el mezclador toma el fotograma más reciente de cada subtrata, los combina alfa en el marco de referencia y genera un único fotograma compuesto.</span><span class="sxs-lookup"><span data-stu-id="edad7-158">For each reference frame, the mixer takes the most recent frame from each substream, alpha-blends them onto the reference frame, and outputs a single composited frame.</span></span> <span data-ttu-id="edad7-159">El mezclador también realiza el desinterlazado y la conversión de color de YUV a RGB si es necesario.</span><span class="sxs-lookup"><span data-stu-id="edad7-159">The mixer also performs deinterlacing and color conversion from YUV to RGB if needed.</span></span> <span data-ttu-id="edad7-160">EvR siempre inserta el mezclador en la canalización de vídeo, independientemente del número de flujos de entrada o del formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="edad7-160">The EVR always inserts the mixer into the video pipeline, regardless of the number of input streams or the video format.</span></span> <span data-ttu-id="edad7-161">En la imagen siguiente se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="edad7-161">The following image illustrates this process.</span></span>

![diagrama que muestra la secuencia de referencia y la subdifusión que apuntan al mezclador, que apunta al presentador, que apunta a la pantalla.](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

<span data-ttu-id="edad7-163">El presentador realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="edad7-163">The presenter performs the following tasks:</span></span>

-   <span data-ttu-id="edad7-164">Establece el formato de salida en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-164">Sets the output format on the mixer.</span></span> <span data-ttu-id="edad7-165">Antes de comenzar el streaming, el presentador establece un tipo de medio en el flujo de salida del mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-165">Before streaming begins, the presenter sets a media type on the mixer's output stream.</span></span> <span data-ttu-id="edad7-166">Este tipo de medio define el formato de la imagen compuesta.</span><span class="sxs-lookup"><span data-stu-id="edad7-166">This media type defines the format of the composited image.</span></span>
-   <span data-ttu-id="edad7-167">Crea el dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="edad7-167">Creates the Direct3D device.</span></span>
-   <span data-ttu-id="edad7-168">Asigna superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="edad7-168">Allocates Direct3D surfaces.</span></span> <span data-ttu-id="edad7-169">El mezclador corta los marcos compuestos en estas superficies.</span><span class="sxs-lookup"><span data-stu-id="edad7-169">The mixer blits the composited frames onto these surfaces.</span></span>
-   <span data-ttu-id="edad7-170">Obtiene la salida del mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-170">Gets the output from the mixer.</span></span>
-   <span data-ttu-id="edad7-171">Programa cuándo se presentan los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="edad7-171">Schedules when the frames are presented.</span></span> <span data-ttu-id="edad7-172">El EVR proporciona el reloj de presentación y el presentador programa fotogramas según este reloj.</span><span class="sxs-lookup"><span data-stu-id="edad7-172">The EVR provides the presentation clock, and the presenter schedules frames according to this clock.</span></span>
-   <span data-ttu-id="edad7-173">Presenta cada fotograma mediante Direct3D.</span><span class="sxs-lookup"><span data-stu-id="edad7-173">Presents each frame using Direct3D.</span></span>
-   <span data-ttu-id="edad7-174">Realiza la depuración y el paso a paso del marco.</span><span class="sxs-lookup"><span data-stu-id="edad7-174">Performs frame stepping and scrubbing.</span></span>

### <a name="presenter-states"></a><span data-ttu-id="edad7-175">Estados del presentador</span><span class="sxs-lookup"><span data-stu-id="edad7-175">Presenter States</span></span>

<span data-ttu-id="edad7-176">En cualquier momento, el presentador se encuentra en uno de los siguientes estados:</span><span class="sxs-lookup"><span data-stu-id="edad7-176">At any time, the presenter is in one of following states:</span></span>

-   <span data-ttu-id="edad7-177">*Iniciado.*</span><span class="sxs-lookup"><span data-stu-id="edad7-177">*Started*.</span></span> <span data-ttu-id="edad7-178">Se está ejecutando el reloj de presentación de EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-178">The EVR's presentation clock is running.</span></span> <span data-ttu-id="edad7-179">El presentador programa fotogramas de vídeo para su presentación a medida que llegan.</span><span class="sxs-lookup"><span data-stu-id="edad7-179">The presenter schedules video frames for presentation as they arrive.</span></span>
-   <span data-ttu-id="edad7-180">*En pausa.*</span><span class="sxs-lookup"><span data-stu-id="edad7-180">*Paused*.</span></span> <span data-ttu-id="edad7-181">Se suspende el reloj de presentación.</span><span class="sxs-lookup"><span data-stu-id="edad7-181">The presentation clock is suspended.</span></span> <span data-ttu-id="edad7-182">El presentador no presenta nuevos ejemplos, pero mantiene su cola de ejemplos programados.</span><span class="sxs-lookup"><span data-stu-id="edad7-182">The presenter does not present any new samples but maintains its queue of scheduled samples.</span></span> <span data-ttu-id="edad7-183">Si se reciben nuevos ejemplos, el presentador los agrega a la cola.</span><span class="sxs-lookup"><span data-stu-id="edad7-183">If new samples are received, the presenter adds them to the queue.</span></span>
-   <span data-ttu-id="edad7-184">*Detenido*.</span><span class="sxs-lookup"><span data-stu-id="edad7-184">*Stopped*.</span></span> <span data-ttu-id="edad7-185">Se detiene el reloj de presentación.</span><span class="sxs-lookup"><span data-stu-id="edad7-185">The presentation clock is stopped.</span></span> <span data-ttu-id="edad7-186">El presentador descarta las muestras que se programaron.</span><span class="sxs-lookup"><span data-stu-id="edad7-186">The presenter discards any samples that were scheduled.</span></span>
-   <span data-ttu-id="edad7-187">*Apague*.</span><span class="sxs-lookup"><span data-stu-id="edad7-187">*Shut down*.</span></span> <span data-ttu-id="edad7-188">El presentador libera todos los recursos relacionados con el streaming, como las superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="edad7-188">The presenter releases any resources related to streaming, such as Direct3D surfaces.</span></span> <span data-ttu-id="edad7-189">Este es el estado inicial del presentador y el estado final antes de que se destruya el presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-189">This is the presenter's initial state, and the final state before the presenter is destroyed.</span></span>

<span data-ttu-id="edad7-190">En el código de ejemplo de este tema, el estado del presentador se representa mediante una enumeración :</span><span class="sxs-lookup"><span data-stu-id="edad7-190">In the example code in this topic, the presenter state is represented by an enumeration:</span></span>


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



<span data-ttu-id="edad7-191">Algunas operaciones no son válidas mientras el presentador está en estado de apagado.</span><span class="sxs-lookup"><span data-stu-id="edad7-191">Some operations are not valid while the presenter is in the shutdown state.</span></span> <span data-ttu-id="edad7-192">El código de ejemplo comprueba este estado mediante una llamada a un método auxiliar:</span><span class="sxs-lookup"><span data-stu-id="edad7-192">The example code checks for this state by calling a helper method:</span></span>


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a><span data-ttu-id="edad7-193">Interfaces de presentador</span><span class="sxs-lookup"><span data-stu-id="edad7-193">Presenter Interfaces</span></span>

<span data-ttu-id="edad7-194">Se requiere un presentador para implementar las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="edad7-194">A presenter is required to implement the following interfaces:</span></span>



| <span data-ttu-id="edad7-195">Interfaz</span><span class="sxs-lookup"><span data-stu-id="edad7-195">Interface</span></span>                                                                | <span data-ttu-id="edad7-196">Descripción</span><span class="sxs-lookup"><span data-stu-id="edad7-196">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edad7-197">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="edad7-197">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | <span data-ttu-id="edad7-198">Notifica al presentador cuándo cambia el estado del reloj de la EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-198">Notifies the presenter when the EVR's clock changes state.</span></span> <span data-ttu-id="edad7-199">Vea [Implementing IMFClockStateSink .](#implementing-imfclockstatesink)</span><span class="sxs-lookup"><span data-stu-id="edad7-199">See [Implementing IMFClockStateSink](#implementing-imfclockstatesink).</span></span>                                   |
| [<span data-ttu-id="edad7-200">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="edad7-200">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | <span data-ttu-id="edad7-201">Proporciona una manera de que la aplicación y otros componentes de la canalización obtengan interfaces del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-201">Provides a way for the application and other components in the pipeline to get interfaces from the presenter.</span></span>                                                       |
| [<span data-ttu-id="edad7-202">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="edad7-202">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | <span data-ttu-id="edad7-203">Permite al presentador obtener interfaces de evr o mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-203">Enables the presenter to get interfaces from the EVR or the mixer.</span></span> <span data-ttu-id="edad7-204">Vea [Implementing IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span><span class="sxs-lookup"><span data-stu-id="edad7-204">See [Implementing IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span></span> |
| [<span data-ttu-id="edad7-205">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="edad7-205">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | <span data-ttu-id="edad7-206">Garantiza que el presentador y el mezclador usan tecnologías compatibles.</span><span class="sxs-lookup"><span data-stu-id="edad7-206">Ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="edad7-207">Vea [Implementing IMFVideoDeviceID](#implementing-imfvideodeviceid).</span><span class="sxs-lookup"><span data-stu-id="edad7-207">See [Implementing IMFVideoDeviceID](#implementing-imfvideodeviceid).</span></span>                          |
| [<span data-ttu-id="edad7-208">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="edad7-208">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | <span data-ttu-id="edad7-209">Procesa los mensajes del EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-209">Processes messages from the EVR.</span></span> <span data-ttu-id="edad7-210">Vea [Implementing IMFVideoPresenter](#implementing-imfvideopresenter).</span><span class="sxs-lookup"><span data-stu-id="edad7-210">See [Implementing IMFVideoPresenter](#implementing-imfvideopresenter).</span></span>                                                             |



 

<span data-ttu-id="edad7-211">Las interfaces siguientes son opcionales:</span><span class="sxs-lookup"><span data-stu-id="edad7-211">The following interfaces are optional:</span></span>



| <span data-ttu-id="edad7-212">Interfaz</span><span class="sxs-lookup"><span data-stu-id="edad7-212">Interface</span></span>                                                | <span data-ttu-id="edad7-213">Descripción</span><span class="sxs-lookup"><span data-stu-id="edad7-213">Description</span></span>                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edad7-214">**IEVRTrustedVideoPlugin**</span><span class="sxs-lookup"><span data-stu-id="edad7-214">**IEVRTrustedVideoPlugin**</span></span>](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | <span data-ttu-id="edad7-215">Permite que el presentador funcione con medios protegidos.</span><span class="sxs-lookup"><span data-stu-id="edad7-215">Enables the presenter to work with protected media.</span></span> <span data-ttu-id="edad7-216">Implemente esta interfaz si el presentador es un componente de confianza diseñado para funcionar en la ruta de acceso multimedia protegida (PMP).</span><span class="sxs-lookup"><span data-stu-id="edad7-216">Implement this interface if your presenter is a trusted component designed to work in the protected media path (PMP).</span></span> |
| [<span data-ttu-id="edad7-217">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="edad7-217">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | <span data-ttu-id="edad7-218">Informa del intervalo de velocidades de reproducción que admite el presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-218">Reports the range of playback rates that the presenter supports.</span></span> <span data-ttu-id="edad7-219">Vea [Implementing IMFRateSupport](#implementing-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="edad7-219">See [Implementing IMFRateSupport](#implementing-imfratesupport).</span></span>                                         |
| [<span data-ttu-id="edad7-220">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="edad7-220">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | <span data-ttu-id="edad7-221">Asigna coordenadas en el fotograma de vídeo de salida a coordenadas en el fotograma de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="edad7-221">Maps coordinates on the output video frame to coordinates on the input video frame.</span></span>                                                                                       |
| [<span data-ttu-id="edad7-222">**IQualProp**</span><span class="sxs-lookup"><span data-stu-id="edad7-222">**IQualProp**</span></span>](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | <span data-ttu-id="edad7-223">Informa de la información de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="edad7-223">Reports performance information.</span></span> <span data-ttu-id="edad7-224">El EVR usa esta información para la administración del control de calidad.</span><span class="sxs-lookup"><span data-stu-id="edad7-224">The EVR uses this information for quality-control management.</span></span> <span data-ttu-id="edad7-225">Esta interfaz se documenta en el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="edad7-225">This interface is documented in the DirectShow SDK.</span></span>                        |



 

<span data-ttu-id="edad7-226">También puede proporcionar interfaces para que la aplicación se comunique con el presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-226">You can also provide interfaces for the application to communicate with the presenter.</span></span> <span data-ttu-id="edad7-227">El presentador estándar implementa la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) para este propósito.</span><span class="sxs-lookup"><span data-stu-id="edad7-227">The standard presenter implements the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface for this purpose.</span></span> <span data-ttu-id="edad7-228">Puede implementar esta interfaz o definir la suya propia.</span><span class="sxs-lookup"><span data-stu-id="edad7-228">You can implement this interface or define your own.</span></span> <span data-ttu-id="edad7-229">La aplicación obtiene interfaces del presentador mediante una llamada [**a IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en la EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-229">The application obtains interfaces from the presenter by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR.</span></span> <span data-ttu-id="edad7-230">Cuando el GUID del **servicio MR_VIDEO_RENDER_SERVICE**, el EVR pasa la **solicitud GetService** al presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-230">When the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR passes the **GetService** request to the presenter.</span></span>

### <a name="implementing-imfvideodeviceid"></a><span data-ttu-id="edad7-231">Implementación de IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="edad7-231">Implementing IMFVideoDeviceID</span></span>

<span data-ttu-id="edad7-232">La [**interfaz IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contiene un método, [**GetDeviceID,**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)que devuelve un GUID de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edad7-232">The [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) interface contains one method, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), which returns a device GUID.</span></span> <span data-ttu-id="edad7-233">El GUID del dispositivo garantiza que el presentador y el mezclador usan tecnologías compatibles.</span><span class="sxs-lookup"><span data-stu-id="edad7-233">The device GUID ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="edad7-234">Si los GUID del dispositivo no coinciden, la EVR no se inicializa.</span><span class="sxs-lookup"><span data-stu-id="edad7-234">If the device GUIDs do not match, the EVR fails to initialize.</span></span>

<span data-ttu-id="edad7-235">Tanto el mezclador estándar como el presentador usan Direct3D 9, con el GUID del dispositivo igual a **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="edad7-235">The standard mixer and presenter both use Direct3D 9, with the device GUID equal to **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="edad7-236">Si piensa usar el presentador personalizado con el mezclador estándar, el GUID del dispositivo del presentador debe **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="edad7-236">If you intend to use your custom presenter with the standard mixer, the presenter's device GUID must be **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="edad7-237">Si reemplaza ambos componentes, podría definir un nuevo GUID de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edad7-237">If you replace both components, you could define a new device GUID.</span></span> <span data-ttu-id="edad7-238">En el resto de este artículo, se supone que el presentador usa Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="edad7-238">For the remainder of this article, it is assumed that the presenter uses Direct3D 9.</span></span> <span data-ttu-id="edad7-239">Esta es la implementación estándar de [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span><span class="sxs-lookup"><span data-stu-id="edad7-239">Here is the standard implementation of [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span></span>


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



<span data-ttu-id="edad7-240">El método debe tener éxito incluso cuando se apague el presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-240">The method should succeed even when the presenter is shut down.</span></span>

### <a name="implementing-imftopologyservicelookupclient"></a><span data-ttu-id="edad7-241">Implementación de IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="edad7-241">Implementing IMFTopologyServiceLookupClient</span></span>

<span data-ttu-id="edad7-242">La [**interfaz IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) permite al presentador obtener punteros de interfaz del EVR y del mezclador como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="edad7-242">The [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) interface enables the presenter to get interface pointers from the EVR and from the mixer as follows:</span></span>

1.  <span data-ttu-id="edad7-243">Cuando el EVR inicializa el presentador, llama al método [**DEMTOPOLOGYServiceLookupClient::InitServicePointers del**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-243">When the EVR initializes the presenter, it calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="edad7-244">El argumento es un puntero a la interfaz [**DEVTOPOLOGYServiceLookup.**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup)</span><span class="sxs-lookup"><span data-stu-id="edad7-244">The argument is a pointer to the EVR's [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) interface.</span></span>
2.  <span data-ttu-id="edad7-245">El presentador llama [**a IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) para obtener punteros de interfaz del EVR o del mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-245">The presenter calls [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) to get interface pointers from either the EVR or the mixer.</span></span>

<span data-ttu-id="edad7-246">El [**método LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) es similar al [**método IMFGetService::GetService.**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)</span><span class="sxs-lookup"><span data-stu-id="edad7-246">The [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) method is similar to the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="edad7-247">Ambos métodos toman un GUID de servicio y un identificador de interfaz (IID) como entrada, pero **LookupService** devuelve una matriz de punteros de interfaz, mientras **que GetService** devuelve un solo puntero.</span><span class="sxs-lookup"><span data-stu-id="edad7-247">Both methods take a service GUID and an interface identifier (IID) as input, but **LookupService** returns an array of interface pointers, while **GetService** returns a single pointer.</span></span> <span data-ttu-id="edad7-248">Sin embargo, en la práctica, siempre puede establecer el tamaño de la matriz en 1.</span><span class="sxs-lookup"><span data-stu-id="edad7-248">In practice, however, you can always set the array size to 1.</span></span> <span data-ttu-id="edad7-249">El objeto que se consulta depende del GUID del servicio:</span><span class="sxs-lookup"><span data-stu-id="edad7-249">The object queried depends on the service GUID:</span></span>

-   <span data-ttu-id="edad7-250">Si el GUID del **servicio MR_VIDEO_RENDER_SERVICE**, se consulta la EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-250">If the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR is queried.</span></span>
-   <span data-ttu-id="edad7-251">Si el GUID del servicio **MR_VIDEO_MIXER_SERVICE**, se consulta el mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-251">If the service GUID is **MR_VIDEO_MIXER_SERVICE**, the mixer is queried.</span></span>

<span data-ttu-id="edad7-252">En la implementación de [**InitServicePointers,**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)obtenga las interfaces siguientes de EVR:</span><span class="sxs-lookup"><span data-stu-id="edad7-252">In your implementation of [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), get the following interfaces from the EVR:</span></span>



| <span data-ttu-id="edad7-253">Interfaz EVR</span><span class="sxs-lookup"><span data-stu-id="edad7-253">EVR Interface</span></span>                                | <span data-ttu-id="edad7-254">Descripción</span><span class="sxs-lookup"><span data-stu-id="edad7-254">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edad7-255">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="edad7-255">**IMediaEventSink**</span></span>](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | <span data-ttu-id="edad7-256">Proporciona una manera de que el presentador envíe mensajes a la EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-256">Provides a way for the presenter to send messages to the EVR.</span></span> <span data-ttu-id="edad7-257">Esta interfaz se define en el SDK de DirectShow, por lo que los mensajes siguen el patrón de eventos de DirectShow, no Media Foundation eventos.</span><span class="sxs-lookup"><span data-stu-id="edad7-257">This interface is defined in the DirectShow SDK, so the messages follow the pattern for DirectShow events, not Media Foundation events.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="edad7-258">**IMFClock**</span><span class="sxs-lookup"><span data-stu-id="edad7-258">**IMFClock**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | <span data-ttu-id="edad7-259">Representa el reloj de la EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-259">Represents the EVR's clock.</span></span> <span data-ttu-id="edad7-260">El presentador usa esta interfaz para programar ejemplos para su presentación.</span><span class="sxs-lookup"><span data-stu-id="edad7-260">The presenter uses this interface to schedule samples for presentation.</span></span> <span data-ttu-id="edad7-261">El EVR se puede ejecutar sin un reloj, por lo que es posible que esta interfaz no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="edad7-261">The EVR can run without a clock, so this interface might not be available.</span></span> <span data-ttu-id="edad7-262">Si no es así, ignore el código de error [**de LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span><span class="sxs-lookup"><span data-stu-id="edad7-262">If not, ignore the error code from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span></span><br/> <span data-ttu-id="edad7-263">El reloj también implementa la [**interfaz IMFTimer.**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)</span><span class="sxs-lookup"><span data-stu-id="edad7-263">The clock also implements the [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) interface.</span></span> <span data-ttu-id="edad7-264">En la Media Foundation, el reloj implementa la [**interfaz IMFPresentationClock.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock)</span><span class="sxs-lookup"><span data-stu-id="edad7-264">In the Media Foundation pipeline, the clock implements the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span> <span data-ttu-id="edad7-265">No implementa esta interfaz en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="edad7-265">It does not implement this interface in DirectShow.</span></span><br/> |



 

<span data-ttu-id="edad7-266">Obtenga las siguientes interfaces del mezclador:</span><span class="sxs-lookup"><span data-stu-id="edad7-266">Get the following interfaces from the mixer:</span></span>



| <span data-ttu-id="edad7-267">Interfaz mezcladora</span><span class="sxs-lookup"><span data-stu-id="edad7-267">Mixer Interface</span></span>                              | <span data-ttu-id="edad7-268">Descripción</span><span class="sxs-lookup"><span data-stu-id="edad7-268">Description</span></span>                                                |
|----------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="edad7-269">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="edad7-269">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | <span data-ttu-id="edad7-270">Permite que el presentador se comunique con el mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-270">Enables the presenter to communicate with the mixer.</span></span>       |
| [<span data-ttu-id="edad7-271">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="edad7-271">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | <span data-ttu-id="edad7-272">Permite al presentador validar el GUID del dispositivo del mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-272">Enables the presenter to validate the mixer's device GUID.</span></span> |



 

<span data-ttu-id="edad7-273">El código siguiente implementa el [**método InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :</span><span class="sxs-lookup"><span data-stu-id="edad7-273">The following code implements the [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method :</span></span>


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="edad7-274">Cuando los punteros de interfaz obtenidos de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) ya no son válidos, el EVR llama a [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span><span class="sxs-lookup"><span data-stu-id="edad7-274">When the interface pointers obtained from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) are no longer valid, the EVR calls [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span></span> <span data-ttu-id="edad7-275">Dentro de este método, suelte todos los punteros de interfaz y establezca el estado del presentador para apagar:</span><span class="sxs-lookup"><span data-stu-id="edad7-275">Inside this method, release all interface pointers and set the presenter state to shut down:</span></span>


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



<span data-ttu-id="edad7-276">El EVR llama [**a ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) por diversos motivos, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="edad7-276">The EVR calls [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) for various reasons, including:</span></span>

-   <span data-ttu-id="edad7-277">Desconectar o volver a conectar los pines (DirectShow) o agregar o quitar receptores de flujo (Media Foundation).</span><span class="sxs-lookup"><span data-stu-id="edad7-277">Disconnecting or reconnecting pins (DirectShow), or adding or removing stream sinks (Media Foundation).</span></span>
-   <span data-ttu-id="edad7-278">Cambiar el formato.</span><span class="sxs-lookup"><span data-stu-id="edad7-278">Changing format.</span></span>
-   <span data-ttu-id="edad7-279">Establecer un nuevo reloj.</span><span class="sxs-lookup"><span data-stu-id="edad7-279">Setting a new clock.</span></span>
-   <span data-ttu-id="edad7-280">Cierre final de la EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-280">Final shutdown of the EVR.</span></span>

<span data-ttu-id="edad7-281">Durante la vigencia del presentador, la EVR podría llamar varias veces a [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) y [**ReleaseServicePointers.**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers)</span><span class="sxs-lookup"><span data-stu-id="edad7-281">During the lifetime of the presenter, the EVR might call [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) and [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) several times.</span></span>

### <a name="implementing-imfvideopresenter"></a><span data-ttu-id="edad7-282">Implementación de IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="edad7-282">Implementing IMFVideoPresenter</span></span>

<span data-ttu-id="edad7-283">La [**interfaz DEPRESENTVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) hereda [**EL VALOR DE LA PROPIEDAD Y agrega**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) dos métodos:</span><span class="sxs-lookup"><span data-stu-id="edad7-283">The [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface inherits [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) and adds two methods:</span></span>



| <span data-ttu-id="edad7-284">Método</span><span class="sxs-lookup"><span data-stu-id="edad7-284">Method</span></span>                                                               | <span data-ttu-id="edad7-285">Descripción</span><span class="sxs-lookup"><span data-stu-id="edad7-285">Description</span></span>                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="edad7-286">**GetCurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="edad7-286">**GetCurrentMediaType**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | <span data-ttu-id="edad7-287">Devuelve el tipo de medio de los fotogramas de vídeo compuestos.</span><span class="sxs-lookup"><span data-stu-id="edad7-287">Returns the media type of the composited video frames.</span></span> |
| [<span data-ttu-id="edad7-288">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="edad7-288">**ProcessMessage**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | <span data-ttu-id="edad7-289">Indica al presentador que realice varias acciones.</span><span class="sxs-lookup"><span data-stu-id="edad7-289">Signals the presenter to perform various actions.</span></span>      |



 

<span data-ttu-id="edad7-290">El [**método GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) devuelve el tipo de medio del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-290">The [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) method returns the presenter's media type.</span></span> <span data-ttu-id="edad7-291">(Para obtener más información sobre cómo establecer el tipo de medio, vea [Formatos de negociación).](#negotiating-formats) El tipo de medio se devuelve como un puntero de [**interfaz IMFVideoMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype)</span><span class="sxs-lookup"><span data-stu-id="edad7-291">(For details about setting the media type, see [Negotiating Formats](#negotiating-formats).) The media type is returned as an [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) interface pointer.</span></span> <span data-ttu-id="edad7-292">En el ejemplo siguiente se da por supuesto que el presentador almacena el tipo de medio como un [**puntero DE TIPO DEMEDIA.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)</span><span class="sxs-lookup"><span data-stu-id="edad7-292">The following example assumes that the presenter stores the media type as an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointer.</span></span> <span data-ttu-id="edad7-293">Para obtener la **interfaz IMFVideoMediaType del** tipo de medio, llame a **QueryInterface**:</span><span class="sxs-lookup"><span data-stu-id="edad7-293">To get the **IMFVideoMediaType** interface from the media type, call **QueryInterface**:</span></span>


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="edad7-294">El [**método ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) es el mecanismo principal para que la EVR se comunique con el presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-294">The [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method is the primary mechanism for the EVR to communicate with the presenter.</span></span> <span data-ttu-id="edad7-295">Se definen los mensajes siguientes.</span><span class="sxs-lookup"><span data-stu-id="edad7-295">The following messages are defined.</span></span> <span data-ttu-id="edad7-296">Los detalles de la implementación de cada mensaje se detallan en el resto de este tema.</span><span class="sxs-lookup"><span data-stu-id="edad7-296">The details of implementing each message are given in the remainder of this topic.</span></span>



| <span data-ttu-id="edad7-297">Message</span><span class="sxs-lookup"><span data-stu-id="edad7-297">Message</span></span>                                | <span data-ttu-id="edad7-298">Descripción</span><span class="sxs-lookup"><span data-stu-id="edad7-298">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edad7-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="edad7-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span></span> | <span data-ttu-id="edad7-300">El tipo de medio de salida del mezclador no es válido.</span><span class="sxs-lookup"><span data-stu-id="edad7-300">The mixer's output media type is invalid.</span></span> <span data-ttu-id="edad7-301">El presentador debe negociar un nuevo tipo de medio con el mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-301">The presenter should negotiate a new media type with the mixer.</span></span> <span data-ttu-id="edad7-302">Vea [Formatos de negociación.](#negotiating-formats)</span><span class="sxs-lookup"><span data-stu-id="edad7-302">See [Negotiating Formats](#negotiating-formats).</span></span>                                                                                         |
| <span data-ttu-id="edad7-303">**MFVP_MESSAGE_BEGINSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="edad7-303">**MFVP_MESSAGE_BEGINSTREAMING**</span></span>      | <span data-ttu-id="edad7-304">Se ha iniciado el streaming.</span><span class="sxs-lookup"><span data-stu-id="edad7-304">Streaming has started.</span></span> <span data-ttu-id="edad7-305">Este mensaje no requiere ninguna acción concreta, pero puede usarla para asignar recursos.</span><span class="sxs-lookup"><span data-stu-id="edad7-305">No particular action is required by this message, but you can use it to allocate resources.</span></span>                                                                                                                                 |
| <span data-ttu-id="edad7-306">**MFVP_MESSAGE_ENDSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="edad7-306">**MFVP_MESSAGE_ENDSTREAMING**</span></span>        | <span data-ttu-id="edad7-307">El streaming ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="edad7-307">Streaming has ended.</span></span> <span data-ttu-id="edad7-308">Libere los recursos que asignó en respuesta al **MFVP_MESSAGE_BEGINSTREAMING** mensaje.</span><span class="sxs-lookup"><span data-stu-id="edad7-308">Release any resources that you allocated in response to the **MFVP_MESSAGE_BEGINSTREAMING** message.</span></span>                                                                                                                        |
| <span data-ttu-id="edad7-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="edad7-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span></span>  | <span data-ttu-id="edad7-310">El mezclador ha recibido un nuevo ejemplo de entrada y puede generar un nuevo marco de salida.</span><span class="sxs-lookup"><span data-stu-id="edad7-310">The mixer has received a new input sample and might be able to generate a new output frame.</span></span> <span data-ttu-id="edad7-311">El presentador debe llamar [**a IMFTransform::P rocessOutput en**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) el mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-311">The presenter should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="edad7-312">Vea [Procesamiento de la salida](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="edad7-312">See [Processing Output](#processing-output).</span></span> |
| <span data-ttu-id="edad7-313">**MFVP_MESSAGE_ENDOFSTREAM**</span><span class="sxs-lookup"><span data-stu-id="edad7-313">**MFVP_MESSAGE_ENDOFSTREAM**</span></span>         | <span data-ttu-id="edad7-314">La presentación ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="edad7-314">The presentation has ended.</span></span> <span data-ttu-id="edad7-315">Vea [End of Stream (Fin de la secuencia).](#end-of-stream)</span><span class="sxs-lookup"><span data-stu-id="edad7-315">See [End of Stream](#end-of-stream).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="edad7-316">**MFVP_MESSAGE_FLUSH**</span><span class="sxs-lookup"><span data-stu-id="edad7-316">**MFVP_MESSAGE_FLUSH**</span></span>               | <span data-ttu-id="edad7-317">El EVR vacíe los datos en su canalización de representación.</span><span class="sxs-lookup"><span data-stu-id="edad7-317">The EVR is flushing the data in its rendering pipeline.</span></span> <span data-ttu-id="edad7-318">El presentador debe descartar los fotogramas de vídeo programados para su presentación.</span><span class="sxs-lookup"><span data-stu-id="edad7-318">The presenter should discard any video frames that are scheduled for presentation.</span></span>                                                                                                         |
| <span data-ttu-id="edad7-319">**MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="edad7-319">**MFVP_MESSAGE_STEP**</span></span>                | <span data-ttu-id="edad7-320">Solicita al presentador que avance N fotogramas.</span><span class="sxs-lookup"><span data-stu-id="edad7-320">Requests the presenter to step forward N frames.</span></span> <span data-ttu-id="edad7-321">El presentador debe descartar los fotogramas N-1 siguientes y mostrar el enésimo fotograma.</span><span class="sxs-lookup"><span data-stu-id="edad7-321">The presenter should discard the next N-1 frames and display the Nth frame.</span></span> <span data-ttu-id="edad7-322">Vea [Paso a paso por fotogramas.](#frame-stepping)</span><span class="sxs-lookup"><span data-stu-id="edad7-322">See [Frame Stepping](#frame-stepping).</span></span>                                                                                |
| <span data-ttu-id="edad7-323">**MFVP_MESSAGE_CANCELSTEP**</span><span class="sxs-lookup"><span data-stu-id="edad7-323">**MFVP_MESSAGE_CANCELSTEP**</span></span>          | <span data-ttu-id="edad7-324">Cancela la ejecución paso a paso del marco.</span><span class="sxs-lookup"><span data-stu-id="edad7-324">Cancels frame stepping.</span></span>                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a><span data-ttu-id="edad7-325">Implementación de IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="edad7-325">Implementing IMFClockStateSink</span></span>

<span data-ttu-id="edad7-326">El presentador debe implementar la interfaz [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) como parte de su implementación de [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), que hereda **LADELOCKStateSink.**</span><span class="sxs-lookup"><span data-stu-id="edad7-326">The presenter must implement the [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) interface as part of its implementation of [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), which inherits **IMFClockStateSink**.</span></span> <span data-ttu-id="edad7-327">El EVR usa esta interfaz para notificar al presentador cada vez que el reloj del EVR cambia de estado.</span><span class="sxs-lookup"><span data-stu-id="edad7-327">The EVR uses this interface to notify the presenter whenever the EVR's clock changes state.</span></span> <span data-ttu-id="edad7-328">Para obtener más información sobre los estados del reloj, vea [Reloj de presentación](presentation-clock.md).</span><span class="sxs-lookup"><span data-stu-id="edad7-328">For more information about the clock states, see [Presentation Clock](presentation-clock.md).</span></span>

<span data-ttu-id="edad7-329">Estas son algunas directrices para implementar los métodos en esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="edad7-329">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="edad7-330">Todos los métodos deben producir un error si el presentador está apagado.</span><span class="sxs-lookup"><span data-stu-id="edad7-330">All of the methods should fail if the presenter is shut down.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="edad7-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="edad7-332">Establezca el estado del presentador en Iniciado.</span><span class="sxs-lookup"><span data-stu-id="edad7-332">Set the presenter state to started.</span></span></li>
<li><span data-ttu-id="edad7-333">Si <em>llClockStartOffset</em> no está <strong>PRESENTATION_CURRENT_POSITION</strong>, vacíe la cola de ejemplos del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-333">If the <em>llClockStartOffset</em> is not <strong>PRESENTATION_CURRENT_POSITION</strong>, flush the presenter's queue of samples.</span></span> <span data-ttu-id="edad7-334">(Esto equivale a recibir un <strong>mensaje MFVP_MESSAGE_FLUSH</strong> mensaje).</span><span class="sxs-lookup"><span data-stu-id="edad7-334">(This is equivalent to receiving an <strong>MFVP_MESSAGE_FLUSH</strong> message.)</span></span></li>
<li><span data-ttu-id="edad7-335">Si una solicitud de paso de fotograma anterior sigue pendiente, procese la solicitud (vea Paso a <a href="#frame-stepping">paso por fotogramas).</a></span><span class="sxs-lookup"><span data-stu-id="edad7-335">If a previous frame-step request is still pending, process the request (see <a href="#frame-stepping">Frame Stepping</a>).</span></span> <span data-ttu-id="edad7-336">De lo contrario, intente procesar la salida del mezclador (consulte <a href="#processing-output">Procesamiento de la salida</a>.</span><span class="sxs-lookup"><span data-stu-id="edad7-336">Otherwise, try to process output from the mixer (see <a href="#processing-output">Processing Output</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edad7-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="edad7-338">Establezca el estado del presentador en detenido.</span><span class="sxs-lookup"><span data-stu-id="edad7-338">Set the presenter state to stopped.</span></span></li>
<li><span data-ttu-id="edad7-339">Vacíe la cola de ejemplos del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-339">Flush the presenter's queue of samples.</span></span></li>
<li><span data-ttu-id="edad7-340">Cancele cualquier operación de paso de fotograma pendiente.</span><span class="sxs-lookup"><span data-stu-id="edad7-340">Cancel any pending frame-step operation.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edad7-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span></span></td>
<td><span data-ttu-id="edad7-342">Establezca el estado del presentador en en pausa.</span><span class="sxs-lookup"><span data-stu-id="edad7-342">Set the presenter state to paused.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edad7-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span></span></td>
<td><span data-ttu-id="edad7-344">Trate lo mismo que <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart,</strong></a> pero no vacíe la cola de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="edad7-344">Treat the same as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> but do not flush the queue of samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edad7-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="edad7-346">Si la velocidad cambia de cero a distinto de cero, cancele la ejecución paso a paso del marco.</span><span class="sxs-lookup"><span data-stu-id="edad7-346">If the rate is changing from zero to nonzero, cancel frame stepping.</span></span></li>
<li><span data-ttu-id="edad7-347">Almacene la nueva velocidad de reloj.</span><span class="sxs-lookup"><span data-stu-id="edad7-347">Store the new clock rate.</span></span> <span data-ttu-id="edad7-348">La velocidad del reloj afecta al momento en que se presentan las muestras.</span><span class="sxs-lookup"><span data-stu-id="edad7-348">The clock rate affects when samples are presented.</span></span> <span data-ttu-id="edad7-349">Para obtener más información, vea <a href="#scheduling-samples">Scheduling Samples</a>.</span><span class="sxs-lookup"><span data-stu-id="edad7-349">For more information, see <a href="#scheduling-samples">Scheduling Samples</a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a><span data-ttu-id="edad7-350">Implementación de IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="edad7-350">Implementing IMFRateSupport</span></span>

<span data-ttu-id="edad7-351">Para admitir velocidades de reproducción diferentes de 1× velocidad, el presentador debe implementar la [**interfaz IMFRateSupport.**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)</span><span class="sxs-lookup"><span data-stu-id="edad7-351">To support playback rates other than 1× speed, the presenter must implement the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface.</span></span> <span data-ttu-id="edad7-352">Estas son algunas directrices para implementar los métodos en esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="edad7-352">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="edad7-353">Todos los métodos deben producir un error después de apagar el presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-353">All of the methods should fail after the presenter is shut down.</span></span> <span data-ttu-id="edad7-354">Para obtener más información sobre esta interfaz, vea [Control de velocidad.](rate-control.md)</span><span class="sxs-lookup"><span data-stu-id="edad7-354">For more information about this interface, see [Rate Control](rate-control.md).</span></span>



| <span data-ttu-id="edad7-355">Valor</span><span class="sxs-lookup"><span data-stu-id="edad7-355">Value</span></span>                                                          | <span data-ttu-id="edad7-356">Descripción</span><span class="sxs-lookup"><span data-stu-id="edad7-356">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edad7-357">**GetSlowestRate**</span><span class="sxs-lookup"><span data-stu-id="edad7-357">**GetSlowestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | <span data-ttu-id="edad7-358">Devuelve cero para indicar que no hay velocidad de reproducción mínima.</span><span class="sxs-lookup"><span data-stu-id="edad7-358">Return zero to indicate no minimum playback rate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="edad7-359">**GetFastestRate**</span><span class="sxs-lookup"><span data-stu-id="edad7-359">**GetFastestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | <span data-ttu-id="edad7-360">En el caso de la reproducción no fina, la velocidad de reproducción no debe superar la frecuencia de actualización del *monitor:* velocidad máxima de actualización (Hz) /velocidad de fotogramas de  =   vídeo (fps). </span><span class="sxs-lookup"><span data-stu-id="edad7-360">For non-thinned playback, the playback rate should not exceed the refresh rate of the monitor: *maximum rate* = *refresh rate* (Hz) / *video frame rate* (fps).</span></span> <span data-ttu-id="edad7-361">La velocidad de fotogramas de vídeo se especifica en el tipo de medio del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-361">The video frame rate is specified in the presenter's media type.</span></span> <br/> <span data-ttu-id="edad7-362">En el caso de la reproducción fina, la velocidad de reproducción es sin enlazar; devuelve el valor **FLT_MAX**.</span><span class="sxs-lookup"><span data-stu-id="edad7-362">For thinned playback, the playback rate is unbounded; return the value **FLT_MAX**.</span></span> <span data-ttu-id="edad7-363">En la práctica, el origen y el descodificador serán los factores de limitación durante la reproducción fina.</span><span class="sxs-lookup"><span data-stu-id="edad7-363">In practice, the source and the decoder will be the limiting factors during thinned playback.</span></span> <br/> <span data-ttu-id="edad7-364">Para la reproducción inversa, devuelve el valor negativo de la velocidad máxima.</span><span class="sxs-lookup"><span data-stu-id="edad7-364">For reverse playback, return the negative of the maximum rate.</span></span><br/> |
| [<span data-ttu-id="edad7-365">**IsRateSupported**</span><span class="sxs-lookup"><span data-stu-id="edad7-365">**IsRateSupported**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | <span data-ttu-id="edad7-366">Devuelve **MF_E_UNSUPPORTED_RATE** si el valor absoluto de *flRate* supera la velocidad de reproducción máxima del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-366">Return **MF_E_UNSUPPORTED_RATE** if the absolute value of *flRate* exceeds the presenter's maximum playback rate.</span></span> <span data-ttu-id="edad7-367">Calcule la velocidad de reproducción máxima como se describe [**para GetFastestRate.**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)</span><span class="sxs-lookup"><span data-stu-id="edad7-367">Calculate the maximum playback rate as described for [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span></span>                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="edad7-368">En el ejemplo siguiente se muestra cómo implementar el [**método GetFastestRate:**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)</span><span class="sxs-lookup"><span data-stu-id="edad7-368">The following example shows how to implement the [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) method:</span></span>


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



<span data-ttu-id="edad7-369">En el ejemplo anterior se llama a un método auxiliar, GetMaxRate, para calcular la velocidad máxima de reproducción hacia delante:</span><span class="sxs-lookup"><span data-stu-id="edad7-369">The previous example calls a helper method, GetMaxRate, to calculate the maximum forward playback rate:</span></span>

<span data-ttu-id="edad7-370">En el ejemplo siguiente se muestra cómo implementar el [**método IsRateSupported:**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported)</span><span class="sxs-lookup"><span data-stu-id="edad7-370">The following example shows how to implement the [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method:</span></span>


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a><span data-ttu-id="edad7-371">Envío de eventos al EVR</span><span class="sxs-lookup"><span data-stu-id="edad7-371">Sending Events to the EVR</span></span>

<span data-ttu-id="edad7-372">El presentador debe notificar al EVR varios eventos.</span><span class="sxs-lookup"><span data-stu-id="edad7-372">The presenter must notify the EVR of various events.</span></span> <span data-ttu-id="edad7-373">Para ello, usa la interfaz [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) de EVR, obtenida cuando el EVR llama al método [**DEVTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-373">To do so, it uses the EVR's [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) interface, obtained when the EVR calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="edad7-374">(La **interfaz IMediaEventSink** es originalmente una interfaz DirectShow, pero se usa tanto en la EVR de DirectShow como en la Media Foundation). El código siguiente muestra cómo enviar un evento al EVR:</span><span class="sxs-lookup"><span data-stu-id="edad7-374">(The **IMediaEventSink** interface is originally a DirectShow interface, but is used in both the DirectShow EVR and the Media Foundation.) The following code shows how to send an event to the EVR:</span></span>


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



<span data-ttu-id="edad7-375">En la tabla siguiente se enumeran los eventos que envía el presentador, junto con los parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="edad7-375">The following table lists the events that the presenter sends, along with the event parameters.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="edad7-376">Evento</span><span class="sxs-lookup"><span data-stu-id="edad7-376">Event</span></span></th>
<th><span data-ttu-id="edad7-377">Descripción</span><span class="sxs-lookup"><span data-stu-id="edad7-377">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="edad7-378"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-378"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="edad7-379">El presentador ha terminado de representar todos los fotogramas después del MFVP_MESSAGE_ENDOFSTREAM mensaje.</span><span class="sxs-lookup"><span data-stu-id="edad7-379">The presenter has finished rendering all frames after the MFVP_MESSAGE_ENDOFSTREAM message.</span></span><br/>
<ul>
<li><span data-ttu-id="edad7-380"><em>Param1:</em>HRESULT que indica el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="edad7-380"><em>Param1</em>: HRESULT indicating the status of the operation.</span></span></li>
<li><span data-ttu-id="edad7-381"><em>Param2:</em>no se usa.</span><span class="sxs-lookup"><span data-stu-id="edad7-381"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="edad7-382">Para obtener más información, vea <a href="#end-of-stream">End of Stream</a>.</span><span class="sxs-lookup"><span data-stu-id="edad7-382">For more information, see <a href="#end-of-stream">End of Stream</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edad7-383"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-383"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span></span></td>
<td><span data-ttu-id="edad7-384">El dispositivo Direct3D ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="edad7-384">The Direct3D device has changed.</span></span><br/>
<ul>
<li><span data-ttu-id="edad7-385"><em>Param1:</em>No se usa.</span><span class="sxs-lookup"><span data-stu-id="edad7-385"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="edad7-386"><em>Param2:</em>no se usa.</span><span class="sxs-lookup"><span data-stu-id="edad7-386"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="edad7-387">Para obtener más información, consulte <a href="#managing-the-direct3d-device">Administración del dispositivo Direct3D.</a></span><span class="sxs-lookup"><span data-stu-id="edad7-387">For more information, see <a href="#managing-the-direct3d-device">Managing the Direct3D Device</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edad7-388"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-388"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span></span></td>
<td><span data-ttu-id="edad7-389">Se ha producido un error que requiere que el streaming se detenga.</span><span class="sxs-lookup"><span data-stu-id="edad7-389">An error has occurred that requires streaming to stop.</span></span><br/>
<ul>
<li><span data-ttu-id="edad7-390"><em>Param1:</em> <strong>HRESULT</strong> que indica el error que se produjo.</span><span class="sxs-lookup"><span data-stu-id="edad7-390"><em>Param1</em>: <strong>HRESULT</strong> indicating the error that occurred.</span></span></li>
<li><span data-ttu-id="edad7-391"><em>Param2:</em>no se usa.</span><span class="sxs-lookup"><span data-stu-id="edad7-391"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edad7-392"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-392"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="edad7-393">Especifica la cantidad de tiempo que tarda el presentador en representar cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="edad7-393">Specifies the amount of time that the presenter is taking to render each frame.</span></span> <span data-ttu-id="edad7-394">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="edad7-394">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="edad7-395"><em>Param1:</em>puntero a un valor <strong>LONGLONG</strong> constante que contiene la cantidad de tiempo para procesar el fotograma, en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="edad7-395"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the amount of time to process the frame, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="edad7-396"><em>Param2:</em>no se usa.</span><span class="sxs-lookup"><span data-stu-id="edad7-396"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="edad7-397">Para obtener más información, vea <a href="#processing-output">Procesamiento de la salida</a>.</span><span class="sxs-lookup"><span data-stu-id="edad7-397">For more information, see <a href="#processing-output">Processing Output</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edad7-398"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-398"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="edad7-399">Especifica el tiempo de retraso actual en la representación de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="edad7-399">Specifies the current lag time in rendering samples.</span></span> <span data-ttu-id="edad7-400">Si el valor es positivo, los ejemplos están detrás de la programación.</span><span class="sxs-lookup"><span data-stu-id="edad7-400">If the value is positive, samples are behind schedule.</span></span> <span data-ttu-id="edad7-401">Si el valor es negativo, los ejemplos se adelantan a la programación.</span><span class="sxs-lookup"><span data-stu-id="edad7-401">If the value is negative, samples are ahead of schedule.</span></span> <span data-ttu-id="edad7-402">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="edad7-402">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="edad7-403"><em>Param1:</em>puntero a un valor <strong>LONGLONG</strong> constante que contiene el tiempo de retraso, en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="edad7-403"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the lag time, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="edad7-404"><em>Param2:</em>no se usa.</span><span class="sxs-lookup"><span data-stu-id="edad7-404"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edad7-405"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-405"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span></span></td>
<td><span data-ttu-id="edad7-406">Se envía inmediatamente <strong>después EC_STEP_COMPLETE</strong> si la velocidad de reproducción es cero.</span><span class="sxs-lookup"><span data-stu-id="edad7-406">Sent immediately after <strong>EC_STEP_COMPLETE</strong> if the playback rate is zero.</span></span> <span data-ttu-id="edad7-407">Este evento contiene la marca de tiempo del fotograma que se ha mostrado.</span><span class="sxs-lookup"><span data-stu-id="edad7-407">This event contains the time stamp of the frame that was displayed.</span></span><br/>
<ul>
<li><span data-ttu-id="edad7-408"><em>Param1:</em>32 bits inferiores de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="edad7-408"><em>Param1</em>: Lower 32 bits of the time stamp.</span></span></li>
<li><span data-ttu-id="edad7-409"><em>Param2:</em>32 bits superiores de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="edad7-409"><em>Param2</em>: Upper 32 bits of the time stamp.</span></span></li>
</ul>
<span data-ttu-id="edad7-410">Para obtener más información, vea <a href="#frame-stepping">Frame Stepping</a>.</span><span class="sxs-lookup"><span data-stu-id="edad7-410">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edad7-411"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="edad7-411"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="edad7-412">El presentador ha completado o cancelado un paso de fotograma.</span><span class="sxs-lookup"><span data-stu-id="edad7-412">The presenter has completed or canceled a frame step.</span></span><br/>
<ul>
<li><span data-ttu-id="edad7-413"><em>Param1:</em>No se usa.</span><span class="sxs-lookup"><span data-stu-id="edad7-413"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="edad7-414"><em>Param2:</em>no se usa.</span><span class="sxs-lookup"><span data-stu-id="edad7-414"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="edad7-415">Para obtener más información, vea <a href="#frame-stepping">Frame Stepping</a>.</span><span class="sxs-lookup"><span data-stu-id="edad7-415">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="edad7-416">Una versión anterior de la documentación descrita <em>param1 incorrectamente.</em></span><span class="sxs-lookup"><span data-stu-id="edad7-416">A previous version of the documentation described <em>Param1</em> incorrectly.</span></span> <span data-ttu-id="edad7-417">Este parámetro no se usa para este evento.</span><span class="sxs-lookup"><span data-stu-id="edad7-417">This parameter is not used for this event.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a><span data-ttu-id="edad7-418">Formatos de negociación</span><span class="sxs-lookup"><span data-stu-id="edad7-418">Negotiating Formats</span></span>

<span data-ttu-id="edad7-419">Cada vez que el presentador **recibe MFVP_MESSAGE_INVALIDATEMEDIATYPE** mensaje de la EVR, debe establecer el formato de salida en el mezclador, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="edad7-419">Whenever the presenter receives an **MFVP_MESSAGE_INVALIDATEMEDIATYPE** message from the EVR, it must set the output format on the mixer, as follows:</span></span>

1.  <span data-ttu-id="edad7-420">Llame [**a IMFTransform::GetOutputAvailableType en**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) el mezclador para obtener un posible tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="edad7-420">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) on the mixer to get a possible output type.</span></span> <span data-ttu-id="edad7-421">Este tipo describe un formato que el mezclador puede producir dadas las secuencias de entrada y las funcionalidades de procesamiento de vídeo del dispositivo gráfico.</span><span class="sxs-lookup"><span data-stu-id="edad7-421">This type describes a format that the mixer can produce given the input streams and the video processing capabilities of the graphics device.</span></span>
2.  <span data-ttu-id="edad7-422">Compruebe si el presentador puede usar este tipo de medio como formato de representación.</span><span class="sxs-lookup"><span data-stu-id="edad7-422">Check whether the presenter can use this media type as its rendering format.</span></span> <span data-ttu-id="edad7-423">Estos son algunos aspectos que debe comprobar, aunque la implementación puede tener sus propios requisitos:</span><span class="sxs-lookup"><span data-stu-id="edad7-423">Here are some things to check, although your implementation might have its own requirements:</span></span>

    -   <span data-ttu-id="edad7-424">El vídeo debe estar descomprimido.</span><span class="sxs-lookup"><span data-stu-id="edad7-424">The video must be uncompressed.</span></span>
    -   <span data-ttu-id="edad7-425">El vídeo solo debe tener fotogramas progresivas.</span><span class="sxs-lookup"><span data-stu-id="edad7-425">The video must have progressive frames only.</span></span> <span data-ttu-id="edad7-426">Compruebe que el [**atributo MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) es igual **a MFVideoInterlace_Progressive**.</span><span class="sxs-lookup"><span data-stu-id="edad7-426">Check that the [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) attribute equals **MFVideoInterlace_Progressive**.</span></span>
    -   <span data-ttu-id="edad7-427">El formato debe ser compatible con el dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="edad7-427">The format must be compatible with the Direct3D device.</span></span>

    <span data-ttu-id="edad7-428">Si el tipo no es aceptable, vuelva al paso 1 y obtenga el siguiente tipo propuesto del mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-428">If the type is not acceptable, return to step 1 and get the mixer's next proposed type.</span></span>

3.  <span data-ttu-id="edad7-429">Cree un nuevo tipo de medio que sea un clon del tipo original y, a continuación, cambie los atributos siguientes:</span><span class="sxs-lookup"><span data-stu-id="edad7-429">Create a new media type that is a clone of the original type and then change the following attributes:</span></span>

    -   <span data-ttu-id="edad7-430">Establezca el [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) atributo igual al ancho y alto que desea para las superficies de Direct3D que va a asignar.</span><span class="sxs-lookup"><span data-stu-id="edad7-430">Set the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute equal to the width and height that you want for the Direct3D surfaces you will allocate.</span></span>
    -   <span data-ttu-id="edad7-431">Establezca el [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) en **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="edad7-431">Set the [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **FALSE**.</span></span>
    -   <span data-ttu-id="edad7-432">Establezca el [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) atributo igual al PAR de la pantalla (normalmente 1:1).</span><span class="sxs-lookup"><span data-stu-id="edad7-432">Set the [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute equal to the PAR of the display (typically 1:1).</span></span>
    -   <span data-ttu-id="edad7-433">Establezca la apertura geométrica [**(MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) atributo) igual a un rectángulo dentro de la superficie de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="edad7-433">Set the geometric aperture ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) attribute) equal to a rectangle within the Direct3D surface.</span></span> <span data-ttu-id="edad7-434">Cuando el mezclador genera un marco de salida, corta la imagen de origen en este rectángulo.</span><span class="sxs-lookup"><span data-stu-id="edad7-434">When the mixer generates an output frame, it blits the source image onto this rectangle.</span></span> <span data-ttu-id="edad7-435">La apertura geométrica puede ser tan grande como la superficie, o puede ser una subrecta dentro de la superficie.</span><span class="sxs-lookup"><span data-stu-id="edad7-435">The geometric aperture can be as large as the surface, or it can be a subrectangle within the surface.</span></span> <span data-ttu-id="edad7-436">Para obtener más información, vea [Rectángulos de origen y destino.](#source-and-destination-rectangles)</span><span class="sxs-lookup"><span data-stu-id="edad7-436">For more information, see [Source and Destination Rectangles](#source-and-destination-rectangles).</span></span>

4.  <span data-ttu-id="edad7-437">Para probar si el mezclador aceptará el tipo de salida **modificado,** llame a [**LALETransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) con la MFT_SET_TYPE_TEST_ONLY entrada.</span><span class="sxs-lookup"><span data-stu-id="edad7-437">To test whether the mixer will accept the modified output type, call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with the **MFT_SET_TYPE_TEST_ONLY** flag.</span></span> <span data-ttu-id="edad7-438">Si el mezclador rechaza el tipo, vuelva al paso 1 y obtenga el siguiente tipo.</span><span class="sxs-lookup"><span data-stu-id="edad7-438">If the mixer rejects the type, go back to step 1 and get the next type.</span></span>
5.  <span data-ttu-id="edad7-439">Asigne un grupo de superficies de Direct3D, como se describe [en Asignación de superficies de Direct3D.](#allocating-direct3d-surfaces)</span><span class="sxs-lookup"><span data-stu-id="edad7-439">Allocate a pool of Direct3D surfaces, as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="edad7-440">El mezclador usará estas superficies cuando dibuje los fotogramas de vídeo compuestos.</span><span class="sxs-lookup"><span data-stu-id="edad7-440">The mixer will use these surfaces when it draws the composited video frames.</span></span>
6.  <span data-ttu-id="edad7-441">Establezca el tipo de salida en el mezclador llamando a [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sin marcas.</span><span class="sxs-lookup"><span data-stu-id="edad7-441">Set the output type on the mixer by calling [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with no flags.</span></span> <span data-ttu-id="edad7-442">Si la primera llamada a **SetOutputType** se ha hecho correctamente en el paso 4, el método debería tener éxito de nuevo.</span><span class="sxs-lookup"><span data-stu-id="edad7-442">If the first call to **SetOutputType** succeeded in step 4, the method should succeed again.</span></span>

<span data-ttu-id="edad7-443">Si el mezclador se queda sin tipos, el [**método GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) devuelve **MF_E_NO_MORE_TYPES**.</span><span class="sxs-lookup"><span data-stu-id="edad7-443">If the mixer runs out of types, the [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method returns **MF_E_NO_MORE_TYPES**.</span></span> <span data-ttu-id="edad7-444">Si el presentador no encuentra un tipo de salida adecuado para el mezclador, la secuencia no se puede representar.</span><span class="sxs-lookup"><span data-stu-id="edad7-444">If the presenter cannot find a suitable output type for the mixer, the stream cannot be rendered.</span></span> <span data-ttu-id="edad7-445">En ese caso, DirectShow o Media Foundation probar otro formato de secuencia.</span><span class="sxs-lookup"><span data-stu-id="edad7-445">In that case, DirectShow or Media Foundation might try another stream format.</span></span> <span data-ttu-id="edad7-446">Por lo tanto, el presentador puede recibir **varios mensajes MFVP_MESSAGE_INVALIDATEMEDIATYPE** en una fila hasta que se encuentra un tipo válido.</span><span class="sxs-lookup"><span data-stu-id="edad7-446">Therefore, the presenter might receive several **MFVP_MESSAGE_INVALIDATEMEDIATYPE** messages in a row until a valid type is found.</span></span>

<span data-ttu-id="edad7-447">El mezclador crea automáticamente un cuadro de texto del vídeo, teniendo en cuenta la relación de aspecto de píxeles (PAR) del origen y el destino.</span><span class="sxs-lookup"><span data-stu-id="edad7-447">The mixer automatically letterboxes the video, taking into account the pixel aspect ratio (PAR) of the source and destination.</span></span> <span data-ttu-id="edad7-448">Para obtener mejores resultados, el ancho y el alto de la superficie y la apertura geométrica deben ser iguales al tamaño real que desea que el vídeo aparezca en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="edad7-448">For best results, the surface width and height and the geometric aperture should be equal to the actual size that you want the video to appear on the display.</span></span> <span data-ttu-id="edad7-449">En la imagen siguiente se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="edad7-449">The following image illustrates this process.</span></span>

![diagrama que muestra un fram compuesto que conduce a una superficie direct3d, que conduce a una ventana](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

<span data-ttu-id="edad7-451">El código siguiente muestra el esquema del proceso.</span><span class="sxs-lookup"><span data-stu-id="edad7-451">The following code shows the outline of the process.</span></span> <span data-ttu-id="edad7-452">Algunos de los pasos se colocan en funciones auxiliares, cuyos detalles exactos dependerán de los requisitos del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-452">Some of the steps are placed in helper functions, the exact details of which will depend on the requirements of your presenter.</span></span>


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



<span data-ttu-id="edad7-453">Para obtener más información sobre los tipos de medios de vídeo, vea [Tipos de medios de vídeo](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="edad7-453">For more information about video media types, see [Video Media Types](video-media-types.md).</span></span>

## <a name="managing-the-direct3d-device"></a><span data-ttu-id="edad7-454">Administración del dispositivo Direct3D</span><span class="sxs-lookup"><span data-stu-id="edad7-454">Managing the Direct3D Device</span></span>

<span data-ttu-id="edad7-455">El presentador crea el dispositivo Direct3D y controla las pérdidas de dispositivos durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="edad7-455">The presenter creates the Direct3D device and handles any device loss during streaming.</span></span> <span data-ttu-id="edad7-456">El presentador también hospeda el administrador de dispositivos Direct3D, que proporciona una manera de que otros componentes usen el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edad7-456">The presenter also hosts the Direct3D device manager, which provides a way for other components to use the same device.</span></span> <span data-ttu-id="edad7-457">Por ejemplo, el mezclador usa el dispositivo Direct3D para mezclar substreams, desinterlace y realizar ajustes de color.</span><span class="sxs-lookup"><span data-stu-id="edad7-457">For example, the mixer uses the Direct3D device to mix substreams, deinterlace, and perform color adjustments.</span></span> <span data-ttu-id="edad7-458">Los descodificadores pueden usar el dispositivo Direct3D para descodificación acelerada por vídeo.</span><span class="sxs-lookup"><span data-stu-id="edad7-458">Decoders can use the Direct3D device for video-accelerated decoding.</span></span> <span data-ttu-id="edad7-459">(Para obtener más información sobre la aceleración de vídeo, [vea DirectX Video Acceleration 2.0).](directx-video-acceleration-2-0.md)</span><span class="sxs-lookup"><span data-stu-id="edad7-459">(For more information about video acceleration, see [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).)</span></span>

<span data-ttu-id="edad7-460">Para configurar el dispositivo Direct3D, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="edad7-460">To set up the Direct3D device, perform the following steps:</span></span>

1.  <span data-ttu-id="edad7-461">Cree el objeto Direct3D mediante una **llamada a Direct3DCreate9** o **Direct3DCreate9Ex.**</span><span class="sxs-lookup"><span data-stu-id="edad7-461">Create the Direct3D object by calling **Direct3DCreate9** or **Direct3DCreate9Ex**.</span></span>
2.  <span data-ttu-id="edad7-462">Cree el dispositivo mediante una llamada **a IDirect3D9::CreateDevice** o **IDirect3D9Ex::CreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="edad7-462">Create the device by calling **IDirect3D9::CreateDevice** or **IDirect3D9Ex::CreateDevice**.</span></span>
3.  <span data-ttu-id="edad7-463">Cree el administrador de dispositivos mediante [**una llamada a DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="edad7-463">Create the device manager by calling [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span>
4.  <span data-ttu-id="edad7-464">Establezca el dispositivo en el administrador de dispositivos mediante una [**llamada a IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="edad7-464">Set the device on the device manager by calling [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span>

<span data-ttu-id="edad7-465">Si otro componente de canalización necesita el administrador de dispositivos, llama a  [**ALGETGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en la EVR, especificando MR_VIDEO_ACCELERATION_SERVICE para el GUID del servicio.</span><span class="sxs-lookup"><span data-stu-id="edad7-465">If another pipeline component needs the device manager, it calls [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR, specifying **MR_VIDEO_ACCELERATION_SERVICE** for the service GUID.</span></span> <span data-ttu-id="edad7-466">El EVR pasa la solicitud al presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-466">The EVR passes the request to the presenter.</span></span> <span data-ttu-id="edad7-467">Una vez que el objeto obtiene el puntero [**IDirect3DDeviceManager9,**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) puede obtener un identificador para el dispositivo llamando a [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span><span class="sxs-lookup"><span data-stu-id="edad7-467">After the object gets the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) pointer, it can get a handle to the device by calling [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span></span> <span data-ttu-id="edad7-468">Cuando el objeto necesita usar el dispositivo, pasa el identificador del dispositivo al método [**IDirect3DDeviceManager9::LockDevice,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) que devuelve un puntero **IDirect3DDevice9.**</span><span class="sxs-lookup"><span data-stu-id="edad7-468">When the object needs to use the device, it passes the device handle to the [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method, which returns an **IDirect3DDevice9** pointer.</span></span>

<span data-ttu-id="edad7-469">Una vez creado el dispositivo, si el presentador destruye el dispositivo y crea uno nuevo, el presentador debe llamar de nuevo a [**ResetDevice.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)</span><span class="sxs-lookup"><span data-stu-id="edad7-469">After the device is created, if the presenter destroys the device and creates a new one, the presenter must call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) again.</span></span> <span data-ttu-id="edad7-470">El **método ResetDevice** invalida los identificadores de dispositivo existentes, lo que hace que [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) devuelva **DXVA2_E_NEW_VIDEO_DEVICE**.</span><span class="sxs-lookup"><span data-stu-id="edad7-470">The **ResetDevice** method invalidates any existing device handles, which causes [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) to return **DXVA2_E_NEW_VIDEO_DEVICE**.</span></span> <span data-ttu-id="edad7-471">Este código de error indica a otros objetos que usan el dispositivo que deben abrir un nuevo identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edad7-471">This error code signals to other objects using the device that they should open a new device handle.</span></span> <span data-ttu-id="edad7-472">Para obtener más información sobre el uso del administrador de dispositivos, [consulte Direct3D Administrador de dispositivos](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="edad7-472">For more information about using the device manager, see [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="edad7-473">El presentador puede crear el dispositivo en modo de ventana o en modo exclusivo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="edad7-473">The presenter can create the device in windowed mode or full-screen exclusive mode.</span></span> <span data-ttu-id="edad7-474">Para el modo de ventana, debe proporcionar una manera de que la aplicación especifique la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="edad7-474">For windowed mode, you should provide a way for the application to specify the video window.</span></span> <span data-ttu-id="edad7-475">El presentador estándar implementa el [**método IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) para este propósito.</span><span class="sxs-lookup"><span data-stu-id="edad7-475">The standard presenter implements the [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) method for this purpose.</span></span> <span data-ttu-id="edad7-476">Debe crear el dispositivo cuando se cree por primera vez el presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-476">You must create the device when the presenter is first created.</span></span> <span data-ttu-id="edad7-477">Normalmente, no conocerá todos los parámetros del dispositivo en este momento, como la ventana o el formato de búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="edad7-477">Typically, you won't know all of the device parameters at this time, such as the window or the back buffer format.</span></span> <span data-ttu-id="edad7-478">Puede crear un dispositivo temporal y reemplazarlo más&;solo tiene que recordar llamar a \# [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) en el administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="edad7-478">You can create a temporary device and replace it later&\#;just remember to call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) on the device manager.</span></span>

<span data-ttu-id="edad7-479">Si crea un dispositivo o llama a **IDirect3DDevice9::Reset** o **IDirect3DDevice9Ex::ResetEx** en un dispositivo existente, envíe un evento [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) a la EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-479">If you create a new device, or if you call **IDirect3DDevice9::Reset** or **IDirect3DDevice9Ex::ResetEx** on an existing device, send an [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) event to the EVR.</span></span> <span data-ttu-id="edad7-480">Este evento notifica al EVR que renegocie el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="edad7-480">This event notifies the EVR to renegotiate the media type.</span></span> <span data-ttu-id="edad7-481">EvR omite los parámetros de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="edad7-481">The EVR ignores the event parameters for this event.</span></span>

### <a name="allocating-direct3d-surfaces"></a><span data-ttu-id="edad7-482">Asignación de superficies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="edad7-482">Allocating Direct3D Surfaces</span></span>

<span data-ttu-id="edad7-483">Después de que el presentador establece el tipo de medio, puede asignar las superficies de Direct3D que usará el mezclador para escribir los fotogramas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="edad7-483">After the presenter sets the media type, it can allocate the Direct3D surfaces, which the mixer will use to write the video frames.</span></span> <span data-ttu-id="edad7-484">La superficie debe coincidir con el tipo de medio del presentador:</span><span class="sxs-lookup"><span data-stu-id="edad7-484">The surface must match the presenter's media type:</span></span>

-   <span data-ttu-id="edad7-485">El formato de superficie debe coincidir con el subtipo multimedia.</span><span class="sxs-lookup"><span data-stu-id="edad7-485">The surface format must match the media subtype.</span></span> <span data-ttu-id="edad7-486">Por ejemplo, si el subtipo **es MFVideoFormat_RGB24**, el formato de superficie debe **ser D3DFMT_X8R8G8B8**.</span><span class="sxs-lookup"><span data-stu-id="edad7-486">For example, if the subtype is **MFVideoFormat_RGB24**, the surface format must be **D3DFMT_X8R8G8B8**.</span></span> <span data-ttu-id="edad7-487">Para obtener más información sobre los subtipos y los formatos de Direct3D, vea [GUID de subtipo de vídeo.](video-subtype-guids.md)</span><span class="sxs-lookup"><span data-stu-id="edad7-487">For more information about subtypes and Direct3D formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="edad7-488">El ancho y el alto de la superficie deben coincidir con las dimensiones dadas en [**el MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) atributo del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="edad7-488">The surface width and height must match the dimensions given in the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute of the media type.</span></span>

<span data-ttu-id="edad7-489">La manera recomendada de asignar superficies depende de si el presentador se ejecuta en ventanas o en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="edad7-489">The recommended way to allocate surfaces depends on whether the presenter runs windowed or full-screen.</span></span>

<span data-ttu-id="edad7-490">Si el dispositivo Direct3D está en ventanas, puede crear varias cadenas de intercambio, cada una con un único búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="edad7-490">If the Direct3D device is windowed, you can create several swap chains, each with a single back buffer.</span></span> <span data-ttu-id="edad7-491">Con este enfoque, puede presentar cada superficie de forma independiente, ya que presentar una cadena de intercambio no interferirá con las otras cadenas de intercambio.</span><span class="sxs-lookup"><span data-stu-id="edad7-491">Using this approach, you can present each surface independently, because presenting one swap chain will not interfere with the other swap chains.</span></span> <span data-ttu-id="edad7-492">El mezclador puede escribir datos en una superficie mientras se programa otra superficie para su presentación.</span><span class="sxs-lookup"><span data-stu-id="edad7-492">The mixer can write data to a surface while another surface is scheduled for presentation.</span></span>

<span data-ttu-id="edad7-493">En primer lugar, decida cuántas cadenas de intercambio crear.</span><span class="sxs-lookup"><span data-stu-id="edad7-493">First, decide how many swap chains to create.</span></span> <span data-ttu-id="edad7-494">Se recomienda un mínimo de tres.</span><span class="sxs-lookup"><span data-stu-id="edad7-494">A minimum of three is recommended.</span></span> <span data-ttu-id="edad7-495">Para cada cadena de intercambio, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="edad7-495">For each swap chain, do the following:</span></span>

1.  <span data-ttu-id="edad7-496">Llame **a IDirect3DDevice9::CreateAdditionalSwapChain** para crear la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="edad7-496">Call **IDirect3DDevice9::CreateAdditionalSwapChain** to create the swap chain.</span></span>
2.  <span data-ttu-id="edad7-497">Llame **a IDirect3DSwapChain9::GetBackBuffer** para obtener un puntero a la superficie del búfer de reserva de la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="edad7-497">Call **IDirect3DSwapChain9::GetBackBuffer** to get a pointer to the swap chain's back buffer surface.</span></span>
3.  <span data-ttu-id="edad7-498">Llame [**a MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) y pase un puntero a la superficie.</span><span class="sxs-lookup"><span data-stu-id="edad7-498">Call [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) and pass in a pointer to the surface.</span></span> <span data-ttu-id="edad7-499">Esta función devuelve un puntero a un objeto de ejemplo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="edad7-499">This function returns a pointer to a video sample object.</span></span> <span data-ttu-id="edad7-500">El objeto de ejemplo de vídeo implementa la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) y el presentador usa esta interfaz para entregar la superficie al mezclador cuando el presentador llama al método [**DELETRANSFORM::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-500">The video sample object implements the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, and the presenter uses this interface to deliver the surface to the mixer when the presenter calls the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="edad7-501">Para obtener más información sobre el objeto de ejemplo de vídeo, vea [Ejemplos de vídeo.](video-samples.md)</span><span class="sxs-lookup"><span data-stu-id="edad7-501">For more information about the video sample object, see [Video Samples](video-samples.md).</span></span>
4.  <span data-ttu-id="edad7-502">Almacene el [**puntero DESEJEMPLO**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) En una cola.</span><span class="sxs-lookup"><span data-stu-id="edad7-502">Store the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer in a queue.</span></span> <span data-ttu-id="edad7-503">El presentador extraerá ejemplos de esta cola durante el procesamiento, tal y como se describe en [Procesamiento de salida.](#processing-output)</span><span class="sxs-lookup"><span data-stu-id="edad7-503">The presenter will pull samples from this queue during processing as described in [Processing Output](#processing-output).</span></span>
5.  <span data-ttu-id="edad7-504">Mantenga una referencia al puntero **IDirect3DSwapChain9** para que no se libera la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="edad7-504">Keep a reference to the **IDirect3DSwapChain9** pointer so the swap chain is not released.</span></span>

<span data-ttu-id="edad7-505">En el modo exclusivo de pantalla completa, el dispositivo no puede tener más de una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="edad7-505">In full-screen exclusive mode, the device cannot have more than one swap chain.</span></span> <span data-ttu-id="edad7-506">Esta cadena de intercambio se crea implícitamente al crear el dispositivo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="edad7-506">This swap chain is created implicitly when you create the full-screen device.</span></span> <span data-ttu-id="edad7-507">La cadena de intercambio puede tener más de un búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="edad7-507">The swap chain can have more than one back buffer.</span></span> <span data-ttu-id="edad7-508">Sin embargo, si presenta un búfer de reserva mientras escribe en otro búfer de reserva en la misma cadena de intercambio, no hay ninguna manera fácil de coordinar las dos operaciones.</span><span class="sxs-lookup"><span data-stu-id="edad7-508">Unfortunately, however, if you present one back buffer while you write to another back buffer in the same swap chain, there is no easy way to coordinate the two operations.</span></span> <span data-ttu-id="edad7-509">Esto se debe a la manera en que Direct3D implementa el volteo de superficie.</span><span class="sxs-lookup"><span data-stu-id="edad7-509">This is because of the way Direct3D implements surface flipping.</span></span> <span data-ttu-id="edad7-510">Cuando se llama a Present, el controlador de gráficos actualiza los punteros de superficie en la memoria de gráficos.</span><span class="sxs-lookup"><span data-stu-id="edad7-510">When you call Present, the graphics driver updates the surface pointers in graphics memory.</span></span> <span data-ttu-id="edad7-511">Si mantiene punteros **IDirect3DSurface9** al llamar a **Present**, apuntarán a distintos búferes después de que se devuelva **la** llamada Present.</span><span class="sxs-lookup"><span data-stu-id="edad7-511">If you are holding any **IDirect3DSurface9** pointers when you call **Present**, they will point to different buffers after the **Present** call returns.</span></span>

<span data-ttu-id="edad7-512">La opción más sencilla es crear un ejemplo de vídeo para la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="edad7-512">The simplest option is to create one video sample for the swap chain.</span></span> <span data-ttu-id="edad7-513">Si elige esta opción, siga los mismos pasos dados para el modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="edad7-513">If you choose this option, follow the same steps given for windowed mode.</span></span> <span data-ttu-id="edad7-514">La única diferencia es que la cola de ejemplo contiene un único ejemplo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="edad7-514">The only difference is that the sample queue contains a single video sample.</span></span> <span data-ttu-id="edad7-515">Otra opción es crear superficies fuera de la pantalla y, a continuación, cortarlas en el búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="edad7-515">Another option is to create offscreen surfaces and then blit them to the back buffer.</span></span> <span data-ttu-id="edad7-516">Las superficies que cree deben admitir el método [**IDirectXVideoProcessor::VideoProcessBlt,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) que el mezclador usa para componer los fotogramas de salida.</span><span class="sxs-lookup"><span data-stu-id="edad7-516">The surfaces that you create must support the [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method, which the mixer uses to composite the output frames.</span></span>

### <a name="tracking-samples"></a><span data-ttu-id="edad7-517">Ejemplos de seguimiento</span><span class="sxs-lookup"><span data-stu-id="edad7-517">Tracking Samples</span></span>

<span data-ttu-id="edad7-518">Cuando el presentador asigna por primera vez los ejemplos de vídeo, los coloca en una cola.</span><span class="sxs-lookup"><span data-stu-id="edad7-518">When the presenter first allocates the video samples, it places them in a queue.</span></span> <span data-ttu-id="edad7-519">El presentador dibuja de esta cola cada vez que necesita obtener un nuevo fotograma del mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-519">The presenter draws from this queue whenever it needs to get a new frame from the mixer.</span></span> <span data-ttu-id="edad7-520">Una vez que el mezclador genera el fotograma, el presentador mueve el ejemplo a una segunda cola.</span><span class="sxs-lookup"><span data-stu-id="edad7-520">After the mixer outputs the frame, the presenter moves the sample into a second queue.</span></span> <span data-ttu-id="edad7-521">La segunda cola es para los ejemplos que están esperando sus tiempos de presentación programados.</span><span class="sxs-lookup"><span data-stu-id="edad7-521">The second queue is for samples that are waiting for their scheduled presentation times.</span></span>

<span data-ttu-id="edad7-522">Para facilitar el seguimiento del estado de cada ejemplo, el objeto de ejemplo de vídeo implementa la [**interfaz IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="edad7-522">To make it easier to track the status of each sample, the video sample object implements the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span> <span data-ttu-id="edad7-523">Puede usar esta interfaz de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="edad7-523">You can use this interface as follows:</span></span>

1.  <span data-ttu-id="edad7-524">Implemente [**la interfaz IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) en el presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-524">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface in your presenter.</span></span>
2.  <span data-ttu-id="edad7-525">Antes de colocar un ejemplo en la cola programada, consulte el objeto de ejemplo de vídeo para la [**interfaz IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="edad7-525">Before you place a sample in the scheduled queue, query the video sample object for the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span>

3.  <span data-ttu-id="edad7-526">Llame [**a IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) con un puntero a la interfaz de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="edad7-526">Call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) with a pointer to your callback interface.</span></span>
4.  <span data-ttu-id="edad7-527">Cuando el ejemplo esté listo para su presentación, quítelo de la cola programada, presentarlo y liberar todas las referencias al ejemplo.</span><span class="sxs-lookup"><span data-stu-id="edad7-527">When the sample is ready for presentation, remove it from the scheduled queue, present it, and release all references to the sample.</span></span>
5.  <span data-ttu-id="edad7-528">El ejemplo invoca la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="edad7-528">The sample invokes the callback.</span></span> <span data-ttu-id="edad7-529">(El objeto de ejemplo no se elimina en este caso porque contiene un recuento de referencias en sí mismo hasta que se invoca la devolución de llamada).</span><span class="sxs-lookup"><span data-stu-id="edad7-529">(The sample object is not deleted in this case because it holds a reference count on itself until the callback is invoked.)</span></span>
6.  <span data-ttu-id="edad7-530">Dentro de la devolución de llamada, devuelva el ejemplo a la cola disponible.</span><span class="sxs-lookup"><span data-stu-id="edad7-530">Inside the callback, return the sample to the available queue.</span></span>

<span data-ttu-id="edad7-531">No es necesario que un presentador use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) para realizar un seguimiento de los ejemplos. puede implementar cualquier técnica que funcione mejor para su diseño.</span><span class="sxs-lookup"><span data-stu-id="edad7-531">A presenter is not required to use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) to track samples; you can implement any technique that works best for your design.</span></span> <span data-ttu-id="edad7-532">Una ventaja de **IMFTrackedSample** es que puede mover las funciones de programación y representación del presentador a objetos auxiliares, y estos objetos no necesitan ningún mecanismo especial para volver a llamar al presentador cuando liberan ejemplos de vídeo porque el objeto de ejemplo proporciona ese mecanismo.</span><span class="sxs-lookup"><span data-stu-id="edad7-532">One advantage of **IMFTrackedSample** is that you can move the presenter's scheduling and rendering functions into helper objects, and these objects do not need any special mechanism for calling back to the presenter when they release video samples because the sample object provides that mechanism.</span></span>

<span data-ttu-id="edad7-533">El código siguiente muestra cómo establecer la devolución de llamada:</span><span class="sxs-lookup"><span data-stu-id="edad7-533">The following code shows how to set the callback:</span></span>


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



<span data-ttu-id="edad7-534">En la devolución de llamada, llame a [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) en el objeto de resultado asincrónico para recuperar un puntero al ejemplo:</span><span class="sxs-lookup"><span data-stu-id="edad7-534">In the callback, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) on the asynchronous result object to retrieve a pointer to the sample:</span></span>


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock ***/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /*** End lock ***/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a><span data-ttu-id="edad7-535">Salida de procesamiento</span><span class="sxs-lookup"><span data-stu-id="edad7-535">Processing Output</span></span>

<span data-ttu-id="edad7-536">Cada vez que el mezclador recibe un nuevo ejemplo de entrada, el EVR envía **un MFVP_MESSAGE_PROCESSINPUTNOTIFY** mensaje al presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-536">Whenever the mixer receives a new input sample, the EVR sends an **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message to the presenter.</span></span> <span data-ttu-id="edad7-537">Este mensaje indica que el mezclador podría tener un nuevo fotograma de vídeo para entregar.</span><span class="sxs-lookup"><span data-stu-id="edad7-537">This message indicates that the mixer might have a new video frame to deliver.</span></span> <span data-ttu-id="edad7-538">En respuesta, el presentador llama [**a IMFTransform::P rocessOutput en**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) el mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-538">In response, the presenter calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="edad7-539">Si el método se realiza correctamente, el presentador programa el ejemplo para su presentación.</span><span class="sxs-lookup"><span data-stu-id="edad7-539">If the method succeeds, the presenter schedules the sample for presentation.</span></span>

<span data-ttu-id="edad7-540">Para obtener la salida del mezclador, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="edad7-540">To get output from the mixer, perform the following steps:</span></span>

1.  <span data-ttu-id="edad7-541">Compruebe el estado del reloj.</span><span class="sxs-lookup"><span data-stu-id="edad7-541">Check the clock state.</span></span> <span data-ttu-id="edad7-542">Si el reloj está en pausa, ignore el **mensaje MFVP_MESSAGE_PROCESSINPUTNOTIFY** a menos que este sea el primer fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="edad7-542">If the clock is paused, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message unless this is the first video frame.</span></span> <span data-ttu-id="edad7-543">Si el reloj se está ejecutando o si este es el primer fotograma de vídeo, continúe.</span><span class="sxs-lookup"><span data-stu-id="edad7-543">If the clock is running, or if this is the first video frame, continue.</span></span>
2.  <span data-ttu-id="edad7-544">Obtenga un ejemplo de la cola de ejemplos disponibles.</span><span class="sxs-lookup"><span data-stu-id="edad7-544">Get a sample from the queue of available samples.</span></span> <span data-ttu-id="edad7-545">Si la cola está vacía, significa que todas las muestras asignadas están actualmente programadas para presentarse.</span><span class="sxs-lookup"><span data-stu-id="edad7-545">If the queue is empty, it means that all allocated samples are currently scheduled for presenting.</span></span> <span data-ttu-id="edad7-546">En ese caso, ignore el **mensaje MFVP_MESSAGE_PROCESSINPUTNOTIFY** en este momento.</span><span class="sxs-lookup"><span data-stu-id="edad7-546">In that case, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message at this time.</span></span> <span data-ttu-id="edad7-547">Cuando el ejemplo siguiente esté disponible, repita los pasos enumerados aquí.</span><span class="sxs-lookup"><span data-stu-id="edad7-547">When the next sample becomes available, repeat the steps listed here.</span></span>
3.  <span data-ttu-id="edad7-548">(Opcional). Si el reloj está disponible, obtenga la hora del reloj actual (*T1*) llamando a [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="edad7-548">(Optional.) If the clock is available, get the current clock time (*T1*) by calling [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span>
4.  <span data-ttu-id="edad7-549">Llame [**a IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-549">Call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="edad7-550">Si **ProcessOutput se** realiza correctamente, el ejemplo contiene un fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="edad7-550">If **ProcessOutput** succeeds, the sample contains a video frame.</span></span> <span data-ttu-id="edad7-551">Si se produce un error en el método, compruebe el código de retorno.</span><span class="sxs-lookup"><span data-stu-id="edad7-551">If the method fails, check the return code.</span></span> <span data-ttu-id="edad7-552">Los siguientes códigos de error de **ProcessOutput** no son errores críticos:</span><span class="sxs-lookup"><span data-stu-id="edad7-552">The following error codes from **ProcessOutput** are not critical failures:</span></span>

    

    | <span data-ttu-id="edad7-553">Código de error</span><span class="sxs-lookup"><span data-stu-id="edad7-553">Error code</span></span>                              | <span data-ttu-id="edad7-554">Descripción</span><span class="sxs-lookup"><span data-stu-id="edad7-554">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="edad7-555">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span><span class="sxs-lookup"><span data-stu-id="edad7-555">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span></span> | <span data-ttu-id="edad7-556">El mezclador necesita más entrada para poder generar un nuevo marco de salida.</span><span class="sxs-lookup"><span data-stu-id="edad7-556">The mixer needs more input before it can produce a new output frame.</span></span><br/> <span data-ttu-id="edad7-557">Si obtiene este código de error, compruebe si el EVR ha llegado al final de la secuencia y responda en consecuencia, como se describe en [Final de la secuencia](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="edad7-557">If you get this error code, check whether the EVR has reached the end of the stream and respond accordingly, as described in [End of Stream](#end-of-stream).</span></span> <span data-ttu-id="edad7-558">De lo contrario, ignore **este MF_E_TRANSFORM_NEED_MORE_INPUT** mensaje.</span><span class="sxs-lookup"><span data-stu-id="edad7-558">Otherwise, ignore this **MF_E_TRANSFORM_NEED_MORE_INPUT** message.</span></span> <span data-ttu-id="edad7-559">La EVR enviará otra cuando el mezclador reciba más entradas.</span><span class="sxs-lookup"><span data-stu-id="edad7-559">The EVR will send another one when the mixer gets more input.</span></span><br/> |
    | <span data-ttu-id="edad7-560">**MF_E_TRANSFORM_STREAM_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="edad7-560">**MF_E_TRANSFORM_STREAM_CHANGE**</span></span>    | <span data-ttu-id="edad7-561">El tipo de salida del mezclador ha pasado a ser no válido, posiblemente debido a un cambio de formato ascendente.</span><span class="sxs-lookup"><span data-stu-id="edad7-561">The mixer's output type has become invalid, possibly due to a format change upstream.</span></span><br/> <span data-ttu-id="edad7-562">Si obtiene este código de error, establezca el tipo de medio del presentador en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="edad7-562">If you get this error code, set the presenter's media type to **NULL**.</span></span> <span data-ttu-id="edad7-563">El EVR solicitará un nuevo formato.</span><span class="sxs-lookup"><span data-stu-id="edad7-563">The EVR will request a new format.</span></span><br/>                                                                                                                                                                         |
    | <span data-ttu-id="edad7-564">**MF_E_TRANSFORM_TYPE_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="edad7-564">**MF_E_TRANSFORM_TYPE_NOT_SET**</span></span>    | <span data-ttu-id="edad7-565">El mezclador requiere un nuevo tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="edad7-565">The mixer requires a new media type.</span></span><br/> <span data-ttu-id="edad7-566">Si recibe este código de error, vuelva a negociar el tipo de salida del mezclador como se describe en [Formatos de negociación](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="edad7-566">If you get this error code, renegotiate the mixer's output type as described in [Negotiating Formats](#negotiating-formats).</span></span><br/>                                                                                                                                                                                                        |

    

     

    <span data-ttu-id="edad7-567">Si [**ProcessOutput se**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) realiza correctamente, continúe.</span><span class="sxs-lookup"><span data-stu-id="edad7-567">If [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) succeeds, continue.</span></span>

5.  <span data-ttu-id="edad7-568">(Opcional). Si el reloj está disponible, obtenga la hora del reloj actual *(T2).*</span><span class="sxs-lookup"><span data-stu-id="edad7-568">(Optional.) If the clock is available, get the current clock time (*T2*).</span></span> <span data-ttu-id="edad7-569">La cantidad de latencia introducida por el mezclador es (*T2*  -  *T1*).</span><span class="sxs-lookup"><span data-stu-id="edad7-569">The amount of latency introduced by the mixer is (*T2* - *T1*).</span></span> <span data-ttu-id="edad7-570">Envíe un **EC_PROCESSING_LATENCY** evento con este valor al EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-570">Send an **EC_PROCESSING_LATENCY** event with this value to the EVR.</span></span> <span data-ttu-id="edad7-571">El EVR usa este valor para el control de calidad.</span><span class="sxs-lookup"><span data-stu-id="edad7-571">The EVR uses this value for quality control.</span></span> <span data-ttu-id="edad7-572">Si no hay ningún reloj disponible, no hay ninguna razón para enviar el **EC_PROCESSING_LATENCY** evento.</span><span class="sxs-lookup"><span data-stu-id="edad7-572">If no clock is available, there is no reason to send the **EC_PROCESSING_LATENCY** event.</span></span>
6.  <span data-ttu-id="edad7-573">(Opcional). Consulte el ejemplo [**para IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) y llame a [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) como se describe en [Ejemplos de seguimiento](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="edad7-573">(Optional.) Query the sample for [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) and call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) as described in [Tracking Samples](#tracking-samples).</span></span>
7.  <span data-ttu-id="edad7-574">Programe el ejemplo para su presentación.</span><span class="sxs-lookup"><span data-stu-id="edad7-574">Schedule the sample for presentation.</span></span>

<span data-ttu-id="edad7-575">Esta secuencia de pasos puede finalizar antes de que el presentador reciba cualquier salida del mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-575">This sequence of steps can terminate before the presenter gets any output from the mixer.</span></span> <span data-ttu-id="edad7-576">Para asegurarse de que no se descarta ninguna solicitud, debe repetir los mismos pasos cuando se produzca lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="edad7-576">To ensure that no requests are dropped, you should repeat the same steps when the following occur:</span></span>

-   <span data-ttu-id="edad7-577">Se llama al método [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) o **IMFClockStateSink::OnClockStart** del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-577">The presenter's [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or **IMFClockStateSink::OnClockStart** method is called.</span></span> <span data-ttu-id="edad7-578">Esto controla el caso en el que el mezclador omite la entrada porque el reloj está en pausa (paso 1).</span><span class="sxs-lookup"><span data-stu-id="edad7-578">This handles the case where the mixer ignores input because the clock is paused (step 1).</span></span>
-   <span data-ttu-id="edad7-579">Se invoca la devolución de [**llamada IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="edad7-579">The [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback is invoked.</span></span> <span data-ttu-id="edad7-580">Esto controla el caso en el que el mezclador recibe la entrada, pero todos los ejemplos de vídeo del presentador están en uso (paso 2).</span><span class="sxs-lookup"><span data-stu-id="edad7-580">This handles the case where the mixer receives input but all of the presenter's video samples are in use (step 2).</span></span>

<span data-ttu-id="edad7-581">En los siguientes ejemplos de código se muestran estos pasos con más detalle.</span><span class="sxs-lookup"><span data-stu-id="edad7-581">The next several code examples show these steps in more detail.</span></span> <span data-ttu-id="edad7-582">El presentador llama al `ProcessInputNotify` método (que se muestra en el ejemplo siguiente) cuando obtiene el **MFVP_MESSAGE_PROCESSINPUTNOTIFY** mensaje.</span><span class="sxs-lookup"><span data-stu-id="edad7-582">The presenter calls the `ProcessInputNotify` method (shown in the following example) when it gets the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message.</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



<span data-ttu-id="edad7-583">Este `ProcessInputNotify` método establece una marca booleana para registrar el hecho de que el mezclador tiene nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="edad7-583">This `ProcessInputNotify` method sets a Boolean flag to record the fact that the mixer has new input.</span></span> <span data-ttu-id="edad7-584">A continuación, `ProcessOutputLoop` llama al método , que se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="edad7-584">Then it calls the `ProcessOutputLoop` method, shown in the next example.</span></span> <span data-ttu-id="edad7-585">Este método intenta extraer tantas muestras como sea posible del mezclador:</span><span class="sxs-lookup"><span data-stu-id="edad7-585">This method attempts to pull as many samples as possible from the mixer:</span></span>


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



<span data-ttu-id="edad7-586">El `ProcessOutput` método , que se muestra en el ejemplo siguiente, intenta obtener un único fotograma de vídeo del mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-586">The `ProcessOutput` method, shown in the next example, attempts to get a single video frame from the mixer.</span></span> <span data-ttu-id="edad7-587">Si no hay ningún fotograma de vídeo disponible, devuelve S_FALSE o un código de error, cualquiera de los cuales `ProcessSample` interrumpe el bucle en `ProcessOutputLoop` .</span><span class="sxs-lookup"><span data-stu-id="edad7-587">If no video frame is available, `ProcessSample` returns S_FALSE or an error code, either of which interrupts the loop in `ProcessOutputLoop`.</span></span> <span data-ttu-id="edad7-588">La mayor parte del trabajo se realiza dentro del `ProcessOutput` método :</span><span class="sxs-lookup"><span data-stu-id="edad7-588">Most of the work is done inside the `ProcessOutput` method:</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



<span data-ttu-id="edad7-589">Algunos comentarios sobre este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="edad7-589">Some remarks about this example:</span></span>

-   <span data-ttu-id="edad7-590">La *m_SamplePool* variable se supone que es un objeto de colección que contiene la cola de ejemplos de vídeo disponibles.</span><span class="sxs-lookup"><span data-stu-id="edad7-590">The *m_SamplePool* variable is assumed to be a collection object that holds the queue of available video samples.</span></span> <span data-ttu-id="edad7-591">El método del objeto `GetSample` devuelve **MF_E_SAMPLEALLOCATOR_EMPTY** si la cola está vacía.</span><span class="sxs-lookup"><span data-stu-id="edad7-591">The object's `GetSample` method returns **MF_E_SAMPLEALLOCATOR_EMPTY** if the queue is empty.</span></span>
-   <span data-ttu-id="edad7-592">Si el método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mezclador devuelve MF_E_TRANSFORM_NEED_MORE_INPUT, significa que el mezclador no puede generar más resultados, por lo que el presentador *borra m_fSampleNotify* marca.</span><span class="sxs-lookup"><span data-stu-id="edad7-592">If the mixer's [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns MF_E_TRANSFORM_NEED_MORE_INPUT, it means the mixer cannot produce any more output, so the presenter clears the *m_fSampleNotify* flag.</span></span>
-   <span data-ttu-id="edad7-593">El `TrackSample` método , que establece la devolución de llamada [**IMFTrackedSample,**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) se muestra en la sección [Ejemplos de seguimiento](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="edad7-593">The `TrackSample` method, which sets the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback, is shown in the section [Tracking Samples](#tracking-samples).</span></span>

### <a name="repainting-frames"></a><span data-ttu-id="edad7-594">Volver a dibujar fotogramas</span><span class="sxs-lookup"><span data-stu-id="edad7-594">Repainting Frames</span></span>

<span data-ttu-id="edad7-595">En ocasiones, es posible que el presentador tenga que volver a dibujar el fotograma de vídeo más reciente.</span><span class="sxs-lookup"><span data-stu-id="edad7-595">Occasionally the presenter might need to repaint the most recent video frame.</span></span> <span data-ttu-id="edad7-596">Por ejemplo, el presentador estándar vuelve a dibujar el marco en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="edad7-596">For example, the standard presenter repaints the frame in the following situations:</span></span>

-   <span data-ttu-id="edad7-597">En modo de ventana, en respuesta a **WM_PAINT** mensajes recibidos por la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edad7-597">In windowed mode, in response to **WM_PAINT** messages received by the application's window.</span></span> <span data-ttu-id="edad7-598">Vea [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="edad7-598">See [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>
-   <span data-ttu-id="edad7-599">Si el rectángulo de destino cambia cuando la aplicación llama [**a IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="edad7-599">If the destination rectangle changes when the application calls [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="edad7-600">Siga estos pasos para solicitar al mezclador que vuelva a crear el fotograma más reciente:</span><span class="sxs-lookup"><span data-stu-id="edad7-600">Use the following steps to request the mixer to re-create the most recent frame:</span></span>

1.  <span data-ttu-id="edad7-601">Obtenga un ejemplo de vídeo de la cola.</span><span class="sxs-lookup"><span data-stu-id="edad7-601">Get a video sample from the queue.</span></span>
2.  <span data-ttu-id="edad7-602">Consulte el ejemplo para la [**interfaz IMFDesiredSample.**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)</span><span class="sxs-lookup"><span data-stu-id="edad7-602">Query the sample for the [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) interface.</span></span>
3.  <span data-ttu-id="edad7-603">Llame [**a IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span><span class="sxs-lookup"><span data-stu-id="edad7-603">Call [**IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span></span> <span data-ttu-id="edad7-604">Especifique la marca de tiempo del fotograma de vídeo más reciente.</span><span class="sxs-lookup"><span data-stu-id="edad7-604">Specify the time stamp of the most recent video frame.</span></span> <span data-ttu-id="edad7-605">(Tendrá que almacenar en caché este valor y actualizarlo para cada fotograma).</span><span class="sxs-lookup"><span data-stu-id="edad7-605">(You will need to cache this value and update it for each frame.)</span></span>
4.  <span data-ttu-id="edad7-606">Llame [**a ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-606">Call [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span>

<span data-ttu-id="edad7-607">Al volver a dibujar un marco, puede omitir el reloj de presentación y presentarlo inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="edad7-607">When repainting a frame, you can ignore the presentation clock and present the frame immediately.</span></span>

### <a name="scheduling-samples"></a><span data-ttu-id="edad7-608">Ejemplos de programación</span><span class="sxs-lookup"><span data-stu-id="edad7-608">Scheduling Samples</span></span>

<span data-ttu-id="edad7-609">Los fotogramas de vídeo pueden llegar a la EVR en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="edad7-609">Video frames can reach the EVR at any time.</span></span> <span data-ttu-id="edad7-610">El presentador es responsable de presentar cada fotograma en el momento correcto, en función de la marca de tiempo del fotograma.</span><span class="sxs-lookup"><span data-stu-id="edad7-610">The presenter is responsible for presenting each frame at the correct time, based on the time stamp of the frame.</span></span> <span data-ttu-id="edad7-611">Cuando el presentador obtiene un nuevo ejemplo del mezclador, coloca el ejemplo en la cola programada.</span><span class="sxs-lookup"><span data-stu-id="edad7-611">When the presenter gets a new sample from the mixer, it puts the sample on the scheduled queue.</span></span> <span data-ttu-id="edad7-612">En un subproceso independiente, el presentador obtiene continuamente el primer ejemplo del principio de la cola y determina si:</span><span class="sxs-lookup"><span data-stu-id="edad7-612">On a separate thread, the presenter continually gets the first sample from the head of the queue and determines whether to:</span></span>

-   <span data-ttu-id="edad7-613">Presente el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="edad7-613">Present the sample.</span></span>
-   <span data-ttu-id="edad7-614">Mantenga el ejemplo en la cola porque es temprano.</span><span class="sxs-lookup"><span data-stu-id="edad7-614">Keep the sample on the queue because it is early.</span></span>
-   <span data-ttu-id="edad7-615">Descarte el ejemplo porque es tarde.</span><span class="sxs-lookup"><span data-stu-id="edad7-615">Discard the sample because it is late.</span></span> <span data-ttu-id="edad7-616">Aunque debe evitar quitar fotogramas si es posible, es posible que deba hacerlo si el presentador se está quedando atrás continuamente.</span><span class="sxs-lookup"><span data-stu-id="edad7-616">Although you should avoid dropping frames if possible, you might need to if the presenter is continually falling behind.</span></span>

<span data-ttu-id="edad7-617">Para obtener la marca de tiempo de un fotograma de vídeo, llame a [**IMFSample::GetSampleTime en**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) el ejemplo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="edad7-617">To get the time stamp for a video frame, call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) on the video sample.</span></span> <span data-ttu-id="edad7-618">La marca de tiempo es relativa al reloj de presentación del EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-618">The time stamp is relative to the EVR's presentation clock.</span></span> <span data-ttu-id="edad7-619">Para obtener la hora del reloj actual, llame [**a IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="edad7-619">To get the current clock time, call [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span> <span data-ttu-id="edad7-620">Si la EVR no tiene un reloj de presentación o si una muestra no tiene una marca de tiempo, puede presentar la muestra inmediatamente después de obtenerla.</span><span class="sxs-lookup"><span data-stu-id="edad7-620">If the EVR does not have a presentation clock, or if a sample does not have a time stamp, you can present the sample immediately after you get it.</span></span>

<span data-ttu-id="edad7-621">Para obtener la duración de cada ejemplo, llame [**a IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span><span class="sxs-lookup"><span data-stu-id="edad7-621">To get the duration of each sample, call [**IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span></span> <span data-ttu-id="edad7-622">Si el ejemplo no tiene una duración, puede usar la función [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) para calcular la duración a partir de la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="edad7-622">If the sample does not have a duration, you can use the [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) function to calculate the duration from the frame rate.</span></span>

<span data-ttu-id="edad7-623">Al programar ejemplos, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="edad7-623">When you schedule samples, keep in mind the following:</span></span>

-   <span data-ttu-id="edad7-624">Si la velocidad de reproducción es más rápida o más lenta que la velocidad normal, el reloj se ejecuta a una velocidad más rápida o más lenta.</span><span class="sxs-lookup"><span data-stu-id="edad7-624">If the playback rate is faster or slower than normal speed, the clock runs at a faster or slower rate.</span></span> <span data-ttu-id="edad7-625">Esto significa que la marca de tiempo de un ejemplo siempre proporciona la hora de destino correcta en relación con el reloj de presentación.</span><span class="sxs-lookup"><span data-stu-id="edad7-625">That means the time stamp on a sample always gives the correct target time relative to the presentation clock.</span></span> <span data-ttu-id="edad7-626">Sin embargo, si traduce los tiempos de presentación a otra hora de reloj (por ejemplo, el contador de rendimiento de alta resolución), debe escalar las horas en función de la velocidad del reloj.</span><span class="sxs-lookup"><span data-stu-id="edad7-626">However, if you translate presentation times into some other clock time (for example, the high-resolution performace counter), then you must scale the times based on the clock speed.</span></span> <span data-ttu-id="edad7-627">Si cambia la velocidad del reloj, la EVR llama al método [**IMFClockStateSink::OnClockSetRate del**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-627">If the clock speed changes, the EVR calls the presenter's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>
-   <span data-ttu-id="edad7-628">La velocidad de reproducción puede ser negativa para la reproducción inversa.</span><span class="sxs-lookup"><span data-stu-id="edad7-628">The playback rate can be negative for reverse playback.</span></span> <span data-ttu-id="edad7-629">Cuando la velocidad de reproducción es negativa, el reloj de presentación se ejecuta hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="edad7-629">When the playback rate is negative, the presentation clock runs backward.</span></span> <span data-ttu-id="edad7-630">En otras palabras, la *hora N* + 1 se produce antes de la *hora N*.</span><span class="sxs-lookup"><span data-stu-id="edad7-630">In other words, time *N* + 1 occurs before time *N*.</span></span>

<span data-ttu-id="edad7-631">En el ejemplo siguiente se calcula lo pronto o tarde que es una muestra, en relación con el reloj de presentación:</span><span class="sxs-lookup"><span data-stu-id="edad7-631">The following example calculates how early or late a sample is, relative to the presentation clock:</span></span>


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



<span data-ttu-id="edad7-632">El reloj de presentación suele estar controlado por el reloj del sistema o el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="edad7-632">The presentation clock is usually driven by the system clock or the audio renderer.</span></span> <span data-ttu-id="edad7-633">(El representador de audio deriva el tiempo de la velocidad a la que la tarjeta de sonido consume audio). En general, el reloj de presentación no se sincroniza con la frecuencia de actualización del monitor.</span><span class="sxs-lookup"><span data-stu-id="edad7-633">(The audio renderer derives the time from the rate at which the sound card consumes audio.) In general, the presentation clock is not synchronized with the refresh rate of the monitor.</span></span>

<span data-ttu-id="edad7-634">Si los parámetros de  presentación de Direct3D especifican D3DPRESENT_INTERVAL_DEFAULT o **D3DPRESENT_INTERVAL_ONE** para el intervalo de presentación, la operación Present espera el seguimiento vertical del monitor. </span><span class="sxs-lookup"><span data-stu-id="edad7-634">If your Direct3D presentation parameters specify **D3DPRESENT_INTERVAL_DEFAULT** or **D3DPRESENT_INTERVAL_ONE** for the presentation interval, the **Present** operation waits for the monitor's vertical retrace.</span></span> <span data-ttu-id="edad7-635">Se trata de una manera fácil de evitar el desgarro, pero reduce la precisión del algoritmo de programación.</span><span class="sxs-lookup"><span data-stu-id="edad7-635">This is an easy way to prevent tearing, but reduces the accuracy of your scheduling algorithm.</span></span> <span data-ttu-id="edad7-636">Por el contrario, si el intervalo de presentación **es D3DPRESENT_INTERVAL_IMMEDIATE**, el método **Present** se ejecuta inmediatamente, lo que provoca el desgarro a menos que el algoritmo de programación sea lo suficientemente preciso como para llamar a **Present** solo durante el período de retroceso vertical.</span><span class="sxs-lookup"><span data-stu-id="edad7-636">Conversely, if the presentation interval is **D3DPRESENT_INTERVAL_IMMEDIATE**, the **Present** method executes immediately, which causes tearing unless your scheduling algorithm is accurate enough that you call **Present** only during the vertical retrace period.</span></span>

<span data-ttu-id="edad7-637">Las siguientes funciones pueden ayudarle a obtener información de control de tiempo precisa:</span><span class="sxs-lookup"><span data-stu-id="edad7-637">The following functions can help you get accurate timing information:</span></span>

-   <span data-ttu-id="edad7-638">**IDirect3DDevice9::GetRasterStatus** devuelve información sobre el trama, incluida la línea de examen actual y si el trama está en el período en blanco vertical.</span><span class="sxs-lookup"><span data-stu-id="edad7-638">**IDirect3DDevice9::GetRasterStatus** returns information about the raster, including the current scan line and whether the raster is in the vertical blank period.</span></span>
-   <span data-ttu-id="edad7-639">**DwmGetCompositionTimingInfo** devuelve información de control de tiempo para el administrador de ventanas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="edad7-639">**DwmGetCompositionTimingInfo** returns timing information for the desktop window manager.</span></span> <span data-ttu-id="edad7-640">Esta información es útil si está habilitada la composición de escritorio.</span><span class="sxs-lookup"><span data-stu-id="edad7-640">This information is useful if desktop composition is enabled.</span></span>

### <a name="presenting-samples"></a><span data-ttu-id="edad7-641">Presentación de ejemplos</span><span class="sxs-lookup"><span data-stu-id="edad7-641">Presenting Samples</span></span>

<span data-ttu-id="edad7-642">En esta sección se supone que ha creado una cadena de intercambio independiente para cada superficie, como se describe en [Asignación de superficies de Direct3D.](#allocating-direct3d-surfaces)</span><span class="sxs-lookup"><span data-stu-id="edad7-642">This section assumes that you created a separate swap chain for each surface as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="edad7-643">Para presentar un ejemplo, obtenga la cadena de intercambio del ejemplo de vídeo como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="edad7-643">To present a sample, get the swap chain from the video sample as follows:</span></span>

1.  <span data-ttu-id="edad7-644">Llame [**a IMFSample::GetBufferByIndex en**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) el ejemplo de vídeo para obtener el búfer.</span><span class="sxs-lookup"><span data-stu-id="edad7-644">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) on the video sample to get the buffer.</span></span>
2.  <span data-ttu-id="edad7-645">Consulte el búfer para la [**interfaz DESGETService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)</span><span class="sxs-lookup"><span data-stu-id="edad7-645">Query the buffer for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
3.  <span data-ttu-id="edad7-646">Llame [**a IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener la **interfaz IDirect3DSurface9** de la superficie de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="edad7-646">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the **IDirect3DSurface9** interface of the Direct3D surface.</span></span> <span data-ttu-id="edad7-647">(Puede combinar este paso y el paso anterior en uno llamando a [**MFGetService).**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)</span><span class="sxs-lookup"><span data-stu-id="edad7-647">(You can combine this step and the previous step into one by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span></span>
4.  <span data-ttu-id="edad7-648">Llame **a IDirect3DSurface9::GetContainer** en la superficie para obtener un puntero a la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="edad7-648">Call **IDirect3DSurface9::GetContainer** on the surface to get a pointer to the swap chain.</span></span>
5.  <span data-ttu-id="edad7-649">Llame **a IDirect3DSwapChain9::P resent** en la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="edad7-649">Call **IDirect3DSwapChain9::Present** on the swap chain.</span></span>

<span data-ttu-id="edad7-650">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="edad7-650">The following code shows these steps:</span></span>


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a><span data-ttu-id="edad7-651">Rectángulos de origen y destino</span><span class="sxs-lookup"><span data-stu-id="edad7-651">Source and Destination Rectangles</span></span>

<span data-ttu-id="edad7-652">El *rectángulo de origen* es la parte del fotograma de vídeo que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="edad7-652">The *source rectangle* is the portion of the video frame to display.</span></span> <span data-ttu-id="edad7-653">Se define en relación con un sistema de coordenadas normalizado, en el que todo el fotograma de vídeo ocupa un rectángulo con coordenadas {0, 0, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="edad7-653">It is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="edad7-654">El *rectángulo de destino* es el área dentro de la superficie de destino donde se dibuja el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="edad7-654">The *destination rectangle* is the area within the destination surface where the video frame is drawn.</span></span> <span data-ttu-id="edad7-655">El presentador estándar permite a una aplicación establecer estos rectángulos mediante una llamada [**a IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="edad7-655">The standard presenter enables an application to set these rectangles by calling [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="edad7-656">Hay varias opciones para aplicar rectángulos de origen y destino.</span><span class="sxs-lookup"><span data-stu-id="edad7-656">There are several options for applying source and destination rectangles.</span></span> <span data-ttu-id="edad7-657">La primera opción es permitir que el mezclador las aplique:</span><span class="sxs-lookup"><span data-stu-id="edad7-657">The first option is to let the mixer apply them:</span></span>

-   <span data-ttu-id="edad7-658">Establezca el rectángulo de origen mediante el [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) origen.</span><span class="sxs-lookup"><span data-stu-id="edad7-658">Set the source rectangle using the [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) attribute.</span></span> <span data-ttu-id="edad7-659">El mezclador aplicará el rectángulo de origen cuando se corta el vídeo a la superficie de destino.</span><span class="sxs-lookup"><span data-stu-id="edad7-659">The mixer will apply the source rectangle when it blits the video to the destination surface.</span></span> <span data-ttu-id="edad7-660">El rectángulo de origen predeterminado del mezclador es todo el marco.</span><span class="sxs-lookup"><span data-stu-id="edad7-660">The mixer's default source rectangle is the entire frame.</span></span>
-   <span data-ttu-id="edad7-661">Establezca el rectángulo de destino como la apertura geométrica en el tipo de salida del mezclador.</span><span class="sxs-lookup"><span data-stu-id="edad7-661">Set the destination rectangle as the geometric aperture in the mixer's output type.</span></span> <span data-ttu-id="edad7-662">Para obtener más información, vea [Formatos de negociación](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="edad7-662">For more information, see [Negotiating Formats](#negotiating-formats).</span></span>

<span data-ttu-id="edad7-663">La segunda opción consiste en aplicar los rectángulos cuando se **IDirect3DSwapChain9::P resent** especificando los parámetros *pSourceRect* y *pDestRect* en el **método Present.**</span><span class="sxs-lookup"><span data-stu-id="edad7-663">The second option is to apply the rectangles when you **IDirect3DSwapChain9::Present** by specifying the *pSourceRect* and *pDestRect* parameters in the **Present** method.</span></span> <span data-ttu-id="edad7-664">Puede combinar estas opciones.</span><span class="sxs-lookup"><span data-stu-id="edad7-664">You can combine these options.</span></span> <span data-ttu-id="edad7-665">Por ejemplo, podría establecer el rectángulo de origen en el mezclador, pero aplicar el rectángulo de destino en el **método Present.**</span><span class="sxs-lookup"><span data-stu-id="edad7-665">For example, you could set the source rectangle on the mixer but apply the destination rectangle in the **Present** method.</span></span>

<span data-ttu-id="edad7-666">Si la aplicación cambia el rectángulo de destino o cambia el tamaño de la ventana, es posible que tenga que asignar nuevas superficies.</span><span class="sxs-lookup"><span data-stu-id="edad7-666">If the application changes the destination rectangle or resizes the window, you might need to allocate new surfaces.</span></span> <span data-ttu-id="edad7-667">Si es así, debe tener cuidado de sincronizar esta operación con el subproceso de programación.</span><span class="sxs-lookup"><span data-stu-id="edad7-667">If so, you must be careful to synchronize this operation with your scheduling thread.</span></span> <span data-ttu-id="edad7-668">Vacíe la cola de programación y descarte las muestras antiguas antes de asignar nuevas superficies.</span><span class="sxs-lookup"><span data-stu-id="edad7-668">Flush the scheduling queue and discard the old samples before allocating new surfaces.</span></span>

### <a name="end-of-stream"></a><span data-ttu-id="edad7-669">Fin de la secuencia</span><span class="sxs-lookup"><span data-stu-id="edad7-669">End of Stream</span></span>

<span data-ttu-id="edad7-670">Cuando ha finalizado cada flujo de entrada en la EVR, la EVR envía un **MFVP_MESSAGE_ENDOFSTREAM** mensaje al presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-670">When every input stream on the EVR has ended, the EVR sends an **MFVP_MESSAGE_ENDOFSTREAM** message to the presenter.</span></span> <span data-ttu-id="edad7-671">Sin embargo, en el momento en que recibe el mensaje, es posible que haya algunos fotogramas de vídeo restantes para procesar.</span><span class="sxs-lookup"><span data-stu-id="edad7-671">At the point when you receive the message, however, there might be a few video frames remaining to be processed.</span></span> <span data-ttu-id="edad7-672">Antes de responder al mensaje de fin de flujo, debe purgar toda la salida del mezclador y presentar todos los fotogramas restantes.</span><span class="sxs-lookup"><span data-stu-id="edad7-672">Before you respond to the end-of-stream message, you must drain all of the output from the mixer and present all of the remaining frames.</span></span> <span data-ttu-id="edad7-673">Después de presentar el último fotograma, envíe un **EC_COMPLETE** evento al EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-673">After the last frame is presented, send an **EC_COMPLETE** event to the EVR.</span></span>

<span data-ttu-id="edad7-674">En el ejemplo siguiente se muestra un método que envía el **EC_COMPLETE** evento si se cumplen varias condiciones.</span><span class="sxs-lookup"><span data-stu-id="edad7-674">The next example shows a method that sends the **EC_COMPLETE** event if various conditions are met.</span></span> <span data-ttu-id="edad7-675">De lo contrario, devuelve S_OK sin enviar el evento:</span><span class="sxs-lookup"><span data-stu-id="edad7-675">Otherwise, it returns S_OK without sending the event:</span></span>


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



<span data-ttu-id="edad7-676">Este método comprueba los estados siguientes:</span><span class="sxs-lookup"><span data-stu-id="edad7-676">This method checks the following states:</span></span>

-   <span data-ttu-id="edad7-677">Si la *variable m_fSampleNotify* es **TRUE,** significa que el mezclador tiene uno o varios fotogramas que aún no se han procesado.</span><span class="sxs-lookup"><span data-stu-id="edad7-677">If the *m_fSampleNotify* variable is **TRUE**, it means the mixer has one or more frames that have not been processed yet.</span></span> <span data-ttu-id="edad7-678">(Para obtener más información, vea [Procesamiento de salida).](#processing-output)</span><span class="sxs-lookup"><span data-stu-id="edad7-678">(For details, see [Processing Output](#processing-output).)</span></span>
-   <span data-ttu-id="edad7-679">La *m_fEndStreaming* variable es una marca booleana cuyo valor inicial **es FALSE.**</span><span class="sxs-lookup"><span data-stu-id="edad7-679">The *m_fEndStreaming* variable is a Boolean flag whose initial value **FALSE**.</span></span> <span data-ttu-id="edad7-680">El presentador establece la marca en **TRUE cuando** el EVR envía **el MFVP_MESSAGE_ENDOFSTREAM** mensaje.</span><span class="sxs-lookup"><span data-stu-id="edad7-680">The presenter sets the flag to **TRUE** when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message.</span></span>
-   <span data-ttu-id="edad7-681">Se supone que el método devuelve TRUE siempre que uno o varios fotogramas `AreSamplesPending` estén esperando en la cola programada. </span><span class="sxs-lookup"><span data-stu-id="edad7-681">The `AreSamplesPending` method is assumed to return **TRUE** as long as one or more frames are waiting in the scheduled queue.</span></span>

<span data-ttu-id="edad7-682">En el [**método IMFVideoPresenter::P rocessMessage,**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) establezca *m_fEndStreaming* en **TRUE** y llame a cuando el EVR envíe el `CheckEndOfStream` **MFVP_MESSAGE_ENDOFSTREAM** mensaje:</span><span class="sxs-lookup"><span data-stu-id="edad7-682">In the [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method, set *m_fEndStreaming* to **TRUE** and call `CheckEndOfStream` when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message:</span></span>


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="edad7-683">Además, llame a `CheckEndOfStream` si el método [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mezclador **devuelve MF_E_TRANSFORM_NEED_MORE_INPUT**.</span><span class="sxs-lookup"><span data-stu-id="edad7-683">In addition, call `CheckEndOfStream` if the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span></span> <span data-ttu-id="edad7-684">Este código de error indica que el mezclador no tiene más ejemplos de entrada (vea [Procesamiento de salida).](#processing-output)</span><span class="sxs-lookup"><span data-stu-id="edad7-684">This error code indicates that the mixer has no more input samples (see [Processing Output](#processing-output)).</span></span>

## <a name="frame-stepping"></a><span data-ttu-id="edad7-685">Ejecución paso a paso de fotogramas</span><span class="sxs-lookup"><span data-stu-id="edad7-685">Frame Stepping</span></span>

<span data-ttu-id="edad7-686">La EVR está diseñada para admitir la ejecución paso a paso de fotogramas en DirectShow y la limpieza en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="edad7-686">The EVR is designed to support frame stepping in DirectShow and scrubbing in Media Foundation.</span></span> <span data-ttu-id="edad7-687">El paso a paso y la limpieza de fotogramas son conceptualmente similares.</span><span class="sxs-lookup"><span data-stu-id="edad7-687">Frame stepping and scrubbing are conceptually similar.</span></span> <span data-ttu-id="edad7-688">En ambos casos, la aplicación solicita un fotograma de vídeo a la vez.</span><span class="sxs-lookup"><span data-stu-id="edad7-688">In both cases, the application requests one video frame at a time.</span></span> <span data-ttu-id="edad7-689">Internamente, el presentador usa el mismo mecanismo para implementar ambas características.</span><span class="sxs-lookup"><span data-stu-id="edad7-689">Internally, the presenter uses the same mechanism to implement both features.</span></span>

<span data-ttu-id="edad7-690">La ejecución paso a paso de fotogramas en DirectShow funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="edad7-690">Frame stepping in DirectShow works as follows:</span></span>

-   <span data-ttu-id="edad7-691">La aplicación llama [**a IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span><span class="sxs-lookup"><span data-stu-id="edad7-691">The application calls [**IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span></span> <span data-ttu-id="edad7-692">El número de pasos se da en el *parámetro dwSteps.*</span><span class="sxs-lookup"><span data-stu-id="edad7-692">The number of steps is given in the *dwSteps* parameter.</span></span> <span data-ttu-id="edad7-693">La EVR envía un **MFVP_MESSAGE_STEP** al presentador, donde el parámetro de mensaje (*ulParam*) es el número de pasos.</span><span class="sxs-lookup"><span data-stu-id="edad7-693">The EVR sends an **MFVP_MESSAGE_STEP** message to the presenter, where the message parameter (*ulParam*) is the number of steps.</span></span>
-   <span data-ttu-id="edad7-694">Si la aplicación llama a [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) o cambia el estado del grafo (en ejecución, en pausa o detenido), la EVR envía un **MFVP_MESSAGE_CANCELSTEP** mensaje.</span><span class="sxs-lookup"><span data-stu-id="edad7-694">If the application calls [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) or changes the graph state (running, paused, or stopped), the EVR sends an **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="edad7-695">La limpieza en Media Foundation funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="edad7-695">Scrubbing in Media Foundation works as follows:</span></span>

-   <span data-ttu-id="edad7-696">La aplicación establece la velocidad de reproducción en cero mediante una llamada [**a IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span><span class="sxs-lookup"><span data-stu-id="edad7-696">The application sets the playback rate to zero by calling [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span></span>
-   <span data-ttu-id="edad7-697">Para representar un nuevo marco, la aplicación llama [**a LANSESIÓNMEDIAMEDIA::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) con la posición deseada.</span><span class="sxs-lookup"><span data-stu-id="edad7-697">To render a new frame, the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the desired position.</span></span> <span data-ttu-id="edad7-698">La EVR envía un **MFVP_MESSAGE_STEP** con *ulParam* igual a 1.</span><span class="sxs-lookup"><span data-stu-id="edad7-698">The EVR sends an **MFVP_MESSAGE_STEP** message with *ulParam* equal to 1.</span></span>
-   <span data-ttu-id="edad7-699">Para detener la limpieza, la aplicación establece la velocidad de reproducción en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="edad7-699">To stop scrubbing, the application sets the playback rate to a nonzero value.</span></span> <span data-ttu-id="edad7-700">La EVR envía el **MFVP_MESSAGE_CANCELSTEP** mensaje.</span><span class="sxs-lookup"><span data-stu-id="edad7-700">The EVR sends the **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="edad7-701">Después de recibir **MFVP_MESSAGE_STEP** mensaje, el presentador espera a que llegue el fotograma de destino.</span><span class="sxs-lookup"><span data-stu-id="edad7-701">After receiving the **MFVP_MESSAGE_STEP** message, the presenter waits for the target frame to arrive.</span></span> <span data-ttu-id="edad7-702">Si el número de pasos es *N*, el presentador descarta las siguientes muestras *(N* - 1) y presenta la *N* muestra.</span><span class="sxs-lookup"><span data-stu-id="edad7-702">If the number of steps is *N*, the presenter discards the next (*N* - 1) samples and presents the *N* th sample.</span></span> <span data-ttu-id="edad7-703">Cuando el presentador completa el paso de fotograma, envía un evento [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) al EVR con *lParam1* establecido en **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="edad7-703">When the presenter completes the frame step, it sends an [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event to the EVR with *lParam1* set to **FALSE**.</span></span> <span data-ttu-id="edad7-704">Además, si la velocidad de reproducción es cero, el presentador envía un [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) evento.</span><span class="sxs-lookup"><span data-stu-id="edad7-704">In addition, if the playback rate is zero, the presenter sends an [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) event.</span></span> <span data-ttu-id="edad7-705">Si el EVR cancela la ejecución paso **a** paso del marco mientras aún está pendiente una operación de paso de fotogramas, el presentador envía un evento EC_STEP_COMPLETE con *lParam1* establecido en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="edad7-705">If the EVR cancels frame stepping while a frame-step operation is still pending, the presenter sends an **EC_STEP_COMPLETE** event with *lParam1* set to **TRUE**.</span></span>

<span data-ttu-id="edad7-706">La aplicación puede enmarcar el paso o limpiar varias veces, por lo que el presentador podría recibir varios mensajes **MFVP_MESSAGE_STEP** antes de obtener un **MFVP_MESSAGE_CANCELSTEP** mensaje.</span><span class="sxs-lookup"><span data-stu-id="edad7-706">The application can frame step or scrub multiple times, so the presenter might receive multiple **MFVP_MESSAGE_STEP** messages before it gets an **MFVP_MESSAGE_CANCELSTEP** message.</span></span> <span data-ttu-id="edad7-707">Además, el presentador puede recibir el **mensaje MFVP_MESSAGE_STEP** antes de que se inicie el reloj o mientras se ejecuta el reloj.</span><span class="sxs-lookup"><span data-stu-id="edad7-707">Also, the presenter can receive the **MFVP_MESSAGE_STEP** message before the clock starts or while the clock is running.</span></span>

### <a name="implementing-frame-stepping"></a><span data-ttu-id="edad7-708">Implementación de la ejecución paso a paso de fotogramas</span><span class="sxs-lookup"><span data-stu-id="edad7-708">Implementing Frame Stepping</span></span>

<span data-ttu-id="edad7-709">En esta sección se describe un algoritmo para implementar la ejecución paso a paso de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="edad7-709">This section describes an algorithm to implement frame stepping.</span></span> <span data-ttu-id="edad7-710">El algoritmo de ejecución paso a paso de fotogramas usa las siguientes variables:</span><span class="sxs-lookup"><span data-stu-id="edad7-710">The frame stepping algorithm uses the following variables:</span></span>

-   <span data-ttu-id="edad7-711">*step_count*.</span><span class="sxs-lookup"><span data-stu-id="edad7-711">*step_count*.</span></span> <span data-ttu-id="edad7-712">Entero sin signo que especifica el número de pasos de la operación de ejecución paso a paso del marco actual.</span><span class="sxs-lookup"><span data-stu-id="edad7-712">An unsigned integer that specifies the number of steps in the current frame stepping operation.</span></span>
-   <span data-ttu-id="edad7-713">*step_queue*.</span><span class="sxs-lookup"><span data-stu-id="edad7-713">*step_queue*.</span></span> <span data-ttu-id="edad7-714">Cola de punteros [**DESAMPLESample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)</span><span class="sxs-lookup"><span data-stu-id="edad7-714">A queue of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointers.</span></span>
-   <span data-ttu-id="edad7-715">*step_state*.</span><span class="sxs-lookup"><span data-stu-id="edad7-715">*step_state*.</span></span> <span data-ttu-id="edad7-716">En cualquier momento, el presentador puede estar en uno de los siguientes estados con respecto a la ejecución paso a paso de fotogramas:</span><span class="sxs-lookup"><span data-stu-id="edad7-716">At any time, the presenter can be in one of the following states with respect to frame stepping:</span></span> 

    | <span data-ttu-id="edad7-717">Estado</span><span class="sxs-lookup"><span data-stu-id="edad7-717">State</span></span>         | <span data-ttu-id="edad7-718">Descripción</span><span class="sxs-lookup"><span data-stu-id="edad7-718">Description</span></span>                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="edad7-719">NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="edad7-719">NOT_STEPPING</span></span> | <span data-ttu-id="edad7-720">No paso a paso de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="edad7-720">Not frame stepping.</span></span>                                                                                                                                                                                             |
    | <span data-ttu-id="edad7-721">EN ESPERA</span><span class="sxs-lookup"><span data-stu-id="edad7-721">WAITING</span></span>       | <span data-ttu-id="edad7-722">El presentador ha recibido el **mensaje MFVP_MESSAGE_STEP,** pero el reloj no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="edad7-722">The presenter has received the **MFVP_MESSAGE_STEP** message, but the clock has not started.</span></span>                                                                                                                  |
    | <span data-ttu-id="edad7-723">PENDING</span><span class="sxs-lookup"><span data-stu-id="edad7-723">PENDING</span></span>       | <span data-ttu-id="edad7-724">El presentador ha recibido el **mensaje MFVP_MESSAGE_STEP** y se ha iniciado el reloj, pero el presentador está esperando recibir el fotograma de destino.</span><span class="sxs-lookup"><span data-stu-id="edad7-724">The presenter has received the **MFVP_MESSAGE_STEP** message and the clock has started, but the presenter is waiting to receive the target frame.</span></span>                                                             |
    | <span data-ttu-id="edad7-725">Programado</span><span class="sxs-lookup"><span data-stu-id="edad7-725">SCHEDULED</span></span>     | <span data-ttu-id="edad7-726">El presentador ha recibido el marco de destino y lo ha programado para su presentación, pero no se ha presentado.</span><span class="sxs-lookup"><span data-stu-id="edad7-726">The presenter has received the target frame and has scheduled it for presentation, but the frame has not been presented.</span></span>                                                                                        |
    | <span data-ttu-id="edad7-727">íntegro</span><span class="sxs-lookup"><span data-stu-id="edad7-727">COMPLETE</span></span>      | <span data-ttu-id="edad7-728">El presentador ha presentado el marco de destino y ha enviado el evento [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) y está esperando el siguiente mensaje **MFVP_MESSAGE_STEP** o **MFVP_MESSAGE_CANCELSTEP** mensaje.</span><span class="sxs-lookup"><span data-stu-id="edad7-728">The presenter has presented the target frame and sent the [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event, and is waiting for the next **MFVP_MESSAGE_STEP** or **MFVP_MESSAGE_CANCELSTEP** message.</span></span> |

    

     

    <span data-ttu-id="edad7-729">Estos estados son independientes de los estados de presentador enumerados en la sección [Estados del presentador](#presenter-states).</span><span class="sxs-lookup"><span data-stu-id="edad7-729">These states are independent of the presenter states listed in the section [Presenter States](#presenter-states).</span></span>

<span data-ttu-id="edad7-730">Los procedimientos siguientes se definen para el algoritmo de paso a paso de fotogramas:</span><span class="sxs-lookup"><span data-stu-id="edad7-730">The following procedures are defined for the frame-stepping algorithm:</span></span>

<span data-ttu-id="edad7-731">Procedimiento PrepareFrameStep</span><span class="sxs-lookup"><span data-stu-id="edad7-731">PrepareFrameStep Procedure</span></span>

1.  <span data-ttu-id="edad7-732">Incrementar *step_count*.</span><span class="sxs-lookup"><span data-stu-id="edad7-732">Increment *step_count*.</span></span>
2.  <span data-ttu-id="edad7-733">Establezca *step_state* en ESPERANDO.</span><span class="sxs-lookup"><span data-stu-id="edad7-733">Set *step_state* to WAITING.</span></span>
3.  <span data-ttu-id="edad7-734">Si el reloj se está ejecutando, llame a StartFrameStep.</span><span class="sxs-lookup"><span data-stu-id="edad7-734">If the clock is running, call StartFrameStep.</span></span>

<span data-ttu-id="edad7-735">Procedimiento StartFrameStep</span><span class="sxs-lookup"><span data-stu-id="edad7-735">StartFrameStep Procedure</span></span>

1.  <span data-ttu-id="edad7-736">Si *step_state* es igual a WAITING, *establezca step_state* en PENDING.</span><span class="sxs-lookup"><span data-stu-id="edad7-736">If *step_state* equals WAITING, set *step_state* to PENDING.</span></span> <span data-ttu-id="edad7-737">Para cada ejemplo de *step_queue*, llame a DeliverFrameStepSample.</span><span class="sxs-lookup"><span data-stu-id="edad7-737">For each sample in *step_queue*, call DeliverFrameStepSample.</span></span>
2.  <span data-ttu-id="edad7-738">Si *step_state* es igual NOT_STEPPING, quite los ejemplos step_queue *programarlos* para su presentación.</span><span class="sxs-lookup"><span data-stu-id="edad7-738">If *step_state* equals NOT_STEPPING, remove any samples from *step_queue* and schedule them for presentation.</span></span>

<span data-ttu-id="edad7-739">Procedimiento CompleteFrameStep</span><span class="sxs-lookup"><span data-stu-id="edad7-739">CompleteFrameStep Procedure</span></span>

1.  <span data-ttu-id="edad7-740">Establezca *step_state* en COMPLETE.</span><span class="sxs-lookup"><span data-stu-id="edad7-740">Set *step_state* to COMPLETE.</span></span>
2.  <span data-ttu-id="edad7-741">Envíe el EC_STEP_COMPLETE evento con *lParam1*  =  **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="edad7-741">Send the EC_STEP_COMPLETE event with *lParam1* = **FALSE**.</span></span>
3.  <span data-ttu-id="edad7-742">Si la velocidad del reloj es cero, envíe el **EC_SCRUB_TIME** evento con la hora de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="edad7-742">If the clock rate is zero, send the **EC_SCRUB_TIME** event with the sample time.</span></span>

<span data-ttu-id="edad7-743">Procedimiento DeliverFrameStepSample</span><span class="sxs-lookup"><span data-stu-id="edad7-743">DeliverFrameStepSample Procedure</span></span>

1.  <span data-ttu-id="edad7-744">Si la velocidad del reloj es cero y *el tiempo de* reloj de la muestra de muestra de  +    <  muestra, descarte la muestra.</span><span class="sxs-lookup"><span data-stu-id="edad7-744">If the clock rate is zero and *sample time* + *sample duration* < *clock time*, discard the sample.</span></span> <span data-ttu-id="edad7-745">Salir.</span><span class="sxs-lookup"><span data-stu-id="edad7-745">Exit.</span></span>
2.  <span data-ttu-id="edad7-746">Si *step_state* es igual a SCHEDULED o COMPLETE, agregue el ejemplo a *step_queue*.</span><span class="sxs-lookup"><span data-stu-id="edad7-746">If *step_state* equals SCHEDULED or COMPLETE, add the sample to *step_queue*.</span></span> <span data-ttu-id="edad7-747">Salir.</span><span class="sxs-lookup"><span data-stu-id="edad7-747">Exit.</span></span>
3.  <span data-ttu-id="edad7-748">Decremento *step_count*.</span><span class="sxs-lookup"><span data-stu-id="edad7-748">Decrement *step_count*.</span></span>
4.  <span data-ttu-id="edad7-749">Si *step_count* > 0, descarte el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="edad7-749">If *step_count* > 0, discard the sample.</span></span> <span data-ttu-id="edad7-750">Salir.</span><span class="sxs-lookup"><span data-stu-id="edad7-750">Exit.</span></span>
5.  <span data-ttu-id="edad7-751">Si *step_state* es igual a WAITING, agregue el ejemplo a *step_queue*.</span><span class="sxs-lookup"><span data-stu-id="edad7-751">If *step_state* equals WAITING, add the sample to *step_queue*.</span></span> <span data-ttu-id="edad7-752">Salir.</span><span class="sxs-lookup"><span data-stu-id="edad7-752">Exit.</span></span>
6.  <span data-ttu-id="edad7-753">Programe el ejemplo para su presentación.</span><span class="sxs-lookup"><span data-stu-id="edad7-753">Schedule the sample for presentation.</span></span>
7.  <span data-ttu-id="edad7-754">Establezca *step_state* en SCHEDULED.</span><span class="sxs-lookup"><span data-stu-id="edad7-754">Set *step_state* to SCHEDULED.</span></span>

<span data-ttu-id="edad7-755">Procedimiento CancelFrameStep</span><span class="sxs-lookup"><span data-stu-id="edad7-755">CancelFrameStep Procedure</span></span>

1.  <span data-ttu-id="edad7-756">Establezca *step_state* en NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="edad7-756">Set *step_state* to NOT_STEPPING</span></span>
2.  <span data-ttu-id="edad7-757">*Restablezca step_count* a cero.</span><span class="sxs-lookup"><span data-stu-id="edad7-757">Reset *step_count* to zero.</span></span>
3.  <span data-ttu-id="edad7-758">Si el valor anterior de *step_state* era WAITING, PENDING o SCHEDULED, EC_STEP_COMPLETE con *lParam1*  =  **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="edad7-758">If the previous value of *step_state* was WAITING, PENDING, or SCHEDULED, send EC_STEP_COMPLETE with *lParam1* = **TRUE**.</span></span>

<span data-ttu-id="edad7-759">Llame a estos procedimientos como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="edad7-759">Call these procedures as follows:</span></span>



| <span data-ttu-id="edad7-760">Mensaje o método del presentador</span><span class="sxs-lookup"><span data-stu-id="edad7-760">Presenter message or method</span></span>                                                   | <span data-ttu-id="edad7-761">Procedimiento</span><span class="sxs-lookup"><span data-stu-id="edad7-761">Procedure</span></span>           |
|-------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="edad7-762">**MFVP_MESSAGE_STEP** mensaje</span><span class="sxs-lookup"><span data-stu-id="edad7-762">**MFVP_MESSAGE_STEP** message</span></span>                                               | `PrepareFrameStep`  |
| <span data-ttu-id="edad7-763">**MFVP_MESSAGE_STEP** mensaje</span><span class="sxs-lookup"><span data-stu-id="edad7-763">**MFVP_MESSAGE_STEP** message</span></span>                                               | `CancelStep`        |
| [<span data-ttu-id="edad7-764">**IMFClockStateSink::OnClockStart**</span><span class="sxs-lookup"><span data-stu-id="edad7-764">**IMFClockStateSink::OnClockStart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [<span data-ttu-id="edad7-765">**IMFClockStateSink::OnClockRestart**</span><span class="sxs-lookup"><span data-stu-id="edad7-765">**IMFClockStateSink::OnClockRestart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| <span data-ttu-id="edad7-766">[**Devolución de llamada DE DEvolución de llamada DE DEVOLUCIÓN DE MUESTREOTRACKEDSAMPLE**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="edad7-766">[**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback</span></span>                         | `CompleteFrameStep` |
| [<span data-ttu-id="edad7-767">**IMFClockStateSink::OnClockStop**</span><span class="sxs-lookup"><span data-stu-id="edad7-767">**IMFClockStateSink::OnClockStop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [<span data-ttu-id="edad7-768">**IMFClockStateSink::OnClockSetRate**</span><span class="sxs-lookup"><span data-stu-id="edad7-768">**IMFClockStateSink::OnClockSetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

<span data-ttu-id="edad7-769">En el siguiente gráfico de flujo se muestran los procedimientos de paso a paso de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="edad7-769">The following flow chart shows the frame-stepping procedures.</span></span>

![diagrama de flujo que muestra las rutas de acceso que comienzan con el paso de mensaje mfvp y el proceso de mensaje \- \- \- \- mfvpinputnotify y terminan en "state = complete"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a><span data-ttu-id="edad7-771">Establecimiento del presentador en la EVR</span><span class="sxs-lookup"><span data-stu-id="edad7-771">Setting the Presenter on the EVR</span></span>

<span data-ttu-id="edad7-772">Después de implementar el presentador, el siguiente paso es configurar la EVR para usarla.</span><span class="sxs-lookup"><span data-stu-id="edad7-772">After implementing the presenter, the next step is to configure the EVR to use it.</span></span>

### <a name="setting-the-presenter-in-directshow"></a><span data-ttu-id="edad7-773">Establecimiento del presentador en DirectShow</span><span class="sxs-lookup"><span data-stu-id="edad7-773">Setting the Presenter in DirectShow</span></span>

<span data-ttu-id="edad7-774">En una aplicación DirectShow, establezca el presentador en la EVR como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="edad7-774">In a DirectShow application, set the presenter on the EVR as follows:</span></span>

1.  <span data-ttu-id="edad7-775">Cree el filtro EVR mediante una llamada **a CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="edad7-775">Create the EVR filter by calling **CoCreateInstance**.</span></span> <span data-ttu-id="edad7-776">El CLSID es **CLSID_EnhancedVideoRenderer**.</span><span class="sxs-lookup"><span data-stu-id="edad7-776">The CLSID is **CLSID_EnhancedVideoRenderer**.</span></span>
2.  <span data-ttu-id="edad7-777">Agregue la EVR al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="edad7-777">Add the EVR to the filter graph.</span></span>
3.  <span data-ttu-id="edad7-778">Cree una instancia del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-778">Create an instance of your presenter.</span></span> <span data-ttu-id="edad7-779">El presentador puede admitir la creación de objetos COM estándar a través **de IClassFactory,** pero esto no es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="edad7-779">Your presenter can support standard COM object creation through **IClassFactory**, but this is not mandatory.</span></span>
4.  <span data-ttu-id="edad7-780">Consulte el filtro EVR para la [**interfaz DEL REPRESENTADORDEVÍDEOVídeo.**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)</span><span class="sxs-lookup"><span data-stu-id="edad7-780">Query the EVR filter for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
5.  <span data-ttu-id="edad7-781">Llame [**a IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="edad7-781">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

### <a name="setting-the-presenter-in-media-foundation"></a><span data-ttu-id="edad7-782">Establecimiento del presentador en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="edad7-782">Setting the Presenter in Media Foundation</span></span>

<span data-ttu-id="edad7-783">En Media Foundation, tiene varias opciones, en función de si crea el receptor de medios EVR o el objeto de activación de EVR.</span><span class="sxs-lookup"><span data-stu-id="edad7-783">In Media Foundation, you have several options, depending on whether you create the EVR media sink or the EVR activation object.</span></span> <span data-ttu-id="edad7-784">Para obtener más información sobre los objetos de activación, vea [Activation Objects](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="edad7-784">For more information about activation objects, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="edad7-785">Para el receptor de medios EVR, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="edad7-785">For the EVR media sink, do the following:</span></span>

1.  <span data-ttu-id="edad7-786">Llame [**a MFCreateVideoRenderer para**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) crear el receptor multimedia.</span><span class="sxs-lookup"><span data-stu-id="edad7-786">Call [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) to create the media sink.</span></span>
2.  <span data-ttu-id="edad7-787">Cree una instancia del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-787">Create an instance of your presenter.</span></span>
3.  <span data-ttu-id="edad7-788">Consulte el receptor de medios EVR para la [**interfaz DEL REPRESENTADORDEVÍDEOVídeo.**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)</span><span class="sxs-lookup"><span data-stu-id="edad7-788">Query the EVR media sink for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
4.  <span data-ttu-id="edad7-789">Llame [**a IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="edad7-789">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

<span data-ttu-id="edad7-790">Para el objeto de activación EVR, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="edad7-790">For the EVR activation object, do the following:</span></span>

1.  <span data-ttu-id="edad7-791">Llame [**a MFCreateVideoRendererActivate para**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) crear el objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="edad7-791">Call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the activation object.</span></span>
2.  <span data-ttu-id="edad7-792">Establezca uno de los atributos siguientes en el objeto de activación:</span><span class="sxs-lookup"><span data-stu-id="edad7-792">Set one of the following attributes on the activation object:</span></span> 

    | <span data-ttu-id="edad7-793">Atributo</span><span class="sxs-lookup"><span data-stu-id="edad7-793">Attribute</span></span>                                                                                                         | <span data-ttu-id="edad7-794">Descripción</span><span class="sxs-lookup"><span data-stu-id="edad7-794">Description</span></span>                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="edad7-795">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="edad7-795">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span></span>](mf-activate-custom-video-presenter-activate-attribute.md) | <span data-ttu-id="edad7-796">Puntero a un objeto de activación para el presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-796">Pointer to an activation object for the presenter.</span></span><br/> <span data-ttu-id="edad7-797">Con esta marca, debe proporcionar un objeto de activación para el presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-797">With this flag, you must provide an activation object for your presenter.</span></span> <span data-ttu-id="edad7-798">El objeto de activación debe implementar la [**interfaz IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)</span><span class="sxs-lookup"><span data-stu-id="edad7-798">The activation object must implement the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span><br/> |
    | [<span data-ttu-id="edad7-799">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span><span class="sxs-lookup"><span data-stu-id="edad7-799">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span></span>](mf-activate-custom-video-presenter-clsid-attribute.md)       | <span data-ttu-id="edad7-800">CLSID del presentador.</span><span class="sxs-lookup"><span data-stu-id="edad7-800">CLSID of the presenter.</span></span><br/> <span data-ttu-id="edad7-801">Con esta marca, el presentador debe admitir la creación de objetos COM estándar a través **de IClassFactory.**</span><span class="sxs-lookup"><span data-stu-id="edad7-801">With this flag, your presenter must support standard COM object creation through **IClassFactory**.</span></span><br/>                                                                                         |

    

     

3.  <span data-ttu-id="edad7-802">Opcionalmente, establezca el [**atributo MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) en el objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="edad7-802">Optionally, set the [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) attribute on the activation object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edad7-803">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edad7-803">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edad7-804">Representador de vídeo mejorado</span><span class="sxs-lookup"><span data-stu-id="edad7-804">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="edad7-805">Ejemplo EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="edad7-805">EVRPresenter Sample</span></span>](evrpresenter-sample.md)
</dt> </dl>

 

 
