---
description: En Windows 7, el panel de control multimedia Windows, Mmsys.cpl, proporciona una nueva pestaña Comunicaciones.
ms.assetid: bec2127d-fb82-436d-beee-d43e8fef5c35
title: Uso de un dispositivo de comunicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f677245e650cf11c71c879b2c26d3183ff4a0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164774"
---
# <a name="using-a-communication-device"></a>Uso de un dispositivo de comunicación

En Windows 7, el panel de control multimedia Windows, Mmsys.cpl, proporciona una **nueva** pestaña Comunicaciones. Esta pestaña contiene opciones que permiten al usuario establecer opciones que definen cómo el sistema administra un *dispositivo de comunicación.* Un dispositivo de comunicación se usa principalmente para colocar o recibir llamadas telefónicas en el equipo. Para un equipo que solo tiene un dispositivo de representación (altavoz) y un dispositivo de captura (micrófono), estos dispositivos de audio también actúan como dispositivos de comunicación predeterminados. Cuando un usuario conecta un nuevo dispositivo, como un casco USB, el sistema realiza la detección automática de roles de dispositivo mediante la búsqueda de las opciones de configuración que rellena el OEM. Si el sistema determina que un dispositivo es más adecuado para fines de comunicación, el sistema asigna el rol **eCommunications** al dispositivo. Para estos dispositivos, Windows 7 Mmsys.cpl proporciona la  opción Dispositivo de comunicación predeterminado que permite al usuario seleccionar un dispositivo de comunicación para la representación de audio **(pestaña** Reproducción) y la captura de audio **(pestaña** Grabación). El sistema realiza la detección automática de roles, pero no establece un dispositivo determinado que se usará para las comunicaciones. Esto lo debe hacer el usuario. El nuevo **rol eCommunications** permite a una aplicación distinguir entre un dispositivo elegido por el usuario para controlar las llamadas telefónicas y un dispositivo que se usará como dispositivo multimedia (reproducción de música). Por ejemplo, si el usuario tiene un casco y un altavoz conectados al equipo, el sistema asigna el rol **eConsole** al hablante y el rol **eCommunications** al casco. Una vez que el usuario selecciona el casco que se va a usar como dispositivo de comunicación, para desarrollar una aplicación de comunicación, puede seleccionar el casco específicamente para representar una secuencia de audio. Una aplicación que el usuario no puede cambiar el rol de dispositivo asignado por el sistema. Para obtener más información sobre los roles de dispositivo, vea [Roles de dispositivo](device-roles.md).

Las aplicaciones de comunicación, como voIP y las aplicaciones de comunicación unificada, coloca y recibe llamadas telefónicas a través de un equipo. Por ejemplo, una aplicación VoIP podría asignar una secuencia que contiene la notificación de anillo al punto de conexión de un conjunto de dispositivos de comunicación para representar secuencias de audio. Además, la aplicación podría abrir los flujos de entrada y salida de voz en los dispositivos de punto de conexión de captura y representación que se establecen como dispositivos de comunicación.

Para integrar las funcionalidades de comunicación en las aplicaciones, puede usar:

-   [MMDevice API](mmdevice-api.md): para obtener una referencia al punto de conexión del dispositivo de comunicación.
-   [WASAPI:](wasapi.md)para representar y capturar secuencias de audio a través del dispositivo de comunicación. El sistema operativo considera que la secuencia abierta en un dispositivo de comunicación es una secuencia *de comunicación*.

La aplicación de comunicación enumera los dispositivos y proporciona administración de flujos para un flujo de comunicación (representación o captura) de la misma manera que administraría una secuencia que no es de comunicación mediante las API de audio principal.

Una de las características que puede integrar en la aplicación de comunicación *es* la atenuación de flujo o *de achacación.* Este comportamiento define lo que debe ocurrir con otros sonidos cuando se abre un flujo de comunicación, como cuando se recibe una llamada telefónica en el dispositivo de comunicación. El sistema puede silenciar o reducir el volumen de audio de la secuencia que no es de comunicación en función de la elección del usuario. El sistema de audio genera eventos de agachamiento cuando se abre o se cierra una secuencia de comunicación para representar o capturar secuencias. De forma predeterminada, el sistema operativo proporciona una experiencia de agachamiento predeterminada. Una aplicación multimedia puede reemplazar el comportamiento predeterminado y controlar estos eventos para proporcionar una experiencia de agachamiento personalizada.

En las secciones siguientes se describe cómo usar core audio API para proporcionar una experiencia de afición personalizada.

-   [Experiencia de agachamiento predeterminada](stream-attenuation.md)
-   [Deshabilitación de la experiencia de agachamiento predeterminada](disabling-the-ducking-experience.md)
-   [Proporcionar un comportamiento de agachamiento personalizado](providing-a-custom-ducking-experience.md)
-   [Consideraciones de implementación para las notificaciones de achacamiento](handling-audio-ducking-events-from-communication-devices.md)
-   [Obtener eventos de agachamiento](getting-ducking-events-from-a-communication-device.md)

### <a name="getting-a-reference-to-the-communication-device-endpoint"></a>Obtener una referencia al punto de conexión del dispositivo de comunicación

Para usar el dispositivo de comunicación, un cliente WASAPI directo debe enumerar los dispositivos mediante el enumerador de dispositivos. Obtenga una referencia al punto de conexión del dispositivo de comunicación predeterminado llamando a [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). En esta llamada, la aplicación debe especificar **eCommunications** en el *parámetro Role* para restringir la enumeración de dispositivos a los dispositivos de comunicación. Después de obtener una referencia al punto de conexión del dispositivo, puede activar los servicios que están limitados para el punto de conexión mediante una llamada a [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Por ejemplo, puede pasar el identificador de servicio **\_ IID IAudioClient** para activar un objeto de cliente de audio y usarlo para la administración de flujos, el identificador **\_ IID IAudioEndpointVolume** para obtener acceso a los controles de volumen del punto de conexión del dispositivo de comunicación o el identificador **\_ IID IAudioSessionManager** para activar el administrador de sesiones que le permite interactuar con el motor de directivas del punto de conexión. Para obtener información sobre las operaciones de flujo, vea [Stream Management](stream-management.md).

Mediante la referencia [**de IMMDevice,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) también puede acceder al almacén de propiedades para el punto de conexión del dispositivo. El OEM rellena estos valores de propiedad, como el nombre descriptivo del dispositivo y el nombre del fabricante, y permiten a una aplicación determinar las características de un dispositivo de comunicación. Para obtener más información, vea [Propiedades del dispositivo.](device-properties.md)

El código de ejemplo siguiente obtiene una referencia al punto de conexión del dispositivo de comunicación predeterminado para representar una secuencia de audio.


```C++
IMMDevice *defaultDevice = NULL;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), NULL,
            CLSCTX_INPROC_SERVER, 
            __uuidof(IMMDeviceEnumerator), 
            (LPVOID *)&deviceEnumerator);

hr = deviceEnumerator->GetDefaultAudioEndpoint(eRender, 
            eCommunications, &defaultDevice);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de flujos](stream-management.md)
</dt> </dl>

 

 



