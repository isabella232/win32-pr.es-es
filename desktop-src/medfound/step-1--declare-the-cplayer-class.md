---
description: Este tema es el paso 1 del tutorial sobre cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: 10767bbf-3b47-4df1-be73-18678397c0ab
title: 'Paso 1: declarar la clase CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1593842ecece68fcd3c4cca35a7e2e28eac503c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715484"
---
# <a name="step-1-declare-the-cplayer-class"></a>Paso 1: declarar la clase CPlayer

Este tema es el paso 1 del tutorial [sobre cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md). El código completo se muestra en el tema [ejemplo de reproducción de sesión de medio](media-session-playback-example.md).

En este tutorial, la funcionalidad de reproducción se encapsula en la `CPlayer` clase. La clase `CPlayer` se declara de la forma siguiente:


```C++
const UINT WM_APP_PLAYER_EVENT = WM_APP + 1;   

    // WPARAM = IMFMediaEvent*, WPARAM = MediaEventType

enum PlayerState
{
    Closed = 0,     // No session.
    Ready,          // Session was created, ready to open a file. 
    OpenPending,    // Session is opening a file.
    Started,        // Session is playing a file.
    Paused,         // Session is paused.
    Stopped,        // Session is stopped (ready to play). 
    Closing         // Application has closed the session, but is waiting for MESessionClosed.
};

class CPlayer : public IMFAsyncCallback
{
public:
    static HRESULT CreateInstance(HWND hVideo, HWND hEvent, CPlayer **ppPlayer);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP  GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP  Invoke(IMFAsyncResult* pAsyncResult);

    // Playback
    HRESULT       OpenURL(const WCHAR *sURL);
    HRESULT       Play();
    HRESULT       Pause();
    HRESULT       Stop();
    HRESULT       Shutdown();
    HRESULT       HandleEvent(UINT_PTR pUnkPtr);
    PlayerState   GetState() const { return m_state; }

    // Video functionality
    HRESULT       Repaint();
    HRESULT       ResizeVideo(WORD width, WORD height);
    
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }

protected:
    
    // Constructor is private. Use static CreateInstance method to instantiate.
    CPlayer(HWND hVideo, HWND hEvent);

    // Destructor is private. Caller should call Release.
    virtual ~CPlayer(); 

    HRESULT Initialize();
    HRESULT CreateSession();
    HRESULT CloseSession();
    HRESULT StartPlayback();

    // Media event handlers
    virtual HRESULT OnTopologyStatus(IMFMediaEvent *pEvent);
    virtual HRESULT OnPresentationEnded(IMFMediaEvent *pEvent);
    virtual HRESULT OnNewPresentation(IMFMediaEvent *pEvent);

    // Override to handle additional session events.
    virtual HRESULT OnSessionEvent(IMFMediaEvent*, MediaEventType) 
    { 
        return S_OK; 
    }

protected:
    long                    m_nRefCount;        // Reference count.

    IMFMediaSession         *m_pSession;
    IMFMediaSource          *m_pSource;
    IMFVideoDisplayControl  *m_pVideoDisplay;

    HWND                    m_hwndVideo;        // Video window.
    HWND                    m_hwndEvent;        // App window to receive events.
    PlayerState             m_state;            // Current state of the media session.
    HANDLE                  m_hCloseEvent;      // Event to wait on while closing.
};
```



Estos son algunos aspectos que se deben tener en cuenta `CPlayer` :

-   El **evento de \_ \_ reproductor de \_ aplicaciones de WM** constante define un mensaje de ventana privada. Este mensaje se utiliza para notificar a la aplicación sobre eventos de sesión multimedia. Vea [paso 5: controlar eventos de sesión multimedia](step-5--handle-media-session-events.md).
-   La `PlayerState` enumeración define los posibles estados del `CPlayer` objeto.
-   La `CPlayer` clase implementa la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , que se usa para obtener notificaciones de eventos de la sesión multimedia.
-   El `CPlayer` constructor es privado. La aplicación llama al `CreateInstance` método estático para crear una instancia de la `CPlayer` clase.
-   El `CPlayer` destructor también es privado. La `CPlayer` clase implementa **IUnknown**, por lo que la duración del objeto se controla a través de su recuento de referencias (*m \_ nRefCount*). Para destruir el objeto, la aplicación llama a **IUnknown:: Release**, no a **Delete**.
-   El `CPlayer` objeto administra la sesión multimedia y el origen multimedia.

## <a name="implement-iunknown"></a>Implementar IUnknown

La `CPlayer` clase implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), que hereda **IUnknown**.

El código que se muestra aquí es una implementación bastante estándar de **IUnknown**. Si lo prefiere, puede usar el Active Template Library (ATL) para implementar estos métodos. Sin embargo, no `CPlayer` es compatible con [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ni con características com avanzadas, por lo que no hay ninguna razón ABRUMADORA para usar ATL aquí.


```C++
HRESULT CPlayer::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CPlayer, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

ULONG CPlayer::AddRef()
{
    return InterlockedIncrement(&m_nRefCount);
}

ULONG CPlayer::Release()
{
    ULONG uCount = InterlockedDecrement(&m_nRefCount);
    if (uCount == 0)
    {
        delete this;
    }
    return uCount;
}
```



Siguiente: [paso 2: crear el objeto CPlayer](step-2--create-the-cplayer-object.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> <dt>

[Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
