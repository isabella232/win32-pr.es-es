---
description: Enumerar dispositivos de audio
ms.assetid: 20110ffc-5eff-4279-abea-53115803b6ee
title: Enumerar dispositivos de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707b9a88181c83344757c711af1c0199c19ebc16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080219"
---
# <a name="enumerating-audio-devices"></a>Enumerar dispositivos de audio

La primera tarea de una aplicación de audio de cliente es encontrar un dispositivo de audio adecuado para su uso. La [API de MMDevice](mmdevice-api.md) permite que los clientes detecten los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md) en el sistema y determinen qué dispositivos son adecuados para la aplicación. Esta API permite a los clientes recuperar recopilaciones de los dispositivos de punto de conexión disponibles y obtener las capacidades de cada dispositivo. El archivo de encabezado Mmdeviceapi. h define las interfaces de la API de MMDevice.

Un adaptador de audio puede contener varios dispositivos (por ejemplo, un dispositivo de representación de ondas y un dispositivo de captura de onda). Son dispositivos de adaptador en lugar de dispositivos de punto de conexión. Como se mencionó anteriormente, el administrador de Plug and Play registra los dispositivos de adaptador, a diferencia de los dispositivos de punto de conexión registrados por el administrador de puntos de conexión. Cada dispositivo adaptador normalmente admite uno o varios dispositivos de punto de conexión. Un dispositivo de extremo de representación (por ejemplo, auriculares) puede recibir un flujo de datos de audio de una aplicación cliente y un dispositivo de extremo de captura (por ejemplo, un micrófono) puede enviar una secuencia de audio a una aplicación cliente.

Antes de enumerar los dispositivos de extremo en el sistema, el cliente debe llamar primero a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) de Windows para crear un enumerador de dispositivos. Un enumerador de dispositivo es un objeto con una interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Para obtener información sobre **CoCreateInstance**, consulte la documentación de Windows SDK.

El cliente llama al método [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) para crear una colección de objetos de extremo. Cada objeto de extremo representa un dispositivo de punto de conexión de audio en el sistema. En esta llamada, el cliente especifica si la colección debe contener todos los dispositivos de representación del sistema, todos los dispositivos de captura o ambos.

Una colección de dispositivos es un objeto con una interfaz [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) . Cada elemento de una colección de dispositivos es un objeto de punto de conexión con al menos las dos interfaces siguientes:

-   Una interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) . Un cliente obtiene una referencia a la interfaz **IMMDevice** de un objeto de punto de conexión en una colección de dispositivos llamando al método [**IMMDeviceCollection:: Item**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item) .
-   Una interfaz [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint) . Un cliente obtiene una referencia a la interfaz **IMMEndpoint** de un objeto de punto de conexión llamando al método [**IMMDevice:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

Después de recuperar una colección de dispositivos de punto de conexión, el cliente puede consultar las propiedades de los dispositivos individuales de la colección para determinar su idoneidad para su uso. Para ver un ejemplo de código que muestra cómo enumerar los dispositivos de punto de conexión y consultar sus propiedades, consulte [propiedades de dispositivo](device-properties.md).

Después de seleccionar un dispositivo adecuado, el cliente puede llamar al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para activar las interfaces específicas del dispositivo en [WASAPI](wasapi.md), la [API de DeviceTopology](devicetopology-api.md)y la [API de EndpointVolume](endpointvolume-api.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> </dl>

 

 
