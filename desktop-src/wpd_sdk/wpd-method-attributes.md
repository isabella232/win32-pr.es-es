---
description: Para Windows 7, Windows Portable Devices admite los atributos siguientes para los métodos de un servicio de dispositivo. El método IPortableDeviceServiceCapabilities::GetMethodAttributes devuelve estos atributos.
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Atributos de método (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256065"
---
# <a name="method-attributes"></a>Atributos de método

Para Windows 7, Windows Portable Devices admite los atributos siguientes para los métodos de un servicio de dispositivo. El método [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) devuelve estos atributos.




| Atributo                                      | VarType         | Descripción                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| **ACCESO A ATRIBUTOS \_ DEL MÉTODO \_ \_ WPD**             | **VT \_ CLSID**   | Acceso al método necesario.                                                                                               |
| **FORMATO ASOCIADO DE \_ ATRIBUTO \_ DE MÉTODO \_ \_ WPD** | **VT \_ CLSID**   | Formato asociado al método o **GUID \_ NULL** si no hay ningún formato asociado.                                |
| **NOMBRE DE ATRIBUTO \_ DEL MÉTODO \_ \_ WPD**               | **VT \_ LPWSTR**  | Cadena que especifica el nombre descriptivo del script del método. Los caracteres válidos son alfanuméricos \[ a-zA-Z0-9 \] y \_ ''. |
| **PARÁMETROS DE ATRIBUTO \_ DEL MÉTODO WPD \_ \_**         | **VT \_ UNKNOWN** | Interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contiene los parámetros del método.    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




