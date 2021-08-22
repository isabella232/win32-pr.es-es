---
description: Interfaces de cliente
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: Interfaces de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b44db8fdd42b20fb2ff7a3224bccf5214147069baa9187facdb1c832c375a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590404"
---
# <a name="client-interfaces"></a>Interfaces de cliente

Las aplicaciones usan los métodos admitidos por las interfaces siguientes para realizar operaciones en dispositivos portátiles. Estas operaciones incluyen la apertura de una conexión a un dispositivo, la recuperación de datos de un dispositivo, la escritura de datos en un dispositivo, y así sucesivamente.



| Interfaz                                                                              | Descripción                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)                   | Enumera los objetos de un dispositivo portátil.                                                                                                                                                                                        |
| [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                                             | Proporciona acceso de bajo nivel a un dispositivo portátil.                                                                                                                                                                                     |
| [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                     | Recupera una variedad de funcionalidades de dispositivo, incluidos los formatos admitidos, los comandos y los objetos funcionales.                                                                                                                          |
| [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                               | Proporciona métodos para crear, enumerar y eliminar contenido en un dispositivo.                                                                                                                                                              |
| [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)                         | Expone métodos adicionales en un **IStream usado** para las transferencias de datos.                                                                                                                                                               |
| [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)                   | Implementado por la aplicación para recibir devoluciones de llamada asincrónicas.                                                                                                                                                                   |
| [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)                               | Enumera los dispositivos conectados al equipo y proporciona una manera sencilla de solicitar información de instalación para el dispositivo (incluido el fabricante, el nombre descriptivo y la descripción).                                       |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                         | Lee y escribe las propiedades de un objeto en el dispositivo.                                                                                                                                                                              |
| [**IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)                 | Lee y escribe varias propiedades en varios objetos de un dispositivo de forma asincrónica.                                                                                                                                               |
| [**IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback) | Implementado por la aplicación para realizar un seguimiento del progreso de una operación asincrónica que se inició mediante la **interfaz IPortableDevicePropertiesBulk.**                                                                          |
| [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)                           | Proporciona acceso a los datos de un objeto.                                                                                                                                                                                                |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | Windows 7 solo. Proporciona acceso de bajo nivel a un servicio de dispositivo portátil.                                                                                                                                                             |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | Windows 7 solo. Recupera una variedad de funcionalidades de servicio, incluidos los formatos, comandos, métodos y perfiles de representación admitidos.                                                                                                |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | Windows 7 solo. Invoca métodos de forma sincrónica y asincrónica en un servicio.                                                                                                                                                      |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | Windows 7 solo. Implementado por la aplicación para realizar un seguimiento de la finalización de una operación de método de servicio asincrónica iniciada mediante una llamada a [ **IPortableDeviceServiceMethods::InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | Windows 7 solo. Enumera los servicios admitidos por un dispositivo y recupera el dispositivo asociado a un servicio.                                                                                                             |



 

En el diagrama siguiente se muestra cómo una aplicación obtiene la mayoría de las interfaces que necesita. No se muestran todos los métodos de todas las interfaces o interfaces implementadas por la aplicación.

![diagrama que muestra la creación y recuperación de la mayoría de las interfaces de cliente necesarias](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



