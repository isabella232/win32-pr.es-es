---
description: MFPlay es una API para crear aplicaciones de reproducción multimedia en C++.
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: Introducción con MFPlay
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9e0405d3138a22e0d20e94849d416b29d62945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496799"
---
# <a name="getting-started-with-mfplay"></a><span data-ttu-id="6e3c1-103">Introducción con MFPlay</span><span class="sxs-lookup"><span data-stu-id="6e3c1-103">Getting Started with MFPlay</span></span>

<span data-ttu-id="6e3c1-104">\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6e3c1-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6e3c1-106">\]</span><span class="sxs-lookup"><span data-stu-id="6e3c1-106">\]</span></span>

<span data-ttu-id="6e3c1-107">MFPlay es una API para crear aplicaciones de reproducción multimedia en C++.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-107">MFPlay is an API for creating media playback applications in C++.</span></span>

<span data-ttu-id="6e3c1-108">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="6e3c1-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="6e3c1-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e3c1-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6e3c1-110">Acerca de MFPlay</span><span class="sxs-lookup"><span data-stu-id="6e3c1-110">About MFPlay</span></span>](#about-mfplay)
-   [<span data-ttu-id="6e3c1-111">Reproducir un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="6e3c1-111">Playing a Media File</span></span>](#playing-a-media-file)
-   [<span data-ttu-id="6e3c1-112">Controlar la reproducción</span><span class="sxs-lookup"><span data-stu-id="6e3c1-112">Controlling Playback</span></span>](#controlling-playback)
-   [<span data-ttu-id="6e3c1-113">Recibir eventos del reproductor</span><span class="sxs-lookup"><span data-stu-id="6e3c1-113">Receiving Events From the Player</span></span>](#receiving-events-from-the-player)
-   [<span data-ttu-id="6e3c1-114">Obtención de información acerca de un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="6e3c1-114">Getting Information About a Media File</span></span>](#getting-information-about-a-media-file)
-   [<span data-ttu-id="6e3c1-115">Administrar la reproducción de vídeo</span><span class="sxs-lookup"><span data-stu-id="6e3c1-115">Managing Video Playback</span></span>](#managing-video-playback)
-   [<span data-ttu-id="6e3c1-116">Limitaciones de MFPlay</span><span class="sxs-lookup"><span data-stu-id="6e3c1-116">Limitations of MFPlay</span></span>](#limitations-of-mfplay)
-   [<span data-ttu-id="6e3c1-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e3c1-117">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="6e3c1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e3c1-118">Requirements</span></span>

<span data-ttu-id="6e3c1-119">MFPlay requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-119">MFPlay requires Windows 7.</span></span>

## <a name="about-mfplay"></a><span data-ttu-id="6e3c1-120">Acerca de MFPlay</span><span class="sxs-lookup"><span data-stu-id="6e3c1-120">About MFPlay</span></span>

<span data-ttu-id="6e3c1-121">MFPlay tiene un modelo de programación simple, a la vez que proporciona el conjunto principal de características que necesitan la mayoría de las aplicaciones de reproducción.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-121">MFPlay has a simple programming model, while providing the core set of features that most playback applications need.</span></span> <span data-ttu-id="6e3c1-122">Una aplicación crea un objeto de *reproductor* que controla la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-122">An application creates a *player* object that controls playback.</span></span> <span data-ttu-id="6e3c1-123">Para reproducir un archivo multimedia, el objeto reproductor crea un *elemento multimedia*, que se puede utilizar para obtener información sobre el contenido del archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-123">To play a media file, the player object creates a *media item*, which can be used to get information about the contents of the media file.</span></span> <span data-ttu-id="6e3c1-124">La aplicación controla la reproducción a través de métodos en la interfaz [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) del objeto Player.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-124">The application controls playback through methods on the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="6e3c1-125">Opcionalmente, la aplicación puede obtener notificaciones de eventos a través de una interfaz de devolución de llamada. el siguiente diagrama ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-125">Optionally, the application can get event notifications through a callback interface The following diagram illustrates this process.</span></span>

![diagrama conceptual: la aplicación y el jugador apuntan entre sí, ambos apuntan al elemento multimedia, que apunta a un archivo multimedia](images/mfplay.png)

## <a name="playing-a-media-file"></a><span data-ttu-id="6e3c1-127">Reproducir un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="6e3c1-127">Playing a Media File</span></span>

<span data-ttu-id="6e3c1-128">Para reproducir un archivo multimedia, llame a la función [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-128">To play a media file, call the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>


```C++
// Global variables
IMFPMediaPlayer *g_pPlayer = NULL;

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

HRESULT PlayVideo(HWND hwnd, const WCHAR* sURL)
{
    // Create the player object and play a video file.

    return MFPCreateMediaPlayer(
        sURL,
        TRUE,   // Start playback automatically?
        0,      // Flags.
        NULL,   // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



<span data-ttu-id="6e3c1-129">La función [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) crea una nueva instancia del objeto MFPlay Player.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-129">The [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function creates a new instance of the MFPlay player object.</span></span> <span data-ttu-id="6e3c1-130">La función toma los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6e3c1-130">The function takes the following parameters:</span></span>

-   <span data-ttu-id="6e3c1-131">El primer parámetro es la dirección URL del archivo que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-131">The first parameter is the URL of the file to open.</span></span> <span data-ttu-id="6e3c1-132">Puede ser un archivo local o un archivo en un servidor multimedia.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-132">This can be a local file or a file on a media server.</span></span>
-   <span data-ttu-id="6e3c1-133">El segundo parámetro especifica si la reproducción se inicia automáticamente.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-133">The second parameter specifies whether playback starts automatically.</span></span> <span data-ttu-id="6e3c1-134">Al establecer este valor de parámetros en **true**, el archivo se reproducirá en cuanto MFPlay lo cargue.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-134">By setting this paremeter to **TRUE**, the file will play as soon as MFPlay loads it.</span></span>
-   <span data-ttu-id="6e3c1-135">El tercer parámetro establece varias opciones.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-135">The third parameter sets various options.</span></span> <span data-ttu-id="6e3c1-136">Para las opciones predeterminadas, pase cero (0).</span><span class="sxs-lookup"><span data-stu-id="6e3c1-136">For the default options, pass zero (0).</span></span>
-   <span data-ttu-id="6e3c1-137">El cuarto parámetro es un puntero a una interfaz de devolución de llamada opcional.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-137">The fourth parameter is a pointer to an optional callback interface.</span></span> <span data-ttu-id="6e3c1-138">Este parámetro puede ser **null**, como se muestra.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-138">This parameter can be **NULL**, as shown.</span></span> <span data-ttu-id="6e3c1-139">La devolución de llamada se describe en la sección [recepción de eventos del reproductor](#receiving-events-from-the-player).</span><span class="sxs-lookup"><span data-stu-id="6e3c1-139">The callback is described in the section [Receiving Events From the Player](#receiving-events-from-the-player).</span></span>
-   <span data-ttu-id="6e3c1-140">El quinto parámetro es un identificador de la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-140">The fifth parameter is a handle to the application window.</span></span> <span data-ttu-id="6e3c1-141">Si el archivo multimedia contiene una secuencia de vídeo, el vídeo aparecerá dentro del área de cliente de esta ventana.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-141">If the media file contains a video stream, the video will appear inside the client area of this window.</span></span> <span data-ttu-id="6e3c1-142">Para la reproducción de solo audio, este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-142">For audio-only playback, this parameter can be **NULL**.</span></span>

<span data-ttu-id="6e3c1-143">El último parámetro recibe un puntero a la interfaz [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) del objeto Player.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-143">The last parameter receives a pointer to the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span>

<span data-ttu-id="6e3c1-144">Antes de que se cierre la aplicación, asegúrese de liberar el puntero [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-144">Before the application shuts down, be sure to release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) pointer.</span></span> <span data-ttu-id="6e3c1-145">Puede hacerlo en el controlador de mensajes de **\_ cierre de WM** .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-145">You can do this in your **WM\_CLOSE** message handler.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> <span data-ttu-id="6e3c1-146">En este ejemplo se usa la función [SafeRelease](saferelease.md) para liberar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-146">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="6e3c1-147">Para una reproducción de vídeo sencilla, todo el código que necesita.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-147">For simple video playback, that's all the code you need.</span></span> <span data-ttu-id="6e3c1-148">En el resto de este tutorial se muestra cómo agregar más características, empezando por el modo de controlar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-148">The rest of this tutorial will show how to add more features, starting with how to control playback.</span></span>

## <a name="controlling-playback"></a><span data-ttu-id="6e3c1-149">Controlar la reproducción</span><span class="sxs-lookup"><span data-stu-id="6e3c1-149">Controlling Playback</span></span>

<span data-ttu-id="6e3c1-150">El código mostrado en la sección anterior reproducirá el archivo multimedia hasta que llegue al final del archivo.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-150">The code shown in the previous section will play the media file until it reaches the end of the file.</span></span> <span data-ttu-id="6e3c1-151">Puede detener e iniciar la reproducción llamando a los métodos siguientes en la interfaz [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) :</span><span class="sxs-lookup"><span data-stu-id="6e3c1-151">You can stop and start playback by calling the following methods on the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface:</span></span>

-   <span data-ttu-id="6e3c1-152">[**IMFPMediaPlayer::P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) pone en pausa la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-152">[**IMFPMediaPlayer::Pause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) pauses playback.</span></span> <span data-ttu-id="6e3c1-153">Mientras se pausa la reproducción, se muestra el fotograma de vídeo más reciente y el audio es silencioso.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-153">While playback is paused, the most recent video frame is displayed, and audio is silent.</span></span>
-   <span data-ttu-id="6e3c1-154">[**IMFPMediaPlayer:: Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) detiene la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-154">[**IMFPMediaPlayer::Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) stops playback.</span></span> <span data-ttu-id="6e3c1-155">No se muestra ningún vídeo y la posición de reproducción se restablece al inicio del archivo.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-155">No video is displayed, and the playback position resets to the start of the file.</span></span>
-   <span data-ttu-id="6e3c1-156">[**IMFPMediaPlayer::P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) se reanuda la reproducción después de detenerse o pausarse.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-156">[**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) resumes playback after stopping or pausing.</span></span>

<span data-ttu-id="6e3c1-157">El código siguiente pausa o reanuda la reproducción al presionar la **barra espaciadora**.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-157">The following code pauses or resumes playback when you press the **SPACEBAR**.</span></span>


```C++
//-------------------------------------------------------------------
// OnKeyDown
//
// Handles the WM_KEYDOWN message.
//-------------------------------------------------------------------

void OnKeyDown(HWND hwnd, UINT vk, BOOL fDown, int cRepeat, UINT flags)
{
    HRESULT hr = S_OK;

    switch (vk)
    {
    case VK_SPACE:

        // Toggle between playback and paused/stopped.
        if (g_pPlayer)
        {
            MFP_MEDIAPLAYER_STATE state = MFP_MEDIAPLAYER_STATE_EMPTY;
            
            g_pPlayer->GetState(&state);

            if (state == MFP_MEDIAPLAYER_STATE_PAUSED ||  
                state == MFP_MEDIAPLAYER_STATE_STOPPED)
            {
                g_pPlayer->Play();
            }
            else if (state == MFP_MEDIAPLAYER_STATE_PLAYING)
            {
                g_pPlayer->Pause();
            }
        }
        break;
    }
}
```



<span data-ttu-id="6e3c1-158">En este ejemplo se llama al método [**IMFPMediaPlayer:: GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) para obtener el estado de reproducción actual (en pausa, detenido o en reproducción) y se pone en pausa o se reanuda en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-158">This example calls the [**IMFPMediaPlayer::GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) method to get the current playback state (paused, stopped, or playing) and pauses or resumes accordingly.</span></span>

## <a name="receiving-events-from-the-player"></a><span data-ttu-id="6e3c1-159">Recibir eventos del reproductor</span><span class="sxs-lookup"><span data-stu-id="6e3c1-159">Receiving Events From the Player</span></span>

<span data-ttu-id="6e3c1-160">MFPlay usa una interfaz de devolución de llamada para enviar eventos a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-160">MFPlay uses a callback interface to send events to your application.</span></span> <span data-ttu-id="6e3c1-161">Existen dos razones para esta devolución de llamada:</span><span class="sxs-lookup"><span data-stu-id="6e3c1-161">There are two reasons for this callback:</span></span>

-   <span data-ttu-id="6e3c1-162">La reproducción se produce en un subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-162">Playback occurs on a separate thread.</span></span> <span data-ttu-id="6e3c1-163">Durante la reproducción, pueden producirse ciertos eventos, como alcanzar el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-163">During playback, certain events might occur, such as reaching the end of the file.</span></span> <span data-ttu-id="6e3c1-164">MFPlay utiliza la devolución de llamada para notificar a la aplicación el evento.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-164">MFPlay uses the callback to notify your application of the event.</span></span>
-   <span data-ttu-id="6e3c1-165">Muchos de los métodos [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) son asincrónicos, lo que significa que devuelven antes de que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-165">Many of the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) methods are asynchronous, meaning they return before the operation completes.</span></span> <span data-ttu-id="6e3c1-166">Los métodos asincrónicos permiten iniciar una operación desde el subproceso de interfaz de usuario que puede tardar mucho tiempo en completarse, sin que provoque que la interfaz de usuario se bloquee.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-166">Asynchronous methods let you start an operation from your UI thread that might take a long time to complete, without it causing your UI to block.</span></span> <span data-ttu-id="6e3c1-167">Una vez finalizada la operación, MFPlay señala la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-167">After the operation completes, MFPlay signals the callback.</span></span>

<span data-ttu-id="6e3c1-168">Para recibir notificaciones de devolución de llamada, implemente la interfaz [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-168">To receive callback notifications, implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="6e3c1-169">Esta interfaz hereda **IUnknown** y define un método único, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="6e3c1-169">This interface inherits **IUnknown** and defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="6e3c1-170">Para configurar la devolución de llamada, pase un puntero a la implementación de **IMFPMediaPlayerCallback** en el parámetro *pCallback* de la función [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-170">To set up the callback, pass a pointer to your **IMFPMediaPlayerCallback** implementation in the *pCallback* parameter of the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>

<span data-ttu-id="6e3c1-171">Este es el primer ejemplo de este tutorial, modificado para incluir la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-171">Here is the first example from this tutorial, modified to include the callback.</span></span>


```
// Global variables.
IMFPMediaPlayer *g_pPlayer = NULL;
IMFPMediaPlayerCallback *g_pCallback = NULL;

// Call an application-defined function to create the callback object.
hr = CreateMyCallback(&g_pCallback);

// Create the player object and play a video file.

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

if (SUCCEEDED(hr))
{
    hr = MFPCreateMediaPlayer(
        sURL,
        TRUE,        // Start playback automatically?
        0,           // Flags.
        g_pCallback, // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



<span data-ttu-id="6e3c1-172">El método [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) tiene un único parámetro, que es un puntero a la estructura de [**\_ \_ encabezado del evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-172">The [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method has a single parameter, which is a pointer to the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="6e3c1-173">El miembro **eEventType** de esta estructura indica qué evento se ha producido.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-173">The **eEventType** member of this structure tells you which event occurred.</span></span> <span data-ttu-id="6e3c1-174">Por ejemplo, cuando se inicia la reproducción, MFPlay envía el evento de **\_ reproducción del \_ tipo \_ de evento MFP** .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-174">For example, when playback starts, MFPlay sends the **MFP\_EVENT\_TYPE\_PLAY** event.</span></span>

<span data-ttu-id="6e3c1-175">Cada tipo de evento tiene una estructura de datos correspondiente que contiene información para ese evento.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-175">Each event type has a corresponding data structure that contains information for that event.</span></span> <span data-ttu-id="6e3c1-176">Cada una de estas estructuras comienza con una estructura de [**\_ \_ encabezado de evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-176">Each of these structures starts with an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="6e3c1-177">En la devolución de llamada, convierta el puntero de **\_ \_ encabezado de evento MFP** en la estructura de datos específica del evento.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-177">In your callback, cast the **MFP\_EVENT\_HEADER** pointer to the event-specific data structure.</span></span> <span data-ttu-id="6e3c1-178">Por ejemplo, si el tipo de evento es el **\_ \_ evento de reproducción de MFP**, la estructura de datos es el [**\_ \_ evento de reproducción de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span><span class="sxs-lookup"><span data-stu-id="6e3c1-178">For example, if the event type is **MFP\_PLAY\_EVENT**, the data structure is [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span></span> <span data-ttu-id="6e3c1-179">En el código siguiente se muestra cómo controlar este evento en la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-179">The following code shows how to handle this event in the callback.</span></span>


```
void STDMETHODCALLTYPE MediaPlayerCallback::OnMediaPlayerEvent(
    MFP_EVENT_HEADER *pEventHeader
    )
{
    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_PLAY:
        OnPlay(MFP_GET_PLAY_EVENT(pEventHeader));
        break;

    // Other event types (not shown).

    }
}

// Function to handle the event.
void OnPlay(MFP_PLAY_EVENT *pEvent)
{
    if (FAILED(pEvent->header.hrEvent))
    {  
        // Error occurred during playback.
    }  
}
```



<span data-ttu-id="6e3c1-180">En este ejemplo se usa el evento de [**\_ \_ \_ evento MFP Get Play**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) para convertir el puntero *PEventHeader* en una estructura de [**\_ \_ evento MFP Play**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-180">This example uses the [**MFP\_GET\_PLAY\_EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) event to cast the *pEventHeader* pointer to an [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) structure.</span></span> <span data-ttu-id="6e3c1-181">El **valor HRESULT** de la operación que desencadenó el evento se almacena en el campo **hrEvent** de la estructura.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-181">The **HRESULT** from the operation that triggered the event is stored in the **hrEvent** field of the structure.</span></span>

<span data-ttu-id="6e3c1-182">Para obtener una lista de todos los tipos de evento y las estructuras de datos correspondientes, vea [**\_ \_ tipo de evento MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span><span class="sxs-lookup"><span data-stu-id="6e3c1-182">For a list of all the event types and the corresponding data structures, see [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span></span>

<span data-ttu-id="6e3c1-183">Nota sobre el subprocesamiento: de forma predeterminada, MFPlay invoca la devolución de llamada del mismo subproceso que llamó a [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span><span class="sxs-lookup"><span data-stu-id="6e3c1-183">A note about threading: By default, MFPlay invokes the callback from the same thread that called [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span></span> <span data-ttu-id="6e3c1-184">Este subproceso debe tener un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-184">This thread must have a message loop.</span></span> <span data-ttu-id="6e3c1-185">Como alternativa, puede pasar la **opción MFP \_ \_ Free \_ threaded \_ callback** Flag en el parámetro *creationOptions* de **MFPCreateMediaPlayer**.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-185">Alternatively, you can pass the **MFP\_OPTION\_FREE\_THREADED\_CALLBACK** flag in the *creationOptions* parameter of **MFPCreateMediaPlayer**.</span></span> <span data-ttu-id="6e3c1-186">Esta marca hace que MFPlay invoque devoluciones de llamada desde un subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-186">This flag causes MFPlay to invoke callbacks from a separate thread.</span></span> <span data-ttu-id="6e3c1-187">Ambas opciones tienen implicaciones en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-187">Either option has implications for your application.</span></span> <span data-ttu-id="6e3c1-188">La opción predeterminada significa que la devolución de llamada no puede hacer nada que espere en el bucle de mensajes, como esperar una acción de la interfaz de usuario, porque bloqueará el procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-188">The default option means your callback cannot do anything that waits on your message loop, such as waiting for a UI action, because that will block your window procedure.</span></span> <span data-ttu-id="6e3c1-189">La opción de subprocesamiento libre significa que es necesario usar secciones críticas para proteger los datos a los que se tiene acceso en la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-189">The free-threaded option means you need to use critical sections to protect any data that you access in your callback.</span></span> <span data-ttu-id="6e3c1-190">En la mayoría de los casos, la opción predeterminada es más sencilla.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-190">In most cases, the default option is simplest.</span></span>

## <a name="getting-information-about-a-media-file"></a><span data-ttu-id="6e3c1-191">Obtención de información acerca de un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="6e3c1-191">Getting Information About a Media File</span></span>

<span data-ttu-id="6e3c1-192">Al abrir un archivo multimedia en MFPlay, el reproductor crea un objeto denominado *elemento multimedia* que representa el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-192">When you open a media file in MFPlay, the player creates an object called a *media item* that represents the media file.</span></span> <span data-ttu-id="6e3c1-193">Este objeto expone la interfaz [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , que puede usar para obtener información sobre el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-193">This object exposes the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which you can use to get information about the media file.</span></span> <span data-ttu-id="6e3c1-194">Muchas de las estructuras de eventos MFPlay contienen un puntero al elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-194">Many of the MFPlay event structures contain a pointer to the current media item.</span></span> <span data-ttu-id="6e3c1-195">También puede obtener el elemento multimedia actual llamando a [**IMFPMediaPlayer:: GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) en el reproductor.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-195">You can also get the current media item by calling [**IMFPMediaPlayer::GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) on the player.</span></span>

<span data-ttu-id="6e3c1-196">Dos métodos especialmente útiles son [**IMFPMediaItem:: HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) y [**IMFPMediaItem:: HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span><span class="sxs-lookup"><span data-stu-id="6e3c1-196">Two particularly useful methods are [**IMFPMediaItem::HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) and [**IMFPMediaItem::HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span></span> <span data-ttu-id="6e3c1-197">Estos métodos consultan si el origen multimedia contiene vídeo o audio.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-197">These methods query whether the media source contains video or audio.</span></span>

<span data-ttu-id="6e3c1-198">Por ejemplo, el código siguiente comprueba si el archivo multimedia actual contiene una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-198">For example, the following code tests whether the current media file contains a video stream.</span></span>


```
IMFPMediaItem *pItem;
BOOL bHasVideo = FALSE;
BOOL bIsSelected = FALSE;

hr = g_pPlayer->GetMediaItem(TRUE, &pItem);
if (SUCCEEDED(hr))
{
    hr = pItem->HasVideo(&bHasVideo, &bIsSelected);
    pItem->Release();
}
```



<span data-ttu-id="6e3c1-199">Si el archivo de origen contiene una secuencia de vídeo seleccionada para la reproducción, *bHasVideo* y *bIsSelected* se establecen en **true**.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-199">If the source file contains a video stream that is selected for playback, *bHasVideo* and *bIsSelected* are both set to **TRUE**.</span></span>

## <a name="managing-video-playback"></a><span data-ttu-id="6e3c1-200">Administrar la reproducción de vídeo</span><span class="sxs-lookup"><span data-stu-id="6e3c1-200">Managing Video Playback</span></span>

<span data-ttu-id="6e3c1-201">Cuando MFPlay reproduce un archivo de vídeo, lo dibuja en la ventana que especificó en la función [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-201">When MFPlay plays a video file, it draws the video in the window that you specified in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span> <span data-ttu-id="6e3c1-202">Esto sucede en un subproceso independiente propiedad de la canalización de reproducción Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-202">This occurs on a separate thread owned by the Microsoft Media Foundation playback pipeline.</span></span> <span data-ttu-id="6e3c1-203">En su mayor parte, no es necesario que la aplicación administre este proceso.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-203">For the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="6e3c1-204">Sin embargo, hay dos situaciones en las que la aplicación debe notificar a MFPlay para actualizar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-204">However, there are two situations where the application must notify MFPlay to update the video.</span></span>

-   <span data-ttu-id="6e3c1-205">Si la reproducción está en pausa o se detiene, se debe notificar a MFPlay cada vez que la ventana de vídeo de la aplicación recibe un mensaje de dibujo de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-205">If playback is paused or stopped, MFPlay must be notified whenever the application's video window receives a WM\_PAINT message.</span></span> <span data-ttu-id="6e3c1-206">Esto permite que MFPlay vuelva a dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-206">This allows MFPlay to repaint the window.</span></span>
-   <span data-ttu-id="6e3c1-207">Si se cambia el tamaño de la ventana, se debe notificar a MFPlay para que pueda escalar el vídeo para que coincida con el nuevo tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-207">If the window is resized, MFPlay must be notified so that it can scale the video to match the new window size.</span></span>

<span data-ttu-id="6e3c1-208">El método [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) controla ambos casos.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-208">The [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method handles both cases.</span></span> <span data-ttu-id="6e3c1-209">Llame a este método dentro de los \_ \_ controladores de mensajes de tamaño de WM y de WM para la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-209">Call this method inside both the WM\_PAINT and WM\_SIZE message handlers for the video window.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e3c1-210">Llame a la función **BeginPaint** de GDI antes de llamar a [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span><span class="sxs-lookup"><span data-stu-id="6e3c1-210">Call the GDI **BeginPaint** function before calling [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span>

 


```
IMFPMediaPlayer *g_pPlayer;   // MFPlay player object

void OnSize(HWND hwnd, UINT state, int cx, int cy)
{
    HDC hdc;
    PAINTSTRUCT ps;

    if (g_pPlayer && (state == SIZE_RESTORED))
    {
        hdc = BeginPaint(hwnd, &ps);
        g_pPlayer->UpdateVideo();
         EndPaint(hwnd, &ps);
    }
}

void OnPaint(HWND hwnd)
{
    HDC hdc;
    PAINTSTRUCT ps;

    hdc = BeginPaint(hwnd, &ps);
    if (g_pPlayer)
    {
        g_pPlayer->UpdateVideo();
    }
      EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="6e3c1-211">A menos que especifique lo contrario, MFPlay muestra el vídeo con la relación de aspecto correcta, mediante el uso de la panorámica si es necesario.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-211">Unless you specify otherwise, MFPlay shows the video at the correct aspect ratio, using letterboxing if needed.</span></span> <span data-ttu-id="6e3c1-212">Si no desea conservar la relación de aspecto, llame a [**IMFPMediaPlayer:: SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) con la marca **MFVideoARMode \_ None** .</span><span class="sxs-lookup"><span data-stu-id="6e3c1-212">If you do not want to preserve the aspect ratio, call [**IMFPMediaPlayer::SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) with the **MFVideoARMode\_None** flag.</span></span> <span data-ttu-id="6e3c1-213">Esto hará que MFPlay estire el vídeo para rellenar todo el rectángulo, sin ninguna panorámica.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-213">This will cause MFPlay to stretch the video to fill the entire rectangle, with no letterboxing.</span></span> <span data-ttu-id="6e3c1-214">Normalmente, debe usar la configuración predeterminada y dejar que MFPlay la panorámica del vídeo.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-214">Typically you should use the default setting and let MFPlay letterbox the video.</span></span> <span data-ttu-id="6e3c1-215">El color de pantalla ancha predeterminado es negro, pero puede cambiarlo llamando a [**IMFPMediaPlayer:: SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span><span class="sxs-lookup"><span data-stu-id="6e3c1-215">The default letterbox color is black, but you can change this by calling [**IMFPMediaPlayer::SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span></span>

## <a name="limitations-of-mfplay"></a><span data-ttu-id="6e3c1-216">Limitaciones de MFPlay</span><span class="sxs-lookup"><span data-stu-id="6e3c1-216">Limitations of MFPlay</span></span>

<span data-ttu-id="6e3c1-217">La versión actual de MFPlay tiene las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="6e3c1-217">The current version of MFPlay has the following limitations:</span></span>

-   <span data-ttu-id="6e3c1-218">MFPlay no admite contenido protegido con DRM.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-218">MFPlay does not support DRM-protected content.</span></span>
-   <span data-ttu-id="6e3c1-219">De forma predeterminada, MFPlay no admite protocolos de transmisión por secuencias de red.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-219">By default, MFPlay does not support network streaming protocols.</span></span> <span data-ttu-id="6e3c1-220">Para obtener más información, vea [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span><span class="sxs-lookup"><span data-stu-id="6e3c1-220">For more information, see [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span>
-   <span data-ttu-id="6e3c1-221">MFPlay no admite listas de reproducción del lado servidor (SSPLs) ni otros tipos de origen que reproduzcan más de un segmento.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-221">MFPlay does not support server-side playlists (SSPLs) or other types of source that play more than one segment.</span></span> <span data-ttu-id="6e3c1-222">En términos técnicos, MFPlay detiene la reproducción después de la primera presentación y omite cualquier evento [MENewPresentation](menewpresentation.md) del origen de medios.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-222">In technical terms, MFPlay stops playback after the first presentation, and ignores any [MENewPresentation](menewpresentation.md) events from the media source.</span></span>
-   <span data-ttu-id="6e3c1-223">MFPlay no admite transiciones sin problemas entre orígenes de medios.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-223">MFPlay does not support seamless transitions between media sources.</span></span>
-   <span data-ttu-id="6e3c1-224">MFPlay no admite la combinación de varias secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-224">MFPlay does not support mixing multiple video streams.</span></span>
-   <span data-ttu-id="6e3c1-225">MFPlay solo admite formatos multimedia compatibles de forma nativa en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6e3c1-225">Only media formats supported natively in Media Foundation are supported by MFPlay.</span></span> <span data-ttu-id="6e3c1-226">(Esto incluye componentes de Media Foundation de terceros que podrían estar instalados en el sistema).</span><span class="sxs-lookup"><span data-stu-id="6e3c1-226">(This includes third-party Media Foundation components that might be installed on the system.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e3c1-227">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e3c1-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e3c1-228">Uso de MFPlay para la reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="6e3c1-228">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



