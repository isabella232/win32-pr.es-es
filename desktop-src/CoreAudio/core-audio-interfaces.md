---
description: 'Esta referencia de programación para el SDK de audio básico incluye las siguientes interfaces:'
ms.assetid: b18e2094-e974-4c23-b70b-ace5a168132d
title: Interfaces de audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eed875bad93bed1625a175bd74b849f139a0140
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152754"
---
# <a name="core-audio-interfaces"></a>Interfaces de audio principales

Esta referencia de programación para el SDK de audio básico incluye las siguientes interfaces:

## <a name="mmdevice-api"></a>API de MMDevice

La API de dispositivo multimedia de Windows (MMDevice) permite a los clientes de audio detectar [dispositivos de punto de conexión de audio](audio-endpoint-devices.md), determinar sus capacidades y crear instancias de controlador para esos dispositivos. El archivo de encabezado Mmdeviceapi. h define las interfaces de la API de MMDevice. Para obtener más información, consulte Acerca de la [API de MMDevice](mmdevice-api.md).

En la tabla siguiente se enumeran las interfaces de MMDevice disponibles con el SDK de Core Audio para Windows Vista.



| Interfaz                                              | Descripción                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                         | Representa un dispositivo de audio.                                                                                                                                                                    |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)     | Representa una colección de dispositivos de audio.                                                                                                                                                      |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)     | Proporciona métodos para enumerar los dispositivos de audio.                                                                                                                                                |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                     | Representa un dispositivo de punto de conexión de audio.                                                                                                                                                           |
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Proporciona notificaciones cuando se agrega o se quita un dispositivo de punto de conexión de audio, cuando cambia el estado o las propiedades de un dispositivo, o cuando se produce un cambio en el rol predeterminado que se asigna a un dispositivo. |



 

## <a name="wasapi"></a>WASAPI

La API de sesión de audio de Windows (WASAPI) permite a las aplicaciones cliente administrar el flujo de datos de audio entre la aplicación y un [dispositivo de punto de conexión de audio](audio-endpoint-devices.md). Los archivos de encabezado Audioclient. h y Audiopolicy. h definen las interfaces de WASAPI. Para obtener más información, vea [acerca de WASAPI](wasapi.md).

En la tabla siguiente se enumeran las interfaces de WASAPI disponibles con el SDK de audio básico para Windows Vista y versiones posteriores.



| Interfaz                                                                                    | Descripción                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActivateAudioInterfaceAsyncOperation**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation)       | Representa una operación asincrónica que activa una interfaz [WASAPI](wasapi.md) y proporciona un método para recuperar los resultados de la activación.<br/> Se aplica a partir de Windows 8.<br/> |
| [**IActivateAudioInterfaceCompletionHandler**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler) | Proporciona una devolución de llamada para indicar que se ha completado la activación de una interfaz [WASAPI](wasapi.md) .<br/> Se aplica a partir de Windows 8.<br/>                                                  |
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)                                           | Permite a un cliente leer los datos de entrada de un búfer de extremo de captura.                                                                                                                                       |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                                                         | Permite a un cliente crear e inicializar una secuencia de audio entre una aplicación de audio y el motor de audio o el búfer de hardware de un dispositivo de punto de conexión de audio.                                           |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                                                           | Permite a un cliente supervisar la velocidad de datos de una secuencia y la posición actual en la secuencia.                                                                                                                  |
| [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)<br/>                                              | Permite a un cliente obtener la posición actual del dispositivo.<br/>                                                                                                                                           |
| [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)<br/>                            | Permite a un cliente establecer la velocidad de muestra de una secuencia.<br/>                                                                                                                                           |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)                                             | Permite que un cliente escriba los datos de salida en un búfer de punto de conexión de representación.                                                                                                                                     |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)                                         | Permite a un cliente configurar los parámetros de control para una sesión de audio y supervisar los eventos de la sesión.                                                                                           |
| [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)<br/>                            | Permite a un cliente obtener información acerca de la sesión de audio.<br/>                                                                                                                                   |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)                                         | Permite que un cliente tenga acceso a los controles de sesión y a los controles de volumen tanto para sesiones de audio de proceso cruzado como de proceso.                                                                           |
| [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)<br/>                            | Administra todas las submezclas, incluida la enumeración y la notificación de submezclas. También proporciona compatibilidad para las notificaciones de patos.<br/>                                                                   |
| [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)<br/>                        | Permite a un cliente enumerar las sesiones de audio.<br/>                                                                                                                                                  |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)                                             | Permite a un cliente controlar y supervisar los niveles de volumen de todos los canales de una secuencia de audio.                                                                                                     |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)                                           | Permite que un cliente controle los niveles de volumen de todos los canales de la sesión de audio a la que pertenece la secuencia.                                                                                    |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)                                             | Permite a un cliente controlar el nivel de volumen maestro de una sesión de audio.                                                                                                                                  |
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)                                           | Proporciona notificaciones de eventos relacionados con la sesión, como cambios en el nivel de volumen, nombre para mostrar y estado de sesión.                                                                                    |
| [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)<br/>                    | Envía notificaciones cuando se producen cambios en la sesión. <br/>                                                                                                                                               |
| [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)<br/>              | Envía notificaciones sobre los cambios de perdedor del sistema pendientes.<br/>                                                                                                                                      |



 

## <a name="devicetopology-api"></a>API de DeviceTopology

La API DeviceTopology proporciona a las aplicaciones cliente la capacidad de atravesar las topologías de hardware funcional de los dispositivos de captura y representación de audio. El archivo de encabezado Devicetopology. h define las interfaces de la API de DeviceTopology. Para más información, consulte [topologías de dispositivos](device-topologies.md) y [**API de DeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology).

En la tabla siguiente se enumeran las interfaces de DeviceTopology disponibles con el SDK de audio básico para Windows Vista y versiones posteriores.



| Interfaz                                                           | Descripción                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)              | Proporciona acceso a un control de ganancia automática (AGC) de hardware.                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                                    | Proporciona acceso a un control de nivel bajo de hardware.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)                  | Proporciona acceso a un control de configuración de canal de hardware.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)                  | Proporciona acceso a un control de multiplexor de hardware (selector de entrada).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                            | Proporciona acceso a un control de compensación de "sonoridad".                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                            | Proporciona acceso a un control de nivel de intervalo medio de hardware.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                                    | Proporciona acceso a un control de silencio de hardware.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)                | Proporciona acceso a un control de desmultiplexador de hardware (selector de resultados).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                          | Proporciona acceso a un control de medidor máximo de hardware.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                                | Proporciona acceso a un control de nivel de agudos de hardware.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)                      | Proporciona acceso a un control de volumen de hardware.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                                    | Representa un punto de conexión entre los componentes.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)                      | Representa una interfaz de control en un elemento (subunidad o conector).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)          | Representa una propiedad específica del dispositivo de un conector o de una subunidad.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                          | Proporciona acceso a la topología de un dispositivo de audio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)                        | Proporciona información sobre los formatos de datos de audio admitidos por una conexión de e/s configurada por software (normalmente un canal DMA) entre el dispositivo de audio y la memoria del sistema.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)                    | Proporciona información acerca de las clavijas o conectores internos que proporcionan una conexión física entre un dispositivo de un adaptador de audio y un dispositivo de extremo externo o interno (por ejemplo, un micrófono o reproductor de CD). |
| [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)<br/>       | Proporciona un acceso cómodo a la propiedad **KSPROPERTY \_ Jack \_ DESCRIPTION2** de un conector a un dispositivo de extremo.<br/>                                                                                            |
| [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)<br/> | Proporciona información sobre el receptor de conectores si el conector es compatible con el hardware.<br/>                                                                                                                             |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                              | Representa una parte (conector o subunidad) de una topología de dispositivo.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                                    | Representa una lista de elementos (conectores y subunidades).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)                    | Representa una interfaz de control de subunidad genérica que proporciona control por canal sobre el nivel de volumen, en decibelios, de una secuencia de audio o de una banda de frecuencia en una secuencia de audio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                                        | Representa una subunidad de hardware (por ejemplo, un control de nivel de volumen) que se encuentra en la ruta de acceso de datos entre un cliente y un dispositivo de punto de conexión de audio.                                                                             |
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify)                | Proporciona notificaciones cuando cambia el estado de una parte (conector o subunidad).                                                                                                                                          |



 

## <a name="endpointvolume-api"></a>API de EndpointVolume

La API de EndpointVolume permite a los clientes especializados controlar y supervisar los niveles de volumen de los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md). El archivo de encabezado Endpointvolume. h define las interfaces de la API de EndpointVolume. Para obtener más información, consulte [**ENDPOINTVOLUME API**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) .

En la tabla siguiente se enumeran las interfaces de EndpointVolume disponibles con el SDK de Core Audio para Windows Vista.



| **Interfaz**                                                        | **Descripción**                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)                 | Representa los controles de volumen en la secuencia de audio hacia o desde un dispositivo de punto de conexión de audio.           |
| [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)<br/>  | Proporciona controles de volumen en la secuencia de audio hacia o desde un punto de conexión de dispositivo.<br/>             |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation)             | Representa un medidor de picos en la secuencia de audio hacia o desde un dispositivo de punto de conexión de audio.                  |
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Proporciona notificaciones cuando cambia el nivel de volumen o el estado de silenciación de un dispositivo de punto de conexión de audio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> </dl>

 

