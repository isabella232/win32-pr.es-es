---
description: Un usuario puede deshabilitar la experiencia predeterminada de la forma predeterminada que proporciona el sistema mediante las opciones que están disponibles en la pestaña comunicaciones del panel de control multimedia de Windows, Mmsys.cpl.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Deshabilitación de la experiencia de patos predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed33fa7d9473cb5c68a018b98bff8a826612387e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153521"
---
# <a name="disabling-the-default-ducking-experience"></a>Deshabilitación de la experiencia de patos predeterminada

Un usuario puede deshabilitar la [experiencia predeterminada](stream-attenuation.md) de la forma predeterminada que proporciona el sistema mediante las opciones que están disponibles en la pestaña **comunicaciones** del panel de control multimedia de Windows, Mmsys.cpl.

Cuando se aplica la pato, se usa un efecto de fundido y fundido para un período de 1 segundo. Es posible que una aplicación de juego no quiera que la secuencia de comunicación interfiera con el audio del juego. Es posible que algunas aplicaciones multimedia descubran que la experiencia de reproducción es discordante cuando la música se vuelve a atenuar. Estos tipos de aplicaciones pueden optar por no participar en la experiencia de los patos.

Mediante programación, un cliente de WASAPI directo puede optar por usar el administrador de sesión para la sesión de audio que proporciona control de volumen para las secuencias que no son de comunicación. Tenga en cuenta que, incluso si un cliente no se puede utilizar, sigue recibiendo notificaciones de patos del sistema.

Para no participar, el cliente debe obtener una referencia a la interfaz [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) del administrador de sesión. Para no participar en la experiencia de los patos, siga estos pasos:

1.  Cree una instancia del enumerador de dispositivos y Úsela para obtener una referencia al punto de conexión del dispositivo que usa la aplicación multimedia para representar la secuencia que no es de comunicación.
2.  Active el administrador de sesión desde el punto de conexión del dispositivo y obtenga una referencia a la interfaz [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) del administrador de sesión.
3.  Mediante el puntero [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , obtenga una referencia a la interfaz [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) del administrador de sesión.
4.  Consulte el [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) de la interfaz [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .
5.  Llame a [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) y pase **true** o **false** para especificar la preferencia de pato. La preferencia especificada se puede cambiar dinámicamente durante la sesión. Tenga en cuenta que el cambio de cancelación no surte efecto hasta que la secuencia se detiene y se inicia de nuevo.

En el código siguiente se muestra cómo una aplicación puede especificar su preferencia de pato. El autor de la llamada de la función debe pasar **true** o **false** en el parámetro DuckingOptOutChecked. En función del valor que se pase, se habilitará o deshabilitará la función de pato a través de [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).


```C++
////////////////////////////////////////////////////////////////////
//Description: Specifies the ducking options for the application.
//Parameters: 
//    If DuckingOptOutChecked is TRUE system ducking is disabled; 
//    FALSE, system ducking is enabled.
////////////////////////////////////////////////////////////////////

HRESULT DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;


    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>(&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(NULL, 0, &pSessionControl);
        
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                  __uuidof(IAudioSessionControl2),
                  (void**)&pSessionControl2);
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    //  Sync the ducking state with the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionControl2->SetDuckingPreference(TRUE);
        }
        else
        {
            hr = pSessionControl2->SetDuckingPreference(FALSE);
        }
        pSessionControl2->Release();
        pSessionControl2 = NULL;
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

[Proporcionar un comportamiento personalizado de patos](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Consideraciones de implementación para las notificaciones de patos](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtención de eventos de pato](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



