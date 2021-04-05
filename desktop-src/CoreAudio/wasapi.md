---
description: Acerca de WASAPI
ms.assetid: 452b9725-b0b9-4888-bbb5-a23e0067e840
title: Acerca de WASAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f869319f3100b797e58c7b43597869c9767ac037
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000636"
---
# <a name="about-wasapi"></a>Acerca de WASAPI

La API de sesión de audio de Windows (WASAPI) permite a las aplicaciones cliente administrar el flujo de datos de audio entre la aplicación y un [dispositivo de punto de conexión de audio](audio-endpoint-devices.md).

Los archivos de encabezado Audioclient. h y Audiopolicy. h definen las interfaces de WASAPI.

Cada secuencia de audio es un miembro de una [sesión de audio](audio-sessions.md). A través de la abstracción de la sesión, un cliente de WASAPI puede identificar una secuencia de audio como miembro de un grupo de secuencias de audio relacionadas. El sistema puede administrar todas las secuencias de la sesión como una sola unidad.

El motor de audio es el [componente de audio de modo de usuario](user-mode-audio-components.md) a través del cual las aplicaciones comparten el acceso a un dispositivo de punto de conexión de audio. El motor de audio transporta datos de audio entre un búfer de punto de conexión y un dispositivo de extremo. Para reproducir una secuencia de audio a través de un dispositivo de punto de conexión de representación, una aplicación escribe periódicamente datos de audio en un búfer de punto de conexión de representación. El motor de audio mezcla los flujos de las distintas aplicaciones. Para registrar una secuencia de audio desde un dispositivo de punto de conexión de captura, una aplicación Lee periódicamente datos de audio desde un búfer de punto de conexión de captura.

WASAPI consta de varias interfaces. La primera de ellas es la interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) . Para acceder a las interfaces de WASAPI, un cliente obtiene primero una referencia a la interfaz **IAudioClient** de un dispositivo de punto de conexión de audio llamando al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con el *IID* de parámetro establecido en **REFIID** IID \_ IAudioClient. El cliente llama al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) para inicializar una secuencia en un dispositivo de extremo. Después de inicializar un flujo, el cliente puede obtener referencias a las otras interfaces de WASAPI llamando al método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .

Muchos de los métodos de WASAPI devuelven el código de error AUDCLNT \_ E \_ \_ se invalidan si el dispositivo de punto de conexión de audio que utiliza una aplicación cliente no es válido. Con frecuencia, la aplicación puede recuperarse de este error. Para obtener más información, consulte [recuperación de un error de Invalid-Device](recovering-from-an-invalid-device-error.md).

WASAPI implementa las interfaces siguientes.



| Interfaz                                            | Descripción                                                                                                                                                     |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)   | Permite a un cliente leer los datos de entrada de un búfer de extremo de captura.                                                                                             |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                 | Permite a un cliente crear e inicializar una secuencia de audio entre una aplicación de audio y el motor de audio o el búfer de hardware de un dispositivo de punto de conexión de audio. |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                   | Permite a un cliente supervisar la velocidad de datos de una secuencia y la posición actual en la secuencia.                                                                        |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)     | Permite que un cliente escriba los datos de salida en un búfer de punto de conexión de representación.                                                                                           |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) | Permite a un cliente configurar los parámetros de control para una sesión de audio y supervisar los eventos de la sesión.                                                 |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) | Permite que un cliente tenga acceso a los controles de sesión y a los controles de volumen tanto para sesiones de audio de proceso cruzado como de proceso.                                 |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)     | Permite a un cliente controlar y supervisar los niveles de volumen de todos los canales de una secuencia de audio.                                                           |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)   | Permite que un cliente controle los niveles de volumen de todos los canales de la sesión de audio a la que pertenece la secuencia.                                          |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)     | Permite a un cliente controlar el nivel de volumen maestro de una sesión de audio.                                                                                        |



 

Los clientes de WASAPI que requieren la notificación de eventos relacionados con la sesión deben implementar la siguiente interfaz.



| Interfaz                                          | Descripción                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) | Proporciona notificaciones de eventos relacionados con la sesión, como cambios en el nivel de volumen, nombre para mostrar y estado de sesión. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de flujos](stream-management.md)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



