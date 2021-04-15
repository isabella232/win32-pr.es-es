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
# <a name="step-1-declare-the-cplayer-class"></a><span data-ttu-id="becb3-103">Paso 1: declarar la clase CPlayer</span><span class="sxs-lookup"><span data-stu-id="becb3-103">Step 1: Declare the CPlayer Class</span></span>

<span data-ttu-id="becb3-104">Este tema es el paso 1 del tutorial [sobre cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="becb3-104">This topic is step 1 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="becb3-105">El código completo se muestra en el tema [ejemplo de reproducción de sesión de medio](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="becb3-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="becb3-106">En este tutorial, la funcionalidad de reproducción se encapsula en la `CPlayer` clase.</span><span class="sxs-lookup"><span data-stu-id="becb3-106">In this tutorial, playback functionality is encapsulated in the `CPlayer` class.</span></span> <span data-ttu-id="becb3-107">La clase `CPlayer` se declara de la forma siguiente:</span><span class="sxs-lookup"><span data-stu-id="becb3-107">The `CPlayer` class is declared as follows:</span></span>


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



<span data-ttu-id="becb3-108">Estos son algunos aspectos que se deben tener en cuenta `CPlayer` :</span><span class="sxs-lookup"><span data-stu-id="becb3-108">Here are some things to note about `CPlayer`:</span></span>

-   <span data-ttu-id="becb3-109">El **evento de \_ \_ reproductor de \_ aplicaciones de WM** constante define un mensaje de ventana privada.</span><span class="sxs-lookup"><span data-stu-id="becb3-109">The constant **WM\_APP\_PLAYER\_EVENT** defines a private window message.</span></span> <span data-ttu-id="becb3-110">Este mensaje se utiliza para notificar a la aplicación sobre eventos de sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="becb3-110">This message is used to notify the application about Media Session events.</span></span> <span data-ttu-id="becb3-111">Vea [paso 5: controlar eventos de sesión multimedia](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="becb3-111">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>
-   <span data-ttu-id="becb3-112">La `PlayerState` enumeración define los posibles estados del `CPlayer` objeto.</span><span class="sxs-lookup"><span data-stu-id="becb3-112">The `PlayerState` enumeration defines the possible states of the `CPlayer` object.</span></span>
-   <span data-ttu-id="becb3-113">La `CPlayer` clase implementa la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , que se usa para obtener notificaciones de eventos de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="becb3-113">The `CPlayer` class implements the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which is used to get event notifications from the Media Session.</span></span>
-   <span data-ttu-id="becb3-114">El `CPlayer` constructor es privado.</span><span class="sxs-lookup"><span data-stu-id="becb3-114">The `CPlayer` constructor is private.</span></span> <span data-ttu-id="becb3-115">La aplicación llama al `CreateInstance` método estático para crear una instancia de la `CPlayer` clase.</span><span class="sxs-lookup"><span data-stu-id="becb3-115">The application calls the static `CreateInstance` method to create an instance of the `CPlayer` class.</span></span>
-   <span data-ttu-id="becb3-116">El `CPlayer` destructor también es privado.</span><span class="sxs-lookup"><span data-stu-id="becb3-116">The `CPlayer` destructor is also private.</span></span> <span data-ttu-id="becb3-117">La `CPlayer` clase implementa **IUnknown**, por lo que la duración del objeto se controla a través de su recuento de referencias (*m \_ nRefCount*).</span><span class="sxs-lookup"><span data-stu-id="becb3-117">The `CPlayer` class implements **IUnknown**, so the object's lifetime is controlled through its reference count (*m\_nRefCount*).</span></span> <span data-ttu-id="becb3-118">Para destruir el objeto, la aplicación llama a **IUnknown:: Release**, no a **Delete**.</span><span class="sxs-lookup"><span data-stu-id="becb3-118">To destroy the object, the application calls **IUnknown::Release**, not **delete**.</span></span>
-   <span data-ttu-id="becb3-119">El `CPlayer` objeto administra la sesión multimedia y el origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="becb3-119">The `CPlayer` object manages both the Media Session and the media source.</span></span>

## <a name="implement-iunknown"></a><span data-ttu-id="becb3-120">Implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="becb3-120">Implement IUnknown</span></span>

<span data-ttu-id="becb3-121">La `CPlayer` clase implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), que hereda **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="becb3-121">The `CPlayer` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), which inherits **IUnknown**.</span></span>

<span data-ttu-id="becb3-122">El código que se muestra aquí es una implementación bastante estándar de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="becb3-122">The code shown here is a fairly standard implementation of **IUnknown**.</span></span> <span data-ttu-id="becb3-123">Si lo prefiere, puede usar el Active Template Library (ATL) para implementar estos métodos.</span><span class="sxs-lookup"><span data-stu-id="becb3-123">If you prefer, you can use the Active Template Library (ATL) to implement these methods.</span></span> <span data-ttu-id="becb3-124">Sin embargo, no `CPlayer` es compatible con [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ni con características com avanzadas, por lo que no hay ninguna razón ABRUMADORA para usar ATL aquí.</span><span class="sxs-lookup"><span data-stu-id="becb3-124">However, `CPlayer` does not support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or any advanced COM features, so there is no overwhelming reason to use ATL here.</span></span>


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



<span data-ttu-id="becb3-125">Siguiente: [paso 2: crear el objeto CPlayer](step-2--create-the-cplayer-object.md)</span><span class="sxs-lookup"><span data-stu-id="becb3-125">Next: [Step 2: Create the CPlayer Object](step-2--create-the-cplayer-object.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="becb3-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="becb3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="becb3-127">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="becb3-127">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="becb3-128">Cómo reproducir archivos multimedia con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="becb3-128">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
