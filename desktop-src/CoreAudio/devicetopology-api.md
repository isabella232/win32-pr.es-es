---
description: DeviceTopology API
ms.assetid: 051311ef-dd29-4014-bb9c-4cdccf7ce7de
title: DeviceTopology API
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 3b79def9f1cb1f5ec9342074b813e50993cbc37e7a7af2a9e0b577c730156247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406760"
---
# <a name="devicetopology-api"></a>DeviceTopology API

Consulte la captura [de voz de alta calidad de Microsoft DMO ejemplo](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/audio/aecmicarray).

DeviceTopology API proporciona a las aplicaciones cliente la capacidad de recorrer las topologías de hardware funcionales de los dispositivos de representación y captura de audio. A través de las interfaces y los métodos de la API DeviceTopology, los clientes pueden detectar las subunidades funcionales (por ejemplo, el control de volumen) que se encuentran a lo largo de las rutas de acceso de datos que conducen a y desde dispositivos de punto de conexión de [audio.](audio-endpoint-devices.md) Los clientes pueden recorrer las topologías internas de los dispositivos del adaptador de audio y los dispositivos de punto de conexión de audio y recorrer paso a paso las conexiones que vinculan un dispositivo a otro. Para obtener más información, vea [Topologías de dispositivo.](device-topologies.md)

El archivo de encabezado Devicetopology.h define las interfaces de DeviceTopology API.

Para acceder a las interfaces de la API DeviceTopology, un cliente obtiene primero una referencia a la interfaz [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) para un dispositivo de punto de conexión de audio siguiendo estos pasos:

1.  Mediante una de las técnicas descritas en IMMDevice Interface (Interfaz [**IMMDevice),**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)obtenga una referencia a la **interfaz IMMDevice** para un dispositivo de punto de conexión de audio.
2.  Llame al [**método IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con el *parámetro iid* establecido en **REFIID** \_ IID IDeviceTopology.

El cliente puede obtener referencias a las demás interfaces de la API DeviceTopology llamando a los métodos de la [**interfaz IDeviceTopology.**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)

DeviceTopology API implementa las interfaces siguientes.



| Interfaz                                                  | Descripción                                                                                                                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | Proporciona acceso a un control de ganancia automática de hardware (AGC).                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | Proporciona acceso a un control de nivel de hardware.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | Proporciona acceso a un control de configuración de canal de hardware.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | Proporciona acceso a un control multiplexador de hardware (selector de entrada).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | Proporciona acceso a un control de compensación de "sonoridad".                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | Proporciona acceso a un control de nivel medio de hardware.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | Proporciona acceso a un control de exclusión mutua de hardware.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | Proporciona acceso a un control de demultiplexador de hardware (selector de salida).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | Proporciona acceso a un control de medidor máximo de hardware.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | Proporciona acceso a un control de nivel triple de hardware.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | Proporciona acceso a un control de volumen de hardware.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                           | Representa un punto de conexión entre componentes.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)             | Representa una interfaz de control en un elemento (subunidad o conector).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | Representa una propiedad específica del dispositivo de un conector o una subunidad.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                 | Proporciona acceso a la topología de un dispositivo de audio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)               | Proporciona información sobre los formatos de datos de audio que son compatibles con una conexión de E/S configurada por software (normalmente un canal DMA) entre el dispositivo de audio y la memoria del sistema.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)           | Proporciona información sobre los conectores internos o los conectores que proporcionan una conexión física entre un dispositivo en un adaptador de audio y un dispositivo de punto de conexión externo o interno (por ejemplo, un micrófono o un reproductor de CD). |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                     | Representa una parte (conector o subunidad) de una topología de dispositivo.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                           | Representa una lista de elementos (conectores y subunidades).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)           | Representa una interfaz de control de subunidades genérica que proporciona control por canal sobre el nivel de volumen, en decibelios, de una secuencia de audio o de una banda de frecuencia en una secuencia de audio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                               | Representa una subunidad de hardware (por ejemplo, un control de nivel de volumen) que se encuentra en la ruta de acceso de datos entre un cliente y un dispositivo de punto de conexión de audio.                                                                             |



 

Los clientes de DEVICETopology API que requieren la notificación de eventos de cambio de control en conectores y subunidades deben implementar la siguiente interfaz.



| Interfaz                                            | Descripción                                                                      |
|------------------------------------------------------|----------------------------------------------------------------------------------|
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify) | Proporciona notificaciones cuando cambia el estado de un elemento (conector o subunidad). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Topologías de dispositivo](device-topologies.md)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 
