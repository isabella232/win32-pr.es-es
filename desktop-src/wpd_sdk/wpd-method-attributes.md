---
description: 'En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los métodos de un servicio de dispositivo. Estos atributos son devueltos por el método IPortableDeviceServiceCapabilities:: GetMethodAttributes.'
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Atributos de método (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699552"
---
# <a name="method-attributes"></a>Atributos de método

En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los métodos de un servicio de dispositivo. Estos atributos son devueltos por el método [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) .




| Atributo                                      | VarType         | Descripción                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ acceso a atributos del método WPD \_**             | **VT \_ CLSID**   | Acceso al método necesario.                                                                                               |
| **\_ \_ formato asociado al atributo de método WPD \_ \_** | **VT \_ CLSID**   | Formato asociado al método o **GUID \_ null** si no hay ningún formato asociado.                                |
| **\_nombre del \_ atributo del método WPD \_**               | **VT \_ LPWStr**  | Cadena que especifica el nombre descriptivo del script del método. Los caracteres válidos son alfanuméricos a \[ -Za-z0-9 \] y ' \_ '. |
| **\_parámetros de \_ atributo del método WPD \_**         | **VT \_ desconocido** | Una interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contiene los parámetros del método.    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




