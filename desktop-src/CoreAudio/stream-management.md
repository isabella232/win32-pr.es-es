---
description: Administración de flujos
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Administración de flujos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07180d8b46f4d079c08f4b619cf4a7773a6104d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164790"
---
# <a name="stream-management"></a>Administración de flujos

Después de enumerar los dispositivos de punto de conexión de [audio](audio-endpoint-devices.md) en el sistema e identificar un dispositivo de representación o captura adecuado, la siguiente tarea de una aplicación cliente de audio es abrir una conexión con el dispositivo de punto de conexión y administrar el flujo de datos de audio a través de esa conexión. [WASAPI](wasapi.md) permite a los clientes crear y administrar secuencias de audio.

WASAPI implementa varias interfaces para proporcionar servicios de administración de flujos a los clientes de audio. La interfaz principal es [**IAudioClient.**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) Un cliente obtiene la interfaz **IAudioClient** para un dispositivo de punto de conexión de audio mediante una llamada al método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (con el parámetro *iid* establecido en **REFIID** \_ IID IAudioClient) en el objeto de punto de conexión.

El cliente llama a los métodos de la [**interfaz IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) para hacer lo siguiente:

-   Descubra qué formatos de audio admite el dispositivo de punto de conexión.
-   Obtiene el tamaño del búfer del punto de conexión.
-   Obtenga el formato de secuencia y la latencia.
-   Inicie, detenga y restablezca la secuencia que fluye a través del dispositivo del punto de conexión.
-   Acceso a servicios de audio adicionales.

Para crear una secuencia, un cliente llama al [**método IAudioClient::Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) A través de este método, el cliente especifica el formato de datos para la secuencia, el tamaño del búfer del punto de conexión y si la secuencia funciona en modo compartido o exclusivo.

Los métodos restantes de [**la interfaz IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) se agrupan en dos grupos:

-   Métodos a los que se puede llamar solo después de que el flujo se haya abierto [**mediante IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Métodos a los que se puede llamar en cualquier momento antes o después de la [**llamada a Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

Solo se puede llamar a los métodos siguientes después de llamar a [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):

-   [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [**IAudioClient::GetStreamLatency**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [**IAudioClient::Reset**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [**IAudioClient::Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [**IAudioClient::Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

Se puede llamar a los métodos siguientes antes o después de [**la llamada AAudioClient::Initialize:**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

-   [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

Para acceder a los servicios de cliente de audio adicionales, el cliente llama al [**método IAudioClient::GetService.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) A través de este método, el cliente puede obtener referencias a las interfaces siguientes:

-   [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    Escribe datos de representación en un búfer de punto de conexión de representación de audio.

-   [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    Lee los datos capturados de un búfer de punto de conexión de captura de audio.

-   [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    Se comunica con el administrador de sesión de audio para configurar y administrar la sesión de audio asociada a la secuencia.

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    Controla el nivel de volumen de la sesión de audio asociada a la secuencia.

-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    Controla los niveles de volumen de los canales individuales de la sesión de audio asociada a la secuencia.

-   [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    Supervisa la velocidad de datos del flujo y la posición del flujo.

Además, los clientes WASAPI que requieren la notificación de eventos relacionados con la sesión deben implementar la siguiente interfaz:

-   [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    Para recibir notificaciones de eventos, el cliente pasa un puntero a su interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) al método [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) como parámetro de llamada.

Por último, un cliente podría usar una API de nivel superior para crear una secuencia de audio, pero también requerir acceso a los controles de sesión y controles de volumen para la sesión que contiene la secuencia. Normalmente, una API de nivel superior no proporciona este acceso. El cliente puede obtener los controles de una sesión determinada a través de la [**interfaz IAudioSessionManager.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) Esta interfaz permite al cliente obtener las interfaces [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) e [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) para una sesión sin necesidad de que el cliente use la interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) para crear una secuencia y asignar la secuencia a la sesión. Un cliente obtiene la interfaz **IAudioSessionManager** para un dispositivo de punto de conexión de audio llamando al método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (con el parámetro *iid* establecido en **REFIID** IAudioSessionManager) en el objeto de punto de \_ conexión.

Las [**interfaces IAudioSessionControl,**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)e [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) se definen en el archivo de encabezado Audiopolicy.h. Todas las demás interfaces WASAPI se definen en el archivo de encabezado Audioclient.h.

En las secciones siguientes se describe cómo usar WASAPI para administrar secuencias de audio:

-   [Acerca de WASAPI](wasapi.md)
-   [Representación de una secuencia](rendering-a-stream.md)
-   [Captura de una secuencia](capturing-a-stream.md)
-   [Grabación de bucles bucles](loopback-recording.md)
-   [Modo exclusivo Secuencias](exclusive-mode-streams.md)
-   [Recuperación de un error Invalid-Device error](recovering-from-an-invalid-device-error.md)
-   [Uso de un dispositivo de comunicación](using-the-communication-device.md)
-   [Enrutamiento de flujos](stream-routing.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 



