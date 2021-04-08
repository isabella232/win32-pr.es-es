---
description: Acerca de la API de MMDevice
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Acerca de la API de MMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807735"
---
# <a name="about-mmdevice-api"></a>Acerca de la API de MMDevice

La API de dispositivo multimedia de Windows (MMDevice) permite a los clientes de audio detectar [dispositivos de punto de conexión de audio](audio-endpoint-devices.md), determinar sus capacidades y crear instancias de controlador para esos dispositivos.

El archivo de encabezado Mmdeviceapi. h define las interfaces de la API de MMDevice.

La API de MMDevice consta de varias interfaces. La primera de ellas es la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Para acceder a las interfaces de la API de MMDevice, un cliente obtiene una referencia a la interfaz **IMMDeviceEnumerator** de un objeto de enumerador de dispositivo mediante una llamada a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , tal como se muestra en el siguiente fragmento de código:


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



En el fragmento de código anterior, CLSID \_ MMDeviceEnumerator y IID \_ IMMDeviceEnumerator son los valores GUID que se adjuntan como atributos al objeto de la clase **MMDeviceEnumerator** y a la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . La llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pasa estos valores por referencia. `hr`La variable es de tipo **HRESULT** y `pEnumerator` la variable es un puntero a la interfaz **IMMDeviceEnumerator** de un objeto de enumerador de dispositivo. **IMMDeviceEnumerator** proporciona métodos para enumerar los dispositivos de punto de conexión de audio. Para obtener información sobre el operador **\_ \_ uuidof** , la función **CoCreateInstance** y las constantes \_ *XXX* de CLSCTX, consulte la documentación de Windows SDK.

A través de la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) , el cliente puede obtener referencias a las otras interfaces de la API de MMDevice. La API de MMDevice implementa las interfaces siguientes.



| Interfaz                                          | Descripción                                     |
|----------------------------------------------------|-------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | Representa un dispositivo de audio.                     |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | Representa una colección de dispositivos de audio.       |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | Proporciona métodos para enumerar los dispositivos de audio. |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | Representa un dispositivo de punto de conexión de audio.            |



 

Además, los clientes de la API de MMDevice que requieran notificación de cambios de estado en los dispositivos de punto de conexión de audio deben implementar la siguiente interfaz.



| Interfaz                                              | Descripción                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Proporciona notificaciones cuando se agrega o se quita un dispositivo de punto de conexión de audio, cuando cambia el estado o las propiedades de un dispositivo, o cuando se produce un cambio en el rol predeterminado que se asigna a un dispositivo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 
