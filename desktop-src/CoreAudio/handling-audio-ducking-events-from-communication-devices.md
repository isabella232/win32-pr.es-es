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
# <a name="implementation-considerations-for-ducking-notifications"></a>Consideraciones de implementación para las notificaciones de patos

La [experiencia de uso de la forma predeterminada](stream-attenuation.md) que proporciona el sistema es pato en todas las secuencias que no son de comunicación disponibles en el sistema cuando se abre un flujo de comunicación. Una aplicación multimedia puede invalidar el control predeterminado si sabe cuándo se inicia y finaliza la sesión de comunicación.

Considere el escenario implementado por la aplicación multimedia en el ejemplo [DuckingMediaPlayer](duckingmediaplayer.md) . La aplicación pone en pausa la secuencia de audio que se está reproduciendo cuando recibe una notificación de Duck y continúa la reproducción cuando recibe una notificación de despato. Los eventos pausar y continuar se reflejan en la interfaz de usuario de la aplicación multimedia. Esto se admite a través de dos mensajes de ventana definidos por la aplicación, la sesión de aplicación de WM \_ \_ y la \_ sesión de aplicación de WM \_ \_ \_ unpatod. Las notificaciones de patos se reciben asincrónicamente en segundo plano y la aplicación multimedia no debe bloquear el subproceso de notificación para procesar los mensajes de ventana. Los mensajes de la ventana deben procesarse en el subproceso de la interfaz de usuario.

El comportamiento de los patos funciona a través de un mecanismo de notificación. Para proporcionar una experiencia personalizada, la aplicación multimedia debe implementar la interfaz [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) y registrar la implementación en el sistema de audio. Tras el registro correcto, la aplicación multimedia recibe notificaciones de eventos en forma de devoluciones de llamada a través de los métodos de la interfaz. El administrador de sesión que controla la sesión de comunicación llama a [**IAudioVolumeDuckNotification:: OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) cuando se abre el flujo de comunicación y, a continuación, llama a [**IAudioVolumeDuckNotification:: OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) cuando se cierra la secuencia en el dispositivo de comunicación.

En el código siguiente se muestra una implementación de ejemplo de la interfaz [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) . Para obtener la definición de CMediaPlayer::D uckingOptOut, consulte el artículo sobre la obtención de eventos de un dispositivo de comunicación.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de un dispositivo de comunicación](using-the-communication-device.md)
</dt> <dt>

[Experiencia predeterminada de los patos](stream-attenuation.md)
</dt> <dt>

[Deshabilitación de la experiencia de patos predeterminada](disabling-the-ducking-experience.md)
</dt> <dt>

[Proporcionar un comportamiento personalizado de patos](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Obtención de eventos de pato](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



