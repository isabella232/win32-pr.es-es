---
description: Recuperar propiedades para varios objetos por formato de objeto
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Recuperar propiedades para varios objetos por formato de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574273"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a>Recuperar propiedades para varios objetos por formato de objeto

Además de una recuperación masiva de propiedades para una colección de identificadores de objeto, una aplicación también puede realizar una recuperación masiva de propiedades para todos los objetos de un tipo determinado. Como en el ejemplo anterior, la recuperación masiva para un tipo determinado requiere que el controlador de dispositivo admita recuperaciones masivas.

La aplicación puede realizar una recuperación masiva mediante las interfaces descritas en la tabla siguiente.



| Interfaz                                                                                      | Descripción                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**IPortableDeviceContent (interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Proporciona acceso a los métodos específicos del contenido.                   |
| [**IPortableDeviceKeyCollection (interfaz)**](iportabledevicekeycollection.md)                 | Se usa para identificar las propiedades que se recuperarán.                   |
| [**IPortableDeviceProperties (interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Se usa para determinar si un controlador determinado admite operaciones masivas. |
| [**IPortableDevicePropertiesBulk (interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Admite la operación de recuperación masiva.                             |
| [**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md) | Se usa para almacenar los identificadores de objeto para la operación masiva.       |



 

La función ReadContentPropertiesBulkFilteringFormat del módulo ContentProperties.cpp de la aplicación de ejemplo muestra una operación de recuperación masiva para objetos de un tipo o formato determinados.

El código que se encuentra en la función ReadContentPropertiesBulkFilteringFormat es casi idéntico al código que se encuentra en la función ReadContentPropertiesBulk. (Vea el [tema Recuperación de propiedades para varios objetos](retrieving-properties-for-multiple-objects.md) para obtener una descripción completa de esta función).

La única diferencia principal se produce cuando la operación está en cola. Al filtrar por tipo o formato, se llama al método [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) en lugar del método [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectList.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist)


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

[**IPortableDevice (interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent (interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceKeyCollection (interfaz)**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceProperties (interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**IPortableDevicePropertiesBulk (interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



