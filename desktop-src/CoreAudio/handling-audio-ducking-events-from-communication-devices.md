---
description: La experiencia de uso de la forma predeterminada que proporciona el sistema es pato en todas las secuencias que no son de comunicación disponibles en el sistema cuando se abre un flujo de comunicación.
ms.assetid: 1b92574e-7cde-49c0-a68e-223492412361
title: Consideraciones de implementación para las notificaciones de patos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de07ea23b7cdc8d726ab68a5a6554bf1713a921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153214"
---
# <a name="implementation-considerations-for-ducking-notifications"></a><span data-ttu-id="0dc82-103">Consideraciones de implementación para las notificaciones de patos</span><span class="sxs-lookup"><span data-stu-id="0dc82-103">Implementation Considerations for Ducking Notifications</span></span>

<span data-ttu-id="0dc82-104">La [experiencia de uso de la forma predeterminada](stream-attenuation.md) que proporciona el sistema es pato en todas las secuencias que no son de comunicación disponibles en el sistema cuando se abre un flujo de comunicación.</span><span class="sxs-lookup"><span data-stu-id="0dc82-104">The [Default Ducking Experience](stream-attenuation.md) provided by the system ducks all non-communication streams available in the system when a communication stream opens.</span></span> <span data-ttu-id="0dc82-105">Una aplicación multimedia puede invalidar el control predeterminado si sabe cuándo se inicia y finaliza la sesión de comunicación.</span><span class="sxs-lookup"><span data-stu-id="0dc82-105">A media application can override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="0dc82-106">Considere el escenario implementado por la aplicación multimedia en el ejemplo [DuckingMediaPlayer](duckingmediaplayer.md) .</span><span class="sxs-lookup"><span data-stu-id="0dc82-106">Consider the scenario implemented by the media application in the [DuckingMediaPlayer](duckingmediaplayer.md) sample.</span></span> <span data-ttu-id="0dc82-107">La aplicación pone en pausa la secuencia de audio que se está reproduciendo cuando recibe una notificación de Duck y continúa la reproducción cuando recibe una notificación de despato.</span><span class="sxs-lookup"><span data-stu-id="0dc82-107">The application pauses the audio stream that it is playing when it receives a duck notification and continues playback when it receives an unduck notification.</span></span> <span data-ttu-id="0dc82-108">Los eventos pausar y continuar se reflejan en la interfaz de usuario de la aplicación multimedia.</span><span class="sxs-lookup"><span data-stu-id="0dc82-108">The pause and continue events are reflected in the media application's user interface.</span></span> <span data-ttu-id="0dc82-109">Esto se admite a través de dos mensajes de ventana definidos por la aplicación, la sesión de aplicación de WM \_ \_ y la \_ sesión de aplicación de WM \_ \_ \_ unpatod.</span><span class="sxs-lookup"><span data-stu-id="0dc82-109">This is supported through two application-defined window messages, WM\_APP\_SESSION\_DUCKED and WM\_APP\_SESSION\_UNDUCKED.</span></span> <span data-ttu-id="0dc82-110">Las notificaciones de patos se reciben asincrónicamente en segundo plano y la aplicación multimedia no debe bloquear el subproceso de notificación para procesar los mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="0dc82-110">The ducking notifications are received asynchronously in the background and the media application must not block the notification thread to process the window messages.</span></span> <span data-ttu-id="0dc82-111">Los mensajes de la ventana deben procesarse en el subproceso de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0dc82-111">The window messages must be processed on the user interface thread.</span></span>

<span data-ttu-id="0dc82-112">El comportamiento de los patos funciona a través de un mecanismo de notificación.</span><span class="sxs-lookup"><span data-stu-id="0dc82-112">The ducking behavior works through a notification mechanism.</span></span> <span data-ttu-id="0dc82-113">Para proporcionar una experiencia personalizada, la aplicación multimedia debe implementar la interfaz [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) y registrar la implementación en el sistema de audio.</span><span class="sxs-lookup"><span data-stu-id="0dc82-113">To provide a customized experience, the media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="0dc82-114">Tras el registro correcto, la aplicación multimedia recibe notificaciones de eventos en forma de devoluciones de llamada a través de los métodos de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="0dc82-114">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="0dc82-115">El administrador de sesión que controla la sesión de comunicación llama a [**IAudioVolumeDuckNotification:: OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) cuando se abre el flujo de comunicación y, a continuación, llama a [**IAudioVolumeDuckNotification:: OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) cuando se cierra la secuencia en el dispositivo de comunicación.</span><span class="sxs-lookup"><span data-stu-id="0dc82-115">The session manager handling the communication session calls [**IAudioVolumeDuckNotification::OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) when the communication stream opens and then calls [**IAudioVolumeDuckNotification::OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) when the stream is closed on the communication device.</span></span>

<span data-ttu-id="0dc82-116">En el código siguiente se muestra una implementación de ejemplo de la interfaz [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) .</span><span class="sxs-lookup"><span data-stu-id="0dc82-116">The following code shows a sample implementation of the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface.</span></span> <span data-ttu-id="0dc82-117">Para obtener la definición de CMediaPlayer::D uckingOptOut, consulte el artículo sobre la obtención de eventos de un dispositivo de comunicación.</span><span class="sxs-lookup"><span data-stu-id="0dc82-117">For the definition of CMediaPlayer::DuckingOptOut, see Getting Ducking Events from a Communication Device.</span></span>


```C++
class CMediaPlayer : public IAudioVolumeDuckNotification
{
    LONG _refCount;

    HWND _AppWindow;

    ~CMediaPlayer();

    STDMETHOD(OnVolumeDuckNotification) (LPCWSTR sessionID, 
                  UINT32 countCommunicationSessions);
    STDMETHOD(OnVolumeUnduckNotification) (LPCWSTR sessionID);

public:
    CDuckingImpl(HWND hWnd);
    HRESULT DuckingOptOut(bool GetDuckEvents);

    // IUnknown
    IFACEMETHODIMP QueryInterface(__in REFIID riid, __deref_out void **ppv);
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
};

CMediaPlayer::CMediaPlayer(HWND AppWindow) :
        _AppWindow(AppWindow),
        _refCount(1)
{
}
CMediaPlayer::~CMediaPlayer()
{
}

// When we receive a duck notification, 
// post a "Session Ducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeDuckNotification(LPCWSTR SessionID, 
                                                    UINT32 CountCommunicationsSessions)
{
    PostMessage(_AppWindow, WM_APP_SESSION_DUCKED, 0, 0);
    return 0;
}


// When we receive an unduck notification, 
// post a "Session Unducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeUnduckNotification(LPCWSTR SessionID)
{
    PostMessage(_AppWindow, WM_APP_SESSION_UNDUCKED, 0, 0);
    return 0;
}

IFACEMETHODIMP CMediaPlayer::QueryInterface(REFIID iid, void **pvObject)
{
    if (pvObject == NULL)
    {
        return E_POINTER;
    }
    *pvObject = NULL;
    if (iid == IID_IUnknown)
    {
        *pvObject = static_cast<IUnknown *>(static_cast<IAudioVolumeDuckNotification *>
                                                                              (this));
        AddRef();
    }
    else if (iid == __uuidof(IAudioVolumeDuckNotification))
    {
        *pvObject = static_cast<IAudioVolumeDuckNotification *>(this);
        AddRef();
    }
    else
    {
        return E_NOINTERFACE;
    }
    return S_OK;
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::AddRef()
{
    return InterlockedIncrement(&_refCount);
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::Release()
{
    LONG refs = InterlockedDecrement(&_refCount);

    if (refs == 0)
    {
        delete this; 
    }

    return refs;   
}
```



## <a name="related-topics"></a><span data-ttu-id="0dc82-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0dc82-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dc82-119">Uso de un dispositivo de comunicación</span><span class="sxs-lookup"><span data-stu-id="0dc82-119">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="0dc82-120">Experiencia predeterminada de los patos</span><span class="sxs-lookup"><span data-stu-id="0dc82-120">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="0dc82-121">Deshabilitación de la experiencia de patos predeterminada</span><span class="sxs-lookup"><span data-stu-id="0dc82-121">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="0dc82-122">Proporcionar un comportamiento personalizado de patos</span><span class="sxs-lookup"><span data-stu-id="0dc82-122">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="0dc82-123">Obtención de eventos de pato</span><span class="sxs-lookup"><span data-stu-id="0dc82-123">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



