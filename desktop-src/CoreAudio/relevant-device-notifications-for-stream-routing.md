---
description: Obtenga información sobre las notificaciones para el enrutamiento de flujos. Las API implementan el enrutamiento de flujos controlando el cambio de secuencia a un nuevo punto de conexión de audio predeterminado.
ms.assetid: caf831bb-b8de-467f-bdb4-f9f8991dc7a8
title: Notificaciones pertinentes para el enrutamiento de flujos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a843c1d8b5cfd740ada5049cb9428e7745072d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164849"
---
# <a name="relevant-notifications-for-stream-routing"></a>Notificaciones pertinentes para el enrutamiento de flujos

En Windows 7, las API de plataforma de alto nivel que usan core audio API, como las API de Media Foundation, Direct Sound y Wave, implementan la característica de enrutamiento de secuencias mediante el control de la conmutación de secuencias de un dispositivo existente a un nuevo punto de conexión de audio predeterminado. Las aplicaciones multimedia que usan estas API usan el comportamiento de enrutamiento de flujos sin modificaciones en el origen. Los clientes WASAPI directos pueden usar las notificaciones enviadas por los componentes de Core Audio e implementar la característica de enrutamiento de secuencias.

Para implementar la característica de enrutamiento de flujos, un cliente debe escuchar dos tipos de eventos: notificaciones de cambio de dispositivo y notificaciones de desconexión de sesión. En la implementación proporcionada por las API de alto nivel, estos eventos se envían para los puntos de conexión de dispositivo predeterminados creados mediante una llamada a [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Para obtener más información, consulte [Getting the Device Endpoint for Stream Routing](getting-the-default-device-endpoint-for-stream-routing.md).

El componente de audio principal MMDeviceAPI ofrece devoluciones de llamada de notificación cuando se agregan, quitan o modifican dispositivos de audio. Los cambios de formato y de sesión de audio se notifican como eventos a través de WASAPI.

## <a name="device-change-notifications"></a>Notificaciones de cambio de dispositivo

MMDeviceAPI genera eventos cuando se agregan, quitan o modifican dispositivos de audio. Si el cliente va a proporcionar la funcionalidad de enrutamiento de flujos, debe implementar la interfaz [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) y registrar su implementación con MMDeviceAPI.

Para obtener notificaciones de cambio de dispositivo, el cliente debe realizar las siguientes tareas:

-   Implemente [**la interfaz IMMNotificationClient para**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) controlar las notificaciones de cambio de dispositivo enviadas por MMDeviceAPI.
-   Registre la [**implementación de IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) con MMDeviceAPI llamando al método [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback)

Una vez registrada la implementación del cliente de estas interfaces, el cliente recibe notificaciones en forma de devoluciones de llamada a través de los métodos de estas interfaces. MMDeviceAPI llama a los métodos [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) cuando genera eventos de nivel de punto de conexión (cambios de estado del punto de conexión, llegadas de nuevos puntos de conexión, eliminaciones de puntos de conexión, cambios de punto de conexión predeterminados y cambios en las propiedades del punto de conexión).

Si el cliente desea proporcionar enrutamiento de secuencias para el dispositivo predeterminado, el cliente debe implementar el comportamiento de cambio del dispositivo cuando recibe la notificación a través de la devolución de llamada [**IMMNotificationClient::OnDefaultDeviceChanged.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged)

## <a name="audio-session-change-notifications"></a>Notificaciones de cambio de sesión de audio

Los cambios de sesión de audio y los cambios de formato se notifican como eventos de sesión de audio a través de WASAPI. Un cliente WASAPI implementa la [**interfaz IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) y registra la implementación con WASAPI.

Para obtener notificaciones de cambio de sesión de audio, el cliente debe realizar las siguientes tareas:

-   Implemente la [**interfaz IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para controlar las notificaciones de cambio de formato enviadas por WASAPI.
-   Registre la [**implementación de IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) con WASAPI llamando al [**método IAudioSessionControl::RegisterAudioSessionNotification.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification)

[**WASAPI llama a los métodos IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) cuando se producen cambios en la sesión de audio. Estos eventos se genera cuando cambia el nombre para mostrar, la ruta de acceso del icono, el volumen, el parámetro de agrupación o el estado de la sesión.

Para implementar la característica de enrutamiento de flujos, el cliente debe esperar a la notificación de desconexión de sesión. Cuando se desconecta una sesión de audio o se cambia el formato de un dispositivo, WASAPI envía las notificaciones de cliente en forma de devoluciones de llamada a través de [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Con la notificación de desconexión, WASAPI también envía un valor que indica por qué se desconectó la sesión. Esto puede ocurrir por varios motivos, como que el dispositivo se quitó, el servidor se detuvo, y así sucesivamente. Para obtener la lista completa de motivos, vea la **enumeración AudioSessionDisconnectReason** definida en AudioPolicy.h. Si cambia el dispositivo predeterminado, el cliente debe esperar las notificaciones (si aún no se han recibido) que van acompañadas de un valor **DisconnectReasonDeviceRemoval.** En respuesta a estas notificaciones, el cliente podría volver a abrir la secuencia en el nuevo dispositivo predeterminado.

Dado que todas estas operaciones son asícrticas, no se puede predecir el orden en el que la aplicación recibe notificaciones. Sin embargo, normalmente, la aplicación recibe el **valor AudioSessionDisconnect** antes de la notificación de cambio de dispositivo predeterminada.

### <a name="format-change-notifications"></a>Dar formato a las notificaciones de cambio

Los cambios de formato de audio se producen cuando cambia el formato de la secuencia. Esto puede ocurrir cuando el usuario selecciona un nuevo formato en el panel de **control** Sonido o el nuevo dispositivo predeterminado admite un nuevo formato (por ejemplo, HDMI o determinadas interfaces de audio profesionales con un ajuste manual de la frecuencia de muestreo). Para notificar al cliente estos tipos de cambios de formato, WASAPI envía una notificación de sesión mediante la implementación registrada de [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) con un motivo de **desconexión de DisconnectReasonFormatChanged**. El cliente puede controlar la notificación si vuelve a abrir la secuencia en el nuevo formato.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de MMDevice API](mmdevice-api.md)
</dt> <dt>

[Acerca de WASAPI](wasapi.md)
</dt> <dt>

[Enrutamiento de flujos](stream-routing.md)
</dt> </dl>

 

 



