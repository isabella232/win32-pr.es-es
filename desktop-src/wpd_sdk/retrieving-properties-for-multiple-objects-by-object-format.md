---
description: Recuperar propiedades de varios objetos por formato de objeto
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Recuperar propiedades de varios objetos por formato de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497848"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a>Recuperar propiedades de varios objetos por formato de objeto

Además de una recuperación masiva de las propiedades de una colección de identificadores de objeto, una aplicación también puede realizar una recuperación masiva de propiedades para todos los objetos de un tipo determinado. Como en el ejemplo anterior, la recuperación masiva para un tipo determinado requiere que el controlador de dispositivo admita recuperaciones masivas.

La aplicación puede realizar una recuperación masiva con las interfaces descritas en la tabla siguiente.



| Interfaz                                                                                      | Descripción                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Proporciona acceso a los métodos específicos del contenido.                   |
| [**Interfaz IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Se utiliza para identificar las propiedades que se van a recuperar.                   |
| [**Interfaz IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Se utiliza para determinar si un controlador determinado admite operaciones masivas. |
| [**Interfaz IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Admite la operación de recuperación masiva.                             |
| [**Interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Se utiliza para almacenar los identificadores de objeto para la operación masiva.       |



 

La función ReadContentPropertiesBulkFilteringFormat del módulo ContentProperties. cpp de la aplicación de ejemplo muestra una operación de recuperación masiva para objetos de un tipo o formato determinado.

El código que se encuentra en la función ReadContentPropertiesBulkFilteringFormat es casi idéntico al código que se encuentra en la función ReadContentPropertiesBulk. (Vea el tema [recuperar propiedades de varios objetos](retrieving-properties-for-multiple-objects.md) para obtener una descripción completa de esta función).

La diferencia principal se produce cuando la operación se pone en cola. Al filtrar por tipo o formato, se llama al método [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) en lugar del método [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) .


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interfaz IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Interfaz IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Interfaz IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



