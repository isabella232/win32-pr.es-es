---
description: Una aplicación multimedia que desea proporcionar una experiencia personalizada de pato debe escuchar las notificaciones de eventos cuando se abre o se cierra una secuencia de comunicación en el sistema.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Obtención de eventos de pato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e45557c25570a89452a39683a0b6732b9632129
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538944"
---
# <a name="getting-ducking-events"></a>Obtención de eventos de pato

Una aplicación multimedia que desea proporcionar una experiencia personalizada de pato debe escuchar las notificaciones de eventos cuando se abre o se cierra una secuencia de comunicación en el sistema. La implementación personalizada se puede proporcionar mediante MediaFoundation, DirectShow o DirectSound, que usan las API de audio principales. Un cliente de WASAPI directo también puede invalidar el control predeterminado si sabe cuándo se inicia y finaliza la sesión de comunicación.

Para proporcionar una implementación personalizada, una aplicación multimedia necesita recibir notificaciones del sistema cuando una aplicación de comunicación inicia o finaliza una secuencia de comunicación. La aplicación multimedia debe implementar la interfaz [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) y registrar la implementación con el sistema de audio. Tras el registro correcto, la aplicación multimedia recibe notificaciones de eventos en forma de devoluciones de llamada a través de los métodos de la interfaz. Para obtener más información, consulte [consideraciones de implementación para las notificaciones de patos](handling-audio-ducking-events-from-communication-devices.md).

Para enviar notificaciones de patos, el sistema de audio debe saber qué sesión de audio está escuchando los eventos de perdedor. Cada sesión de audio se identifica de forma única con un GUID: identificador de instancia de sesión. El administrador de sesión permite a una aplicación obtener información sobre la sesión, como el título de la sesión de audio, el estado de representación y el identificador de la instancia de sesión. El identificador se puede recuperar mediante la interfaz de control de directivas, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).

En los pasos siguientes se resume el proceso de obtención del identificador de instancia de sesión de la aplicación multimedia:

1.  Cree una instancia del enumerador de dispositivos y Úsela para obtener una referencia al punto de conexión del dispositivo que usa la aplicación multimedia para representar la secuencia que no es de comunicación.
2.  Active el administrador de sesión desde el punto de conexión del dispositivo y obtenga una referencia a la interfaz [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) del administrador de sesión.
3.  Mediante el puntero [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , obtenga una referencia a la interfaz [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) del administrador de sesión.
4.  Consulte el [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) de la interfaz [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .
5.  Llame a [**IAudioSessionControl2:: GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) y recupere una cadena que contenga el identificador de sesión para la sesión de audio actual.

Para obtener notificaciones de patos sobre las secuencias de comunicación, la aplicación multimedia llama a [**IAudioSessionManager2:: RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification). La aplicación multimedia suministra su identificador de instancia de sesión al sistema de audio y un puntero a la implementación de [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) . La aplicación ahora puede recibir notificaciones de eventos cuando se abre una secuencia en el dispositivo de comunicación. Para dejar de recibir notificaciones, la aplicación multimedia debe llamar a [**IAudioSessionManager2:: UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).

En el código siguiente se muestra cómo se puede registrar una aplicación para obtener notificaciones de patos. La clase CMediaPlayer se define en [consideraciones de implementación para las notificaciones de patos](handling-audio-ducking-events-from-communication-devices.md). En el ejemplo [DuckingMediaPlayer](duckingmediaplayer.md) se implementa esta funcionalidad.


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

[Experiencia predeterminada de los patos](stream-attenuation.md)
</dt> <dt>

[Deshabilitación de la experiencia de patos predeterminada](disabling-the-ducking-experience.md)
</dt> <dt>

[Proporcionar un comportamiento personalizado de patos](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Consideraciones de implementación para las notificaciones de patos](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



