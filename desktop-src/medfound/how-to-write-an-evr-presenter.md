---
description: En este artículo se describe cómo escribir un presentador personalizado para el representador de vídeo mejorado (EVR).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Cómo escribir un presentador de EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94933d9eb53b0b03105edc7056ace4fe73238d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557251"
---
# <a name="how-to-write-an-evr-presenter"></a><span data-ttu-id="6b1fa-103">Cómo escribir un presentador de EVR</span><span class="sxs-lookup"><span data-stu-id="6b1fa-103">How to Write an EVR Presenter</span></span>

<span data-ttu-id="6b1fa-104">En este artículo se describe cómo escribir un presentador personalizado para el representador de vídeo mejorado (EVR).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-104">This article describes how to write a custom presenter for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="6b1fa-105">Un presentador personalizado se puede usar con DirectShow y Media Foundation; las interfaces y el modelo de objetos son los mismos para ambas tecnologías, aunque la secuencia exacta de operaciones puede variar.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-105">A custom presenter can be used with both DirectShow and Media Foundation; the interfaces and object model are the same for both technologies, although the exact sequence of operations might vary.</span></span>

<span data-ttu-id="6b1fa-106">El código de ejemplo de este tema se adapta desde el [ejemplo EVRPresenter](evrpresenter-sample.md), que se proporciona en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-106">The example code in this topic is adapted from the [EVRPresenter Sample](evrpresenter-sample.md), which is provided in the Windows SDK.</span></span>

<span data-ttu-id="6b1fa-107">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="6b1fa-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6b1fa-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="6b1fa-109">Modelo de objetos de moderador</span><span class="sxs-lookup"><span data-stu-id="6b1fa-109">Presenter Object Model</span></span>](#presenter-object-model)
    -   [<span data-ttu-id="6b1fa-110">Flujo de datos dentro de EVR</span><span class="sxs-lookup"><span data-stu-id="6b1fa-110">Data Flow Inside the EVR</span></span>](#data-flow-inside-the-evr)
    -   [<span data-ttu-id="6b1fa-111">Estados del presentador</span><span class="sxs-lookup"><span data-stu-id="6b1fa-111">Presenter States</span></span>](#presenter-states)
    -   [<span data-ttu-id="6b1fa-112">Interfaces de moderador</span><span class="sxs-lookup"><span data-stu-id="6b1fa-112">Presenter Interfaces</span></span>](#presenter-interfaces)
    -   [<span data-ttu-id="6b1fa-113">Implementación de IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="6b1fa-113">Implementing IMFVideoDeviceID</span></span>](#implementing-imfvideodeviceid)
    -   [<span data-ttu-id="6b1fa-114">Implementación de IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="6b1fa-114">Implementing IMFTopologyServiceLookupClient</span></span>](#implementing-imftopologyservicelookupclient)
    -   [<span data-ttu-id="6b1fa-115">Implementación de IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="6b1fa-115">Implementing IMFVideoPresenter</span></span>](#implementing-imfvideopresenter)
    -   [<span data-ttu-id="6b1fa-116">Implementación de IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="6b1fa-116">Implementing IMFClockStateSink</span></span>](#implementing-imfclockstatesink)
    -   [<span data-ttu-id="6b1fa-117">Implementación de IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="6b1fa-117">Implementing IMFRateSupport</span></span>](#implementing-imfratesupport)
    -   [<span data-ttu-id="6b1fa-118">Envío de eventos a EVR</span><span class="sxs-lookup"><span data-stu-id="6b1fa-118">Sending Events to the EVR</span></span>](#sending-events-to-the-evr)
-   [<span data-ttu-id="6b1fa-119">Formatos de negociación</span><span class="sxs-lookup"><span data-stu-id="6b1fa-119">Negotiating Formats</span></span>](#negotiating-formats)
-   [<span data-ttu-id="6b1fa-120">Administrar el dispositivo Direct3D</span><span class="sxs-lookup"><span data-stu-id="6b1fa-120">Managing the Direct3D Device</span></span>](#managing-the-direct3d-device)
    -   [<span data-ttu-id="6b1fa-121">Asignación de superficies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="6b1fa-121">Allocating Direct3D Surfaces</span></span>](#allocating-direct3d-surfaces)
    -   [<span data-ttu-id="6b1fa-122">Ejemplos de seguimiento</span><span class="sxs-lookup"><span data-stu-id="6b1fa-122">Tracking Samples</span></span>](#tracking-samples)
-   [<span data-ttu-id="6b1fa-123">Procesar la salida</span><span class="sxs-lookup"><span data-stu-id="6b1fa-123">Processing Output</span></span>](#processing-output)
    -   [<span data-ttu-id="6b1fa-124">Volver a dibujar marcos</span><span class="sxs-lookup"><span data-stu-id="6b1fa-124">Repainting Frames</span></span>](#repainting-frames)
    -   [<span data-ttu-id="6b1fa-125">Ejemplos de programación</span><span class="sxs-lookup"><span data-stu-id="6b1fa-125">Scheduling Samples</span></span>](#scheduling-samples)
    -   [<span data-ttu-id="6b1fa-126">Presentar ejemplos</span><span class="sxs-lookup"><span data-stu-id="6b1fa-126">Presenting Samples</span></span>](#presenting-samples)
    -   [<span data-ttu-id="6b1fa-127">Rectángulos de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="6b1fa-127">Source and Destination Rectangles</span></span>](#source-and-destination-rectangles)
    -   [<span data-ttu-id="6b1fa-128">Final de la secuencia</span><span class="sxs-lookup"><span data-stu-id="6b1fa-128">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="6b1fa-129">Recorrido de fotogramas</span><span class="sxs-lookup"><span data-stu-id="6b1fa-129">Frame Stepping</span></span>](#frame-stepping)
    -   [<span data-ttu-id="6b1fa-130">Implementación del recorrido de fotogramas</span><span class="sxs-lookup"><span data-stu-id="6b1fa-130">Implementing Frame Stepping</span></span>](#implementing-frame-stepping)
-   [<span data-ttu-id="6b1fa-131">Establecer el presentador en el EVR</span><span class="sxs-lookup"><span data-stu-id="6b1fa-131">Setting the Presenter on the EVR</span></span>](#setting-the-presenter-on-the-evr)
    -   [<span data-ttu-id="6b1fa-132">Establecer el presentador en DirectShow</span><span class="sxs-lookup"><span data-stu-id="6b1fa-132">Setting the Presenter in DirectShow</span></span>](#setting-the-presenter-in-directshow)
    -   [<span data-ttu-id="6b1fa-133">Establecer el presentador en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b1fa-133">Setting the Presenter in Media Foundation</span></span>](#setting-the-presenter-in-media-foundation)
-   [<span data-ttu-id="6b1fa-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b1fa-134">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="6b1fa-135">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6b1fa-135">Prerequisites</span></span>

<span data-ttu-id="6b1fa-136">Antes de escribir un presentador personalizado, debe estar familiarizado con las siguientes tecnologías:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-136">Before writing a custom presenter, you should be familiar with the following technologies:</span></span>

-   <span data-ttu-id="6b1fa-137">El representador de vídeo mejorado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-137">The enhanced video renderer.</span></span> <span data-ttu-id="6b1fa-138">Consulte [representador de vídeo mejorado](enhanced-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-138">See [Enhanced Video Renderer](enhanced-video-renderer.md).</span></span>
-   <span data-ttu-id="6b1fa-139">Gráficos de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-139">Direct3D graphics.</span></span> <span data-ttu-id="6b1fa-140">No es necesario comprender los gráficos 3D para escribir un presentador, pero debe saber cómo crear un dispositivo Direct3D y administrar superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-140">You don't need to understand 3-D graphics to write a presenter, but you must know how to create a Direct3D device and manage Direct3D surfaces.</span></span> <span data-ttu-id="6b1fa-141">Si no está familiarizado con Direct3D, lea las secciones "dispositivos Direct3D" y "recursos de Direct3D" en la documentación del SDK de gráficos de DirectX.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-141">If you aren't familiar with Direct3D, read the sections "Direct3D Devices" and "Direct3D Resources" in the DirectX Graphics SDK documentation.</span></span>
-   <span data-ttu-id="6b1fa-142">Gráficos de filtros de DirectShow o la canalización de Media Foundation, en función de la tecnología que utilizará la aplicación para representar vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-142">DirectShow filter graphs or the Media Foundation pipeline, depending on which technology your application will use to render video.</span></span>
-   <span data-ttu-id="6b1fa-143">[Media Foundation transformaciones](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-143">[Media Foundation Transforms](media-foundation-transforms.md).</span></span> <span data-ttu-id="6b1fa-144">EVR mixer es una transformación de Media Foundation y el presentador llama a los métodos directamente en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-144">The EVR mixer is a Media Foundation transform, and the presenter calls methods directly on the mixer.</span></span>
-   <span data-ttu-id="6b1fa-145">Implementar objetos COM.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-145">Implementing COM objects.</span></span> <span data-ttu-id="6b1fa-146">El presentador es un objeto COM en proceso y de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-146">The presenter is an in-process, free-threaded COM object.</span></span>

## <a name="presenter-object-model"></a><span data-ttu-id="6b1fa-147">Modelo de objetos de moderador</span><span class="sxs-lookup"><span data-stu-id="6b1fa-147">Presenter Object Model</span></span>

<span data-ttu-id="6b1fa-148">Esta sección contiene información general sobre el modelo de objetos y las interfaces del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-148">This section contains an overview the presenter object model and interfaces.</span></span>

### <a name="data-flow-inside-the-evr"></a><span data-ttu-id="6b1fa-149">Flujo de datos dentro de EVR</span><span class="sxs-lookup"><span data-stu-id="6b1fa-149">Data Flow Inside the EVR</span></span>

<span data-ttu-id="6b1fa-150">EVR usa dos componentes de complemento para representar vídeo: el *mezclador* y el *presentador*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-150">The EVR uses two plug-in components to render video: the *mixer* and the *presenter*.</span></span> <span data-ttu-id="6b1fa-151">El mezclador combina las secuencias de vídeo y desentrelaza el vídeo si es necesario.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-151">The mixer blends the video streams and deinterlaces the video if needed.</span></span> <span data-ttu-id="6b1fa-152">El presentador dibuja (o *presenta*) el vídeo en la pantalla y programa Cuándo se dibuja cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-152">The presenter draws (or *presents*) the video onto the display and schedules when each frame is drawn.</span></span> <span data-ttu-id="6b1fa-153">Las aplicaciones pueden reemplazar cualquiera de estos objetos por una implementación personalizada.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-153">Applications can replace either of these objects with a custom implementation.</span></span>

<span data-ttu-id="6b1fa-154">EVR tiene uno o varios flujos de entrada y el mezclador tiene un número correspondiente de flujos de entrada.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-154">The EVR has one or more input streams, and the mixer has a corresponding number of input streams.</span></span> <span data-ttu-id="6b1fa-155">Stream 0 siempre es el *flujo de referencia*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-155">Stream 0 is always the *reference stream*.</span></span> <span data-ttu-id="6b1fa-156">Los demás flujos son *subflujos*, que el mezclador alfa combina en el flujo de referencia.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-156">The other streams are *substreams*, which the mixer alpha-blends onto the reference stream.</span></span> <span data-ttu-id="6b1fa-157">La secuencia de referencia determina la velocidad de fotogramas principal del vídeo compuesto.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-157">The reference stream determines the master frame-rate for the composited video.</span></span> <span data-ttu-id="6b1fa-158">En cada fotograma de referencia, el mezclador toma el fotograma más reciente de cada subflujo, lo combina alfa en el fotograma de referencia y genera un único fotograma compuesto.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-158">For each reference frame, the mixer takes the most recent frame from each substream, alpha-blends them onto the reference frame, and outputs a single composited frame.</span></span> <span data-ttu-id="6b1fa-159">El mezclador también realiza desentrelazado y conversión de color de YUV a RGB si es necesario.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-159">The mixer also performs deinterlacing and color conversion from YUV to RGB if needed.</span></span> <span data-ttu-id="6b1fa-160">EVR siempre inserta el mezclador en la canalización de vídeo, independientemente del número de flujos de entrada o el formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-160">The EVR always inserts the mixer into the video pipeline, regardless of the number of input streams or the video format.</span></span> <span data-ttu-id="6b1fa-161">En la imagen siguiente se ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-161">The following image illustrates this process.</span></span>

![diagrama que muestra la secuencia de referencia y el subflujo que apunta al mezclador, que señala al presentador, que apunta a la pantalla.](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

<span data-ttu-id="6b1fa-163">El presentador realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-163">The presenter performs the following tasks:</span></span>

-   <span data-ttu-id="6b1fa-164">Establece el formato de salida en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-164">Sets the output format on the mixer.</span></span> <span data-ttu-id="6b1fa-165">Antes de que comience el streaming, el presentador establece un tipo de medio en el flujo de salida del mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-165">Before streaming begins, the presenter sets a media type on the mixer's output stream.</span></span> <span data-ttu-id="6b1fa-166">Este tipo de medio define el formato de la imagen compuesta.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-166">This media type defines the format of the composited image.</span></span>
-   <span data-ttu-id="6b1fa-167">Crea el dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-167">Creates the Direct3D device.</span></span>
-   <span data-ttu-id="6b1fa-168">Asigna superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-168">Allocates Direct3D surfaces.</span></span> <span data-ttu-id="6b1fa-169">El mezclador blits los fotogramas compuestos en estas superficies.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-169">The mixer blits the composited frames onto these surfaces.</span></span>
-   <span data-ttu-id="6b1fa-170">Obtiene el resultado del mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-170">Gets the output from the mixer.</span></span>
-   <span data-ttu-id="6b1fa-171">Programa Cuándo se presentan los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-171">Schedules when the frames are presented.</span></span> <span data-ttu-id="6b1fa-172">EVR proporciona el reloj de la presentación y el presentador programa fotogramas según este reloj.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-172">The EVR provides the presentation clock, and the presenter schedules frames according to this clock.</span></span>
-   <span data-ttu-id="6b1fa-173">Presenta cada fotograma mediante Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-173">Presents each frame using Direct3D.</span></span>
-   <span data-ttu-id="6b1fa-174">Realiza el recorrido y la limpieza de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-174">Performs frame stepping and scrubbing.</span></span>

### <a name="presenter-states"></a><span data-ttu-id="6b1fa-175">Estados del presentador</span><span class="sxs-lookup"><span data-stu-id="6b1fa-175">Presenter States</span></span>

<span data-ttu-id="6b1fa-176">En cualquier momento, el presentador se encuentra en uno de los siguientes Estados:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-176">At any time, the presenter is in one of following states:</span></span>

-   <span data-ttu-id="6b1fa-177">*Iniciado*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-177">*Started*.</span></span> <span data-ttu-id="6b1fa-178">El reloj de la presentación de EVR se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-178">The EVR's presentation clock is running.</span></span> <span data-ttu-id="6b1fa-179">El presentador programa fotogramas de vídeo para su presentación a medida que llegan.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-179">The presenter schedules video frames for presentation as they arrive.</span></span>
-   <span data-ttu-id="6b1fa-180">En *pausa*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-180">*Paused*.</span></span> <span data-ttu-id="6b1fa-181">El reloj de la presentación se suspende.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-181">The presentation clock is suspended.</span></span> <span data-ttu-id="6b1fa-182">El presentador no presenta ningún ejemplo nuevo, sino que mantiene su cola de ejemplos programados.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-182">The presenter does not present any new samples but maintains its queue of scheduled samples.</span></span> <span data-ttu-id="6b1fa-183">Si se reciben muestras nuevas, el presentador las agrega a la cola.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-183">If new samples are received, the presenter adds them to the queue.</span></span>
-   <span data-ttu-id="6b1fa-184">*Detenido*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-184">*Stopped*.</span></span> <span data-ttu-id="6b1fa-185">El reloj de la presentación está detenido.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-185">The presentation clock is stopped.</span></span> <span data-ttu-id="6b1fa-186">El presentador descarta cualquier ejemplo programado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-186">The presenter discards any samples that were scheduled.</span></span>
-   <span data-ttu-id="6b1fa-187">*Apagar*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-187">*Shut down*.</span></span> <span data-ttu-id="6b1fa-188">El presentador libera todos los recursos relacionados con el streaming, como las superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-188">The presenter releases any resources related to streaming, such as Direct3D surfaces.</span></span> <span data-ttu-id="6b1fa-189">Este es el estado inicial del presentador y el estado final antes de que se destruya el presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-189">This is the presenter's initial state, and the final state before the presenter is destroyed.</span></span>

<span data-ttu-id="6b1fa-190">En el código de ejemplo de este tema, el estado del presentador se representa mediante una enumeración:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-190">In the example code in this topic, the presenter state is represented by an enumeration:</span></span>


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



<span data-ttu-id="6b1fa-191">Algunas operaciones no son válidas mientras el presentador se encuentra en estado de cierre.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-191">Some operations are not valid while the presenter is in the shutdown state.</span></span> <span data-ttu-id="6b1fa-192">En el código de ejemplo se comprueba este estado llamando a un método auxiliar:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-192">The example code checks for this state by calling a helper method:</span></span>


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



### <a name="presenter-interfaces"></a><span data-ttu-id="6b1fa-193">Interfaces de moderador</span><span class="sxs-lookup"><span data-stu-id="6b1fa-193">Presenter Interfaces</span></span>

<span data-ttu-id="6b1fa-194">Se requiere un presentador para implementar las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-194">A presenter is required to implement the following interfaces:</span></span>



| <span data-ttu-id="6b1fa-195">Interfaz</span><span class="sxs-lookup"><span data-stu-id="6b1fa-195">Interface</span></span>                                                                | <span data-ttu-id="6b1fa-196">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b1fa-196">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b1fa-197">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-197">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | <span data-ttu-id="6b1fa-198">Notifica al presentador cuando el reloj de EVR cambia de estado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-198">Notifies the presenter when the EVR's clock changes state.</span></span> <span data-ttu-id="6b1fa-199">Consulte [implementación de IMFClockStateSink](#implementing-imfclockstatesink).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-199">See [Implementing IMFClockStateSink](#implementing-imfclockstatesink).</span></span>                                   |
| [<span data-ttu-id="6b1fa-200">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-200">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | <span data-ttu-id="6b1fa-201">Proporciona una forma para que la aplicación y otros componentes de la canalización obtengan interfaces del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-201">Provides a way for the application and other components in the pipeline to get interfaces from the presenter.</span></span>                                                       |
| [<span data-ttu-id="6b1fa-202">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-202">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | <span data-ttu-id="6b1fa-203">Permite al presentador obtener interfaces de EVR o del mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-203">Enables the presenter to get interfaces from the EVR or the mixer.</span></span> <span data-ttu-id="6b1fa-204">Consulte [implementación de IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-204">See [Implementing IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span></span> |
| [<span data-ttu-id="6b1fa-205">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-205">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | <span data-ttu-id="6b1fa-206">Garantiza que el presentador y el mezclador usan tecnologías compatibles.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-206">Ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="6b1fa-207">Consulte [implementación de IMFVideoDeviceID](#implementing-imfvideodeviceid).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-207">See [Implementing IMFVideoDeviceID](#implementing-imfvideodeviceid).</span></span>                          |
| [<span data-ttu-id="6b1fa-208">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-208">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | <span data-ttu-id="6b1fa-209">Procesa los mensajes de EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-209">Processes messages from the EVR.</span></span> <span data-ttu-id="6b1fa-210">Consulte [implementación de IMFVideoPresenter](#implementing-imfvideopresenter).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-210">See [Implementing IMFVideoPresenter](#implementing-imfvideopresenter).</span></span>                                                             |



 

<span data-ttu-id="6b1fa-211">Las siguientes interfaces son opcionales:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-211">The following interfaces are optional:</span></span>



| <span data-ttu-id="6b1fa-212">Interfaz</span><span class="sxs-lookup"><span data-stu-id="6b1fa-212">Interface</span></span>                                                | <span data-ttu-id="6b1fa-213">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b1fa-213">Description</span></span>                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b1fa-214">**IEVRTrustedVideoPlugin**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-214">**IEVRTrustedVideoPlugin**</span></span>](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | <span data-ttu-id="6b1fa-215">Permite al presentador trabajar con medios protegidos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-215">Enables the presenter to work with protected media.</span></span> <span data-ttu-id="6b1fa-216">Implemente esta interfaz si el presentador es un componente de confianza diseñado para funcionar en la ruta de acceso a medios protegidos (PMP).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-216">Implement this interface if your presenter is a trusted component designed to work in the protected media path (PMP).</span></span> |
| [<span data-ttu-id="6b1fa-217">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-217">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | <span data-ttu-id="6b1fa-218">Indica el intervalo de velocidades de reproducción que admite el presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-218">Reports the range of playback rates that the presenter supports.</span></span> <span data-ttu-id="6b1fa-219">Consulte [implementación de IMFRateSupport](#implementing-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-219">See [Implementing IMFRateSupport](#implementing-imfratesupport).</span></span>                                         |
| [<span data-ttu-id="6b1fa-220">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-220">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | <span data-ttu-id="6b1fa-221">Asigna coordenadas del fotograma de vídeo de salida a las coordenadas del fotograma de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-221">Maps coordinates on the output video frame to coordinates on the input video frame.</span></span>                                                                                       |
| [<span data-ttu-id="6b1fa-222">**IQualProp**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-222">**IQualProp**</span></span>](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | <span data-ttu-id="6b1fa-223">Informa de la información de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-223">Reports performance information.</span></span> <span data-ttu-id="6b1fa-224">EVR usa esta información para la administración del control de calidad.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-224">The EVR uses this information for quality-control management.</span></span> <span data-ttu-id="6b1fa-225">Esta interfaz está documentada en el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-225">This interface is documented in the DirectShow SDK.</span></span>                        |



 

<span data-ttu-id="6b1fa-226">También puede proporcionar interfaces para que la aplicación se comunique con el presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-226">You can also provide interfaces for the application to communicate with the presenter.</span></span> <span data-ttu-id="6b1fa-227">El presentador estándar implementa la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) para este propósito.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-227">The standard presenter implements the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface for this purpose.</span></span> <span data-ttu-id="6b1fa-228">Puede implementar esta interfaz o definir la suya propia.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-228">You can implement this interface or define your own.</span></span> <span data-ttu-id="6b1fa-229">La aplicación obtiene las interfaces del presentador llamando a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-229">The application obtains interfaces from the presenter by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR.</span></span> <span data-ttu-id="6b1fa-230">Cuando se **MR_VIDEO_RENDER_SERVICE** el GUID de servicio, el EVR pasa la solicitud **GetService** al presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-230">When the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR passes the **GetService** request to the presenter.</span></span>

### <a name="implementing-imfvideodeviceid"></a><span data-ttu-id="6b1fa-231">Implementación de IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="6b1fa-231">Implementing IMFVideoDeviceID</span></span>

<span data-ttu-id="6b1fa-232">La interfaz [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contiene un método, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), que devuelve un GUID de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-232">The [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) interface contains one method, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), which returns a device GUID.</span></span> <span data-ttu-id="6b1fa-233">El GUID del dispositivo garantiza que el presentador y el mezclador usan tecnologías compatibles.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-233">The device GUID ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="6b1fa-234">Si los GUID del dispositivo no coinciden, el EVR no se puede inicializar.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-234">If the device GUIDs do not match, the EVR fails to initialize.</span></span>

<span data-ttu-id="6b1fa-235">El mezclador y el presentador estándar usan Direct3D 9, con el GUID de dispositivo igual a **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-235">The standard mixer and presenter both use Direct3D 9, with the device GUID equal to **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="6b1fa-236">Si piensa usar el presentador personalizado con el mezclador estándar, el GUID del dispositivo del presentador debe estar **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-236">If you intend to use your custom presenter with the standard mixer, the presenter's device GUID must be **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="6b1fa-237">Si reemplaza ambos componentes, podría definir un nuevo GUID de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-237">If you replace both components, you could define a new device GUID.</span></span> <span data-ttu-id="6b1fa-238">En el resto de este artículo, se supone que el presentador usa Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-238">For the remainder of this article, it is assumed that the presenter uses Direct3D 9.</span></span> <span data-ttu-id="6b1fa-239">Esta es la implementación estándar de [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span><span class="sxs-lookup"><span data-stu-id="6b1fa-239">Here is the standard implementation of [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span></span>


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



<span data-ttu-id="6b1fa-240">El método debe tener éxito incluso cuando se cierre el presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-240">The method should succeed even when the presenter is shut down.</span></span>

### <a name="implementing-imftopologyservicelookupclient"></a><span data-ttu-id="6b1fa-241">Implementación de IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="6b1fa-241">Implementing IMFTopologyServiceLookupClient</span></span>

<span data-ttu-id="6b1fa-242">La interfaz [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) permite al presentador obtener punteros de interfaz de EVR y del mezclador como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-242">The [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) interface enables the presenter to get interface pointers from the EVR and from the mixer as follows:</span></span>

1.  <span data-ttu-id="6b1fa-243">Cuando EVR inicializa el presentador, llama al método [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-243">When the EVR initializes the presenter, it calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="6b1fa-244">El argumento es un puntero a la interfaz [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) de EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-244">The argument is a pointer to the EVR's [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) interface.</span></span>
2.  <span data-ttu-id="6b1fa-245">El presentador llama a [**IMFTopologyServiceLookup:: LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) para obtener punteros de interfaz desde EVR o el mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-245">The presenter calls [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) to get interface pointers from either the EVR or the mixer.</span></span>

<span data-ttu-id="6b1fa-246">El método [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) es similar al método [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-246">The [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) method is similar to the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="6b1fa-247">Ambos métodos toman un GUID de servicio y un identificador de interfaz (IID) como entrada, pero **LookupService** devuelve una matriz de punteros de interfaz, mientras que **GetService** devuelve un solo puntero.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-247">Both methods take a service GUID and an interface identifier (IID) as input, but **LookupService** returns an array of interface pointers, while **GetService** returns a single pointer.</span></span> <span data-ttu-id="6b1fa-248">En la práctica, sin embargo, siempre puede establecer el tamaño de la matriz en 1.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-248">In practice, however, you can always set the array size to 1.</span></span> <span data-ttu-id="6b1fa-249">El objeto consultado depende del GUID del servicio:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-249">The object queried depends on the service GUID:</span></span>

-   <span data-ttu-id="6b1fa-250">Si se **MR_VIDEO_RENDER_SERVICE** el GUID de servicio, se consulta el EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-250">If the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR is queried.</span></span>
-   <span data-ttu-id="6b1fa-251">Si se **MR_VIDEO_MIXER_SERVICE** el GUID de servicio, se consulta el mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-251">If the service GUID is **MR_VIDEO_MIXER_SERVICE**, the mixer is queried.</span></span>

<span data-ttu-id="6b1fa-252">En la implementación de [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), obtenga las siguientes interfaces de EVR:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-252">In your implementation of [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), get the following interfaces from the EVR:</span></span>



| <span data-ttu-id="6b1fa-253">Interfaz EVR</span><span class="sxs-lookup"><span data-stu-id="6b1fa-253">EVR Interface</span></span>                                | <span data-ttu-id="6b1fa-254">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b1fa-254">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b1fa-255">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-255">**IMediaEventSink**</span></span>](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | <span data-ttu-id="6b1fa-256">Proporciona una manera para que el presentador envíe mensajes a EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-256">Provides a way for the presenter to send messages to the EVR.</span></span> <span data-ttu-id="6b1fa-257">Esta interfaz se define en el SDK de DirectShow, por lo que los mensajes siguen el patrón para los eventos de DirectShow, no Media Foundation eventos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-257">This interface is defined in the DirectShow SDK, so the messages follow the pattern for DirectShow events, not Media Foundation events.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="6b1fa-258">**IMFClock**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-258">**IMFClock**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | <span data-ttu-id="6b1fa-259">Representa el reloj de EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-259">Represents the EVR's clock.</span></span> <span data-ttu-id="6b1fa-260">El presentador usa esta interfaz para programar ejemplos de presentación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-260">The presenter uses this interface to schedule samples for presentation.</span></span> <span data-ttu-id="6b1fa-261">El EVR se puede ejecutar sin un reloj, por lo que es posible que esta interfaz no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-261">The EVR can run without a clock, so this interface might not be available.</span></span> <span data-ttu-id="6b1fa-262">Si no es así, omita el código de error de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-262">If not, ignore the error code from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span></span><br/> <span data-ttu-id="6b1fa-263">El reloj también implementa la interfaz [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-263">The clock also implements the [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) interface.</span></span> <span data-ttu-id="6b1fa-264">En la canalización de Media Foundation, el reloj implementa la interfaz [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-264">In the Media Foundation pipeline, the clock implements the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span> <span data-ttu-id="6b1fa-265">No implementa esta interfaz en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-265">It does not implement this interface in DirectShow.</span></span><br/> |



 

<span data-ttu-id="6b1fa-266">Obtenga las siguientes interfaces del mezclador:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-266">Get the following interfaces from the mixer:</span></span>



| <span data-ttu-id="6b1fa-267">Mezclador (interfaz)</span><span class="sxs-lookup"><span data-stu-id="6b1fa-267">Mixer Interface</span></span>                              | <span data-ttu-id="6b1fa-268">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b1fa-268">Description</span></span>                                                |
|----------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="6b1fa-269">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-269">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | <span data-ttu-id="6b1fa-270">Permite al presentador comunicarse con el mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-270">Enables the presenter to communicate with the mixer.</span></span>       |
| [<span data-ttu-id="6b1fa-271">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-271">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | <span data-ttu-id="6b1fa-272">Permite al presentador validar el GUID del dispositivo del mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-272">Enables the presenter to validate the mixer's device GUID.</span></span> |



 

<span data-ttu-id="6b1fa-273">El código siguiente implementa el método [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :</span><span class="sxs-lookup"><span data-stu-id="6b1fa-273">The following code implements the [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method :</span></span>


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



<span data-ttu-id="6b1fa-274">Cuando los punteros de interfaz obtenidos de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) ya no son válidos, el EVR llama a [**IMFTopologyServiceLookupClient:: ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-274">When the interface pointers obtained from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) are no longer valid, the EVR calls [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span></span> <span data-ttu-id="6b1fa-275">Dentro de este método, libere todos los punteros de interfaz y establezca el estado del presentador en Apagar:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-275">Inside this method, release all interface pointers and set the presenter state to shut down:</span></span>


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



<span data-ttu-id="6b1fa-276">EVR llama a [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) por diversos motivos, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-276">The EVR calls [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) for various reasons, including:</span></span>

-   <span data-ttu-id="6b1fa-277">Desconectar o volver a conectar los pin (DirectShow), o agregar o quitar receptores de secuencias (Media Foundation).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-277">Disconnecting or reconnecting pins (DirectShow), or adding or removing stream sinks (Media Foundation).</span></span>
-   <span data-ttu-id="6b1fa-278">Cambiando el formato.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-278">Changing format.</span></span>
-   <span data-ttu-id="6b1fa-279">Establecer un nuevo reloj.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-279">Setting a new clock.</span></span>
-   <span data-ttu-id="6b1fa-280">Cierre final de EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-280">Final shutdown of the EVR.</span></span>

<span data-ttu-id="6b1fa-281">Durante la vigencia del presentador, el EVR podría llamar varias veces a [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) y [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-281">During the lifetime of the presenter, the EVR might call [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) and [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) several times.</span></span>

### <a name="implementing-imfvideopresenter"></a><span data-ttu-id="6b1fa-282">Implementación de IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="6b1fa-282">Implementing IMFVideoPresenter</span></span>

<span data-ttu-id="6b1fa-283">La interfaz [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) hereda [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) y agrega dos métodos:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-283">The [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface inherits [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) and adds two methods:</span></span>



| <span data-ttu-id="6b1fa-284">Método</span><span class="sxs-lookup"><span data-stu-id="6b1fa-284">Method</span></span>                                                               | <span data-ttu-id="6b1fa-285">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b1fa-285">Description</span></span>                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="6b1fa-286">**GetCurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-286">**GetCurrentMediaType**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | <span data-ttu-id="6b1fa-287">Devuelve el tipo de medio de los fotogramas de vídeo compuestos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-287">Returns the media type of the composited video frames.</span></span> |
| [<span data-ttu-id="6b1fa-288">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-288">**ProcessMessage**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | <span data-ttu-id="6b1fa-289">Indica al presentador que realice varias acciones.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-289">Signals the presenter to perform various actions.</span></span>      |



 

<span data-ttu-id="6b1fa-290">El método [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) devuelve el tipo de medio del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-290">The [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) method returns the presenter's media type.</span></span> <span data-ttu-id="6b1fa-291">(Para obtener más información acerca de cómo establecer el tipo de medio, vea [negociar formatos](#negotiating-formats)). El tipo de medio se devuelve como un puntero de interfaz [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-291">(For details about setting the media type, see [Negotiating Formats](#negotiating-formats).) The media type is returned as an [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) interface pointer.</span></span> <span data-ttu-id="6b1fa-292">En el ejemplo siguiente se da por supuesto que el presentador almacena el tipo de medio como un puntero [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-292">The following example assumes that the presenter stores the media type as an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointer.</span></span> <span data-ttu-id="6b1fa-293">Para obtener la interfaz **IMFVideoMediaType** del tipo de archivo multimedia, llame a **QueryInterface**:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-293">To get the **IMFVideoMediaType** interface from the media type, call **QueryInterface**:</span></span>


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



<span data-ttu-id="6b1fa-294">El método [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) es el mecanismo principal para que EVR se comunique con el presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-294">The [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method is the primary mechanism for the EVR to communicate with the presenter.</span></span> <span data-ttu-id="6b1fa-295">Se definen los siguientes mensajes.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-295">The following messages are defined.</span></span> <span data-ttu-id="6b1fa-296">En el resto de este tema se proporcionan los detalles de la implementación de cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-296">The details of implementing each message are given in the remainder of this topic.</span></span>



| <span data-ttu-id="6b1fa-297">Message</span><span class="sxs-lookup"><span data-stu-id="6b1fa-297">Message</span></span>                                | <span data-ttu-id="6b1fa-298">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b1fa-298">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b1fa-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span></span> | <span data-ttu-id="6b1fa-300">El tipo de medio de salida del mezclador no es válido.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-300">The mixer's output media type is invalid.</span></span> <span data-ttu-id="6b1fa-301">El presentador debe negociar un nuevo tipo de medio con el mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-301">The presenter should negotiate a new media type with the mixer.</span></span> <span data-ttu-id="6b1fa-302">Vea [negociar formatos](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-302">See [Negotiating Formats](#negotiating-formats).</span></span>                                                                                         |
| <span data-ttu-id="6b1fa-303">**MFVP_MESSAGE_BEGINSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-303">**MFVP_MESSAGE_BEGINSTREAMING**</span></span>      | <span data-ttu-id="6b1fa-304">Se ha iniciado la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-304">Streaming has started.</span></span> <span data-ttu-id="6b1fa-305">Este mensaje no requiere ninguna acción concreta, pero se puede utilizar para asignar recursos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-305">No particular action is required by this message, but you can use it to allocate resources.</span></span>                                                                                                                                 |
| <span data-ttu-id="6b1fa-306">**MFVP_MESSAGE_ENDSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-306">**MFVP_MESSAGE_ENDSTREAMING**</span></span>        | <span data-ttu-id="6b1fa-307">La transmisión por secuencias ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-307">Streaming has ended.</span></span> <span data-ttu-id="6b1fa-308">Libere todos los recursos asignados en respuesta al mensaje de **MFVP_MESSAGE_BEGINSTREAMING** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-308">Release any resources that you allocated in response to the **MFVP_MESSAGE_BEGINSTREAMING** message.</span></span>                                                                                                                        |
| <span data-ttu-id="6b1fa-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span></span>  | <span data-ttu-id="6b1fa-310">El mezclador ha recibido una nueva muestra de entrada y es posible que pueda generar un nuevo fotograma de salida.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-310">The mixer has received a new input sample and might be able to generate a new output frame.</span></span> <span data-ttu-id="6b1fa-311">El presentador debe llamar a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-311">The presenter should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="6b1fa-312">Consulte [procesar la salida](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-312">See [Processing Output](#processing-output).</span></span> |
| <span data-ttu-id="6b1fa-313">**MFVP_MESSAGE_ENDOFSTREAM**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-313">**MFVP_MESSAGE_ENDOFSTREAM**</span></span>         | <span data-ttu-id="6b1fa-314">La presentación ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-314">The presentation has ended.</span></span> <span data-ttu-id="6b1fa-315">Vea [final de la secuencia](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-315">See [End of Stream](#end-of-stream).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="6b1fa-316">**MFVP_MESSAGE_FLUSH**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-316">**MFVP_MESSAGE_FLUSH**</span></span>               | <span data-ttu-id="6b1fa-317">EVR está vaciando los datos en su canalización de representación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-317">The EVR is flushing the data in its rendering pipeline.</span></span> <span data-ttu-id="6b1fa-318">El presentador debe descartar los fotogramas de vídeo programados para la presentación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-318">The presenter should discard any video frames that are scheduled for presentation.</span></span>                                                                                                         |
| <span data-ttu-id="6b1fa-319">**MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-319">**MFVP_MESSAGE_STEP**</span></span>                | <span data-ttu-id="6b1fa-320">Solicita al presentador que reenvíe N fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-320">Requests the presenter to step forward N frames.</span></span> <span data-ttu-id="6b1fa-321">El presentador debe descartar los siguientes N-1 fotogramas y mostrar el marco N.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-321">The presenter should discard the next N-1 frames and display the Nth frame.</span></span> <span data-ttu-id="6b1fa-322">Consulte [recorrido de fotogramas](#frame-stepping).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-322">See [Frame Stepping](#frame-stepping).</span></span>                                                                                |
| <span data-ttu-id="6b1fa-323">**MFVP_MESSAGE_CANCELSTEP**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-323">**MFVP_MESSAGE_CANCELSTEP**</span></span>          | <span data-ttu-id="6b1fa-324">Cancela la ejecución del fotograma.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-324">Cancels frame stepping.</span></span>                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a><span data-ttu-id="6b1fa-325">Implementación de IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="6b1fa-325">Implementing IMFClockStateSink</span></span>

<span data-ttu-id="6b1fa-326">El presentador debe implementar la interfaz [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) como parte de su implementación de [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), que hereda **IMFClockStateSink**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-326">The presenter must implement the [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) interface as part of its implementation of [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), which inherits **IMFClockStateSink**.</span></span> <span data-ttu-id="6b1fa-327">EVR usa esta interfaz para notificar al presentador cada vez que el reloj del EVR cambie de estado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-327">The EVR uses this interface to notify the presenter whenever the EVR's clock changes state.</span></span> <span data-ttu-id="6b1fa-328">Para obtener más información sobre los Estados de reloj, vea [reloj de presentación](presentation-clock.md).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-328">For more information about the clock states, see [Presentation Clock](presentation-clock.md).</span></span>

<span data-ttu-id="6b1fa-329">Estas son algunas directrices para implementar los métodos en esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-329">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="6b1fa-330">Se producirá un error en todos los métodos si se cierra el presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-330">All of the methods should fail if the presenter is shut down.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b1fa-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="6b1fa-332">Establezca el estado del presentador en iniciado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-332">Set the presenter state to started.</span></span></li>
<li><span data-ttu-id="6b1fa-333">Si <em>llClockStartOffset</em> no se <strong>PRESENTATION_CURRENT_POSITION</strong>, vacíe la cola de ejemplos del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-333">If the <em>llClockStartOffset</em> is not <strong>PRESENTATION_CURRENT_POSITION</strong>, flush the presenter's queue of samples.</span></span> <span data-ttu-id="6b1fa-334">(Esto equivale a recibir un mensaje <strong>MFVP_MESSAGE_FLUSH</strong> ).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-334">(This is equivalent to receiving an <strong>MFVP_MESSAGE_FLUSH</strong> message.)</span></span></li>
<li><span data-ttu-id="6b1fa-335">Si aún está pendiente una solicitud de paso de marco anterior, procese la solicitud (consulte <a href="#frame-stepping">ejecución de fotogramas</a>).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-335">If a previous frame-step request is still pending, process the request (see <a href="#frame-stepping">Frame Stepping</a>).</span></span> <span data-ttu-id="6b1fa-336">De lo contrario, intente procesar la salida del mezclador (consulte <a href="#processing-output">procesamiento de salida</a>.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-336">Otherwise, try to process output from the mixer (see <a href="#processing-output">Processing Output</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b1fa-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="6b1fa-338">Establezca el estado del presentador en detenido.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-338">Set the presenter state to stopped.</span></span></li>
<li><span data-ttu-id="6b1fa-339">Vacíe la cola de ejemplos del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-339">Flush the presenter's queue of samples.</span></span></li>
<li><span data-ttu-id="6b1fa-340">Cancele cualquier operación pendiente de paso de marco.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-340">Cancel any pending frame-step operation.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b1fa-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span></span></td>
<td><span data-ttu-id="6b1fa-342">Establezca el estado del presentador en pausado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-342">Set the presenter state to paused.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b1fa-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span></span></td>
<td><span data-ttu-id="6b1fa-344">Trate lo mismo que <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> pero no vacíe la cola de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-344">Treat the same as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> but do not flush the queue of samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b1fa-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="6b1fa-346">Si la velocidad cambia de cero a un valor distinto de cero, cancele el recorrido de los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-346">If the rate is changing from zero to nonzero, cancel frame stepping.</span></span></li>
<li><span data-ttu-id="6b1fa-347">Almacenar la nueva velocidad de reloj.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-347">Store the new clock rate.</span></span> <span data-ttu-id="6b1fa-348">La velocidad de reloj afecta a la presentación de los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-348">The clock rate affects when samples are presented.</span></span> <span data-ttu-id="6b1fa-349">Para obtener más información, vea <a href="#scheduling-samples">ejemplos de programación</a>.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-349">For more information, see <a href="#scheduling-samples">Scheduling Samples</a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a><span data-ttu-id="6b1fa-350">Implementación de IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="6b1fa-350">Implementing IMFRateSupport</span></span>

<span data-ttu-id="6b1fa-351">Para admitir velocidades de reproducción distintas de 1 × velocidad, el presentador debe implementar la interfaz [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-351">To support playback rates other than 1× speed, the presenter must implement the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface.</span></span> <span data-ttu-id="6b1fa-352">Estas son algunas directrices para implementar los métodos en esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-352">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="6b1fa-353">Se debe producir un error en todos los métodos después de apagar el presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-353">All of the methods should fail after the presenter is shut down.</span></span> <span data-ttu-id="6b1fa-354">Para obtener más información sobre esta interfaz, vea [control de tasa](rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-354">For more information about this interface, see [Rate Control](rate-control.md).</span></span>



|                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b1fa-355">**GetSlowestRate**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-355">**GetSlowestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | <span data-ttu-id="6b1fa-356">Devuelve cero para indicar que no hay ninguna velocidad mínima de reproducción.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-356">Return zero to indicate no minimum playback rate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="6b1fa-357">**GetFastestRate**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-357">**GetFastestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | <span data-ttu-id="6b1fa-358">En el caso de la reproducción no simplificada, la velocidad de reproducción no debe superar la frecuencia de actualización del monitor: frecuencia de actualización de *velocidad máxima*  =   (Hz)/ *velocidad de fotogramas de vídeo* (FPS).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-358">For non-thinned playback, the playback rate should not exceed the refresh rate of the monitor: *maximum rate* = *refresh rate* (Hz) / *video frame rate* (fps).</span></span> <span data-ttu-id="6b1fa-359">La velocidad de fotogramas de vídeo se especifica en el tipo de medio del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-359">The video frame rate is specified in the presenter's media type.</span></span> <br/> <span data-ttu-id="6b1fa-360">Para la reproducción simplificada, la velocidad de reproducción es ilimitada; Devuelve el valor **FLT_MAX**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-360">For thinned playback, the playback rate is unbounded; return the value **FLT_MAX**.</span></span> <span data-ttu-id="6b1fa-361">En la práctica, el origen y el descodificador serán los factores de limitación durante la reproducción simplificada.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-361">In practice, the source and the decoder will be the limiting factors during thinned playback.</span></span> <br/> <span data-ttu-id="6b1fa-362">Para la reproducción inversa, devuelva el valor negativo de la velocidad máxima.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-362">For reverse playback, return the negative of the maximum rate.</span></span><br/> |
| [<span data-ttu-id="6b1fa-363">**IsRateSupported**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-363">**IsRateSupported**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | <span data-ttu-id="6b1fa-364">Devuelve **MF_E_UNSUPPORTED_RATE** si el valor absoluto de *flRate* supera la velocidad de reproducción máxima del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-364">Return **MF_E_UNSUPPORTED_RATE** if the absolute value of *flRate* exceeds the presenter's maximum playback rate.</span></span> <span data-ttu-id="6b1fa-365">Calcule la velocidad de reproducción máxima tal y como se describe en [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-365">Calculate the maximum playback rate as described for [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span></span>                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="6b1fa-366">En el ejemplo siguiente se muestra cómo implementar el método [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) :</span><span class="sxs-lookup"><span data-stu-id="6b1fa-366">The following example shows how to implement the [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) method:</span></span>


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



<span data-ttu-id="6b1fa-367">En el ejemplo anterior se llama a un método auxiliar, GetMaxRate, para calcular la velocidad máxima de reproducción de avance:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-367">The previous example calls a helper method, GetMaxRate, to calculate the maximum forward playback rate:</span></span>

<span data-ttu-id="6b1fa-368">En el ejemplo siguiente se muestra cómo implementar el método [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) :</span><span class="sxs-lookup"><span data-stu-id="6b1fa-368">The following example shows how to implement the [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method:</span></span>


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



### <a name="sending-events-to-the-evr"></a><span data-ttu-id="6b1fa-369">Envío de eventos a EVR</span><span class="sxs-lookup"><span data-stu-id="6b1fa-369">Sending Events to the EVR</span></span>

<span data-ttu-id="6b1fa-370">El presentador debe notificar a EVR de varios eventos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-370">The presenter must notify the EVR of various events.</span></span> <span data-ttu-id="6b1fa-371">Para ello, usa la interfaz [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) de EVR, que se obtiene cuando EVR llama al método [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-371">To do so, it uses the EVR's [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) interface, obtained when the EVR calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="6b1fa-372">(La interfaz **IMediaEventSink** es originalmente una interfaz de DirectShow, pero se usa tanto en el EVR de DirectShow como en el Media Foundation). En el código siguiente se muestra cómo enviar un evento a EVR:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-372">(The **IMediaEventSink** interface is originally a DirectShow interface, but is used in both the DirectShow EVR and the Media Foundation.) The following code shows how to send an event to the EVR:</span></span>


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



<span data-ttu-id="6b1fa-373">En la tabla siguiente se enumeran los eventos que envía el presentador, junto con los parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-373">The following table lists the events that the presenter sends, along with the event parameters.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b1fa-374">Evento</span><span class="sxs-lookup"><span data-stu-id="6b1fa-374">Event</span></span></th>
<th><span data-ttu-id="6b1fa-375">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b1fa-375">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b1fa-376"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-376"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="6b1fa-377">El presentador ha finalizado la representación de todos los marcos después del mensaje de MFVP_MESSAGE_ENDOFSTREAM.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-377">The presenter has finished rendering all frames after the MFVP_MESSAGE_ENDOFSTREAM message.</span></span><br/>
<ul>
<li><span data-ttu-id="6b1fa-378"><em>Parám1</em>: HRESULT que indica el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-378"><em>Param1</em>: HRESULT indicating the status of the operation.</span></span></li>
<li><span data-ttu-id="6b1fa-379"><em>Parám2</em>: no se usa.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-379"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="6b1fa-380">Para obtener más información, vea <a href="#end-of-stream">final de la secuencia</a>.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-380">For more information, see <a href="#end-of-stream">End of Stream</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b1fa-381"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-381"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span></span></td>
<td><span data-ttu-id="6b1fa-382">El dispositivo Direct3D ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-382">The Direct3D device has changed.</span></span><br/>
<ul>
<li><span data-ttu-id="6b1fa-383"><em>Parám1</em>: no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-383"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="6b1fa-384"><em>Parám2</em>: no se usa.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-384"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="6b1fa-385">Para obtener más información, vea <a href="#managing-the-direct3d-device">administrar el dispositivo Direct3D</a>.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-385">For more information, see <a href="#managing-the-direct3d-device">Managing the Direct3D Device</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b1fa-386"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-386"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span></span></td>
<td><span data-ttu-id="6b1fa-387">Se ha producido un error que requiere que se detenga la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-387">An error has occurred that requires streaming to stop.</span></span><br/>
<ul>
<li><span data-ttu-id="6b1fa-388"><em>Parám1</em>: <strong>HRESULT</strong> que indica el error que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-388"><em>Param1</em>: <strong>HRESULT</strong> indicating the error that occurred.</span></span></li>
<li><span data-ttu-id="6b1fa-389"><em>Parám2</em>: no se usa.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-389"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b1fa-390"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-390"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="6b1fa-391">Especifica la cantidad de tiempo que tarda el presentador en representar cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-391">Specifies the amount of time that the presenter is taking to render each frame.</span></span> <span data-ttu-id="6b1fa-392">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-392">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="6b1fa-393"><em>Parám1</em>: puntero a un valor de <strong>LONGLONG</strong> constante que contiene la cantidad de tiempo que se va a procesar el marco, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-393"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the amount of time to process the frame, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="6b1fa-394"><em>Parám2</em>: no se usa.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-394"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="6b1fa-395">Para obtener más información, vea <a href="#processing-output">procesar la salida</a>.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-395">For more information, see <a href="#processing-output">Processing Output</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b1fa-396"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-396"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="6b1fa-397">Especifica el tiempo de retraso actual en los ejemplos de representación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-397">Specifies the current lag time in rendering samples.</span></span> <span data-ttu-id="6b1fa-398">Si el valor es positivo, los ejemplos están detrás de la programación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-398">If the value is positive, samples are behind schedule.</span></span> <span data-ttu-id="6b1fa-399">Si el valor es negativo, los ejemplos están por encima de la programación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-399">If the value is negative, samples are ahead of schedule.</span></span> <span data-ttu-id="6b1fa-400">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-400">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="6b1fa-401"><em>Parám1</em>: puntero a un valor de <strong>LONGLONG</strong> constante que contiene el tiempo de retardo, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-401"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the lag time, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="6b1fa-402"><em>Parám2</em>: no se usa.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-402"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b1fa-403"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-403"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span></span></td>
<td><span data-ttu-id="6b1fa-404">Se envía inmediatamente después de <strong>EC_STEP_COMPLETE</strong> si la velocidad de reproducción es cero.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-404">Sent immediately after <strong>EC_STEP_COMPLETE</strong> if the playback rate is zero.</span></span> <span data-ttu-id="6b1fa-405">Este evento contiene la marca de tiempo del marco que se mostró.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-405">This event contains the time stamp of the frame that was displayed.</span></span><br/>
<ul>
<li><span data-ttu-id="6b1fa-406"><em>Parám1</em>: menos 32 bits de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-406"><em>Param1</em>: Lower 32 bits of the time stamp.</span></span></li>
<li><span data-ttu-id="6b1fa-407"><em>Parám2</em>: los 32 bits superiores de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-407"><em>Param2</em>: Upper 32 bits of the time stamp.</span></span></li>
</ul>
<span data-ttu-id="6b1fa-408">Para obtener más información, consulte <a href="#frame-stepping">recorrido de fotogramas</a>.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-408">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b1fa-409"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b1fa-409"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="6b1fa-410">El presentador ha completado o cancelado un paso del marco.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-410">The presenter has completed or canceled a frame step.</span></span><br/>
<ul>
<li><span data-ttu-id="6b1fa-411"><em>Parám1</em>: no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-411"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="6b1fa-412"><em>Parám2</em>: no se usa.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-412"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="6b1fa-413">Para obtener más información, consulte <a href="#frame-stepping">recorrido de fotogramas</a>.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-413">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6b1fa-414">Una versión anterior de la documentación que se describe en <em>parám1</em> incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-414">A previous version of the documentation described <em>Param1</em> incorrectly.</span></span> <span data-ttu-id="6b1fa-415">Este parámetro no se utiliza para este evento.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-415">This parameter is not used for this event.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a><span data-ttu-id="6b1fa-416">Formatos de negociación</span><span class="sxs-lookup"><span data-stu-id="6b1fa-416">Negotiating Formats</span></span>

<span data-ttu-id="6b1fa-417">Siempre que el presentador recibe un mensaje **MFVP_MESSAGE_INVALIDATEMEDIATYPE** de EVR, debe establecer el formato de salida en el mezclador, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-417">Whenever the presenter receives an **MFVP_MESSAGE_INVALIDATEMEDIATYPE** message from the EVR, it must set the output format on the mixer, as follows:</span></span>

1.  <span data-ttu-id="6b1fa-418">Llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) en el mezclador para obtener un tipo de resultado posible.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-418">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) on the mixer to get a possible output type.</span></span> <span data-ttu-id="6b1fa-419">Este tipo describe un formato que el mezclador puede producir en función de los flujos de entrada y las capacidades de procesamiento de vídeo del dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-419">This type describes a format that the mixer can produce given the input streams and the video processing capabilities of the graphics device.</span></span>
2.  <span data-ttu-id="6b1fa-420">Compruebe si el presentador puede utilizar este tipo de medio como su formato de representación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-420">Check whether the presenter can use this media type as its rendering format.</span></span> <span data-ttu-id="6b1fa-421">Estos son algunos aspectos que se deben comprobar, aunque la implementación puede tener sus propios requisitos:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-421">Here are some things to check, although your implementation might have its own requirements:</span></span>

    -   <span data-ttu-id="6b1fa-422">El vídeo se debe descomprimir.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-422">The video must be uncompressed.</span></span>
    -   <span data-ttu-id="6b1fa-423">El vídeo solo debe tener tramas progresivas.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-423">The video must have progressive frames only.</span></span> <span data-ttu-id="6b1fa-424">Compruebe que el atributo [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) sea igual a **MFVideoInterlace_Progressive**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-424">Check that the [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) attribute equals **MFVideoInterlace_Progressive**.</span></span>
    -   <span data-ttu-id="6b1fa-425">El formato debe ser compatible con el dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-425">The format must be compatible with the Direct3D device.</span></span>

    <span data-ttu-id="6b1fa-426">Si el tipo no es aceptable, vuelva al paso 1 y obtenga el siguiente tipo propuesto del mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-426">If the type is not acceptable, return to step 1 and get the mixer's next proposed type.</span></span>

3.  <span data-ttu-id="6b1fa-427">Cree un nuevo tipo de medio que sea un clon del tipo original y, a continuación, cambie los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-427">Create a new media type that is a clone of the original type and then change the following attributes:</span></span>

    -   <span data-ttu-id="6b1fa-428">Establezca el atributo de [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) igual que el ancho y el alto que desee para las superficies de Direct3D que va a asignar.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-428">Set the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute equal to the width and height that you want for the Direct3D surfaces you will allocate.</span></span>
    -   <span data-ttu-id="6b1fa-429">Establezca el atributo [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) en **false**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-429">Set the [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **FALSE**.</span></span>
    -   <span data-ttu-id="6b1fa-430">Establezca el atributo [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) igual que el par de la pantalla (normalmente 1:1).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-430">Set the [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute equal to the PAR of the display (typically 1:1).</span></span>
    -   <span data-ttu-id="6b1fa-431">Establezca la abertura geométrica ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) atributo) igual a un rectángulo dentro de la superficie de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-431">Set the geometric aperture ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) attribute) equal to a rectangle within the Direct3D surface.</span></span> <span data-ttu-id="6b1fa-432">Cuando el mezclador genera un fotograma de salida, blits la imagen de origen en este rectángulo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-432">When the mixer generates an output frame, it blits the source image onto this rectangle.</span></span> <span data-ttu-id="6b1fa-433">La abertura geométrica puede ser tan grande como la superficie o puede ser un subrectángulo dentro de la superficie.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-433">The geometric aperture can be as large as the surface, or it can be a subrectangle within the surface.</span></span> <span data-ttu-id="6b1fa-434">Para obtener más información, vea [rectángulos de origen y de destino](#source-and-destination-rectangles).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-434">For more information, see [Source and Destination Rectangles](#source-and-destination-rectangles).</span></span>

4.  <span data-ttu-id="6b1fa-435">Para probar si el mezclador va a aceptar el tipo de salida modificado, llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) con la marca **MFT_SET_TYPE_TEST_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-435">To test whether the mixer will accept the modified output type, call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with the **MFT_SET_TYPE_TEST_ONLY** flag.</span></span> <span data-ttu-id="6b1fa-436">Si el mezclador rechaza el tipo, vuelva al paso 1 y obtenga el siguiente tipo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-436">If the mixer rejects the type, go back to step 1 and get the next type.</span></span>
5.  <span data-ttu-id="6b1fa-437">Asigne un grupo de superficies de Direct3D, tal como se describe en [asignación de superficies de Direct3D](#allocating-direct3d-surfaces).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-437">Allocate a pool of Direct3D surfaces, as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="6b1fa-438">El mezclador usará estas superficies cuando dibuje los fotogramas de vídeo compuestos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-438">The mixer will use these surfaces when it draws the composited video frames.</span></span>
6.  <span data-ttu-id="6b1fa-439">Establezca el tipo de salida en el mezclador llamando a [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sin marcas.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-439">Set the output type on the mixer by calling [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with no flags.</span></span> <span data-ttu-id="6b1fa-440">Si la primera llamada a **SetOutputType** se realizó correctamente en el paso 4, el método debería volver a tener éxito.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-440">If the first call to **SetOutputType** succeeded in step 4, the method should succeed again.</span></span>

<span data-ttu-id="6b1fa-441">Si el mezclador se queda sin tipos, el método [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) devuelve **MF_E_NO_MORE_TYPES**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-441">If the mixer runs out of types, the [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method returns **MF_E_NO_MORE_TYPES**.</span></span> <span data-ttu-id="6b1fa-442">Si el presentador no encuentra un tipo de salida adecuado para el mezclador, no se puede representar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-442">If the presenter cannot find a suitable output type for the mixer, the stream cannot be rendered.</span></span> <span data-ttu-id="6b1fa-443">En ese caso, DirectShow o Media Foundation podrían intentar otro formato de secuencia.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-443">In that case, DirectShow or Media Foundation might try another stream format.</span></span> <span data-ttu-id="6b1fa-444">Por consiguiente, el presentador podría recibir varios mensajes de **MFVP_MESSAGE_INVALIDATEMEDIATYPE** en una fila hasta que se encuentre un tipo válido.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-444">Therefore, the presenter might receive several **MFVP_MESSAGE_INVALIDATEMEDIATYPE** messages in a row until a valid type is found.</span></span>

<span data-ttu-id="6b1fa-445">El mezclador realiza automáticamente la panorámica del vídeo, teniendo en cuenta la relación de aspecto de píxeles (PAR) del origen y el destino.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-445">The mixer automatically letterboxes the video, taking into account the pixel aspect ratio (PAR) of the source and destination.</span></span> <span data-ttu-id="6b1fa-446">Para obtener los mejores resultados, el ancho y el alto de la superficie y la abertura geométrica deben ser iguales al tamaño real en el que desea que aparezca el vídeo en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-446">For best results, the surface width and height and the geometric aperture should be equal to the actual size that you want the video to appear on the display.</span></span> <span data-ttu-id="6b1fa-447">En la imagen siguiente se ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-447">The following image illustrates this process.</span></span>

![diagrama que muestra un fotogramas compuesto que conduce a una superficie de Direct3D, que conduce a una ventana](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

<span data-ttu-id="6b1fa-449">En el código siguiente se muestra el esquema del proceso.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-449">The following code shows the outline of the process.</span></span> <span data-ttu-id="6b1fa-450">Algunos de los pasos se colocan en funciones auxiliares, los detalles exactos de los cuales dependerán de los requisitos del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-450">Some of the steps are placed in helper functions, the exact details of which will depend on the requirements of your presenter.</span></span>


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



<span data-ttu-id="6b1fa-451">Para obtener más información sobre los tipos de medios de vídeo, consulte [tipos de medios de vídeo](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-451">For more information about video media types, see [Video Media Types](video-media-types.md).</span></span>

## <a name="managing-the-direct3d-device"></a><span data-ttu-id="6b1fa-452">Administrar el dispositivo Direct3D</span><span class="sxs-lookup"><span data-stu-id="6b1fa-452">Managing the Direct3D Device</span></span>

<span data-ttu-id="6b1fa-453">El presentador crea el dispositivo Direct3D y controla cualquier pérdida de dispositivo durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-453">The presenter creates the Direct3D device and handles any device loss during streaming.</span></span> <span data-ttu-id="6b1fa-454">El presentador también hospeda el administrador de dispositivos de Direct3D, que proporciona una manera para que otros componentes usen el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-454">The presenter also hosts the Direct3D device manager, which provides a way for other components to use the same device.</span></span> <span data-ttu-id="6b1fa-455">Por ejemplo, el mezclador usa el dispositivo Direct3D para mezclar subsecuencias, Desentrelazar y realizar ajustes de color.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-455">For example, the mixer uses the Direct3D device to mix substreams, deinterlace, and perform color adjustments.</span></span> <span data-ttu-id="6b1fa-456">Los descodificadores pueden usar el dispositivo Direct3D para la descodificación acelerada en vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-456">Decoders can use the Direct3D device for video-accelerated decoding.</span></span> <span data-ttu-id="6b1fa-457">(Para obtener más información sobre la aceleración de vídeo, consulte [aceleración de vídeo de DirectX 2,0](directx-video-acceleration-2-0.md)).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-457">(For more information about video acceleration, see [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).)</span></span>

<span data-ttu-id="6b1fa-458">Para configurar el dispositivo Direct3D, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-458">To set up the Direct3D device, perform the following steps:</span></span>

1.  <span data-ttu-id="6b1fa-459">Cree el objeto de Direct3D mediante una llamada a **Direct3DCreate9** o **Direct3DCreate9Ex**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-459">Create the Direct3D object by calling **Direct3DCreate9** or **Direct3DCreate9Ex**.</span></span>
2.  <span data-ttu-id="6b1fa-460">Cree el dispositivo mediante una llamada a **IDirect3D9:: CreateDevice** o **IDirect3D9Ex:: CreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-460">Create the device by calling **IDirect3D9::CreateDevice** or **IDirect3D9Ex::CreateDevice**.</span></span>
3.  <span data-ttu-id="6b1fa-461">Cree el administrador de dispositivos mediante una llamada a [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-461">Create the device manager by calling [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span>
4.  <span data-ttu-id="6b1fa-462">Establezca el dispositivo en el administrador de dispositivos mediante una llamada a [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-462">Set the device on the device manager by calling [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span>

<span data-ttu-id="6b1fa-463">Si otro componente de canalización necesita el administrador de dispositivos, llama a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el EVR, especificando **MR_VIDEO_ACCELERATION_SERVICE** para el GUID de servicio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-463">If another pipeline component needs the device manager, it calls [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR, specifying **MR_VIDEO_ACCELERATION_SERVICE** for the service GUID.</span></span> <span data-ttu-id="6b1fa-464">EVR pasa la solicitud al presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-464">The EVR passes the request to the presenter.</span></span> <span data-ttu-id="6b1fa-465">Una vez que el objeto obtiene el puntero [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) , puede obtener un identificador para el dispositivo mediante una llamada a [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-465">After the object gets the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) pointer, it can get a handle to the device by calling [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span></span> <span data-ttu-id="6b1fa-466">Cuando el objeto necesita usar el dispositivo, pasa el identificador del dispositivo al método [**IDirect3DDeviceManager9:: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) , que devuelve un puntero **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-466">When the object needs to use the device, it passes the device handle to the [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method, which returns an **IDirect3DDevice9** pointer.</span></span>

<span data-ttu-id="6b1fa-467">Una vez creado el dispositivo, si el presentador destruye el dispositivo y crea uno nuevo, el presentador debe volver a llamar a [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-467">After the device is created, if the presenter destroys the device and creates a new one, the presenter must call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) again.</span></span> <span data-ttu-id="6b1fa-468">El método **ResetDevice** invalida todos los identificadores de dispositivo existentes, lo que hace que [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) devuelva **DXVA2_E_NEW_VIDEO_DEVICE**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-468">The **ResetDevice** method invalidates any existing device handles, which causes [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) to return **DXVA2_E_NEW_VIDEO_DEVICE**.</span></span> <span data-ttu-id="6b1fa-469">Este código de error señala a otros objetos mediante el dispositivo que deben abrir un nuevo identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-469">This error code signals to other objects using the device that they should open a new device handle.</span></span> <span data-ttu-id="6b1fa-470">Para obtener más información acerca del uso del administrador de dispositivos, consulte [Direct3D administrador de dispositivos](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-470">For more information about using the device manager, see [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="6b1fa-471">El presentador puede crear el dispositivo en modo de ventana o en modo exclusivo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-471">The presenter can create the device in windowed mode or full-screen exclusive mode.</span></span> <span data-ttu-id="6b1fa-472">En el modo de ventana, debe proporcionar una forma para que la aplicación especifique la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-472">For windowed mode, you should provide a way for the application to specify the video window.</span></span> <span data-ttu-id="6b1fa-473">El presentador estándar implementa el método [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) para este propósito.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-473">The standard presenter implements the [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) method for this purpose.</span></span> <span data-ttu-id="6b1fa-474">Debe crear el dispositivo cuando el presentador se cree por primera vez.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-474">You must create the device when the presenter is first created.</span></span> <span data-ttu-id="6b1fa-475">Normalmente, no se sabrán todos los parámetros de dispositivo en este momento, como el formato de ventana o de búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-475">Typically, you won't know all of the device parameters at this time, such as the window or the back buffer format.</span></span> <span data-ttu-id="6b1fa-476">Puede crear un dispositivo temporal y reemplazarlo más tarde&\# ; simplemente Recuerde llamar a [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) en el administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-476">You can create a temporary device and replace it later&\#;just remember to call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) on the device manager.</span></span>

<span data-ttu-id="6b1fa-477">Si crea un nuevo dispositivo, o si llama a **IDirect3DDevice9:: RESET** o **IDirect3DDevice9Ex:: ResetEx** en un dispositivo existente, envíe un evento [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) a EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-477">If you create a new device, or if you call **IDirect3DDevice9::Reset** or **IDirect3DDevice9Ex::ResetEx** on an existing device, send an [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) event to the EVR.</span></span> <span data-ttu-id="6b1fa-478">Este evento notifica a EVR que vuelva a negociar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-478">This event notifies the EVR to renegotiate the media type.</span></span> <span data-ttu-id="6b1fa-479">EVR omite los parámetros de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-479">The EVR ignores the event parameters for this event.</span></span>

### <a name="allocating-direct3d-surfaces"></a><span data-ttu-id="6b1fa-480">Asignación de superficies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="6b1fa-480">Allocating Direct3D Surfaces</span></span>

<span data-ttu-id="6b1fa-481">Después de que el presentador establezca el tipo de medio, puede asignar las superficies de Direct3D, que el mezclador usará para escribir los fotogramas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-481">After the presenter sets the media type, it can allocate the Direct3D surfaces, which the mixer will use to write the video frames.</span></span> <span data-ttu-id="6b1fa-482">La superficie debe coincidir con el tipo de medio del presentador:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-482">The surface must match the presenter's media type:</span></span>

-   <span data-ttu-id="6b1fa-483">El formato de superficie debe coincidir con el subtipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-483">The surface format must match the media subtype.</span></span> <span data-ttu-id="6b1fa-484">Por ejemplo, si el subtipo es **MFVideoFormat_RGB24**, el formato de la superficie debe ser **D3DFMT_X8R8G8B8**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-484">For example, if the subtype is **MFVideoFormat_RGB24**, the surface format must be **D3DFMT_X8R8G8B8**.</span></span> <span data-ttu-id="6b1fa-485">Para obtener más información sobre los subtipos y los formatos de Direct3D, vea [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-485">For more information about subtypes and Direct3D formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="6b1fa-486">El ancho y el alto de la superficie deben coincidir con las dimensiones especificadas en el atributo [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-486">The surface width and height must match the dimensions given in the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute of the media type.</span></span>

<span data-ttu-id="6b1fa-487">La manera recomendada de asignar superficies depende de si el presentador se ejecuta en ventana o en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-487">The recommended way to allocate surfaces depends on whether the presenter runs windowed or full-screen.</span></span>

<span data-ttu-id="6b1fa-488">Si el dispositivo Direct3D está en la ventana, puede crear varias cadenas de intercambio, cada una con un solo búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-488">If the Direct3D device is windowed, you can create several swap chains, each with a single back buffer.</span></span> <span data-ttu-id="6b1fa-489">Con este enfoque, puede presentar cada superficie de forma independiente, ya que la presentación de una cadena de intercambio no interferirá con las demás cadenas de intercambio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-489">Using this approach, you can present each surface independently, because presenting one swap chain will not interfere with the other swap chains.</span></span> <span data-ttu-id="6b1fa-490">El mezclador puede escribir datos en una superficie mientras otra superficie está programada para la presentación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-490">The mixer can write data to a surface while another surface is scheduled for presentation.</span></span>

<span data-ttu-id="6b1fa-491">En primer lugar, decida cuántas cadenas de intercambio desea crear.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-491">First, decide how many swap chains to create.</span></span> <span data-ttu-id="6b1fa-492">Se recomienda un mínimo de tres.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-492">A minimum of three is recommended.</span></span> <span data-ttu-id="6b1fa-493">Para cada cadena de intercambio, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-493">For each swap chain, do the following:</span></span>

1.  <span data-ttu-id="6b1fa-494">Llame a **IDirect3DDevice9:: CreateAdditionalSwapChain** para crear la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-494">Call **IDirect3DDevice9::CreateAdditionalSwapChain** to create the swap chain.</span></span>
2.  <span data-ttu-id="6b1fa-495">Llame a **IDirect3DSwapChain9:: GetBackBuffer** para obtener un puntero a la superficie del búfer de reserva de la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-495">Call **IDirect3DSwapChain9::GetBackBuffer** to get a pointer to the swap chain's back buffer surface.</span></span>
3.  <span data-ttu-id="6b1fa-496">Llame a [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) y pase un puntero a la superficie.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-496">Call [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) and pass in a pointer to the surface.</span></span> <span data-ttu-id="6b1fa-497">Esta función devuelve un puntero a un objeto de ejemplo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-497">This function returns a pointer to a video sample object.</span></span> <span data-ttu-id="6b1fa-498">El objeto de ejemplo de vídeo implementa la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) y el presentador usa esta interfaz para proporcionar la superficie al mezclador cuando el presentador llama al método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) de mixer.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-498">The video sample object implements the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, and the presenter uses this interface to deliver the surface to the mixer when the presenter calls the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="6b1fa-499">Para obtener más información sobre el objeto de ejemplo de vídeo, consulte [ejemplos de vídeo](video-samples.md).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-499">For more information about the video sample object, see [Video Samples](video-samples.md).</span></span>
4.  <span data-ttu-id="6b1fa-500">Almacene el puntero [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) en una cola.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-500">Store the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer in a queue.</span></span> <span data-ttu-id="6b1fa-501">El presentador extraerá ejemplos de esta cola durante el procesamiento, tal y como se describe en [procesamiento de salida](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-501">The presenter will pull samples from this queue during processing as described in [Processing Output](#processing-output).</span></span>
5.  <span data-ttu-id="6b1fa-502">Mantenga una referencia al puntero **IDirect3DSwapChain9** para que no se libere la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-502">Keep a reference to the **IDirect3DSwapChain9** pointer so the swap chain is not released.</span></span>

<span data-ttu-id="6b1fa-503">En el modo exclusivo de pantalla completa, el dispositivo no puede tener más de una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-503">In full-screen exclusive mode, the device cannot have more than one swap chain.</span></span> <span data-ttu-id="6b1fa-504">Esta cadena de intercambio se crea implícitamente cuando se crea el dispositivo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-504">This swap chain is created implicitly when you create the full-screen device.</span></span> <span data-ttu-id="6b1fa-505">La cadena de intercambio puede tener más de un búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-505">The swap chain can have more than one back buffer.</span></span> <span data-ttu-id="6b1fa-506">Desafortunadamente, sin embargo, si presenta un búfer de reserva mientras escribe en otro búfer de reserva en la misma cadena de intercambio, no hay ninguna manera fácil de coordinar las dos operaciones.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-506">Unfortunately, however, if you present one back buffer while you write to another back buffer in the same swap chain, there is no easy way to coordinate the two operations.</span></span> <span data-ttu-id="6b1fa-507">Esto se debe a la manera en que Direct3D implementa el volteo de la superficie.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-507">This is because of the way Direct3D implements surface flipping.</span></span> <span data-ttu-id="6b1fa-508">Cuando se llama a Present, el controlador de gráficos actualiza los punteros de la superficie en la memoria de gráficos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-508">When you call Present, the graphics driver updates the surface pointers in graphics memory.</span></span> <span data-ttu-id="6b1fa-509">Si está manteniendo los punteros de **IDirect3DSurface9** al llamar a **present**, apuntarán a distintos búferes después de que se devuelva la llamada **actual** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-509">If you are holding any **IDirect3DSurface9** pointers when you call **Present**, they will point to different buffers after the **Present** call returns.</span></span>

<span data-ttu-id="6b1fa-510">La opción más sencilla consiste en crear un ejemplo de vídeo para la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-510">The simplest option is to create one video sample for the swap chain.</span></span> <span data-ttu-id="6b1fa-511">Si elige esta opción, siga los mismos pasos indicados para el modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-511">If you choose this option, follow the same steps given for windowed mode.</span></span> <span data-ttu-id="6b1fa-512">La única diferencia es que la cola de ejemplo contiene una sola muestra de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-512">The only difference is that the sample queue contains a single video sample.</span></span> <span data-ttu-id="6b1fa-513">Otra opción consiste en crear superficies ocultas y, a continuación, transformarlas en el búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-513">Another option is to create offscreen surfaces and then blit them to the back buffer.</span></span> <span data-ttu-id="6b1fa-514">Las superficies que cree deben admitir el método [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) , que el mezclador usa para componer los fotogramas de salida.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-514">The surfaces that you create must support the [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method, which the mixer uses to composite the output frames.</span></span>

### <a name="tracking-samples"></a><span data-ttu-id="6b1fa-515">Ejemplos de seguimiento</span><span class="sxs-lookup"><span data-stu-id="6b1fa-515">Tracking Samples</span></span>

<span data-ttu-id="6b1fa-516">Cuando el presentador asigna primero los ejemplos de vídeo, los coloca en una cola.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-516">When the presenter first allocates the video samples, it places them in a queue.</span></span> <span data-ttu-id="6b1fa-517">El presentador dibuja desde esta cola cada vez que necesita obtener un nuevo fotograma del mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-517">The presenter draws from this queue whenever it needs to get a new frame from the mixer.</span></span> <span data-ttu-id="6b1fa-518">Una vez que el mezclador envía el fotograma, el presentador mueve el ejemplo a una segunda cola.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-518">After the mixer outputs the frame, the presenter moves the sample into a second queue.</span></span> <span data-ttu-id="6b1fa-519">La segunda cola es para los ejemplos que están a la espera de los tiempos de presentación programados.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-519">The second queue is for samples that are waiting for their scheduled presentation times.</span></span>

<span data-ttu-id="6b1fa-520">Para facilitar el seguimiento del estado de cada ejemplo, el objeto de ejemplo de vídeo implementa la interfaz [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-520">To make it easier to track the status of each sample, the video sample object implements the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span> <span data-ttu-id="6b1fa-521">Puede usar esta interfaz como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-521">You can use this interface as follows:</span></span>

1.  <span data-ttu-id="6b1fa-522">Implemente la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) en el presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-522">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface in your presenter.</span></span>
2.  <span data-ttu-id="6b1fa-523">Antes de colocar un ejemplo en la cola programada, consulte el objeto de ejemplo de vídeo para la interfaz [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-523">Before you place a sample in the scheduled queue, query the video sample object for the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span>

3.  <span data-ttu-id="6b1fa-524">Llame a [**IMFTrackedSample:: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) con un puntero a la interfaz de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-524">Call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) with a pointer to your callback interface.</span></span>
4.  <span data-ttu-id="6b1fa-525">Cuando el ejemplo esté listo para su presentación, quítelo de la cola programada, preséntela y suelte todas las referencias al ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-525">When the sample is ready for presentation, remove it from the scheduled queue, present it, and release all references to the sample.</span></span>
5.  <span data-ttu-id="6b1fa-526">En el ejemplo se invoca la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-526">The sample invokes the callback.</span></span> <span data-ttu-id="6b1fa-527">(El objeto de ejemplo no se elimina en este caso porque contiene un recuento de referencias en sí mismo hasta que se invoca la devolución de llamada).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-527">(The sample object is not deleted in this case because it holds a reference count on itself until the callback is invoked.)</span></span>
6.  <span data-ttu-id="6b1fa-528">Dentro de la devolución de llamada, devuelva el ejemplo a la cola disponible.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-528">Inside the callback, return the sample to the available queue.</span></span>

<span data-ttu-id="6b1fa-529">No es necesario que un presentador use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) para realizar un seguimiento de los ejemplos; puede implementar cualquier técnica que funcione mejor para el diseño.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-529">A presenter is not required to use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) to track samples; you can implement any technique that works best for your design.</span></span> <span data-ttu-id="6b1fa-530">Una ventaja de **IMFTrackedSample** es que puede trasladar las funciones de programación y representación del presentador a objetos auxiliares, y estos objetos no necesitan ningún mecanismo especial para volver a llamar al presentador cuando lanzan muestras de vídeo, ya que el objeto de ejemplo proporciona ese mecanismo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-530">One advantage of **IMFTrackedSample** is that you can move the presenter's scheduling and rendering functions into helper objects, and these objects do not need any special mechanism for calling back to the presenter when they release video samples because the sample object provides that mechanism.</span></span>

<span data-ttu-id="6b1fa-531">En el código siguiente se muestra cómo establecer la devolución de llamada:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-531">The following code shows how to set the callback:</span></span>


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



<span data-ttu-id="6b1fa-532">En la devolución de llamada, llame a [**IMFAsyncResult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) en el objeto de resultado asincrónico para recuperar un puntero al ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-532">In the callback, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) on the asynchronous result object to retrieve a pointer to the sample:</span></span>


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

    /*** Begin lock **_/

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

    /_*_ End lock _*_/

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



## <a name="processing-output"></a><span data-ttu-id="6b1fa-533">Procesar la salida</span><span class="sxs-lookup"><span data-stu-id="6b1fa-533">Processing Output</span></span>

<span data-ttu-id="6b1fa-534">Siempre que el mezclador recibe un nuevo ejemplo de entrada, el EVR envía un mensaje _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY*\* al presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-534">Whenever the mixer receives a new input sample, the EVR sends an _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY*\* message to the presenter.</span></span> <span data-ttu-id="6b1fa-535">Este mensaje indica que el mezclador podría tener un nuevo fotograma de vídeo para entregarlo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-535">This message indicates that the mixer might have a new video frame to deliver.</span></span> <span data-ttu-id="6b1fa-536">En respuesta, el presentador llama a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-536">In response, the presenter calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="6b1fa-537">Si el método se ejecuta correctamente, el presentador programa el ejemplo para la presentación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-537">If the method succeeds, the presenter schedules the sample for presentation.</span></span>

<span data-ttu-id="6b1fa-538">Para obtener la salida del mezclador, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-538">To get output from the mixer, perform the following steps:</span></span>

1.  <span data-ttu-id="6b1fa-539">Compruebe el estado del reloj.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-539">Check the clock state.</span></span> <span data-ttu-id="6b1fa-540">Si el reloj está en pausa, pase por alto el mensaje de **MFVP_MESSAGE_PROCESSINPUTNOTIFY** a menos que sea el primer fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-540">If the clock is paused, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message unless this is the first video frame.</span></span> <span data-ttu-id="6b1fa-541">Si el reloj se está ejecutando, o si se trata del primer fotograma de vídeo, continúe.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-541">If the clock is running, or if this is the first video frame, continue.</span></span>
2.  <span data-ttu-id="6b1fa-542">Obtener un ejemplo de la cola de ejemplos disponibles.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-542">Get a sample from the queue of available samples.</span></span> <span data-ttu-id="6b1fa-543">Si la cola está vacía, significa que todos los ejemplos asignados están programados actualmente para su presentación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-543">If the queue is empty, it means that all allocated samples are currently scheduled for presenting.</span></span> <span data-ttu-id="6b1fa-544">En ese caso, omita el mensaje de **MFVP_MESSAGE_PROCESSINPUTNOTIFY** en este momento.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-544">In that case, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message at this time.</span></span> <span data-ttu-id="6b1fa-545">Cuando el siguiente ejemplo esté disponible, repita los pasos que se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-545">When the next sample becomes available, repeat the steps listed here.</span></span>
3.  <span data-ttu-id="6b1fa-546">(Opcional). Si el reloj está disponible, obtenga la hora de reloj actual (*T1*) mediante una llamada a [**IMFClock:: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-546">(Optional.) If the clock is available, get the current clock time (*T1*) by calling [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span>
4.  <span data-ttu-id="6b1fa-547">Llame a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-547">Call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="6b1fa-548">Si **ProcessOutput** se ejecuta correctamente, el ejemplo contiene un fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-548">If **ProcessOutput** succeeds, the sample contains a video frame.</span></span> <span data-ttu-id="6b1fa-549">Si se produce un error en el método, compruebe el código de retorno.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-549">If the method fails, check the return code.</span></span> <span data-ttu-id="6b1fa-550">Los siguientes códigos de error de **ProcessOutput** no son errores críticos:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-550">The following error codes from **ProcessOutput** are not critical failures:</span></span>

    

    | <span data-ttu-id="6b1fa-551">Código de error</span><span class="sxs-lookup"><span data-stu-id="6b1fa-551">Error code</span></span>                              | <span data-ttu-id="6b1fa-552">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b1fa-552">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="6b1fa-553">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-553">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span></span> | <span data-ttu-id="6b1fa-554">El mezclador necesita más información para poder generar un nuevo fotograma de salida.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-554">The mixer needs more input before it can produce a new output frame.</span></span><br/> <span data-ttu-id="6b1fa-555">Si obtiene este código de error, compruebe si EVR ha alcanzado el final de la secuencia y responda según corresponda, como se describe en [final de la secuencia](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-555">If you get this error code, check whether the EVR has reached the end of the stream and respond accordingly, as described in [End of Stream](#end-of-stream).</span></span> <span data-ttu-id="6b1fa-556">De lo contrario, pase por alto este mensaje **MF_E_TRANSFORM_NEED_MORE_INPUT** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-556">Otherwise, ignore this **MF_E_TRANSFORM_NEED_MORE_INPUT** message.</span></span> <span data-ttu-id="6b1fa-557">El EVR enviará otro cuando el mezclador Obtenga más entradas.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-557">The EVR will send another one when the mixer gets more input.</span></span><br/> |
    | <span data-ttu-id="6b1fa-558">**MF_E_TRANSFORM_STREAM_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-558">**MF_E_TRANSFORM_STREAM_CHANGE**</span></span>    | <span data-ttu-id="6b1fa-559">El tipo de salida del mezclador ha dejado de ser válido, posiblemente debido a un cambio de formato ascendente.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-559">The mixer's output type has become invalid, possibly due to a format change upstream.</span></span><br/> <span data-ttu-id="6b1fa-560">Si obtiene este código de error, establezca el tipo de medio del presentador en **null**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-560">If you get this error code, set the presenter's media type to **NULL**.</span></span> <span data-ttu-id="6b1fa-561">El EVR solicitará un nuevo formato.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-561">The EVR will request a new format.</span></span><br/>                                                                                                                                                                         |
    | <span data-ttu-id="6b1fa-562">**MF_E_TRANSFORM_TYPE_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-562">**MF_E_TRANSFORM_TYPE_NOT_SET**</span></span>    | <span data-ttu-id="6b1fa-563">El mezclador requiere un nuevo tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-563">The mixer requires a new media type.</span></span><br/> <span data-ttu-id="6b1fa-564">Si obtiene este código de error, renegocie el tipo de salida del mezclador como se describe en [negociar formatos](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-564">If you get this error code, renegotiate the mixer's output type as described in [Negotiating Formats](#negotiating-formats).</span></span><br/>                                                                                                                                                                                                        |

    

     

    <span data-ttu-id="6b1fa-565">Si [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) se ejecuta correctamente, continúe.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-565">If [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) succeeds, continue.</span></span>

5.  <span data-ttu-id="6b1fa-566">(Opcional). Si el reloj está disponible, obtenga la hora actual del reloj (*T2*).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-566">(Optional.) If the clock is available, get the current clock time (*T2*).</span></span> <span data-ttu-id="6b1fa-567">La cantidad de latencia introducida por el mezclador es (*T2*  -  *T1*).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-567">The amount of latency introduced by the mixer is (*T2* - *T1*).</span></span> <span data-ttu-id="6b1fa-568">Envíe un evento de **EC_PROCESSING_LATENCY** con este valor a EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-568">Send an **EC_PROCESSING_LATENCY** event with this value to the EVR.</span></span> <span data-ttu-id="6b1fa-569">EVR usa este valor para el control de calidad.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-569">The EVR uses this value for quality control.</span></span> <span data-ttu-id="6b1fa-570">Si no hay ningún reloj disponible, no hay ningún motivo para enviar el evento de **EC_PROCESSING_LATENCY** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-570">If no clock is available, there is no reason to send the **EC_PROCESSING_LATENCY** event.</span></span>
6.  <span data-ttu-id="6b1fa-571">(Opcional). Consulte el ejemplo de [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) y llame a [**IMFTrackedSample:: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) tal y como se describe en [ejemplos de seguimiento](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-571">(Optional.) Query the sample for [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) and call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) as described in [Tracking Samples](#tracking-samples).</span></span>
7.  <span data-ttu-id="6b1fa-572">Programe el ejemplo para la presentación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-572">Schedule the sample for presentation.</span></span>

<span data-ttu-id="6b1fa-573">Esta secuencia de pasos puede finalizar antes de que el presentador obtenga cualquier salida del mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-573">This sequence of steps can terminate before the presenter gets any output from the mixer.</span></span> <span data-ttu-id="6b1fa-574">Para asegurarse de que no se quita ninguna solicitud, debe repetir los mismos pasos cuando se produzca lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-574">To ensure that no requests are dropped, you should repeat the same steps when the following occur:</span></span>

-   <span data-ttu-id="6b1fa-575">Se llama al método [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) o **IMFClockStateSink:: OnClockStart** del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-575">The presenter's [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or **IMFClockStateSink::OnClockStart** method is called.</span></span> <span data-ttu-id="6b1fa-576">Esto controla el caso en el que el mezclador omite la entrada porque el reloj está en pausa (paso 1).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-576">This handles the case where the mixer ignores input because the clock is paused (step 1).</span></span>
-   <span data-ttu-id="6b1fa-577">Se invoca la devolución de llamada [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-577">The [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback is invoked.</span></span> <span data-ttu-id="6b1fa-578">Esto controla el caso en el que el mezclador recibe la entrada, pero todas las muestras de vídeo del presentador están en uso (paso 2).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-578">This handles the case where the mixer receives input but all of the presenter's video samples are in use (step 2).</span></span>

<span data-ttu-id="6b1fa-579">En los siguientes ejemplos de código se muestran estos pasos con más detalle.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-579">The next several code examples show these steps in more detail.</span></span> <span data-ttu-id="6b1fa-580">El presentador llama al `ProcessInputNotify` método (que se muestra en el ejemplo siguiente) cuando obtiene el mensaje de **MFVP_MESSAGE_PROCESSINPUTNOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-580">The presenter calls the `ProcessInputNotify` method (shown in the following example) when it gets the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message.</span></span>


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



<span data-ttu-id="6b1fa-581">Este `ProcessInputNotify` método establece una marca booleana para registrar el hecho de que el mezclador tiene una entrada nueva.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-581">This `ProcessInputNotify` method sets a Boolean flag to record the fact that the mixer has new input.</span></span> <span data-ttu-id="6b1fa-582">A continuación, llama al `ProcessOutputLoop` método, que se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-582">Then it calls the `ProcessOutputLoop` method, shown in the next example.</span></span> <span data-ttu-id="6b1fa-583">Este método intenta extraer tantas muestras como sea posible del mezclador:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-583">This method attempts to pull as many samples as possible from the mixer:</span></span>


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



<span data-ttu-id="6b1fa-584">El `ProcessOutput` método, que se muestra en el ejemplo siguiente, intenta obtener un único fotograma de vídeo del mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-584">The `ProcessOutput` method, shown in the next example, attempts to get a single video frame from the mixer.</span></span> <span data-ttu-id="6b1fa-585">Si no hay ningún fotograma de vídeo disponible, `ProcessSample` devuelve S_FALSE o un código de error, cualquiera de los cuales interrumpe el bucle en `ProcessOutputLoop` .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-585">If no video frame is available, `ProcessSample` returns S_FALSE or an error code, either of which interrupts the loop in `ProcessOutputLoop`.</span></span> <span data-ttu-id="6b1fa-586">La mayor parte del trabajo se realiza dentro del `ProcessOutput` método:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-586">Most of the work is done inside the `ProcessOutput` method:</span></span>


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



<span data-ttu-id="6b1fa-587">Algunos comentarios sobre este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-587">Some remarks about this example:</span></span>

-   <span data-ttu-id="6b1fa-588">Se supone que la variable *m_SamplePool* es un objeto de colección que contiene la cola de ejemplos de vídeo disponibles.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-588">The *m_SamplePool* variable is assumed to be a collection object that holds the queue of available video samples.</span></span> <span data-ttu-id="6b1fa-589">El método del objeto `GetSample` devuelve **MF_E_SAMPLEALLOCATOR_EMPTY** si la cola está vacía.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-589">The object's `GetSample` method returns **MF_E_SAMPLEALLOCATOR_EMPTY** if the queue is empty.</span></span>
-   <span data-ttu-id="6b1fa-590">Si el método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mezclador devuelve MF_E_TRANSFORM_NEED_MORE_INPUT, significa que el mezclador no puede producir ningún resultado más, por lo que el presentador borra la marca *m_fSampleNotify* .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-590">If the mixer's [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns MF_E_TRANSFORM_NEED_MORE_INPUT, it means the mixer cannot produce any more output, so the presenter clears the *m_fSampleNotify* flag.</span></span>
-   <span data-ttu-id="6b1fa-591">El `TrackSample` método, que establece la devolución de llamada [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) , se muestra en la sección de [ejemplos de seguimiento](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-591">The `TrackSample` method, which sets the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback, is shown in the section [Tracking Samples](#tracking-samples).</span></span>

### <a name="repainting-frames"></a><span data-ttu-id="6b1fa-592">Volver a dibujar marcos</span><span class="sxs-lookup"><span data-stu-id="6b1fa-592">Repainting Frames</span></span>

<span data-ttu-id="6b1fa-593">En ocasiones, es posible que el presentador tenga que volver a pintar el fotograma de vídeo más reciente.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-593">Occasionally the presenter might need to repaint the most recent video frame.</span></span> <span data-ttu-id="6b1fa-594">Por ejemplo, el presentador estándar vuelve a dibujar el marco en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-594">For example, the standard presenter repaints the frame in the following situations:</span></span>

-   <span data-ttu-id="6b1fa-595">En modo de ventana, en respuesta a **WM_PAINT** mensajes recibidos por la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-595">In windowed mode, in response to **WM_PAINT** messages received by the application's window.</span></span> <span data-ttu-id="6b1fa-596">Vea [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-596">See [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>
-   <span data-ttu-id="6b1fa-597">Si el rectángulo de destino cambia cuando la aplicación llama a [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-597">If the destination rectangle changes when the application calls [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="6b1fa-598">Siga estos pasos para solicitar al mezclador que vuelva a crear el fotograma más reciente:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-598">Use the following steps to request the mixer to re-create the most recent frame:</span></span>

1.  <span data-ttu-id="6b1fa-599">Obtener un ejemplo de vídeo de la cola.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-599">Get a video sample from the queue.</span></span>
2.  <span data-ttu-id="6b1fa-600">Consulte el ejemplo de la interfaz [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-600">Query the sample for the [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) interface.</span></span>
3.  <span data-ttu-id="6b1fa-601">Llame a [**IMFDesiredSample:: SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-601">Call [**IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span></span> <span data-ttu-id="6b1fa-602">Especifique la marca de tiempo del fotograma de vídeo más reciente.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-602">Specify the time stamp of the most recent video frame.</span></span> <span data-ttu-id="6b1fa-603">(Tendrá que almacenar en caché este valor y actualizarlo para cada fotograma).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-603">(You will need to cache this value and update it for each frame.)</span></span>
4.  <span data-ttu-id="6b1fa-604">Llame a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-604">Call [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span>

<span data-ttu-id="6b1fa-605">Al volver a pintar un fotograma, puede omitir el reloj de la presentación y presentar el marco inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-605">When repainting a frame, you can ignore the presentation clock and present the frame immediately.</span></span>

### <a name="scheduling-samples"></a><span data-ttu-id="6b1fa-606">Ejemplos de programación</span><span class="sxs-lookup"><span data-stu-id="6b1fa-606">Scheduling Samples</span></span>

<span data-ttu-id="6b1fa-607">Los fotogramas de vídeo pueden alcanzar el EVR en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-607">Video frames can reach the EVR at any time.</span></span> <span data-ttu-id="6b1fa-608">El presentador es responsable de presentar cada fotograma en el momento correcto, en función de la marca de tiempo del marco.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-608">The presenter is responsible for presenting each frame at the correct time, based on the time stamp of the frame.</span></span> <span data-ttu-id="6b1fa-609">Cuando el presentador obtiene un nuevo ejemplo del mezclador, coloca el ejemplo en la cola programada.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-609">When the presenter gets a new sample from the mixer, it puts the sample on the scheduled queue.</span></span> <span data-ttu-id="6b1fa-610">En un subproceso independiente, el presentador obtiene continuamente la primera muestra del encabezado de la cola y determina si:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-610">On a separate thread, the presenter continually gets the first sample from the head of the queue and determines whether to:</span></span>

-   <span data-ttu-id="6b1fa-611">Presente el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-611">Present the sample.</span></span>
-   <span data-ttu-id="6b1fa-612">Mantenga el ejemplo en la cola porque es pronto.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-612">Keep the sample on the queue because it is early.</span></span>
-   <span data-ttu-id="6b1fa-613">Descarte el ejemplo porque está retrasado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-613">Discard the sample because it is late.</span></span> <span data-ttu-id="6b1fa-614">Aunque debe evitar la eliminación de fotogramas si es posible, es posible que necesite si el presentador está continuamente por detrás.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-614">Although you should avoid dropping frames if possible, you might need to if the presenter is continually falling behind.</span></span>

<span data-ttu-id="6b1fa-615">Para obtener la marca de tiempo de un fotograma de vídeo, llame a [**IMFSample:: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) en el ejemplo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-615">To get the time stamp for a video frame, call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) on the video sample.</span></span> <span data-ttu-id="6b1fa-616">La marca de tiempo es relativa al reloj de presentación de EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-616">The time stamp is relative to the EVR's presentation clock.</span></span> <span data-ttu-id="6b1fa-617">Para obtener la hora actual del reloj, llame a [**IMFClock:: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-617">To get the current clock time, call [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span> <span data-ttu-id="6b1fa-618">Si el EVR no tiene un reloj de presentación o si un ejemplo no tiene una marca de tiempo, puede presentar el ejemplo inmediatamente después de obtenerlo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-618">If the EVR does not have a presentation clock, or if a sample does not have a time stamp, you can present the sample immediately after you get it.</span></span>

<span data-ttu-id="6b1fa-619">Para obtener la duración de cada ejemplo, llame a [**IMFSample:: GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-619">To get the duration of each sample, call [**IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span></span> <span data-ttu-id="6b1fa-620">Si el ejemplo no tiene una duración, puede usar la función [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) para calcular la duración a partir de la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-620">If the sample does not have a duration, you can use the [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) function to calculate the duration from the frame rate.</span></span>

<span data-ttu-id="6b1fa-621">Al programar ejemplos, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-621">When you schedule samples, keep in mind the following:</span></span>

-   <span data-ttu-id="6b1fa-622">Si la velocidad de reproducción es más rápida o más lenta que la velocidad normal, el reloj se ejecuta a una velocidad mayor o menor.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-622">If the playback rate is faster or slower than normal speed, the clock runs at a faster or slower rate.</span></span> <span data-ttu-id="6b1fa-623">Esto significa que la marca de tiempo de una muestra siempre proporciona el tiempo de destino correcto en relación con el reloj de la presentación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-623">That means the time stamp on a sample always gives the correct target time relative to the presentation clock.</span></span> <span data-ttu-id="6b1fa-624">Sin embargo, si traduce los tiempos de presentación en otro tiempo de reloj (por ejemplo, el contador de rendimiento de alta resolución), debe escalar las horas en función de la velocidad del reloj.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-624">However, if you translate presentation times into some other clock time (for example, the high-resolution performace counter), then you must scale the times based on the clock speed.</span></span> <span data-ttu-id="6b1fa-625">Si cambia la velocidad del reloj, EVR llama al método [**IMFClockStateSink:: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-625">If the clock speed changes, the EVR calls the presenter's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>
-   <span data-ttu-id="6b1fa-626">La velocidad de reproducción puede ser negativa para la reproducción inversa.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-626">The playback rate can be negative for reverse playback.</span></span> <span data-ttu-id="6b1fa-627">Cuando la velocidad de reproducción es negativa, el reloj de la presentación se ejecuta hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-627">When the playback rate is negative, the presentation clock runs backward.</span></span> <span data-ttu-id="6b1fa-628">En otras palabras, el tiempo *n* + 1 se produce antes de la hora *n*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-628">In other words, time *N* + 1 occurs before time *N*.</span></span>

<span data-ttu-id="6b1fa-629">En el ejemplo siguiente se calcula la antelación o la finalización de un ejemplo, en relación con el reloj de la presentación:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-629">The following example calculates how early or late a sample is, relative to the presentation clock:</span></span>


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



<span data-ttu-id="6b1fa-630">El reloj del sistema o el procesador de audio normalmente controla el reloj de la presentación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-630">The presentation clock is usually driven by the system clock or the audio renderer.</span></span> <span data-ttu-id="6b1fa-631">(El representador de audio deriva el tiempo desde la velocidad a la que la tarjeta de sonido consume audio). En general, el reloj de la presentación no se sincroniza con la frecuencia de actualización del monitor.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-631">(The audio renderer derives the time from the rate at which the sound card consumes audio.) In general, the presentation clock is not synchronized with the refresh rate of the monitor.</span></span>

<span data-ttu-id="6b1fa-632">Si los parámetros de presentación de Direct3D especifican **D3DPRESENT_INTERVAL_DEFAULT** o **D3DPRESENT_INTERVAL_ONE** para el intervalo de presentación, la operación **present** espera el reseguimiento vertical del monitor.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-632">If your Direct3D presentation parameters specify **D3DPRESENT_INTERVAL_DEFAULT** or **D3DPRESENT_INTERVAL_ONE** for the presentation interval, the **Present** operation waits for the monitor's vertical retrace.</span></span> <span data-ttu-id="6b1fa-633">Esta es una manera fácil de evitar el desgarro, pero reduce la precisión del algoritmo de programación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-633">This is an easy way to prevent tearing, but reduces the accuracy of your scheduling algorithm.</span></span> <span data-ttu-id="6b1fa-634">Por el contrario, si el intervalo de presentación es **D3DPRESENT_INTERVAL_IMMEDIATE**, el método **actual** se ejecuta inmediatamente, lo que provoca que se corte a menos que el algoritmo de programación sea lo suficientemente preciso como para que llame a **present** solo durante el período de reseguimiento vertical.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-634">Conversely, if the presentation interval is **D3DPRESENT_INTERVAL_IMMEDIATE**, the **Present** method executes immediately, which causes tearing unless your scheduling algorithm is accurate enough that you call **Present** only during the vertical retrace period.</span></span>

<span data-ttu-id="6b1fa-635">Las siguientes funciones pueden ayudarle a obtener información de tiempo precisa:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-635">The following functions can help you get accurate timing information:</span></span>

-   <span data-ttu-id="6b1fa-636">**IDirect3DDevice9:: GetRasterStatus** devuelve información sobre la trama, incluida la línea de exploración actual y si la trama está en el período en blanco vertical.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-636">**IDirect3DDevice9::GetRasterStatus** returns information about the raster, including the current scan line and whether the raster is in the vertical blank period.</span></span>
-   <span data-ttu-id="6b1fa-637">**DwmGetCompositionTimingInfo** devuelve información de tiempo para el administrador de ventanas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-637">**DwmGetCompositionTimingInfo** returns timing information for the desktop window manager.</span></span> <span data-ttu-id="6b1fa-638">Esta información es útil si la composición del escritorio está habilitada.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-638">This information is useful if desktop composition is enabled.</span></span>

### <a name="presenting-samples"></a><span data-ttu-id="6b1fa-639">Presentar ejemplos</span><span class="sxs-lookup"><span data-stu-id="6b1fa-639">Presenting Samples</span></span>

<span data-ttu-id="6b1fa-640">En esta sección se supone que ha creado una cadena de intercambio independiente para cada superficie, tal como se describe en [asignación de superficies de Direct3D](#allocating-direct3d-surfaces).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-640">This section assumes that you created a separate swap chain for each surface as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="6b1fa-641">Para presentar un ejemplo, obtenga la cadena de intercambio del ejemplo de vídeo como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-641">To present a sample, get the swap chain from the video sample as follows:</span></span>

1.  <span data-ttu-id="6b1fa-642">Llame a [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) en el ejemplo de vídeo para obtener el búfer.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-642">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) on the video sample to get the buffer.</span></span>
2.  <span data-ttu-id="6b1fa-643">Consulte el búfer para la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-643">Query the buffer for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
3.  <span data-ttu-id="6b1fa-644">Llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener la interfaz **IDirect3DSurface9** de la superficie de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-644">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the **IDirect3DSurface9** interface of the Direct3D surface.</span></span> <span data-ttu-id="6b1fa-645">(Puede combinar este paso y el paso anterior en uno llamando a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-645">(You can combine this step and the previous step into one by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span></span>
4.  <span data-ttu-id="6b1fa-646">Llame a **IDirect3DSurface9:: GetContainer** en la superficie para obtener un puntero a la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-646">Call **IDirect3DSurface9::GetContainer** on the surface to get a pointer to the swap chain.</span></span>
5.  <span data-ttu-id="6b1fa-647">Llame a **IDirect3DSwapChain9::P reenviar** en la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-647">Call **IDirect3DSwapChain9::Present** on the swap chain.</span></span>

<span data-ttu-id="6b1fa-648">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-648">The following code shows these steps:</span></span>


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



### <a name="source-and-destination-rectangles"></a><span data-ttu-id="6b1fa-649">Rectángulos de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="6b1fa-649">Source and Destination Rectangles</span></span>

<span data-ttu-id="6b1fa-650">El *rectángulo de origen* es la parte del fotograma de vídeo que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-650">The *source rectangle* is the portion of the video frame to display.</span></span> <span data-ttu-id="6b1fa-651">Se define en relación con un sistema de coordenadas normalizado, en el que todo el fotograma de vídeo ocupa un rectángulo con las coordenadas {0, 0, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-651">It is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="6b1fa-652">El *rectángulo de destino* es el área de la superficie de destino donde se dibuja el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-652">The *destination rectangle* is the area within the destination surface where the video frame is drawn.</span></span> <span data-ttu-id="6b1fa-653">El presentador estándar permite a una aplicación establecer estos rectángulos mediante una llamada a [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-653">The standard presenter enables an application to set these rectangles by calling [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="6b1fa-654">Hay varias opciones para aplicar los rectángulos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-654">There are several options for applying source and destination rectangles.</span></span> <span data-ttu-id="6b1fa-655">La primera opción es dejar que el mezclador las aplique:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-655">The first option is to let the mixer apply them:</span></span>

-   <span data-ttu-id="6b1fa-656">Establezca el rectángulo de origen mediante el atributo [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-656">Set the source rectangle using the [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) attribute.</span></span> <span data-ttu-id="6b1fa-657">El mezclador aplicará el rectángulo de origen cuando blits el vídeo a la superficie de destino.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-657">The mixer will apply the source rectangle when it blits the video to the destination surface.</span></span> <span data-ttu-id="6b1fa-658">El rectángulo de origen predeterminado del mezclador es todo el marco.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-658">The mixer's default source rectangle is the entire frame.</span></span>
-   <span data-ttu-id="6b1fa-659">Establezca el rectángulo de destino como la abertura geométrica en el tipo de salida del mezclador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-659">Set the destination rectangle as the geometric aperture in the mixer's output type.</span></span> <span data-ttu-id="6b1fa-660">Para obtener más información, vea [negociar formatos](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-660">For more information, see [Negotiating Formats](#negotiating-formats).</span></span>

<span data-ttu-id="6b1fa-661">La segunda opción consiste en aplicar los rectángulos al **IDirect3DSwapChain9::P reenviar** especificando los parámetros *pSourceRect* y *pDestRect* en el método **present** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-661">The second option is to apply the rectangles when you **IDirect3DSwapChain9::Present** by specifying the *pSourceRect* and *pDestRect* parameters in the **Present** method.</span></span> <span data-ttu-id="6b1fa-662">Puede combinar estas opciones.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-662">You can combine these options.</span></span> <span data-ttu-id="6b1fa-663">Por ejemplo, podría establecer el rectángulo de origen en el mezclador, pero aplicar el rectángulo de destino en el método **actual** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-663">For example, you could set the source rectangle on the mixer but apply the destination rectangle in the **Present** method.</span></span>

<span data-ttu-id="6b1fa-664">Si la aplicación cambia el rectángulo de destino o cambia el tamaño de la ventana, es posible que tenga que asignar nuevas superficies.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-664">If the application changes the destination rectangle or resizes the window, you might need to allocate new surfaces.</span></span> <span data-ttu-id="6b1fa-665">Si es así, debe tener cuidado de sincronizar esta operación con el subproceso de programación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-665">If so, you must be careful to synchronize this operation with your scheduling thread.</span></span> <span data-ttu-id="6b1fa-666">Vacíe la cola de programación y descarte los ejemplos anteriores antes de asignar nuevas superficies.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-666">Flush the scheduling queue and discard the old samples before allocating new surfaces.</span></span>

### <a name="end-of-stream"></a><span data-ttu-id="6b1fa-667">Final de la secuencia</span><span class="sxs-lookup"><span data-stu-id="6b1fa-667">End of Stream</span></span>

<span data-ttu-id="6b1fa-668">Cuando finaliza cada flujo de entrada en el EVR, el EVR envía un mensaje de **MFVP_MESSAGE_ENDOFSTREAM** al presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-668">When every input stream on the EVR has ended, the EVR sends an **MFVP_MESSAGE_ENDOFSTREAM** message to the presenter.</span></span> <span data-ttu-id="6b1fa-669">Sin embargo, cuando reciba el mensaje, es posible que haya algunos fotogramas de vídeo pendientes de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-669">At the point when you receive the message, however, there might be a few video frames remaining to be processed.</span></span> <span data-ttu-id="6b1fa-670">Antes de responder al mensaje de final de secuencia, debe purgar todos los resultados del mezclador y presentar todos los marcos restantes.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-670">Before you respond to the end-of-stream message, you must drain all of the output from the mixer and present all of the remaining frames.</span></span> <span data-ttu-id="6b1fa-671">Después de presentar el último fotograma, envíe un evento de **EC_COMPLETE** a EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-671">After the last frame is presented, send an **EC_COMPLETE** event to the EVR.</span></span>

<span data-ttu-id="6b1fa-672">En el ejemplo siguiente se muestra un método que envía el evento **EC_COMPLETE** si se cumplen varias condiciones.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-672">The next example shows a method that sends the **EC_COMPLETE** event if various conditions are met.</span></span> <span data-ttu-id="6b1fa-673">De lo contrario, Devuelve S_OK sin enviar el evento:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-673">Otherwise, it returns S_OK without sending the event:</span></span>


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



<span data-ttu-id="6b1fa-674">Este método comprueba los Estados siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-674">This method checks the following states:</span></span>

-   <span data-ttu-id="6b1fa-675">Si la variable de *m_fSampleNotify* es **true**, significa que el mezclador tiene uno o varios fotogramas que aún no se han procesado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-675">If the *m_fSampleNotify* variable is **TRUE**, it means the mixer has one or more frames that have not been processed yet.</span></span> <span data-ttu-id="6b1fa-676">(Para obtener más información, consulte [procesar la salida](#processing-output)).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-676">(For details, see [Processing Output](#processing-output).)</span></span>
-   <span data-ttu-id="6b1fa-677">La variable *m_fEndStreaming* es una marca booleana cuyo valor inicial es **false**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-677">The *m_fEndStreaming* variable is a Boolean flag whose initial value **FALSE**.</span></span> <span data-ttu-id="6b1fa-678">El presentador establece la marca en **true** cuando EVR envía el mensaje de **MFVP_MESSAGE_ENDOFSTREAM** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-678">The presenter sets the flag to **TRUE** when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message.</span></span>
-   <span data-ttu-id="6b1fa-679">`AreSamplesPending`Se supone que el método devuelve **true** siempre que uno o varios fotogramas estén esperando en la cola programada.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-679">The `AreSamplesPending` method is assumed to return **TRUE** as long as one or more frames are waiting in the scheduled queue.</span></span>

<span data-ttu-id="6b1fa-680">En el método [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) , establezca *m_fEndStreaming* en **true** y llame a `CheckEndOfStream` cuando EVR envíe el mensaje **MFVP_MESSAGE_ENDOFSTREAM** :</span><span class="sxs-lookup"><span data-stu-id="6b1fa-680">In the [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method, set *m_fEndStreaming* to **TRUE** and call `CheckEndOfStream` when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message:</span></span>


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



<span data-ttu-id="6b1fa-681">Además, llame a `CheckEndOfStream` si el método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mezclador devuelve **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-681">In addition, call `CheckEndOfStream` if the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span></span> <span data-ttu-id="6b1fa-682">Este código de error indica que el mezclador no tiene más ejemplos de entrada (vea la [salida de procesamiento](#processing-output)).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-682">This error code indicates that the mixer has no more input samples (see [Processing Output](#processing-output)).</span></span>

## <a name="frame-stepping"></a><span data-ttu-id="6b1fa-683">Recorrido de fotogramas</span><span class="sxs-lookup"><span data-stu-id="6b1fa-683">Frame Stepping</span></span>

<span data-ttu-id="6b1fa-684">La EVR está diseñada para admitir la ejecución de fotogramas en DirectShow y la limpieza en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-684">The EVR is designed to support frame stepping in DirectShow and scrubbing in Media Foundation.</span></span> <span data-ttu-id="6b1fa-685">El recorrido y la limpieza de fotogramas son conceptualmente similares.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-685">Frame stepping and scrubbing are conceptually similar.</span></span> <span data-ttu-id="6b1fa-686">En ambos casos, la aplicación solicita un fotograma de vídeo cada vez.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-686">In both cases, the application requests one video frame at a time.</span></span> <span data-ttu-id="6b1fa-687">Internamente, el presentador utiliza el mismo mecanismo para implementar ambas características.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-687">Internally, the presenter uses the same mechanism to implement both features.</span></span>

<span data-ttu-id="6b1fa-688">La ejecución paso a paso en DirectShow funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-688">Frame stepping in DirectShow works as follows:</span></span>

-   <span data-ttu-id="6b1fa-689">La aplicación llama a [**IVideoFrameStep:: Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-689">The application calls [**IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span></span> <span data-ttu-id="6b1fa-690">El número de pasos se proporciona en el parámetro *dwSteps* .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-690">The number of steps is given in the *dwSteps* parameter.</span></span> <span data-ttu-id="6b1fa-691">El EVR envía un mensaje de **MFVP_MESSAGE_STEP** al presentador, donde el parámetro de mensaje (*ulParam*) es el número de pasos.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-691">The EVR sends an **MFVP_MESSAGE_STEP** message to the presenter, where the message parameter (*ulParam*) is the number of steps.</span></span>
-   <span data-ttu-id="6b1fa-692">Si la aplicación llama a [**IVideoFrameStep:: CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) o cambia el estado del gráfico (en ejecución, en pausa o detenido), EVR envía un mensaje de **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-692">If the application calls [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) or changes the graph state (running, paused, or stopped), the EVR sends an **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="6b1fa-693">La limpieza en Media Foundation funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-693">Scrubbing in Media Foundation works as follows:</span></span>

-   <span data-ttu-id="6b1fa-694">La aplicación establece la velocidad de reproducción en cero llamando a [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-694">The application sets the playback rate to zero by calling [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span></span>
-   <span data-ttu-id="6b1fa-695">Para representar un nuevo marco, la aplicación llama a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) con la posición deseada.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-695">To render a new frame, the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the desired position.</span></span> <span data-ttu-id="6b1fa-696">EVR envía un mensaje de **MFVP_MESSAGE_STEP** con *ulParam* igual a 1.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-696">The EVR sends an **MFVP_MESSAGE_STEP** message with *ulParam* equal to 1.</span></span>
-   <span data-ttu-id="6b1fa-697">Para detener la limpieza, la aplicación establece la velocidad de reproducción en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-697">To stop scrubbing, the application sets the playback rate to a nonzero value.</span></span> <span data-ttu-id="6b1fa-698">EVR envía el mensaje de **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-698">The EVR sends the **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="6b1fa-699">Después de recibir el mensaje de **MFVP_MESSAGE_STEP** , el presentador espera a que llegue el marco de destino.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-699">After receiving the **MFVP_MESSAGE_STEP** message, the presenter waits for the target frame to arrive.</span></span> <span data-ttu-id="6b1fa-700">Si el número de pasos es *N*, el presentador descarta los siguientes (*N* -1) ejemplos y presenta el ejemplo *N* .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-700">If the number of steps is *N*, the presenter discards the next (*N* - 1) samples and presents the *N* th sample.</span></span> <span data-ttu-id="6b1fa-701">Cuando el presentador completa el paso del marco, envía un evento [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) a EVR con *LParam1* establecido en **false**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-701">When the presenter completes the frame step, it sends an [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event to the EVR with *lParam1* set to **FALSE**.</span></span> <span data-ttu-id="6b1fa-702">Además, si la velocidad de reproducción es cero, el presentador envía un evento [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-702">In addition, if the playback rate is zero, the presenter sends an [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) event.</span></span> <span data-ttu-id="6b1fa-703">Si el EVR cancela el recorrido de fotogramas mientras una operación de fotogramas sigue pendiente, el presentador envía un evento **EC_STEP_COMPLETE** con *LParam1* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-703">If the EVR cancels frame stepping while a frame-step operation is still pending, the presenter sends an **EC_STEP_COMPLETE** event with *lParam1* set to **TRUE**.</span></span>

<span data-ttu-id="6b1fa-704">La aplicación puede enmarcar el paso o borrar varias veces, por lo que el presentador podría recibir varios mensajes de **MFVP_MESSAGE_STEP** antes de que obtenga un mensaje **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-704">The application can frame step or scrub multiple times, so the presenter might receive multiple **MFVP_MESSAGE_STEP** messages before it gets an **MFVP_MESSAGE_CANCELSTEP** message.</span></span> <span data-ttu-id="6b1fa-705">Además, el presentador puede recibir el mensaje de **MFVP_MESSAGE_STEP** antes de que se inicie el reloj o mientras se esté ejecutando el reloj.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-705">Also, the presenter can receive the **MFVP_MESSAGE_STEP** message before the clock starts or while the clock is running.</span></span>

### <a name="implementing-frame-stepping"></a><span data-ttu-id="6b1fa-706">Implementación del recorrido de fotogramas</span><span class="sxs-lookup"><span data-stu-id="6b1fa-706">Implementing Frame Stepping</span></span>

<span data-ttu-id="6b1fa-707">En esta sección se describe un algoritmo para implementar el recorrido de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-707">This section describes an algorithm to implement frame stepping.</span></span> <span data-ttu-id="6b1fa-708">El algoritmo Stepping de fotogramas utiliza las siguientes variables:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-708">The frame stepping algorithm uses the following variables:</span></span>

-   <span data-ttu-id="6b1fa-709">*step_count*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-709">*step_count*.</span></span> <span data-ttu-id="6b1fa-710">Entero sin signo que especifica el número de pasos de la operación de recorrido del marco actual.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-710">An unsigned integer that specifies the number of steps in the current frame stepping operation.</span></span>
-   <span data-ttu-id="6b1fa-711">*step_queue*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-711">*step_queue*.</span></span> <span data-ttu-id="6b1fa-712">Una cola de punteros [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-712">A queue of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointers.</span></span>
-   <span data-ttu-id="6b1fa-713">*step_state*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-713">*step_state*.</span></span> <span data-ttu-id="6b1fa-714">En cualquier momento, el presentador puede estar en uno de los siguientes Estados con respecto a la ejecución de fotogramas:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-714">At any time, the presenter can be in one of the following states with respect to frame stepping:</span></span> 

    | <span data-ttu-id="6b1fa-715">Estado</span><span class="sxs-lookup"><span data-stu-id="6b1fa-715">State</span></span>         | <span data-ttu-id="6b1fa-716">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b1fa-716">Description</span></span>                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="6b1fa-717">NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="6b1fa-717">NOT_STEPPING</span></span> | <span data-ttu-id="6b1fa-718">Sin recorrido de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-718">Not frame stepping.</span></span>                                                                                                                                                                                             |
    | <span data-ttu-id="6b1fa-719">EN ESPERA</span><span class="sxs-lookup"><span data-stu-id="6b1fa-719">WAITING</span></span>       | <span data-ttu-id="6b1fa-720">El presentador ha recibido el mensaje de **MFVP_MESSAGE_STEP** , pero el reloj no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-720">The presenter has received the **MFVP_MESSAGE_STEP** message, but the clock has not started.</span></span>                                                                                                                  |
    | <span data-ttu-id="6b1fa-721">PENDING</span><span class="sxs-lookup"><span data-stu-id="6b1fa-721">PENDING</span></span>       | <span data-ttu-id="6b1fa-722">El presentador ha recibido el mensaje de **MFVP_MESSAGE_STEP** y se ha iniciado el reloj, pero el presentador está esperando recibir el marco de destino.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-722">The presenter has received the **MFVP_MESSAGE_STEP** message and the clock has started, but the presenter is waiting to receive the target frame.</span></span>                                                             |
    | <span data-ttu-id="6b1fa-723">REGULAR</span><span class="sxs-lookup"><span data-stu-id="6b1fa-723">SCHEDULED</span></span>     | <span data-ttu-id="6b1fa-724">El presentador ha recibido el marco de destino y lo ha programado para su presentación, pero no se ha presentado el marco.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-724">The presenter has received the target frame and has scheduled it for presentation, but the frame has not been presented.</span></span>                                                                                        |
    | <span data-ttu-id="6b1fa-725">FINALIZA</span><span class="sxs-lookup"><span data-stu-id="6b1fa-725">COMPLETE</span></span>      | <span data-ttu-id="6b1fa-726">El presentador ha presentado el marco de destino y ha enviado el evento de [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) y está esperando el siguiente **MFVP_MESSAGE_STEP** o **MFVP_MESSAGE_CANCELSTEP** mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-726">The presenter has presented the target frame and sent the [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event, and is waiting for the next **MFVP_MESSAGE_STEP** or **MFVP_MESSAGE_CANCELSTEP** message.</span></span> |

    

     

    <span data-ttu-id="6b1fa-727">Estos Estados son independientes de los Estados del presentador que aparecen en la sección [Estados del presentador](#presenter-states).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-727">These states are independent of the presenter states listed in the section [Presenter States](#presenter-states).</span></span>

<span data-ttu-id="6b1fa-728">Los procedimientos siguientes se definen para el algoritmo de ejecución de fotogramas:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-728">The following procedures are defined for the frame-stepping algorithm:</span></span>

<span data-ttu-id="6b1fa-729">Procedimiento PrepareFrameStep</span><span class="sxs-lookup"><span data-stu-id="6b1fa-729">PrepareFrameStep Procedure</span></span>

1.  <span data-ttu-id="6b1fa-730">*Step_count* de incremento.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-730">Increment *step_count*.</span></span>
2.  <span data-ttu-id="6b1fa-731">Establezca *step_state* en en espera.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-731">Set *step_state* to WAITING.</span></span>
3.  <span data-ttu-id="6b1fa-732">Si el reloj se está ejecutando, llame a StartFrameStep.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-732">If the clock is running, call StartFrameStep.</span></span>

<span data-ttu-id="6b1fa-733">Procedimiento StartFrameStep</span><span class="sxs-lookup"><span data-stu-id="6b1fa-733">StartFrameStep Procedure</span></span>

1.  <span data-ttu-id="6b1fa-734">Si *step_state* es igual a Waiting, establezca *step_state* en Pending.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-734">If *step_state* equals WAITING, set *step_state* to PENDING.</span></span> <span data-ttu-id="6b1fa-735">Para cada ejemplo en *step_queue*, llame a DeliverFrameStepSample.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-735">For each sample in *step_queue*, call DeliverFrameStepSample.</span></span>
2.  <span data-ttu-id="6b1fa-736">Si *step_state* es igual a NOT_STEPPING, quite cualquier ejemplo de *step_queue* y programe la presentación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-736">If *step_state* equals NOT_STEPPING, remove any samples from *step_queue* and schedule them for presentation.</span></span>

<span data-ttu-id="6b1fa-737">Procedimiento CompleteFrameStep</span><span class="sxs-lookup"><span data-stu-id="6b1fa-737">CompleteFrameStep Procedure</span></span>

1.  <span data-ttu-id="6b1fa-738">Establezca *step_state* en completa.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-738">Set *step_state* to COMPLETE.</span></span>
2.  <span data-ttu-id="6b1fa-739">Envíe el evento EC_STEP_COMPLETE con *lParam1*  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-739">Send the EC_STEP_COMPLETE event with *lParam1* = **FALSE**.</span></span>
3.  <span data-ttu-id="6b1fa-740">Si la velocidad de reloj es cero, envíe el evento **EC_SCRUB_TIME** con la hora de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-740">If the clock rate is zero, send the **EC_SCRUB_TIME** event with the sample time.</span></span>

<span data-ttu-id="6b1fa-741">Procedimiento DeliverFrameStepSample</span><span class="sxs-lookup"><span data-stu-id="6b1fa-741">DeliverFrameStepSample Procedure</span></span>

1.  <span data-ttu-id="6b1fa-742">Si la tasa de reloj es cero y el tiempo de espera de ejemplo de *tiempo de ejemplo*  +    <  , descartará el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-742">If the clock rate is zero and *sample time* + *sample duration* < *clock time*, discard the sample.</span></span> <span data-ttu-id="6b1fa-743">Salir.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-743">Exit.</span></span>
2.  <span data-ttu-id="6b1fa-744">Si *step_state* es igual a programado o completo, agregue el ejemplo a *step_queue*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-744">If *step_state* equals SCHEDULED or COMPLETE, add the sample to *step_queue*.</span></span> <span data-ttu-id="6b1fa-745">Salir.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-745">Exit.</span></span>
3.  <span data-ttu-id="6b1fa-746">Decremento *step_count*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-746">Decrement *step_count*.</span></span>
4.  <span data-ttu-id="6b1fa-747">Si *step_count* > 0, descarte el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-747">If *step_count* > 0, discard the sample.</span></span> <span data-ttu-id="6b1fa-748">Salir.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-748">Exit.</span></span>
5.  <span data-ttu-id="6b1fa-749">Si *step_state* es igual a Waiting, agregue el ejemplo a *step_queue*.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-749">If *step_state* equals WAITING, add the sample to *step_queue*.</span></span> <span data-ttu-id="6b1fa-750">Salir.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-750">Exit.</span></span>
6.  <span data-ttu-id="6b1fa-751">Programe el ejemplo para la presentación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-751">Schedule the sample for presentation.</span></span>
7.  <span data-ttu-id="6b1fa-752">Establezca *step_state* en programado.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-752">Set *step_state* to SCHEDULED.</span></span>

<span data-ttu-id="6b1fa-753">Procedimiento CancelFrameStep</span><span class="sxs-lookup"><span data-stu-id="6b1fa-753">CancelFrameStep Procedure</span></span>

1.  <span data-ttu-id="6b1fa-754">Establezca *step_state* en NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="6b1fa-754">Set *step_state* to NOT_STEPPING</span></span>
2.  <span data-ttu-id="6b1fa-755">Restablezca *step_count* en cero.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-755">Reset *step_count* to zero.</span></span>
3.  <span data-ttu-id="6b1fa-756">Si el valor anterior de *step_state* estaba esperando, pendiente o programado, envíe EC_STEP_COMPLETE con *lParam1*  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-756">If the previous value of *step_state* was WAITING, PENDING, or SCHEDULED, send EC_STEP_COMPLETE with *lParam1* = **TRUE**.</span></span>

<span data-ttu-id="6b1fa-757">Llame a estos procedimientos de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-757">Call these procedures as follows:</span></span>



| <span data-ttu-id="6b1fa-758">Mensaje o método del presentador</span><span class="sxs-lookup"><span data-stu-id="6b1fa-758">Presenter message or method</span></span>                                                   | <span data-ttu-id="6b1fa-759">Procedimiento</span><span class="sxs-lookup"><span data-stu-id="6b1fa-759">Procedure</span></span>           |
|-------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="6b1fa-760">Mensaje **MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-760">**MFVP_MESSAGE_STEP** message</span></span>                                               | `PrepareFrameStep`  |
| <span data-ttu-id="6b1fa-761">Mensaje **MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-761">**MFVP_MESSAGE_STEP** message</span></span>                                               | `CancelStep`        |
| [<span data-ttu-id="6b1fa-762">**IMFClockStateSink::OnClockStart**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-762">**IMFClockStateSink::OnClockStart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [<span data-ttu-id="6b1fa-763">**IMFClockStateSink::OnClockRestart**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-763">**IMFClockStateSink::OnClockRestart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| <span data-ttu-id="6b1fa-764">Devolución de llamada [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="6b1fa-764">[**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback</span></span>                         | `CompleteFrameStep` |
| [<span data-ttu-id="6b1fa-765">**IMFClockStateSink::OnClockStop**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-765">**IMFClockStateSink::OnClockStop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [<span data-ttu-id="6b1fa-766">**IMFClockStateSink::OnClockSetRate**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-766">**IMFClockStateSink::OnClockSetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

<span data-ttu-id="6b1fa-767">En el diagrama de flujo siguiente se muestran los procedimientos de ejecución de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-767">The following flow chart shows the frame-stepping procedures.</span></span>

![diagrama de flujo que muestra las rutas de acceso que comienzan con el \- paso de mensaje mfvp \- y el \- mensaje mfvp \- processinputnotify y terminan en "State = Complete"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a><span data-ttu-id="6b1fa-769">Establecer el presentador en el EVR</span><span class="sxs-lookup"><span data-stu-id="6b1fa-769">Setting the Presenter on the EVR</span></span>

<span data-ttu-id="6b1fa-770">Después de implementar el presentador, el siguiente paso es configurar el EVR para usarlo.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-770">After implementing the presenter, the next step is to configure the EVR to use it.</span></span>

### <a name="setting-the-presenter-in-directshow"></a><span data-ttu-id="6b1fa-771">Establecer el presentador en DirectShow</span><span class="sxs-lookup"><span data-stu-id="6b1fa-771">Setting the Presenter in DirectShow</span></span>

<span data-ttu-id="6b1fa-772">En una aplicación de DirectShow, establezca el presentador en el EVR como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-772">In a DirectShow application, set the presenter on the EVR as follows:</span></span>

1.  <span data-ttu-id="6b1fa-773">Cree el filtro EVR llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-773">Create the EVR filter by calling **CoCreateInstance**.</span></span> <span data-ttu-id="6b1fa-774">El CLSID es **CLSID_EnhancedVideoRenderer**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-774">The CLSID is **CLSID_EnhancedVideoRenderer**.</span></span>
2.  <span data-ttu-id="6b1fa-775">Agregue EVR al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-775">Add the EVR to the filter graph.</span></span>
3.  <span data-ttu-id="6b1fa-776">Cree una instancia del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-776">Create an instance of your presenter.</span></span> <span data-ttu-id="6b1fa-777">El presentador puede admitir la creación de objetos COM estándar mediante **IClassFactory**, pero esto no es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-777">Your presenter can support standard COM object creation through **IClassFactory**, but this is not mandatory.</span></span>
4.  <span data-ttu-id="6b1fa-778">Consulte el filtro EVR para la interfaz [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-778">Query the EVR filter for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
5.  <span data-ttu-id="6b1fa-779">Llame a [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-779">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

### <a name="setting-the-presenter-in-media-foundation"></a><span data-ttu-id="6b1fa-780">Establecer el presentador en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b1fa-780">Setting the Presenter in Media Foundation</span></span>

<span data-ttu-id="6b1fa-781">En Media Foundation, tiene varias opciones, dependiendo de si crea el receptor de medios EVR o el objeto de activación EVR.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-781">In Media Foundation, you have several options, depending on whether you create the EVR media sink or the EVR activation object.</span></span> <span data-ttu-id="6b1fa-782">Para obtener más información sobre los objetos de activación, vea [objetos de activación](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-782">For more information about activation objects, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="6b1fa-783">En el caso del receptor de medios EVR, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-783">For the EVR media sink, do the following:</span></span>

1.  <span data-ttu-id="6b1fa-784">Llame a [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) para crear el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-784">Call [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) to create the media sink.</span></span>
2.  <span data-ttu-id="6b1fa-785">Cree una instancia del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-785">Create an instance of your presenter.</span></span>
3.  <span data-ttu-id="6b1fa-786">Consulte el receptor de medios EVR para la interfaz [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-786">Query the EVR media sink for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
4.  <span data-ttu-id="6b1fa-787">Llame a [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="6b1fa-787">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

<span data-ttu-id="6b1fa-788">Para el objeto de activación EVR, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-788">For the EVR activation object, do the following:</span></span>

1.  <span data-ttu-id="6b1fa-789">Llame a [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear el objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-789">Call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the activation object.</span></span>
2.  <span data-ttu-id="6b1fa-790">Establezca uno de los siguientes atributos en el objeto de activación:</span><span class="sxs-lookup"><span data-stu-id="6b1fa-790">Set one of the following attributes on the activation object:</span></span> 

    | <span data-ttu-id="6b1fa-791">Atributo</span><span class="sxs-lookup"><span data-stu-id="6b1fa-791">Attribute</span></span>                                                                                                         | <span data-ttu-id="6b1fa-792">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b1fa-792">Description</span></span>                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="6b1fa-793">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-793">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span></span>](mf-activate-custom-video-presenter-activate-attribute.md) | <span data-ttu-id="6b1fa-794">Puntero a un objeto de activación para el presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-794">Pointer to an activation object for the presenter.</span></span><br/> <span data-ttu-id="6b1fa-795">Con esta marca, debe proporcionar un objeto de activación para el presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-795">With this flag, you must provide an activation object for your presenter.</span></span> <span data-ttu-id="6b1fa-796">El objeto de activación debe implementar la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="6b1fa-796">The activation object must implement the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span><br/> |
    | [<span data-ttu-id="6b1fa-797">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span><span class="sxs-lookup"><span data-stu-id="6b1fa-797">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span></span>](mf-activate-custom-video-presenter-clsid-attribute.md)       | <span data-ttu-id="6b1fa-798">CLSID del presentador.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-798">CLSID of the presenter.</span></span><br/> <span data-ttu-id="6b1fa-799">Con esta marca, el presentador debe admitir la creación de objetos COM estándar mediante **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-799">With this flag, your presenter must support standard COM object creation through **IClassFactory**.</span></span><br/>                                                                                         |

    

     

3.  <span data-ttu-id="6b1fa-800">Opcionalmente, establezca el atributo [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) en el objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="6b1fa-800">Optionally, set the [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) attribute on the activation object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b1fa-801">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b1fa-801">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b1fa-802">Representador de vídeo mejorado</span><span class="sxs-lookup"><span data-stu-id="6b1fa-802">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="6b1fa-803">Ejemplo de EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="6b1fa-803">EVRPresenter Sample</span></span>](evrpresenter-sample.md)
</dt> </dl>

 

 
