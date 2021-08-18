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
ms.openlocfilehash: ac41b4e9c7273c953a9689ce8c3d9f44d32925aded5b36291c45895b872fa9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026342"
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




