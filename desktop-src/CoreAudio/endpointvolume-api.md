---
description: EndpointVolume API
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: EndpointVolume API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22965e882a2f7d413ae58690fc9bc5f8134aba0e7b26838ca38c74d7f0093c98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018453"
---
# <a name="endpointvolume-api"></a>EndpointVolume API

EndpointVolume API permite a los clientes especializados controlar y supervisar los niveles de volumen de los dispositivos de [punto de conexión de audio.](audio-endpoint-devices.md) Un cliente obtiene referencias a las interfaces de endpointVolume API al obtener la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de un dispositivo de punto de conexión de audio y llamar al [**método IMMDevice::Activate.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)

El archivo de encabezado Endpointvolume.h define las interfaces de EndpointVolume API.

Las aplicaciones de audio que usan [MMDevice API](mmdevice-api.md) y [WASAPI](wasapi.md) suelen usar la interfaz [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) para controlar los niveles de volumen por sesión. Solo dos tipos de aplicaciones de audio requieren el uso de la API EndpointVolume. Estos tipos de aplicación son:

-   Aplicaciones que administran los niveles de volumen maestro de los dispositivos de punto de conexión de audio, de forma similar al programa Windows control de volumen, Sndvol.exe.
-   Professional de audio ("audio pro") que requieren acceso en modo exclusivo a los dispositivos de punto de conexión de audio.

El uso inadecuado de EndpointVolume API puede interferir con Windows directiva de audio e interrumpir la configuración del volumen del sistema del usuario.

Si un dispositivo de punto de conexión de audio implementa controles de volumen de hardware y exclusión mutua, la API EndpointVolume usa esos controles para administrar el volumen del dispositivo. De lo contrario, EndpointVolume API implementa los controles en el software de forma transparente para el cliente.

Si un dispositivo tiene controles de volumen y exclusión mutua de hardware, los cambios realizados en la configuración de volumen y exclusión mutua del dispositivo a través de endpointVolume API afectan al nivel de volumen en modo compartido y modo exclusivo. Si un dispositivo no tiene controles de volumen y exclusión de hardware, los cambios realizados en el volumen de software y los controles de exclusión mutua a través de endpointVolume API afectan al nivel de volumen en modo compartido, pero no en modo exclusivo. En modo exclusivo, el cliente y el dispositivo intercambian datos de audio directamente, omitiendo los controles de software.

En el caso de las aplicaciones que deben administrar controles de volumen y exclusión mutua de hardware, EndpointVolume API ofrece dos ventajas potenciales con respecto a [DeviceTopology API.](devicetopology-api.md)

En primer lugar, varios dispositivos de adaptador de audio carecen de controles de volumen de hardware. Si un dispositivo no tiene un control de volumen de hardware, la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) de endpointVolume API implementa automáticamente un control de volumen de software en el flujo hacia o desde ese dispositivo. Para un cliente de la API EndpointVolume, el resultado es el mismo si el dispositivo o la interfaz de la API EndpointVolume implementan el control de volumen en hardware o en software.

En segundo lugar, incluso si el dispositivo del adaptador implementa controles de volumen de hardware, una aplicación que usa DeviceTopology API para implementar un algoritmo de recorrido de topología podría no encontrar el control que está buscando. Normalmente, esta aplicación está diseñada para recorrer la topología de hardware de un dispositivo determinado o un conjunto de dispositivos relacionados. La aplicación corre el riesgo de errores si intenta atravesar la topología de un dispositivo para el que no se ha diseñado específicamente ni con el que se ha probado.

Solo las aplicaciones especializadas que deben tener acceso a funciones de hardware que no son controles de volumen y exclusión mutua requieren el uso de la API DeviceTopology. En el caso de las aplicaciones que solo requieren el control del nivel de volumen de una secuencia en modo exclusivo, endpointVolume API es más fácil de usar y funciona de forma confiable con una gama más amplia de dispositivos de hardware de audio.

Para ver ejemplos de código que usan las interfaces de EndpointVolume API, consulte los temas siguientes:

-   [Controles de volumen de punto de conexión](endpoint-volume-controls.md)
-   [Medidores máximos](peak-meters.md)

Para ver un ejemplo que usa la API EndpointVolume, consulte [EndpointVolume](endpointvolume.md) en el SDK Windows.

EndpointVolume API implementa las interfaces siguientes.



| Interfaz                                                | Descripción                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | Representa los controles de volumen de la secuencia de audio hacia o desde un dispositivo de punto de conexión de audio. |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | Representa un medidor máximo en la secuencia de audio hacia o desde un dispositivo de punto de conexión de audio.        |



 

Además, los clientes de la API EndpointVolume que requieren la notificación del volumen y los cambios muting en los dispositivos de punto de conexión de audio deben implementar la siguiente interfaz.



| Interfaz                                                            | Descripción                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Proporciona notificaciones cuando cambia el nivel de volumen o el estado muting de un dispositivo de punto de conexión de audio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles de volumen](volume-controls.md)
</dt> <dt>

[**IMMDevice (Interfaz)**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



