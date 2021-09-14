---
description: Acerca de WASAPI
ms.assetid: 452b9725-b0b9-4888-bbb5-a23e0067e840
title: Acerca de WASAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f869319f3100b797e58c7b43597869c9767ac037
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164761"
---
# <a name="about-wasapi"></a>Acerca de WASAPI

La Windows Audio Session API (WASAPI) permite a las aplicaciones cliente administrar el flujo de datos de audio entre la aplicación y un dispositivo de punto de [conexión de audio.](audio-endpoint-devices.md)

Los archivos de encabezado Audioclient.h y Audiopolicy.h definen las interfaces WASAPI.

Cada secuencia de audio es miembro de una sesión [de audio.](audio-sessions.md) Mediante la abstracción de sesión, un cliente WASAPI puede identificar una secuencia de audio como miembro de un grupo de secuencias de audio relacionadas. El sistema puede administrar todas las secuencias de la sesión como una sola unidad.

El motor de audio es el [componente de audio en modo de usuario a](user-mode-audio-components.md) través del cual las aplicaciones comparten acceso a un dispositivo de punto de conexión de audio. El motor de audio transporta datos de audio entre un búfer de punto de conexión y un dispositivo de punto de conexión. Para reproducir una secuencia de audio a través de un dispositivo de punto de conexión de representación, una aplicación escribe periódicamente datos de audio en un búfer de punto de conexión de representación. El motor de audio combina las secuencias de las distintas aplicaciones. Para grabar una secuencia de audio desde un dispositivo de punto de conexión de captura, una aplicación lee periódicamente los datos de audio de un búfer de punto de conexión de captura.

WASAPI consta de varias interfaces. La primera de ellas es la [**interfaz IAudioClient.**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) Para acceder a las interfaces WASAPI, un cliente obtiene primero una referencia a la interfaz **IAudioClient** de un dispositivo de punto de conexión de audio mediante una llamada al método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con el parámetro *iid* establecido en **REFIID** \_ IAudioClient. El cliente llama al [**método IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) para inicializar una secuencia en un dispositivo de punto de conexión. Después de inicializar una secuencia, el cliente puede obtener referencias a las otras interfaces WASAPI llamando al [**método IAudioClient::GetService.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)

Muchos de los métodos de WASAPI devuelven código de error AUDCLNT E DEVICE INVALIDATED si el dispositivo de punto de conexión de audio que usa una aplicación cliente \_ \_ deja de ser \_ válido. Con frecuencia, la aplicación puede recuperarse de este error. Para obtener más información, [vea Recuperación de una Invalid-Device error](recovering-from-an-invalid-device-error.md).

WASAPI implementa las interfaces siguientes.



| Interfaz                                            | Descripción                                                                                                                                                     |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)   | Permite a un cliente leer los datos de entrada de un búfer de punto de conexión de captura.                                                                                             |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                 | Permite a un cliente crear e inicializar una secuencia de audio entre una aplicación de audio y el motor de audio o el búfer de hardware de un dispositivo de punto de conexión de audio. |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                   | Permite a un cliente supervisar la velocidad de datos de un flujo y la posición actual en la secuencia.                                                                        |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)     | Permite a un cliente escribir datos de salida en un búfer de punto de conexión de representación.                                                                                           |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) | Permite a un cliente configurar los parámetros de control de una sesión de audio y supervisar los eventos de la sesión.                                                 |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) | Permite que un cliente acceda a los controles de sesión y controles de volumen para sesiones de audio entre procesos y específicas del proceso.                                 |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)     | Permite a un cliente controlar y supervisar los niveles de volumen de todos los canales de una secuencia de audio.                                                           |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)   | Permite a un cliente controlar los niveles de volumen de todos los canales de la sesión de audio a la que pertenece la secuencia.                                          |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)     | Permite a un cliente controlar el nivel de volumen maestro de una sesión de audio.                                                                                        |



 

Los clientes WASAPI que requieren la notificación de eventos relacionados con la sesión deben implementar la siguiente interfaz.



| Interfaz                                          | Descripción                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) | Proporciona notificaciones de eventos relacionados con la sesión, como cambios en el nivel de volumen, el nombre para mostrar y el estado de sesión. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de flujos](stream-management.md)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



