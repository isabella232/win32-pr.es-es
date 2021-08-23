---
description: Enumeración de dispositivos de audio
ms.assetid: 20110ffc-5eff-4279-abea-53115803b6ee
title: Enumeración de dispositivos de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5d21ec2de2b08ca3c6f26884bd210b2f149caaa9e3b6a4402b69dde9fb7540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018383"
---
# <a name="enumerating-audio-devices"></a>Enumeración de dispositivos de audio

La primera tarea de una aplicación de audio cliente es buscar un dispositivo de audio adecuado para su uso. LA [API MMDevice permite](mmdevice-api.md) a los clientes detectar los dispositivos de punto de conexión de [audio](audio-endpoint-devices.md) en el sistema y determinar qué dispositivos son adecuados para que los use la aplicación. Esta API permite a los clientes recuperar recopilaciones de los dispositivos de punto de conexión disponibles y obtener las funcionalidades de cada dispositivo. El archivo de encabezado Mmdeviceapi.h define las interfaces de la API MMDevice.

Un adaptador de audio puede contener varios dispositivos, por ejemplo, un dispositivo de representación de onda y un dispositivo de captura de onda. Se trata de dispositivos adaptadores en lugar de dispositivos de punto de conexión. Como se mencionó anteriormente, el administrador de Plug and Play registra los dispositivos del adaptador, a diferencia de los dispositivos de punto de conexión, que están registrados por el administrador de puntos de conexión. Cada dispositivo de adaptador normalmente admite uno o varios dispositivos de punto de conexión. Un dispositivo de punto de conexión de representación (por ejemplo, auriculares) puede recibir una secuencia de datos de audio de una aplicación cliente y un dispositivo de punto de conexión de captura (por ejemplo, un micrófono) puede enviar una secuencia de audio a una aplicación cliente.

Antes de enumerar los dispositivos de punto de conexión en el sistema, el cliente debe llamar primero a la Windows [**función CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un enumerador de dispositivos. Un enumerador de dispositivos es un objeto con una [**interfaz IMMDeviceEnumerator.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) Para obtener información sobre **CoCreateInstance,** consulte la documentación Windows SDK.

El cliente llama al [**método IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) para crear una colección de objetos de punto de conexión. Cada objeto de punto de conexión representa un dispositivo de punto de conexión de audio en el sistema. En esta llamada, el cliente especifica si la recopilación debe contener todos los dispositivos de representación del sistema, todos los dispositivos de captura o ambos.

Una colección de dispositivos es un objeto con una [**interfaz IMMDeviceCollection.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) Cada elemento de una colección de dispositivos es un objeto de punto de conexión con al menos las dos interfaces siguientes:

-   Interfaz [**IMMDevice.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) Un cliente obtiene una referencia a la interfaz **IMMDevice** de un objeto de punto de conexión en una colección de dispositivos mediante una llamada al [**método IMMDeviceCollection::Item.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item)
-   Interfaz [**IMMEndpoint.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint) Un cliente obtiene una referencia a la interfaz **IMMEndpoint** de un objeto de punto de conexión mediante una llamada al [**método IMMDevice::QueryInterface.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

Después de recuperar una colección de dispositivos de punto de conexión, el cliente puede consultar las propiedades de los dispositivos individuales de la colección para determinar su idoneidad para su uso. Para obtener un ejemplo de código que muestra cómo enumerar los dispositivos de punto de conexión y consultar sus propiedades, vea [Propiedades del dispositivo](device-properties.md).

Después de seleccionar un dispositivo adecuado, el cliente puede llamar al método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para activar las interfaces específicas del dispositivo en [WASAPI,](wasapi.md) [DeviceTopology API](devicetopology-api.md)y [EndpointVolume API](endpointvolume-api.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> </dl>

 

 
