---
description: 'Esta referencia de programación para core audio SDK incluye las interfaces siguientes:'
ms.assetid: b18e2094-e974-4c23-b70b-ace5a168132d
title: Interfaces de audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 330bb620b48b865db3db2ab5ea5625b7859588bd8e53e1addbcd8fd8ec9bda6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109475"
---
# <a name="core-audio-interfaces"></a>Interfaces de audio principales

Esta referencia de programación para core audio SDK incluye las interfaces siguientes:

## <a name="mmdevice-api"></a>MMDevice API

La API Windows Multimedia Device (MMDevice) permite a los clientes de audio detectar dispositivos de punto de conexión de [audio,](audio-endpoint-devices.md)determinar sus funcionalidades y crear instancias de controlador para esos dispositivos. El archivo de encabezado Mmdeviceapi.h define las interfaces de la API MMDevice. Para obtener más información, consulte [Acerca de MMDevice API.](mmdevice-api.md)

En la tabla siguiente se enumeran las interfaces MMDevice disponibles con core audio SDK para Windows Vista.



| Interfaz                                              | Descripción                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                         | Representa un dispositivo de audio.                                                                                                                                                                    |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)     | Representa una colección de dispositivos de audio.                                                                                                                                                      |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)     | Proporciona métodos para enumerar dispositivos de audio.                                                                                                                                                |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                     | Representa un dispositivo de punto de conexión de audio.                                                                                                                                                           |
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Proporciona notificaciones cuando se agrega o quita un dispositivo de punto de conexión de audio, cuando cambia el estado o las propiedades de un dispositivo, o cuando hay un cambio en el rol predeterminado asignado a un dispositivo. |



 

## <a name="wasapi"></a>WASAPI

La WINDOWS Audio Session API (WASAPI) permite a las aplicaciones cliente administrar el flujo de datos de audio entre la aplicación y un dispositivo de punto de [conexión de audio.](audio-endpoint-devices.md) Los archivos de encabezado Audioclient.h y Audiopolicy.h definen las interfaces WASAPI. Para obtener más información, vea [Acerca de WASAPI.](wasapi.md)

En la tabla siguiente se enumeran las interfaces WASAPI disponibles con core Audio SDK para Windows Vista y versiones posteriores.



| Interfaz                                                                                    | Descripción                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActivateAudioInterfaceAsyncOperation**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation)       | Representa una operación asincrónica que activa una [interfaz WASAPI](wasapi.md) y proporciona un método para recuperar los resultados de la activación.<br/> Se aplica a partir de Windows 8.<br/> |
| [**IActivateAudioInterfaceCompletionHandler**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler) | Proporciona una devolución de llamada para indicar que se ha completado la activación de una interfaz [WASAPI.](wasapi.md)<br/> Se aplica a partir de Windows 8.<br/>                                                  |
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)                                           | Permite a un cliente leer los datos de entrada de un búfer de punto de conexión de captura.                                                                                                                                       |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                                                         | Permite a un cliente crear e inicializar una secuencia de audio entre una aplicación de audio y el motor de audio o el búfer de hardware de un dispositivo de punto de conexión de audio.                                           |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                                                           | Permite a un cliente supervisar la velocidad de datos de un flujo y la posición actual en la secuencia.                                                                                                                  |
| [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)<br/>                                              | Permite que un cliente obtenga la posición actual del dispositivo.<br/>                                                                                                                                           |
| [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)<br/>                            | Permite a un cliente establecer la frecuencia de muestreo de una secuencia.<br/>                                                                                                                                           |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)                                             | Permite a un cliente escribir datos de salida en un búfer de punto de conexión de representación.                                                                                                                                     |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)                                         | Permite a un cliente configurar los parámetros de control para una sesión de audio y supervisar los eventos de la sesión.                                                                                           |
| [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)<br/>                            | Permite a un cliente obtener información sobre la sesión de audio.<br/>                                                                                                                                   |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)                                         | Permite que un cliente acceda a los controles de sesión y controles de volumen para sesiones de audio entre procesos y específicas del proceso.                                                                           |
| [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)<br/>                            | Administra todas las submezclas, incluida la enumeración y la notificación de submezclas. También proporciona compatibilidad con notificaciones de afijo.<br/>                                                                   |
| [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)<br/>                        | Permite a un cliente enumerar sesiones de audio.<br/>                                                                                                                                                  |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)                                             | Permite a un cliente controlar y supervisar los niveles de volumen de todos los canales de una secuencia de audio.                                                                                                     |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)                                           | Permite a un cliente controlar los niveles de volumen de todos los canales de la sesión de audio a la que pertenece la secuencia.                                                                                    |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)                                             | Permite a un cliente controlar el nivel de volumen maestro de una sesión de audio.                                                                                                                                  |
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)                                           | Proporciona notificaciones de eventos relacionados con la sesión, como cambios en el nivel de volumen, el nombre para mostrar y el estado de sesión.                                                                                    |
| [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)<br/>                    | Envía notificaciones cuando se producen cambios en la sesión. <br/>                                                                                                                                               |
| [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)<br/>              | Envía notificaciones sobre los cambios pendientes del sistema.<br/>                                                                                                                                      |



 

## <a name="devicetopology-api"></a>DeviceTopology API

DeviceTopology API proporciona a las aplicaciones cliente la capacidad de recorrer las topologías de hardware funcionales de los dispositivos de representación y captura de audio. El archivo de encabezado Devicetopology.h define las interfaces de DeviceTopology API. Para más información, consulte [Device Topologies](device-topologies.md) and DeviceTopology API ( Topologías de [**dispositivos y Api DeviceTopology).**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)

En la tabla siguiente se enumeran las interfaces DeviceTopology disponibles con core Audio SDK para Windows Vista y versiones posteriores.



| Interfaz                                                           | Descripción                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)              | Proporciona acceso a un control de ganancia automática de hardware (AGC).                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                                    | Proporciona acceso a un control de hardware de nivel de hardware.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)                  | Proporciona acceso a un control de configuración de canal de hardware.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)                  | Proporciona acceso a un control multiplexador de hardware (selector de entrada).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                            | Proporciona acceso a un control de compensación de "sonoridad".                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                            | Proporciona acceso a un control de nivel medio de hardware.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                                    | Proporciona acceso a un control de exclusión mutua de hardware.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)                | Proporciona acceso a un control de demultiplexador de hardware (selector de salida).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                          | Proporciona acceso a un control de medidor máximo de hardware.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                                | Proporciona acceso a un control de nivel triple de hardware.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)                      | Proporciona acceso a un control de volumen de hardware.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                                    | Representa un punto de conexión entre componentes.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)                      | Representa una interfaz de control en un elemento (subunidad o conector).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)          | Representa una propiedad específica del dispositivo de un conector o una subunidad.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                          | Proporciona acceso a la topología de un dispositivo de audio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)                        | Proporciona información sobre los formatos de datos de audio que son compatibles con una conexión de E/S configurada por software (normalmente un canal DMA) entre el dispositivo de audio y la memoria del sistema.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)                    | Proporciona información sobre los conectores internos o los conectores que proporcionan una conexión física entre un dispositivo en un adaptador de audio y un dispositivo de punto de conexión externo o interno (por ejemplo, un micrófono o un reproductor de CD). |
| [**IKs JackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)<br/>       | Proporciona un acceso cómodo a la **propiedad \_ KSPROPERTY JACK \_ DESCRIPTION2** de un conector a un dispositivo de punto de conexión.<br/>                                                                                            |
| [**IKs JackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)<br/> | Proporciona información sobre el receptor del conector si el conector es compatible con el hardware.<br/>                                                                                                                             |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                              | Representa una parte (conector o subunidad) de una topología de dispositivo.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                                    | Representa una lista de elementos (conectores y subunidades).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)                    | Representa una interfaz de control de subunidades genérica que proporciona control por canal sobre el nivel de volumen, en decibelios, de una secuencia de audio o de una banda de frecuencia en una secuencia de audio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                                        | Representa una subunidad de hardware (por ejemplo, un control de nivel de volumen) que se encuentra en la ruta de acceso de datos entre un cliente y un dispositivo de punto de conexión de audio.                                                                             |
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify)                | Proporciona notificaciones cuando cambia el estado de un elemento (conector o subunidad).                                                                                                                                          |



 

## <a name="endpointvolume-api"></a>EndpointVolume API

EndpointVolume API permite a los clientes especializados controlar y supervisar los niveles de volumen de los dispositivos de [punto de conexión de audio.](audio-endpoint-devices.md) El archivo de encabezado Endpointvolume.h define las interfaces de EndpointVolume API. Para más información, consulte [**EndpointVolume API**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) .

En la tabla siguiente se enumeran las interfaces EndpointVolume disponibles con core Audio SDK para Windows Vista.



| **Interfaz**                                                        | **Descripción**                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)                 | Representa los controles de volumen de la secuencia de audio hacia o desde un dispositivo de punto de conexión de audio.           |
| [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)<br/>  | Proporciona controles de volumen en la secuencia de audio hacia o desde un punto de conexión de dispositivo.<br/>             |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation)             | Representa un medidor máximo en la secuencia de audio hacia o desde un dispositivo de punto de conexión de audio.                  |
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Proporciona notificaciones cuando cambia el nivel de volumen o el estado muting de un dispositivo de punto de conexión de audio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> </dl>

 

