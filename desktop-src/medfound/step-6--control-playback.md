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
# <a name="step-6-control-playback"></a>Paso 6: control de la reproducción

En este tema se describe el paso 6 del tutorial sobre [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md). El código completo se muestra en el tema [ejemplo de reproducción de sesión de medio](media-session-playback-example.md).

Este tema contiene las siguientes secciones:

-   [Inicio de la reproducción](#starting-playback)
-   [Pausar la reproducción](#pausing-playback)
-   [Detener la reproducción](#stopping-playback)
-   [Volver a dibujar la ventana de vídeo](#repainting-the-video-window)
-   [Cambiar el tamaño de la ventana de vídeo](#resizing-the-video-window)
-   [Temas relacionados](#related-topics)

## <a name="starting-playback"></a>Inicio de la reproducción

Para iniciar la reproducción, llame a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). En el código siguiente se muestra cómo iniciar desde la posición de reproducción actual.


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



El método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) también puede especificar una posición de inicio relativa al inicio del archivo; Consulte el tema de referencia de la API para obtener más información.

## <a name="pausing-playback"></a>Pausar la reproducción

Para pausar la reproducción, llame a [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).


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



## <a name="stopping-playback"></a>Detener la reproducción

Para detener la reproducción, llame a [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop). Mientras se detiene la reproducción, se borra la imagen de vídeo y la ventana de vídeo se pinta con el color de fondo (de forma predeterminada, de forma predeterminada).


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



## <a name="repainting-the-video-window"></a>Volver a dibujar la ventana de vídeo

El [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR) dibuja el vídeo en la ventana especificada por la aplicación. Esto se produce en un subproceso independiente y, en la mayoría de los casos, no es necesario que la aplicación administre este proceso. Sin embargo, si la reproducción está en pausa o se detiene, se debe notificar a EVR siempre que la ventana de vídeo reciba un mensaje de [**\_ dibujo de WM**](../gdi/wm-paint.md) . Esto permite que EVR vuelva a dibujar la ventana. Para notificar a EVR, llame al método [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) :


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



En el código siguiente se muestra el controlador del mensaje de [**\_ Paint de WM**](../gdi/wm-paint.md) . Se debe llamar a esta función desde el bucle de mensajes de la aplicación.


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



El `HasVideo` método devuelve **true** si el `CPlayer` objeto tiene un puntero [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) válido. (Consulte [paso 1: declarar la clase CPlayer](step-1--declare-the-cplayer-class.md)).


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a>Cambiar el tamaño de la ventana de vídeo

Si cambia el tamaño de la ventana de vídeo, actualice el rectángulo de destino en el EVR llamando al método [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) :


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



Siguiente: [paso 7: apagar la sesión multimedia](step-7--shut-down-the-media-session.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> <dt>

[Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
