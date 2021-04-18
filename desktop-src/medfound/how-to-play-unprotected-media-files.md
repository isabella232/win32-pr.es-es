---
description: En este tutorial se muestra cómo reproducir archivos multimedia mediante el objeto de sesión de medios.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Cómo reproducir archivos multimedia con Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104551624"
---
# <a name="how-to-play-media-files-with-media-foundation"></a><span data-ttu-id="8b5b6-103">Cómo reproducir archivos multimedia con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b5b6-103">How to Play Media Files with Media Foundation</span></span>

<span data-ttu-id="8b5b6-104">En este tutorial se muestra cómo reproducir archivos multimedia mediante el objeto de [sesión de medios](media-session.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5b6-104">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8b5b6-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8b5b6-105">Prerequisites</span></span>

<span data-ttu-id="8b5b6-106">Antes de leer este tema, debe estar familiarizado con los siguientes conceptos de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="8b5b6-106">Before reading this topic, you should be familiar with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="8b5b6-107">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="8b5b6-107">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="8b5b6-108">Solucionador de origen</span><span class="sxs-lookup"><span data-stu-id="8b5b6-108">Source Resolver</span></span>](source-resolver.md)
-   [<span data-ttu-id="8b5b6-109">Topologías</span><span class="sxs-lookup"><span data-stu-id="8b5b6-109">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="8b5b6-110">Generadores de eventos multimedia</span><span class="sxs-lookup"><span data-stu-id="8b5b6-110">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="8b5b6-111">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="8b5b6-111">Presentation Descriptors</span></span>](presentation-descriptors.md)

> [!Note]  
> <span data-ttu-id="8b5b6-112">En este tema no se describe cómo reproducir archivos protegidos con la administración de derechos digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="8b5b6-112">This topic does not describe how to play files that are protected by digital rights management (DRM).</span></span> <span data-ttu-id="8b5b6-113">Para obtener información acerca de DRM en Microsoft Media Foundation, consulte [Cómo reproducir archivos multimedia protegidos](how-to-play-protected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="8b5b6-113">For information about DRM in Microsoft Media Foundation, see [How to Play Protected Media Files](how-to-play-protected-media-files.md).</span></span>

 

## <a name="overview"></a><span data-ttu-id="8b5b6-114">Información general</span><span class="sxs-lookup"><span data-stu-id="8b5b6-114">Overview</span></span>

<span data-ttu-id="8b5b6-115">Los objetos siguientes se usan para reproducir un archivo multimedia con la sesión multimedia:</span><span class="sxs-lookup"><span data-stu-id="8b5b6-115">The following objects are used to play a media file with the Media Session:</span></span>

-   <span data-ttu-id="8b5b6-116">Un *origen multimedia* es un objeto que analiza un archivo multimedia u otro origen de datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-116">A *media source* is an object that parses a media file or other source of media data.</span></span> <span data-ttu-id="8b5b6-117">El origen de medios crea objetos de *secuencia* para cada secuencia de audio o vídeo del archivo.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-117">The media source creates *stream* objects for each audio or video stream in the file.</span></span> <span data-ttu-id="8b5b6-118">Los *descodificadores* convierten los datos multimedia codificados en vídeo y audio sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-118">*Decoders* convert encoded media data into uncompressed video and audio.</span></span>
-   <span data-ttu-id="8b5b6-119">La *resolución de origen* crea un origen multimedia a partir de una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-119">The *Source Resolver* creates a media source from a URL.</span></span>
-   <span data-ttu-id="8b5b6-120">El [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR) representa el vídeo en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-120">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) renders video to the screen.</span></span>
-   <span data-ttu-id="8b5b6-121">[Streaming audio renderer](streaming-audio-renderer.md) (SAR) representa el audio en un altavoz u otro dispositivo de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-121">The [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) renders audio to a speaker or other audio output device.</span></span>
-   <span data-ttu-id="8b5b6-122">Una *topología* define el flujo de datos desde el origen de medios hasta EVR y SAR.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-122">A *topology* defines the flow of data from the media source to the EVR and SAR.</span></span>
-   <span data-ttu-id="8b5b6-123">La *sesión multimedia* controla el flujo de datos y envía los eventos de estado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-123">The *Media Session* controls the data flow and sends status events to the application.</span></span> <span data-ttu-id="8b5b6-124">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-124">The following diagram illustrates this process.</span></span>

![diagrama que muestra la reproducción mediante la sesión multimedia](images/session-playback.gif)

<span data-ttu-id="8b5b6-126">A continuación se describe un esquema general de los pasos necesarios para reproducir un archivo multimedia mediante la sesión multimedia:</span><span class="sxs-lookup"><span data-stu-id="8b5b6-126">The following is a general outline of the steps needed to play a media file using the Media Session:</span></span>

1.  <span data-ttu-id="8b5b6-127">Llame a la función [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar la plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-127">Call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="8b5b6-128">Llame a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear una nueva instancia de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-128">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="8b5b6-129">Utilice el solucionador de origen para crear un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-129">Use the source resolver to create a media source.</span></span> <span data-ttu-id="8b5b6-130">Para obtener más información, vea [usar el solucionador de origen](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="8b5b6-130">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>
4.  <span data-ttu-id="8b5b6-131">Cree una topología que conecte el origen multimedia a EVR y SAR.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-131">Create a topology that connects the media source to the EVR and SAR.</span></span> <span data-ttu-id="8b5b6-132">En este paso, la aplicación crea una topología *parcial* que no incluye los descodificadores.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-132">In this step, the application creates a *partial* topology that does not include the decoders.</span></span> <span data-ttu-id="8b5b6-133">Para obtener más información, consulte [crear topologías de reproducción](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="8b5b6-133">For more information, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="8b5b6-134">Llame a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para establecer la topología en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-134">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
6.  <span data-ttu-id="8b5b6-135">Use la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) para obtener los eventos de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-135">Use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface to get events from the Media Session.</span></span>
7.  <span data-ttu-id="8b5b6-136">Llame a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-136">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start playback.</span></span> <span data-ttu-id="8b5b6-137">Una vez iniciada la reproducción, puede pausarla llamando a [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), o bien detenerla llamando a [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="8b5b6-137">After playback starts, you can pause it by calling [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or stop it by calling [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
8.  <span data-ttu-id="8b5b6-138">Cuando se cierra la aplicación, libera los recursos:</span><span class="sxs-lookup"><span data-stu-id="8b5b6-138">When the application exits, release resources:</span></span>

    1.  <span data-ttu-id="8b5b6-139">Llame a [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para cerrar la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-139">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span> <span data-ttu-id="8b5b6-140">Este método es asincrónico.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-140">This method is asynchronous.</span></span> <span data-ttu-id="8b5b6-141">Cuando se completa, la sesión multimedia envía un evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5b6-141">When it completes, the Media Session sends an [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="8b5b6-142">Después, es seguro realizar los pasos restantes.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-142">Then it is safe to perform the remaining steps.</span></span>
    2.  <span data-ttu-id="8b5b6-143">Llame a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para cerrar el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-143">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
    3.  <span data-ttu-id="8b5b6-144">Llame a [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) para cerrar la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-144">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) to shut down the Media Session.</span></span>
    4.  <span data-ttu-id="8b5b6-145">Llame a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para cerrar la plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8b5b6-145">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>

<span data-ttu-id="8b5b6-146">En las secciones siguientes se muestra un ejemplo de código completo:</span><span class="sxs-lookup"><span data-stu-id="8b5b6-146">The following sections show a complete code example:</span></span>

-   [<span data-ttu-id="8b5b6-147">Paso 1: declarar la clase CPlayer</span><span class="sxs-lookup"><span data-stu-id="8b5b6-147">Step 1: Declare the CPlayer Class</span></span>](step-1--declare-the-cplayer-class.md)
-   [<span data-ttu-id="8b5b6-148">Paso 2: crear el objeto CPlayer</span><span class="sxs-lookup"><span data-stu-id="8b5b6-148">Step 2: Create the CPlayer Object</span></span>](step-2--create-the-cplayer-object.md)
-   [<span data-ttu-id="8b5b6-149">Paso 3: abrir un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="8b5b6-149">Step 3: Open a Media File</span></span>](step-3--open-a-media-file.md)
-   [<span data-ttu-id="8b5b6-150">Paso 4: crear la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="8b5b6-150">Step 4: Create the Media Session</span></span>](step-4--create-the-media-session.md)
-   [<span data-ttu-id="8b5b6-151">Paso 5: controlar los eventos de la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="8b5b6-151">Step 5: Handle Media Session Events</span></span>](step-5--handle-media-session-events.md)
-   [<span data-ttu-id="8b5b6-152">Paso 6: control de la reproducción</span><span class="sxs-lookup"><span data-stu-id="8b5b6-152">Step 6: Control Playback</span></span>](step-6--control-playback.md)
-   [<span data-ttu-id="8b5b6-153">Paso 7: apagar la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="8b5b6-153">Step 7: Shut Down the Media Session</span></span>](step-7--shut-down-the-media-session.md)
-   [<span data-ttu-id="8b5b6-154">Ejemplo de reproducción de sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="8b5b6-154">Media Session Playback Example</span></span>](media-session-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="8b5b6-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b5b6-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b5b6-156">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="8b5b6-156">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="8b5b6-157">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="8b5b6-157">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



