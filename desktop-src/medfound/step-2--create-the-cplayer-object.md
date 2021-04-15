---
description: En este tema se describe el paso 2 del tutorial sobre cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: 'Paso 2: crear el objeto CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021ffa383506c0ab1be8d6c1ca327f67ed8f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715483"
---
# <a name="step-2-create-the-cplayer-object"></a>Paso 2: crear el objeto CPlayer

En este tema se describe el paso 2 del tutorial sobre [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md). El código completo se muestra en el tema [ejemplo de reproducción de sesión de medio](media-session-playback-example.md).

Para crear una instancia de la `CPlayer` clase, la aplicación llama al `CPlayer::CreateInstance` método estático. Este método toma los parámetros siguientes:

-   *hVideo* especifica la ventana en la que se va a mostrar el vídeo.
-   *hEvent* especifica una ventana para recibir eventos. Es válido pasar el mismo identificador para ambos identificadores de ventana.
-   *ppPlayer* recibe un puntero a una nueva `CPlayer` instancia de.

En el código siguiente se muestra el método `CreateInstance`:


```C++
//  Static class method to create the CPlayer object.

HRESULT CPlayer::CreateInstance(
    HWND hVideo,                  // Video window.
    HWND hEvent,                  // Window to receive notifications.
    CPlayer **ppPlayer)           // Receives a pointer to the CPlayer object.
{
    if (ppPlayer == NULL)
    {
        return E_POINTER;
    }

    CPlayer *pPlayer = new (std::nothrow) CPlayer(hVideo, hEvent);
    if (pPlayer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pPlayer->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppPlayer = pPlayer;
    }
    else
    {
        pPlayer->Release();
    }
    return hr;
}

HRESULT CPlayer::Initialize()
{
    // Start up Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        m_hCloseEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
        if (m_hCloseEvent == NULL)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    return hr;
}
```



En el código siguiente se muestra el `CPlayer` constructor:


```C++
CPlayer::CPlayer(HWND hVideo, HWND hEvent) : 
    m_pSession(NULL),
    m_pSource(NULL),
    m_pVideoDisplay(NULL),
    m_hwndVideo(hVideo),
    m_hwndEvent(hEvent),
    m_state(Closed),
    m_hCloseEvent(NULL),
    m_nRefCount(1)
{
}
```



El constructor realiza lo siguiente:

1.  Llama a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar la plataforma Media Foundation.
2.  Crea un evento de restablecimiento automático. Este evento se utiliza al cerrar la sesión multimedia; vea [paso 7: apagar la sesión multimedia](step-7--shut-down-the-media-session.md).

El destructor cierra la sesión multimedia, como se describe en [el paso 7: apagar la sesión multimedia](step-7--shut-down-the-media-session.md).


```C++
CPlayer::~CPlayer()
{
    assert(m_pSession == NULL);  
    // If FALSE, the app did not call Shutdown().

    // When CPlayer calls IMediaEventGenerator::BeginGetEvent on the
    // media session, it causes the media session to hold a reference 
    // count on the CPlayer. 
    
    // This creates a circular reference count between CPlayer and the 
    // media session. Calling Shutdown breaks the circular reference 
    // count.

    // If CreateInstance fails, the application will not call 
    // Shutdown. To handle that case, call Shutdown in the destructor. 

    Shutdown();
}
```



Tenga en cuenta que el constructor y el destructor son métodos de clase protegidos. La aplicación crea el objeto mediante el `CreateInstance` método estático. Destruye el objeto llamando a **IUnknown:: Release**, en lugar de usar explícitamente **Delete**.

Siguiente: [paso 3: abrir un archivo multimedia](step-3--open-a-media-file.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> <dt>

[Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



