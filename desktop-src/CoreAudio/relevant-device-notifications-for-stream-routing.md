---
description: En Windows 7, las API de plataforma de alto nivel que usan las API de audio principales, como las API de Media Foundation, DirectSound y Wave, implementan la característica de enrutamiento de flujo mediante la administración del cambio de secuencia desde un dispositivo existente a un nuevo punto de conexión de audio predeterminado.
ms.assetid: caf831bb-b8de-467f-bdb4-f9f8991dc7a8
title: Notificaciones relevantes para el enrutamiento de flujos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3d253ce2ec5d6e3bef025a33233a9d377ca44b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153134"
---
# <a name="relevant-notifications-for-stream-routing"></a>Notificaciones relevantes para el enrutamiento de flujos

En Windows 7, las API de plataforma de alto nivel que usan las API de audio principales, como las API de Media Foundation, DirectSound y Wave, implementan la característica de enrutamiento de flujo mediante la administración del cambio de secuencia desde un dispositivo existente a un nuevo punto de conexión de audio predeterminado. Las aplicaciones multimedia que usan estas API usan el comportamiento de enrutamiento de flujo sin modificaciones en el origen. Los clientes de WASAPI directos pueden usar las notificaciones enviadas por componentes de audio principales e implementar la característica de enrutamiento de flujo.

Para implementar la característica de enrutamiento de secuencias, un cliente debe escuchar dos tipos de eventos: notificaciones de cambio de dispositivo y notificaciones de desconexión de sesión. En la implementación proporcionada por las API de alto nivel, estos eventos se envían para los puntos de conexión de dispositivo predeterminados creados mediante una llamada a [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Para obtener más información, consulte [obtención del punto de conexión del dispositivo para el enrutamiento de transmisiones](getting-the-default-device-endpoint-for-stream-routing.md).

El componente Core Audio MMDeviceAPI entrega devoluciones de llamada de notificación cuando se agregan, quitan o modifican dispositivos de audio. Los cambios de formato y sesión de audio se informan como eventos a través de WASAPI.

## <a name="device-change-notifications"></a>Notificaciones de cambio de dispositivo

MMDeviceAPI genera eventos cuando se agregan, quitan o modifican dispositivos de audio. Si el cliente va a proporcionar la funcionalidad de enrutamiento de secuencias, debe implementar la interfaz [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) y registrar su implementación con MMDeviceAPI.

Para obtener notificaciones de cambios de dispositivo, el cliente debe realizar las siguientes tareas:

-   Implemente la interfaz [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) para controlar las notificaciones de cambio de dispositivo enviadas por MMDeviceAPI.
-   Registre la implementación de [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) con MMDeviceAPI llamando al método [**IMMDeviceEnumerator:: RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) .

Una vez registrada la implementación del cliente de estas interfaces, el cliente recibe notificaciones en forma de devoluciones de llamada a través de los métodos de estas interfaces. MMDeviceAPI llama a los métodos [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) cuando genera eventos de nivel de extremo (cambios de estado del punto de conexión, nuevas llegadas del punto de conexión, eliminaciones del punto de conexión, cambios de punto de conexión predeterminados y cambios en las propiedades del punto de conexión).

Si el cliente desea proporcionar enrutamiento de flujo para el dispositivo predeterminado, el cliente debe implementar el comportamiento de cambio del dispositivo cuando recibe la notificación a través de la devolución de llamada [**IMMNotificationClient:: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) .

## <a name="audio-session-change-notifications"></a>Notificaciones de cambio de sesión de audio

Los cambios en la sesión de audio y los cambios de formato se muestran como eventos de sesión de audio a través de WASAPI. Un cliente de WASAPI implementa la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) y registra la implementación con WASAPI.

Para obtener las notificaciones de cambio de la sesión de audio, el cliente debe realizar las siguientes tareas:

-   Implemente la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para controlar las notificaciones de cambio de formato enviadas por WASAPI.
-   Registre la implementación de [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) con WASAPI llamando al método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) .

WASAPI llama a los métodos [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) cuando se producen cambios en la sesión de audio. Estos eventos se generan cuando se cambia el nombre para mostrar de la sesión, la ruta de acceso del icono, el volumen, el parámetro de agrupación o el estado.

Para implementar la característica de enrutamiento de secuencias, el cliente debe esperar la notificación de desconexión de sesión. Cuando se desconecta una sesión de audio o se cambia el formato de un dispositivo, WASAPI envía las notificaciones de cliente en forma de devoluciones de llamada a través de [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Con la notificación de desconexión, WASAPI también envía un valor que indica por qué se desconectó la sesión. Esto puede ocurrir por varios motivos, como el dispositivo se quitó, el servidor se detuvo, etc. Para obtener una lista completa de motivos, vea la enumeración **AudioSessionDisconnectReason** definida en AudioPolicy. h. Si el dispositivo predeterminado cambia, el cliente debe esperar las notificaciones (si aún no se han recibido) que están acompañadas de un valor de **DisconnectReasonDeviceRemoval** . En respuesta a estas notificaciones, es posible que el cliente vuelva a abrir la secuencia en el nuevo dispositivo predeterminado.

Dado que todas estas operaciones son asincrónicas, no se puede predecir el orden en el que la aplicación recibe notificaciones. Sin embargo, normalmente, la aplicación recibe el valor **AudioSessionDisconnect** antes de la notificación de cambio de dispositivo predeterminada.

### <a name="format-change-notifications"></a>Notificaciones de cambio de formato

Los cambios de formato de audio se producen cuando cambia el formato de la secuencia. Esto puede ocurrir cuando el usuario selecciona un nuevo formato en el panel de control de **sonido** o el nuevo dispositivo predeterminado admite un nuevo formato (por ejemplo, HDMI o ciertas interfaces de audio profesional con un ajuste de velocidad de muestra manual). Para notificar al cliente sobre estos tipos de cambios de formato, WASAPI envía una notificación de sesión por la implementación registrada de [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) con un motivo de desconexión de **DisconnectReasonFormatChanged**. El cliente puede controlar la notificación si vuelve a abrir la secuencia en el nuevo formato.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API de MMDevice](mmdevice-api.md)
</dt> <dt>

[Acerca de WASAPI](wasapi.md)
</dt> <dt>

[Enrutamiento de flujos](stream-routing.md)
</dt> </dl>

 

 



