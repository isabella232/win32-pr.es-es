---
description: La experiencia de desaconsuelo predeterminada proporcionada por el sistema achaca todos los flujos que no son de comunicación disponibles en el sistema cuando se abre un flujo de comunicación.
ms.assetid: 1b92574e-7cde-49c0-a68e-223492412361
title: Consideraciones de implementación para notificaciones de afijo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61d7e67bd456e962442f62f59c3119c756258aadd75334e7736cbc69fba0867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957324"
---
# <a name="implementation-considerations-for-ducking-notifications"></a>Consideraciones de implementación para notificaciones de afijo

La [experiencia de desaconsuelo](stream-attenuation.md) predeterminada proporcionada por el sistema achaca todos los flujos que no son de comunicación disponibles en el sistema cuando se abre un flujo de comunicación. Una aplicación multimedia puede invalidar el control predeterminado si sabe cuándo se inicia y finaliza la sesión de comunicación.

Considere el escenario implementado por la aplicación multimedia en [el ejemplo DesaingMediaPlayer.](duckingmediaplayer.md) La aplicación pausa la secuencia de audio que está reproduciendo cuando recibe una notificación de agacha y continúa la reproducción cuando recibe una notificación de desaprobación. Los eventos de pausa y continuación se reflejan en la interfaz de usuario de la aplicación multimedia. Esto se admite a través de dos mensajes de ventana definidos por la aplicación, WM APP SESSION DUCKED y \_ WM APP \_ SESSION \_ \_ \_ \_ UNDUCKED. Las notificaciones de afijo se reciben de forma asincrónica en segundo plano y la aplicación multimedia no debe bloquear el subproceso de notificación para procesar los mensajes de ventana. Los mensajes de ventana se deben procesar en el subproceso de la interfaz de usuario.

El comportamiento de afijo funciona a través de un mecanismo de notificación. Para proporcionar una experiencia personalizada, la aplicación multimedia debe implementar la [**interfaz IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) y registrar la implementación con el sistema de audio. Tras el registro correcto, la aplicación multimedia recibe notificaciones de eventos en forma de devoluciones de llamada a través de los métodos de la interfaz . El administrador de sesión que administra la sesión de comunicación llama a [**IAudioVolumeDuckNotification::OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) cuando se abre el flujo de comunicación y, a continuación, llama a [**IAudioVolumeDuckNotification::OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) cuando la secuencia se cierra en el dispositivo de comunicación.

El código siguiente muestra una implementación de ejemplo de [**la interfaz IAudioVolumeDuckNotification.**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) Para obtener la definición de CMediaPlayer::D AptOut, consulte Getting Getting Ducking Events from a Communication Device.


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

[Experiencia de afición predeterminada](stream-attenuation.md)
</dt> <dt>

[Deshabilitación de la experiencia de afición predeterminada](disabling-the-ducking-experience.md)
</dt> <dt>

[Proporcionar un comportamiento de afijo personalizado](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Obtención de eventos de afición](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



