---
description: Un usuario puede deshabilitar la experiencia de acceso predeterminado proporcionada por el sistema mediante las opciones disponibles en la pestaña Comunicaciones del panel de control multimedia de Windows, Mmsys.cpl.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Deshabilitación de la experiencia de agachamiento predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed33fa7d9473cb5c68a018b98bff8a826612387e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165026"
---
# <a name="disabling-the-default-ducking-experience"></a>Deshabilitación de la experiencia de agachamiento predeterminada

Un usuario puede deshabilitar la [experiencia de](stream-attenuation.md) acceso predeterminado proporcionada por  el sistema mediante las opciones disponibles en la pestaña Comunicaciones del panel de control multimedia de Windows, Mmsys.cpl.

Cuando se aplica el agachamiento, se usa un efecto de atenuación y atenuación durante un período de 1 segundo. Es posible que una aplicación de juego no quiera que la secuencia de comunicación interfiera con el audio del juego. Algunas aplicaciones multimedia pueden encontrar que la experiencia de reproducción se está reproduciendo cuando la música vuelve a desvanecerse. Estos tipos de aplicaciones pueden optar por no participar en la experiencia de agachamiento.

Mediante programación, un cliente WASAPI directo puede optar por no usar el administrador de sesiones para la sesión de audio que proporciona control de volumen para las secuencias que no son de comunicación. Tenga en cuenta que, incluso si un cliente opta por no participar en el agachamiento, sigue recibiendo notificaciones de patito del sistema.

Para no participar en el agachamiento, el cliente debe obtener una referencia a la [**interfaz IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) del administrador de sesiones. Para no participar en la experiencia de agachamiento, siga estos pasos:

1.  Cree una instancia del enumerador de dispositivos y úselo para obtener una referencia al punto de conexión del dispositivo que usa la aplicación multimedia para representar el flujo que no es de comunicación.
2.  Active el administrador de sesiones desde el punto de conexión del dispositivo y obtenga una referencia a la [**interfaz IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) del administrador de sesiones.
3.  Mediante el puntero [**IAudioSessionManager2,**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) obtenga una referencia a la [**interfaz IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) del administrador de sesiones.
4.  Consulta de [**IAudioSessionControl2 desde**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) la [**interfaz IAudioSessionControl.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
5.  Llame [**a IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) y pase **TRUE** o **FALSE** para especificar la preferencia de atenuación. La preferencia especificada se puede cambiar dinámicamente durante la sesión. Tenga en cuenta que el cambio de exclusión no tiene efecto hasta que la secuencia se detiene e inicia de nuevo.

El código siguiente muestra cómo una aplicación puede especificar su preferencia de agachamiento. El llamador de la función debe pasar **TRUE** o **FALSE** en el parámetro DuckingOptOutChecked. En función del valor pasado, el agachamiento se habilita o deshabilita a través de [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).


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

[Experiencia de agachamiento predeterminada](stream-attenuation.md)
</dt> <dt>

[Proporcionar un comportamiento de agachamiento personalizado](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Consideraciones de implementación para las notificaciones de achacamiento](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtener eventos de agachamiento](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



