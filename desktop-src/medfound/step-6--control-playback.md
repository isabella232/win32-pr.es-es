---
description: Este tema es el paso 6 del tutorial Cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: e2e3e95b-41b2-45fb-b495-0e700220e5f5
title: 'Paso 6: Controlar la reproducción'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef0aa18f671c994837ba195cddba38976c3ffba990eb95748d2bede09141317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887265"
---
# <a name="step-6-control-playback"></a>Paso 6: Controlar la reproducción

Este tema es el paso 6 del tutorial [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md). El código completo se muestra en el tema [Ejemplo de reproducción de sesión multimedia](media-session-playback-example.md).

Este tema contiene las siguientes secciones:

-   [Inicio de la reproducción](#starting-playback)
-   [Pausar la reproducción](#pausing-playback)
-   [Detención de la reproducción](#stopping-playback)
-   [Volver a dibujar la ventana de vídeo](#repainting-the-video-window)
-   [Redimensionar la ventana de vídeo](#resizing-the-video-window)
-   [Temas relacionados](#related-topics)

## <a name="starting-playback"></a>Inicio de la reproducción

Para iniciar la reproducción, llame [**a IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). El código siguiente muestra cómo empezar desde la posición de reproducción actual.


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



El [**método Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) también puede especificar una posición inicial con respecto al inicio del archivo; Consulte el tema de referencia de API para obtener más información.

## <a name="pausing-playback"></a>Pausar la reproducción

Para pausar la reproducción, llame [**a IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).


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



## <a name="stopping-playback"></a>Detención de la reproducción

Para detener la reproducción, llame [**a IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop). Mientras se detiene la reproducción, la imagen de vídeo se borra y la ventana de vídeo se pinta con el color de fondo (negro de forma predeterminada).


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

El [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR) dibuja el vídeo en la ventana especificada por la aplicación. Esto sucede en un subproceso independiente y, en su mayor parte, la aplicación no necesita administrar este proceso. Sin embargo, si la reproducción está en pausa o detenida, se debe notificar al EVR cada vez que la ventana de vídeo reciba [**un mensaje WM \_ PAINT.**](../gdi/wm-paint.md) Esto permite que el EVR vuelva a dibujar la ventana. Para notificar al EVR, llame al [**método IMFVideoDisplayControl::RepaintVideo:**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo)


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



El código siguiente muestra el controlador para el [**mensaje \_ WM PAINT.**](../gdi/wm-paint.md) Se debe llamar a esta función desde el bucle de mensajes de la aplicación.


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



El `HasVideo` método devuelve TRUE **si** el objeto tiene un `CPlayer` puntero [**VALIDOVideoDisplayControl.**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) (Vea [Paso 1: Declarar la clase CPlayer](step-1--declare-the-cplayer-class.md)).


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a>Redimensionar la ventana de vídeo

Si cambia el tamaño de la ventana de vídeo, actualice el rectángulo de destino en el EVR mediante una llamada al método [**IMFVideoDisplayControl::SetVideoPosition:**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)


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



Siguiente: [Paso 7: Apagar la sesión multimedia](step-7--shut-down-the-media-session.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> <dt>

[Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
