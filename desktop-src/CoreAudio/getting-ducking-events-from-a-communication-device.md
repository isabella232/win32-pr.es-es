---
description: Una aplicación multimedia que quiera proporcionar una experiencia de afijo personalizada debe escuchar las notificaciones de eventos cuando se abre o cierra un flujo de comunicación en el sistema.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Obtención de eventos de afición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5869aa02a64ef3b7d035743b9bee3c91d295448c4d89d659862c5efc81d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828266"
---
# <a name="getting-ducking-events"></a>Obtención de eventos de afición

Una aplicación multimedia que quiera proporcionar una experiencia de afijo personalizada debe escuchar las notificaciones de eventos cuando se abre o cierra un flujo de comunicación en el sistema. La implementación personalizada se puede proporcionar mediante MediaFoundation, DirectShow o Direct Sound, que usan las API core audio. Un cliente WASAPI directo también puede invalidar el control predeterminado si sabe cuándo se inicia y finaliza la sesión de comunicación.

Para proporcionar una implementación personalizada, una aplicación multimedia debe recibir notificaciones del sistema cuando una aplicación de comunicación inicia o finaliza un flujo de comunicación. La aplicación multimedia debe implementar la [**interfaz IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) y registrar la implementación con el sistema de audio. Tras el registro correcto, la aplicación multimedia recibe notificaciones de eventos en forma de devoluciones de llamada a través de los métodos de la interfaz . Para obtener más información, vea [Consideraciones de implementación para notificaciones de atajo.](handling-audio-ducking-events-from-communication-devices.md)

Para enviar notificaciones de afijo, el sistema de audio debe saber qué sesión de audio está escuchando los eventos de afijo. Cada sesión de audio se identifica de forma única con un GUID: identificador de instancia de sesión. El administrador de sesiones permite a una aplicación obtener información sobre la sesión, como el título de la sesión de audio, el estado de representación y el identificador de instancia de sesión. El identificador se puede recuperar mediante la interfaz de control de directivas, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).

En los pasos siguientes se resume el proceso de obtención del identificador de instancia de sesión de la aplicación multimedia:

1.  Cree una instancia del enumerador de dispositivos y úselo para obtener una referencia al punto de conexión del dispositivo que usa la aplicación multimedia para representar el flujo que no es de comunicación.
2.  Active el administrador de sesión desde el punto de conexión del dispositivo y obtenga una referencia a la [**interfaz IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) del administrador de sesiones.
3.  Mediante el puntero [**IAudioSessionManager2,**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) obtenga una referencia a la [**interfaz IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) del administrador de sesiones.
4.  Consulte [**IAudioSessionControl2 desde**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) la [**interfaz IAudioSessionControl.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
5.  Llame [**a IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) y recupere una cadena que contenga el identificador de sesión de la sesión de audio actual.

Para obtener notificaciones de afijo sobre los flujos de comunicación, la aplicación multimedia llama a [**IAudioSessionManager2::RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification). La aplicación multimedia proporciona su identificador de instancia de sesión al sistema de audio y un puntero a la [**implementación de IAudioVolumeDuckNotification.**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) La aplicación ahora puede recibir una notificación de eventos cuando se abre una secuencia en el dispositivo de comunicación. Para dejar de recibir notificaciones, la aplicación multimedia debe llamar a [**IAudioSessionManager2::UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).

El código siguiente muestra cómo se puede registrar una aplicación para recibir notificaciones de afijo. La clase CMediaPlayer se define en Consideraciones de implementación [para notificaciones de atajo.](handling-audio-ducking-events-from-communication-devices.md) El [ejemplo DuckingMediaPlayer](duckingmediaplayer.md) implementa esta funcionalidad.


```C++
////////////////////////////////////////////////////////////////////
//Description: Registers for duck notifications depending on the 
//             the ducking options specified by the caller.
//Parameters: 
//    If DuckingOptOutChecked is TRUE, the client is registered for
//    to receive ducking notifications; 
//    FALSE, the client's registration is deleted.
////////////////////////////////////////////////////////////////////

HRESULT CMediaPlayer::DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;

    LPWSTR sessionId = NULL;

    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(
              eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate the session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>
                                 (&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(
                                  NULL, 0, &pSessionControl);
        
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                               IID_PPV_ARGS(&pSessionControl2));
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    // Get the session instance identifier.
    
    if (SUCCEEDED(hr))
    {
        hr = pSessionControl2->GetSessionInstanceIdentifier(
                                 sessionId);
                
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }

    //  Register for ducking events depending on 
    //  the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionManager2->RegisterDuckNotification(
                                    sessionId, this);
        }
        else
        {
            hr = pSessionManager2->UnregisterDuckNotification
                                      (FALSE);
        }
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }
    return hr;
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

[Consideraciones de implementación para notificaciones de afijo](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



