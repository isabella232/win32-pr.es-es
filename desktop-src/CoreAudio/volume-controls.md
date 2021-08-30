---
description: Controles de volumen
ms.assetid: b1799372-8d2c-4774-995d-e7926a159d0a
title: Controles de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10697a38410a60af912ceb77b13ae8584d47c8fa5e8ac49fedc81d14e05305f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088205"
---
# <a name="volume-controls"></a>Controles de volumen

Los clientes que administran secuencias en modo compartido suelen usar las interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**e IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) en [WASAPI](wasapi.md) para controlar y supervisar los niveles de volumen de flujo. A través de los métodos de la interfaz **ISimpleAudioVolume,** el cliente puede obtener y establecer los niveles de volumen de las sesiones de [audio](audio-sessions.md) a las que pertenecen las secuencias en modo compartido. Si Sndvol u otra aplicación cambia el nivel de volumen de sesión, el cliente puede recibir una notificación del cambio a través de la **interfaz IAudioSessionEvents.**

Los clientes que administran secuencias en modo exclusivo suelen usar las interfaces [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) e [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) en la [API EndpointVolume](endpointvolume-api.md) para controlar y supervisar los niveles de volumen de flujo. A través de los métodos de la **interfaz IAudioEndpointVolume,** el cliente puede obtener y establecer el nivel de volumen de un dispositivo de [punto de conexión de audio.](audio-endpoint-devices.md) Si Sndvol u otra aplicación cambia el nivel de volumen del dispositivo del punto de conexión, el cliente puede recibir una notificación del cambio a través de la interfaz **IAudioEndpointVolumeCallback.**

Como se explica en [Sesiones de audio,](audio-sessions.md)Sndvol es el programa de control de volumen del sistema. Muestra controles de volumen para los dispositivos de punto de conexión de representación de audio en el sistema. (Actualmente, no muestra los controles de volumen para los dispositivos de punto de conexión de captura de audio). Para ver los controles de volumen  de un dispositivo determinado, haga clic en Dispositivo en la barra de menús y seleccione un nombre de dispositivo en la lista de dispositivos disponibles.

La ventana Sndvol separa los controles de volumen de un dispositivo en dos grupos. El cuadro de grupo del lado izquierdo de la ventana tiene la etiqueta **Dispositivo**. El **cuadro** Dispositivo contiene un control de volumen único controlado por la [**interfaz IAudioEndpointVolume.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) Los cambios que el usuario realiza en este control de volumen se pueden supervisar a través de la [**interfaz IAudioEndpointVolumeCallback.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback)

El cuadro de grupo del lado derecho de la ventana de Sndvol tiene la etiqueta **Aplicaciones.** El **cuadro** Aplicaciones contiene los controles de volumen para las aplicaciones que comparten actualmente el dispositivo. En el caso de las aplicaciones que usan el dispositivo en modo compartido, los controles de volumen representan los niveles de volumen controlados por la [**interfaz ISimpleAudioVolume.**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) Los cambios que el usuario realiza en estos controles de volumen se pueden supervisar a través de la [**interfaz IAudioSessionEvents.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

Aunque una aplicación en modo compartido puede usar su interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para supervisar los  cambios que el usuario realiza en el control de volumen de la aplicación en el cuadro Aplicaciones de la ventana Sndvol, la aplicación no puede supervisar los cambios en los controles de volumen de otras aplicaciones no relacionadas. De forma similar, una aplicación puede cambiar los niveles de volumen de sus sesiones de audio a través de la interfaz [**ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) pero no puede cambiar los niveles de volumen de las sesiones que pertenecen a otras aplicaciones no relacionadas.

Sin embargo, dos o más aplicaciones relacionadas (o instancias de la  misma aplicación) pueden compartir el mismo control de volumen en el cuadro Aplicaciones de la ventana Sndvol asignando sus secuencias de audio a la misma sesión entre procesos o asociando sus sesiones respectivas con el mismo parámetro de agrupación. Para obtener más información, vea [Sesiones de audio](audio-sessions.md) y parámetros de [agrupación](grouping-parameters.md).

WASAPI proporciona dos interfaces adicionales, [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume), para controlar los niveles de volumen de las secuencias en modo compartido. Estas interfaces las usan principalmente clientes especializados que requieren control sobre los niveles de volumen de canales individuales en una sesión o secuencias individuales de una sesión.

[DeviceTopology API permite a](devicetopology-api.md) los clientes acceder a los controles de volumen en las topologías de los adaptadores de audio. Sin embargo, los clientes que administran secuencias en modo exclusivo suelen usar EndpointVolume API en lugar de DeviceTopology API para controlar los niveles de volumen de flujo. EndpointVolume API simplifica el control del volumen de un dispositivo de punto de conexión de dos maneras. En primer lugar, si un dispositivo de punto de conexión implementa un control de volumen de hardware, la API DeviceTopology requiere que el cliente recor la topología del dispositivo en busca del control de hardware. Por el contrario, EndpointVolume API busca automáticamente el control de volumen de hardware para el cliente. En segundo lugar, si el dispositivo de punto de conexión no implementa un control de volumen de hardware, un cliente DeviceTopology debe implementar un control de volumen en el software. Por el contrario, EndpointVolume API sustituye automáticamente un control de volumen de software por el control de hardware que falta.

En las secciones siguientes se describen los controles de volumen para sesiones de audio y para dispositivos de punto de conexión de audio:

-   [Controles de volumen de sesión](session-volume-controls.md)
-   [Controles de volumen de punto de conexión](endpoint-volume-controls.md)
-   [EndpointVolume API](endpointvolume-api.md)
-   [Controles de volumen con cinta de audio](audio-tapered-volume-controls.md)
-   [Medidores máximos](peak-meters.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 



