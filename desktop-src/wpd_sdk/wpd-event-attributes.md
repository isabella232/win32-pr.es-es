---
description: Para Windows 7, Windows Portable Devices admite los siguientes atributos para los eventos de un servicio de dispositivo. El método IPortableDeviceServiceCapabilities::GetEventAttributes devuelve estos atributos.
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Atributos de evento (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247088"
---
# <a name="event-attributes-portabledeviceh"></a>Atributos de evento (PortableDevice.h)

Para Windows 7, Windows Portable Devices admite los siguientes atributos para los eventos de un servicio de dispositivo. El método [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) devuelve estos atributos.




| Atributo                             | VarType         | Descripción                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **NOMBRE DEL ATRIBUTO \_ DE \_ EVENTO \_ WPD**       | **VT \_ LPWSTR**  | Cadena que especifica el nombre descriptivo del script del evento. Los caracteres válidos son alfanuméricos \[ a-zA-Z0-9 \] y ' \_ '. |
| **OPCIONES DE ATRIBUTO \_ DE EVENTO \_ WPD \_**    | **VT \_ UNKNOWN** | [**IPortableDeviceValues que**](iportabledevicevalues.md) contiene las opciones de evento.                               |
| **PARÁMETROS DEL ATRIBUTO \_ DE EVENTO WPD \_ \_** | **VT \_ UNKNOWN** | [**IPortableDeviceKeyCollection que**](iportabledevicekeycollection.md) contiene los parámetros del evento.              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




