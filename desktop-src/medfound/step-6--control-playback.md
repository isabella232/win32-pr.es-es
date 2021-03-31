---
description: En este tema se describe el paso 6 del tutorial sobre cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: e2e3e95b-41b2-45fb-b495-0e700220e5f5
title: 'Paso 6: control de la reproducción'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdfecea3484ac6b06cc44e23fd3bd1b3235324e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908371"
---
# <a name="step-6-control-playback"></a><span data-ttu-id="3b8be-103">Paso 6: control de la reproducción</span><span class="sxs-lookup"><span data-stu-id="3b8be-103">Step 6: Control Playback</span></span>

<span data-ttu-id="3b8be-104">En este tema se describe el paso 6 del tutorial sobre [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="3b8be-104">This topic is step 6 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="3b8be-105">El código completo se muestra en el tema [ejemplo de reproducción de sesión de medio](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="3b8be-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="3b8be-106">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="3b8be-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="3b8be-107">Inicio de la reproducción</span><span class="sxs-lookup"><span data-stu-id="3b8be-107">Starting Playback</span></span>](#starting-playback)
-   [<span data-ttu-id="3b8be-108">Pausar la reproducción</span><span class="sxs-lookup"><span data-stu-id="3b8be-108">Pausing Playback</span></span>](#pausing-playback)
-   [<span data-ttu-id="3b8be-109">Detener la reproducción</span><span class="sxs-lookup"><span data-stu-id="3b8be-109">Stopping Playback</span></span>](#stopping-playback)
-   [<span data-ttu-id="3b8be-110">Volver a dibujar la ventana de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b8be-110">Repainting the Video Window</span></span>](#repainting-the-video-window)
-   [<span data-ttu-id="3b8be-111">Cambiar el tamaño de la ventana de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b8be-111">Resizing the Video Window</span></span>](#resizing-the-video-window)
-   [<span data-ttu-id="3b8be-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b8be-112">Related topics</span></span>](#related-topics)

## <a name="starting-playback"></a><span data-ttu-id="3b8be-113">Inicio de la reproducción</span><span class="sxs-lookup"><span data-stu-id="3b8be-113">Starting Playback</span></span>

<span data-ttu-id="3b8be-114">Para iniciar la reproducción, llame a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="3b8be-114">To start playback, call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="3b8be-115">En el código siguiente se muestra cómo iniciar desde la posición de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="3b8be-115">The following code shows how to start from the current playback position.</span></span>


```C++
//  Start playback from the current position. 
HRESULT CPlayer::StartPlayback()
{
    assert(m_pSession != NULL);

    PROPVARIANT varStart;
    PropVariantInit(&varStart);

    HRESULT hr = m_pSession->Start(&GUID_NULL, &varStart);
    if (SUCCEEDED(hr))
    {
        // Note: Start is an asynchronous operation. However, we
        // can treat our state as being already started. If Start
        // fails later, we'll get an MESessionStarted event with
        // an error code, and we will update our state then.
        m_state = Started;
    }
    PropVariantClear(&varStart);
    return hr;
}

//  Start playback from paused or stopped.
HRESULT CPlayer::Play()
{
    if (m_state != Paused && m_state != Stopped)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }
    return StartPlayback();
}

```



<span data-ttu-id="3b8be-116">El método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) también puede especificar una posición de inicio relativa al inicio del archivo; Consulte el tema de referencia de la API para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3b8be-116">The [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method can also specify a starting position relative to the start of the file; see the API reference topic for more information.</span></span>

## <a name="pausing-playback"></a><span data-ttu-id="3b8be-117">Pausar la reproducción</span><span class="sxs-lookup"><span data-stu-id="3b8be-117">Pausing Playback</span></span>

<span data-ttu-id="3b8be-118">Para pausar la reproducción, llame a [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span><span class="sxs-lookup"><span data-stu-id="3b8be-118">To pause playback, call [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span></span>


```C++
//  Pause playback.
HRESULT CPlayer::Pause()    
{
    if (m_state != Started)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = Paused;
    }

    return hr;
}
```



## <a name="stopping-playback"></a><span data-ttu-id="3b8be-119">Detener la reproducción</span><span class="sxs-lookup"><span data-stu-id="3b8be-119">Stopping Playback</span></span>

<span data-ttu-id="3b8be-120">Para detener la reproducción, llame a [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="3b8be-120">To stop playback, call [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span> <span data-ttu-id="3b8be-121">Mientras se detiene la reproducción, se borra la imagen de vídeo y la ventana de vídeo se pinta con el color de fondo (de forma predeterminada, de forma predeterminada).</span><span class="sxs-lookup"><span data-stu-id="3b8be-121">While playback is stopped, the video image is cleared and the video window is painted with the background color (black by default).</span></span>


```C++
// Stop playback.
HRESULT CPlayer::Stop()
{
    if (m_state != Started && m_state != Paused)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = Stopped;
    }
    return hr;
}
```



## <a name="repainting-the-video-window"></a><span data-ttu-id="3b8be-122">Volver a dibujar la ventana de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b8be-122">Repainting the Video Window</span></span>

<span data-ttu-id="3b8be-123">El [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR) dibuja el vídeo en la ventana especificada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b8be-123">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) draws the video in the window specified by the application.</span></span> <span data-ttu-id="3b8be-124">Esto se produce en un subproceso independiente y, en la mayoría de los casos, no es necesario que la aplicación administre este proceso.</span><span class="sxs-lookup"><span data-stu-id="3b8be-124">This occurs on a separate thread, and for the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="3b8be-125">Sin embargo, si la reproducción está en pausa o se detiene, se debe notificar a EVR siempre que la ventana de vídeo reciba un mensaje de [**\_ dibujo de WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="3b8be-125">If playback is paused or stopped, however, the EVR must be notified whenever the video window receives a [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="3b8be-126">Esto permite que EVR vuelva a dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="3b8be-126">This allows the EVR to repaint the window.</span></span> <span data-ttu-id="3b8be-127">Para notificar a EVR, llame al método [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) :</span><span class="sxs-lookup"><span data-stu-id="3b8be-127">To notify the EVR, call the [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) method:</span></span>


```C++
//  Repaint the video window. Call this method on WM_PAINT.

HRESULT CPlayer::Repaint()
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="3b8be-128">En el código siguiente se muestra el controlador del mensaje de [**\_ Paint de WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="3b8be-128">The following code shows the handler for the [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="3b8be-129">Se debe llamar a esta función desde el bucle de mensajes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b8be-129">This function should be called from the application's message loop.</span></span>


```C++
//  Handler for WM_PAINT messages.
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_pPlayer->HasVideo())
    {
        // Video is playing. Ask the player to repaint.
        g_pPlayer->Repaint();
    }
    else
    {
        // The video is not playing, so we must paint the application window.
        RECT rc;
        GetClientRect(hwnd, &rc);
        FillRect(hdc, &rc, (HBRUSH) COLOR_WINDOW);
    }
    EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="3b8be-130">El `HasVideo` método devuelve **true** si el `CPlayer` objeto tiene un puntero [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) válido.</span><span class="sxs-lookup"><span data-stu-id="3b8be-130">The `HasVideo` method returns **TRUE** if the `CPlayer` object has a valid [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) pointer.</span></span> <span data-ttu-id="3b8be-131">(Consulte [paso 1: declarar la clase CPlayer](step-1--declare-the-cplayer-class.md)).</span><span class="sxs-lookup"><span data-stu-id="3b8be-131">(See [Step 1: Declare the CPlayer Class](step-1--declare-the-cplayer-class.md).)</span></span>


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a><span data-ttu-id="3b8be-132">Cambiar el tamaño de la ventana de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b8be-132">Resizing the Video Window</span></span>

<span data-ttu-id="3b8be-133">Si cambia el tamaño de la ventana de vídeo, actualice el rectángulo de destino en el EVR llamando al método [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) :</span><span class="sxs-lookup"><span data-stu-id="3b8be-133">If you resize the video window, update the destination rectangle on the EVR by calling the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method:</span></span>


```C++
//  Resize the video rectangle.
//
//  Call this method if the size of the video window changes.

HRESULT CPlayer::ResizeVideo(WORD width, WORD height)
{
    if (m_pVideoDisplay)
    {
        // Set the destination rectangle.
        // Leave the default source rectangle (0,0,1,1).

        RECT rcDest = { 0, 0, width, height };

        return m_pVideoDisplay->SetVideoPosition(NULL, &rcDest);
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="3b8be-134">Siguiente: [paso 7: apagar la sesión multimedia](step-7--shut-down-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="3b8be-134">Next: [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b8be-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b8be-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b8be-136">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="3b8be-136">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="3b8be-137">Cómo reproducir archivos multimedia con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3b8be-137">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
