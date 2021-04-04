---
description: Interfaces de cliente
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: Interfaces de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7c85ec5cb9b35e30d68b1d784cdebf230fdaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911142"
---
# <a name="client-interfaces"></a>Interfaces de cliente

Las aplicaciones usan los métodos admitidos por las siguientes interfaces para realizar operaciones en dispositivos portátiles. Entre estas operaciones se incluye la apertura de una conexión a un dispositivo, la recuperación de datos de un dispositivo, la escritura de datos en un dispositivo, etc.



| Interfaz                                                                              | Descripción                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)                   | Enumera los objetos de un dispositivo portátil.                                                                                                                                                                                        |
| [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                                             | Proporciona acceso de bajo nivel a un dispositivo portátil.                                                                                                                                                                                     |
| [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                     | Recupera una variedad de funcionalidades del dispositivo, incluidos los formatos, comandos y objetos funcionales admitidos.                                                                                                                          |
| [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                               | Proporciona métodos para crear, enumerar y eliminar contenido en un dispositivo.                                                                                                                                                              |
| [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)                         | Expone métodos adicionales en una **IStream** utilizada para las transferencias de datos.                                                                                                                                                               |
| [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)                   | Implementado por la aplicación para recibir devoluciones de llamada asincrónicas.                                                                                                                                                                   |
| [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)                               | Enumera los dispositivos que están conectados al equipo y proporciona una manera sencilla de solicitar información de instalación para el dispositivo (incluido el fabricante, el nombre descriptivo y la descripción).                                       |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                         | Leer y escribir propiedades para un objeto en el dispositivo.                                                                                                                                                                              |
| [**IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)                 | Lee y escribe varias propiedades en varios objetos de un dispositivo, de forma asincrónica.                                                                                                                                               |
| [**IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback) | Implementado por la aplicación para realizar un seguimiento del progreso de una operación asincrónica que se inició mediante la interfaz **IPortableDevicePropertiesBulk** .                                                                          |
| [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)                           | Proporciona acceso a los datos de un objeto.                                                                                                                                                                                                |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | Solo Windows 7. Proporciona acceso de bajo nivel a un servicio de dispositivo portátil.                                                                                                                                                             |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | Solo Windows 7. Recupera una variedad de capacidades de servicio, incluidos los formatos, los comandos, los métodos y los perfiles de representación admitidos.                                                                                                |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | Solo Windows 7. Invoca métodos sincrónicamente y de forma asincrónica en un servicio.                                                                                                                                                      |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | Solo Windows 7. Implementado por la aplicación para realizar un seguimiento de la finalización de una operación de método de servicio asincrónica iniciada mediante una llamada a [ **IPortableDeviceServiceMethods:: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | Solo Windows 7. Enumera los servicios que admite un dispositivo y recupera el dispositivo asociado a un servicio.                                                                                                             |



 

En el diagrama siguiente se muestra cómo una aplicación obtiene la mayoría de las interfaces que necesita. No se muestran todos los métodos de todas las interfaces o las interfaces implementadas por la aplicación.

![diagrama que muestra la creación y la recuperación de las interfaces de cliente más necesarias](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



