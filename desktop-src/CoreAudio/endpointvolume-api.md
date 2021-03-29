---
description: API de EndpointVolume
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: API de EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807562"
---
# <a name="endpointvolume-api"></a>API de EndpointVolume

La API de EndpointVolume permite a los clientes especializados controlar y supervisar los niveles de volumen de los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md). Un cliente obtiene las referencias a las interfaces de la API de EndpointVolume mediante la obtención de la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de un dispositivo de punto de conexión de audio y la llamada al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) .

El archivo de encabezado Endpointvolume. h define las interfaces de la API de EndpointVolume.

Las aplicaciones de audio que usan la [API MMDevice](mmdevice-api.md) y [WASAPI](wasapi.md) suelen usar la interfaz [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) para controlar los niveles de volumen por sesión. Solo dos tipos de aplicaciones de audio requieren el uso de la API de EndpointVolume. Estos tipos de aplicaciones son:

-   Las aplicaciones que administran los niveles de volumen maestro de los dispositivos de punto de conexión de audio, de forma similar al programa de control de volumen de Windows, Sndvol.exe.
-   Aplicaciones de audio profesional ("Audio Pro") que requieren acceso en modo exclusivo a los dispositivos de punto de conexión de audio.

El uso inadecuado de la API de EndpointVolume puede interferir con la Directiva de audio de Windows e interrumpir la configuración del volumen del sistema del usuario.

Si un dispositivo de punto de conexión de audio implementa controles de volumen y silenciado de hardware, la API de EndpointVolume usa esos controles para administrar el volumen del dispositivo. De lo contrario, la API EndpointVolume implementa los controles del software de forma transparente en el cliente.

Si un dispositivo tiene controles de volumen y silenciado de hardware, los cambios realizados en el volumen del dispositivo y silenciar la configuración a través de la API de EndpointVolume afectan al nivel de volumen en modo compartido y en modo exclusivo. Si un dispositivo no tiene controles de silencio y volumen de hardware, los cambios realizados en el volumen de software y los controles de silencio a través de la API de EndpointVolume afectan al nivel de volumen en modo compartido, pero no en modo exclusivo. En el modo exclusivo, el cliente y el dispositivo intercambian datos de audio directamente, omitiendo los controles de software.

En el caso de las aplicaciones que deben administrar controles de volumen y silenciado de hardware, la API de EndpointVolume ofrece dos ventajas potenciales sobre la [API de DeviceTopology](devicetopology-api.md).

En primer lugar, varios dispositivos de adaptador de audio carecen de controles de volumen de hardware. Si un dispositivo no tiene un control de volumen de hardware, la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) de la API de EndpointVolume implementa automáticamente un control de volumen de software en el flujo hacia o desde ese dispositivo. Para un cliente de la API de EndpointVolume, el resultado es el mismo si el dispositivo o el software de la interfaz de la API de EndpointVolume implementan el control de volumen en el hardware.

En segundo lugar, incluso si el dispositivo adaptador implementa controles de volumen de hardware, una aplicación que use la API DeviceTopology para implementar un algoritmo de recorrido de topología podría no encontrar el control que está buscando. Normalmente, este tipo de aplicación está diseñado para atravesar la topología de hardware de un dispositivo o un conjunto de dispositivos relacionados. La aplicación corre un error si intenta atravesar la topología de un dispositivo para el que no se ha diseñado o probado específicamente.

Solo las aplicaciones especializadas que deben tener acceso a funciones de hardware que no sean controles de volumen y silencio requieren el uso de la API de DeviceTopology. En el caso de las aplicaciones que requieren el control solo del nivel de volumen de una secuencia en modo exclusivo, la API EndpointVolume es más fácil de usar y funciona de forma confiable con una gama más amplia de dispositivos de hardware de audio.

Para obtener ejemplos de código que usan las interfaces de la API de EndpointVolume, vea los temas siguientes:

-   [Controles de volumen de extremo](endpoint-volume-controls.md)
-   [Medidores de pico](peak-meters.md)

Para ver un ejemplo que usa la API de EndpointVolume, consulte [EndpointVolume](endpointvolume.md) en el Windows SDK.

La API de EndpointVolume implementa las interfaces siguientes.



| Interfaz                                                | Descripción                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | Representa los controles de volumen en la secuencia de audio hacia o desde un dispositivo de punto de conexión de audio. |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | Representa un medidor de picos en la secuencia de audio hacia o desde un dispositivo de punto de conexión de audio.        |



 

Además, los clientes de la API de EndpointVolume que requieren notificación de cambios de volumen y de silencio en los dispositivos de punto de conexión de audio deben implementar la siguiente interfaz.



| Interfaz                                                            | Descripción                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Proporciona notificaciones cuando cambia el nivel de volumen o el estado de silenciación de un dispositivo de punto de conexión de audio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles de volumen](volume-controls.md)
</dt> <dt>

[**Interfaz IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



