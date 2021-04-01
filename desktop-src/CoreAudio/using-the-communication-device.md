---
description: En Windows 7, el panel de control multimedia de Windows, Mmsys.cpl, proporciona una nueva pestaña comunicaciones.
ms.assetid: bec2127d-fb82-436d-beee-d43e8fef5c35
title: Uso de un dispositivo de comunicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f677245e650cf11c71c879b2c26d3183ff4a0b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907311"
---
# <a name="using-a-communication-device"></a>Uso de un dispositivo de comunicación

En Windows 7, el panel de control multimedia de Windows, Mmsys.cpl, proporciona una nueva pestaña **comunicaciones** . Esta pestaña contiene opciones que permiten a un usuario establecer opciones que definen el modo en que el sistema administra un *dispositivo de comunicación*. Un dispositivo de comunicación se usa principalmente para colocar o recibir llamadas telefónicas en el equipo. En el caso de un equipo que solo tenga un dispositivo de representación (altavoz) y un dispositivo de captura (micrófono), estos dispositivos de audio también actuarán como dispositivos de comunicación predeterminados. Cuando un usuario conecta un dispositivo nuevo, como un auricular USB, el sistema realiza la detección automática de roles de dispositivo mediante la búsqueda de las opciones de configuración rellenadas por el OEM. Si el sistema determina que un dispositivo es más adecuado para fines de comunicación, el sistema asigna el rol **eCommunications** al dispositivo. Para estos dispositivos, el Mmsys.cpl de Windows 7 proporciona el **dispositivo de comunicación predeterminado** de la opción que permite a un usuario seleccionar un dispositivo de comunicación para cada representación de audio (pestaña **reproducción** ) y captura de audio (pestaña **grabación** ). El sistema realiza la detección automática de roles, pero no establece un dispositivo determinado para su uso en las comunicaciones. Esto debe hacerlo el usuario. El nuevo rol **eCommunications** permite a una aplicación distinguir entre un dispositivo elegido por el usuario para controlar las llamadas telefónicas y un dispositivo que se va a usar como dispositivo multimedia (reproducción de música). Por ejemplo, si el usuario tiene un auricular y un altavoz conectados al equipo, el sistema asigna el rol **eConsole** al altavoz y el rol **eCommunications** a los auriculares. Una vez que el usuario selecciona los auriculares que se van a usar como dispositivo de comunicación, para desarrollar una aplicación de comunicación, puede tener como destino el casco específicamente para representar una secuencia de audio. Una aplicación el usuario no puede cambiar el rol de dispositivo asignado por el sistema. Para obtener más información sobre los roles de dispositivo, consulte [roles de dispositivo](device-roles.md).

Las aplicaciones de comunicación, como las aplicaciones de comunicación unificada y VoIP, colocan y reciben llamadas telefónicas a través de un equipo. Por ejemplo, una aplicación de VoIP podría asignar un flujo que contiene la notificación de timbre al punto de conexión de un conjunto de dispositivos de comunicación para la representación de secuencias de audio. Además, la aplicación puede abrir los flujos de entrada y salida de voz en los dispositivos de extremo de captura y representación que se establecen como dispositivos de comunicación.

Para integrar las funcionalidades de comunicación en las aplicaciones, puede usar:

-   [MMDEVICE API](mmdevice-api.md): para obtener una referencia al punto de conexión del dispositivo de comunicación.
-   [WASAPI](wasapi.md): para representar y capturar flujos de audio a través del dispositivo de comunicación. El sistema operativo considera que el flujo abierto en un dispositivo de comunicación es un *flujo de comunicación*.

La aplicación de comunicación enumera los dispositivos y proporciona administración de transmisiones para una secuencia de flujo de comunicación (representación o captura) de la misma manera en que administraría una secuencia que no es de comunicación mediante el uso de las API de audio principales.

Una de las características que se pueden integrar en la aplicación de comunicación *es la* perdedora o la *atenuación* de la secuencia. Este comportamiento define lo que debe ocurrir con otros sonidos cuando se abre una secuencia de comunicación, como cuando se recibe una llamada telefónica en el dispositivo de comunicación. El sistema podría silenciar o reducir el volumen de audio de la secuencia de no comunicación en función de la elección del usuario. El sistema de audio genera eventos de subprocesos cuando se abre o cierra una secuencia de comunicación para representar o capturar secuencias. De forma predeterminada, el sistema operativo proporciona una experiencia predeterminada de los patos. Una aplicación multimedia puede reemplazar el comportamiento predeterminado y controlar estos eventos para proporcionar una experiencia personalizada de patos.

En las secciones siguientes se describe cómo usar las API de audio principales para proporcionar una experiencia personalizada de patos.

-   [Experiencia predeterminada de los patos](stream-attenuation.md)
-   [Deshabilitación de la experiencia de patos predeterminada](disabling-the-ducking-experience.md)
-   [Proporcionar un comportamiento personalizado de patos](providing-a-custom-ducking-experience.md)
-   [Consideraciones de implementación para las notificaciones de patos](handling-audio-ducking-events-from-communication-devices.md)
-   [Obtención de eventos de pato](getting-ducking-events-from-a-communication-device.md)

### <a name="getting-a-reference-to-the-communication-device-endpoint"></a>Obtener una referencia al punto de conexión del dispositivo de comunicación

Para usar el dispositivo de comunicación, un cliente de WASAPI directo debe enumerar los dispositivos mediante el enumerador de dispositivos. Obtenga una referencia al punto de conexión del dispositivo de comunicación predeterminado mediante una llamada a [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). En esta llamada, la aplicación debe especificar **eCommunications** en el parámetro *role* para restringir la enumeración de dispositivos a los dispositivos de comunicación. Después de obtener una referencia al punto de conexión del dispositivo para el dispositivo, puede activar los servicios cuyo ámbito es el punto de conexión mediante una llamada a [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Por ejemplo, puede pasar el identificador de servicio **IID \_ IAudioClient** para activar un objeto de cliente de audio y usarlo para la administración de transmisiones, el identificador **IID \_ IAudioEndpointVolume** para obtener acceso a los controles de volumen del punto de conexión de dispositivo de comunicación, o el identificador de **\_ IAudioSessionManager de IID** para activar el administrador de sesión que le permite interactuar con el motor de directivas del punto de conexión. Para obtener información sobre las operaciones de Stream, consulte [Administración de transmisiones](stream-management.md).

Mediante el uso de la referencia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , también puede acceder al almacén de propiedades para el punto de conexión del dispositivo. Estos valores de propiedad, como el nombre descriptivo del dispositivo y el nombre del fabricante, se rellenan con el OEM y permiten que una aplicación determine las características de un dispositivo de comunicación. Para obtener más información, consulte [propiedades del dispositivo](device-properties.md).

En el código de ejemplo siguiente se obtiene una referencia al punto de conexión del dispositivo de comunicación predeterminado para representar una secuencia de audio.


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

 

 



