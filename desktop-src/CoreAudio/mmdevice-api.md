---
description: Acerca de MMDevice API
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Acerca de MMDevice API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164950"
---
# <a name="about-mmdevice-api"></a>Acerca de MMDevice API

La API Windows Multimedia Device (MMDevice) permite a los clientes de audio detectar dispositivos de punto de conexión de [audio,](audio-endpoint-devices.md)determinar sus funcionalidades y crear instancias de controlador para esos dispositivos.

El archivo de encabezado Mmdeviceapi.h define las interfaces de la API MMDevice.

MMDevice API consta de varias interfaces. El primero de ellos es la [**interfaz IMMDeviceEnumerator.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) Para acceder a las interfaces de MMDevice API, un cliente obtiene una referencia a la interfaz **IMMDeviceEnumerator** de un objeto de enumerador de dispositivos mediante una llamada a la función [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) como se muestra en el fragmento de código siguiente:


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



En el fragmento de código anterior, CLSID MMDeviceEnumerator e IID IMMDeviceEnumerator son los valores GUID que se adjuntan como atributos al objeto de clase MMDeviceEnumerator y a la interfaz \_ \_ [**IMMDeviceEnumerator.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)  La [**llamada a CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pasa estos valores por referencia. La `hr` variable es de tipo **HRESULT** y la variable es un puntero a la interfaz `pEnumerator` **IMMDeviceEnumerator** de un objeto de enumerador de dispositivos. **IMMDeviceEnumerator proporciona métodos** para enumerar los dispositivos de punto de conexión de audio. Para obtener información sobre el operador **\_ \_ uuidof,** la función **CoCreateInstance** y las constantes XXX de CLSCTX, consulte la \_  documentación Windows SDK.

A través [**de la interfaz IMMDeviceEnumerator,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) el cliente puede obtener referencias a las otras interfaces de la API MMDevice. MMDevice API implementa las interfaces siguientes.



| Interfaz                                          | Descripción                                     |
|----------------------------------------------------|-------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | Representa un dispositivo de audio.                     |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | Representa una colección de dispositivos de audio.       |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | Proporciona métodos para enumerar dispositivos de audio. |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | Representa un dispositivo de punto de conexión de audio.            |



 

Además, los clientes de la API MMDevice que requieren la notificación de los cambios de estado en los dispositivos de punto de conexión de audio deben implementar la siguiente interfaz.



| Interfaz                                              | Descripción                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Proporciona notificaciones cuando se agrega o quita un dispositivo de punto de conexión de audio, cuando cambia el estado o las propiedades de un dispositivo, o cuando hay un cambio en el rol predeterminado asignado a un dispositivo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 
