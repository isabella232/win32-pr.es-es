---
description: Controles de volumen
ms.assetid: b1799372-8d2c-4774-995d-e7926a159d0a
title: Controles de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758fd25d4157030071a47ac8eec26dc0e4d50e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907310"
---
# <a name="volume-controls"></a>Controles de volumen

Los clientes que administran secuencias en modo compartido suelen usar las interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) y [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) en [WASAPI](wasapi.md) para controlar y supervisar los niveles de volumen de la secuencia. A través de los métodos de la interfaz **ISimpleAudioVolume** , el cliente puede obtener y establecer los niveles de volumen de las [sesiones de audio](audio-sessions.md) a las que pertenecen los flujos de modo compartido. Si Sndvol u otra aplicación cambia el nivel de volumen de la sesión, el cliente puede recibir la notificación del cambio a través de la interfaz **IAudioSessionEvents** .

Los clientes que administran secuencias en modo exclusivo usan normalmente las interfaces [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) y [**IAUDIOENDPOINTVOLUMECALLBACK**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) en la [API de EndpointVolume](endpointvolume-api.md) para controlar y supervisar los niveles de volumen de la secuencia. A través de los métodos de la interfaz **IAudioEndpointVolume** , el cliente puede obtener y establecer el nivel de volumen de un [dispositivo de punto de conexión de audio](audio-endpoint-devices.md). Si Sndvol u otra aplicación cambia el nivel de volumen del dispositivo de extremo, el cliente puede recibir la notificación del cambio a través de la interfaz **IAudioEndpointVolumeCallback** .

Como se explica en [sesiones de audio](audio-sessions.md), Sndvol es el programa de control de volumen del sistema. Muestra controles de volumen para los dispositivos de punto de conexión de representación de audio en el sistema. (Actualmente, no se muestran los controles de volumen de los dispositivos de extremo de captura de audio). Para ver los controles de volumen de un dispositivo determinado, haga clic en **dispositivo** en la barra de menús y seleccione un nombre de dispositivo en la lista de dispositivos disponibles.

La ventana Sndvol separa los controles de volumen de un dispositivo en dos grupos. El cuadro de grupo en el lado izquierdo de la ventana tiene la etiqueta **dispositivo**. El cuadro **dispositivo** contiene un control de volumen único controlado por la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) . Los cambios que realiza el usuario en este control de volumen se pueden supervisar a través de la interfaz [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) .

El cuadro de grupo del lado derecho de la ventana de Sndvol se etiqueta como **aplicaciones**. El cuadro **aplicaciones** contiene los controles de volumen de las aplicaciones que comparten actualmente el dispositivo. En el caso de las aplicaciones que usan el dispositivo en modo compartido, los controles de volumen representan los niveles de volumen controlados por la interfaz [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) . Los cambios que realiza el usuario en estos controles de volumen se pueden supervisar a través de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .

Aunque una aplicación en modo compartido puede usar su interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para supervisar los cambios que el usuario realiza en el control de volumen de la aplicación en el cuadro **aplicaciones** de la ventana de Sndvol, la aplicación no puede supervisar los cambios en los controles de volumen de otras aplicaciones no relacionadas. Del mismo modo, una aplicación puede cambiar los niveles de volumen de sus sesiones de audio a través de la interfaz [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) , pero no puede cambiar los niveles de volumen de las sesiones que pertenecen a otras aplicaciones no relacionadas.

Sin embargo, dos o más aplicaciones (o instancias de la misma aplicación) relacionadas pueden compartir el mismo control de volumen en el cuadro **aplicaciones** de la ventana de Sndvol, ya sea asignando sus secuencias de audio a la misma sesión entre procesos o asociando sus respectivas sesiones con el mismo parámetro de agrupación. Para obtener más información, vea [sesiones de audio](audio-sessions.md) y parámetros de [agrupación](grouping-parameters.md).

WASAPI proporciona dos interfaces adicionales, [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) y [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume), para controlar los niveles de volumen de los flujos en modo compartido. Estas interfaces las usan principalmente los clientes especializados que requieren el control sobre los niveles de volumen de los canales individuales de una sesión o de flujos individuales en una sesión.

La [API de DeviceTopology](devicetopology-api.md) permite a los clientes tener acceso a los controles de volumen de las topologías de adaptadores de audio. Sin embargo, los clientes que administran secuencias en modo exclusivo usan normalmente la API EndpointVolume en lugar de la API DeviceTopology para controlar los niveles de volumen de la secuencia. La API EndpointVolume simplifica el control del volumen de un dispositivo de punto de conexión de dos maneras. En primer lugar, si un dispositivo de extremo implementa un control de volumen de hardware, la API de DeviceTopology requiere que el cliente atraviese la topología del dispositivo en la búsqueda del control de hardware. En cambio, la API EndpointVolume busca automáticamente el control de volumen de hardware para el cliente. En segundo lugar, si el dispositivo de extremo no implementa un control de volumen de hardware, un cliente de DeviceTopology debe implementar un control de volumen en el software. En cambio, la API EndpointVolume sustituye automáticamente un control de volumen de software para el control de hardware que falta.

En las secciones siguientes se describen los controles de volumen de las sesiones de audio y los dispositivos de punto de conexión de audio:

-   [Controles de volumen de sesión](session-volume-controls.md)
-   [Controles de volumen de extremo](endpoint-volume-controls.md)
-   [API de EndpointVolume](endpointvolume-api.md)
-   [Controles de volumen con inclinación de audio](audio-tapered-volume-controls.md)
-   [Medidores de pico](peak-meters.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 



