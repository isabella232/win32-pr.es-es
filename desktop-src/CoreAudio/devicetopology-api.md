---
description: API de DeviceTopology
ms.assetid: 051311ef-dd29-4014-bb9c-4cdccf7ce7de
title: API de DeviceTopology
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 472c02cd59ca0cadd922cbe398a768c97cfab73a
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105660111"
---
# <a name="devicetopology-api"></a>API de DeviceTopology

Vea el [ejemplo de la captura de voz de alta calidad de Microsoft DMO](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/audio/aecmicarray).

La API DeviceTopology proporciona a las aplicaciones cliente la capacidad de atravesar las topologías de hardware funcional de los dispositivos de captura y representación de audio. A través de las interfaces y los métodos de la API de DeviceTopology, los clientes pueden detectar las subunidades funcionales (por ejemplo, control de volumen) que se encuentran a lo largo de las rutas de acceso de datos que conducen a los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md)y desde ellos. Los clientes pueden atravesar las topologías internas de los dispositivos de adaptador de audio y los dispositivos de punto de conexión de audio y pasar por las conexiones que vinculan un dispositivo a otro. Para obtener más información, consulte [topologías de dispositivos](device-topologies.md).

El archivo de encabezado Devicetopology. h define las interfaces de la API de DeviceTopology.

Para acceder a las interfaces de la API de DeviceTopology, un cliente obtiene primero una referencia a la interfaz [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) para un dispositivo de punto de conexión de audio siguiendo estos pasos:

1.  Mediante el uso de una de las técnicas descritas en la [**interfaz IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice), obtenga una referencia a la interfaz **IMMDevice** para un dispositivo de punto de conexión de audio.
2.  Llame al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con el *IID* de parámetro establecido en **REFIID** IID \_ IDeviceTopology.

El cliente puede obtener referencias a las otras interfaces de la API de DeviceTopology llamando a los métodos de la interfaz [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) .

La API de DeviceTopology implementa las interfaces siguientes.



| Interfaz                                                  | Descripción                                                                                                                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | Proporciona acceso a un control de ganancia automática (AGC) de hardware.                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | Proporciona acceso a un control de nivel bajo de hardware.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | Proporciona acceso a un control de configuración de canal de hardware.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | Proporciona acceso a un control de multiplexor de hardware (selector de entrada).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | Proporciona acceso a un control de compensación de "sonoridad".                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | Proporciona acceso a un control de nivel de intervalo medio de hardware.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | Proporciona acceso a un control de silencio de hardware.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | Proporciona acceso a un control de desmultiplexador de hardware (selector de resultados).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | Proporciona acceso a un control de medidor máximo de hardware.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | Proporciona acceso a un control de nivel de agudos de hardware.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | Proporciona acceso a un control de volumen de hardware.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                           | Representa un punto de conexión entre los componentes.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)             | Representa una interfaz de control en un elemento (subunidad o conector).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | Representa una propiedad específica del dispositivo de un conector o de una subunidad.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                 | Proporciona acceso a la topología de un dispositivo de audio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)               | Proporciona información sobre los formatos de datos de audio admitidos por una conexión de e/s configurada por software (normalmente un canal DMA) entre el dispositivo de audio y la memoria del sistema.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)           | Proporciona información acerca de las clavijas o conectores internos que proporcionan una conexión física entre un dispositivo de un adaptador de audio y un dispositivo de extremo externo o interno (por ejemplo, un micrófono o reproductor de CD). |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                     | Representa una parte (conector o subunidad) de una topología de dispositivo.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                           | Representa una lista de elementos (conectores y subunidades).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)           | Representa una interfaz de control de subunidad genérica que proporciona control por canal sobre el nivel de volumen, en decibelios, de una secuencia de audio o de una banda de frecuencia en una secuencia de audio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                               | Representa una subunidad de hardware (por ejemplo, un control de nivel de volumen) que se encuentra en la ruta de acceso de datos entre un cliente y un dispositivo de punto de conexión de audio.                                                                             |



 

Los clientes de la API de DeviceTopology que requieren la notificación de eventos de cambio de control en conectores y subunidads deben implementar la siguiente interfaz.



| Interfaz                                            | Descripción                                                                      |
|------------------------------------------------------|----------------------------------------------------------------------------------|
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify) | Proporciona notificaciones cuando cambia el estado de una parte (conector o subunidad). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Topologías de dispositivos](device-topologies.md)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 
