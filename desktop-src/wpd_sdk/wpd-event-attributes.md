---
description: Para Windows 7, Windows Portable Devices admite los atributos siguientes para los eventos de un servicio de dispositivo. El método IPortableDeviceServiceCapabilities::GetEventAttributes devuelve estos atributos.
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
ms.openlocfilehash: 9ee6fe335d5e3906a923dfe5c470142cdf36fb1e521c3498963e478369a9b251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193296"
---
# <a name="event-attributes-portabledeviceh"></a>Atributos de evento (PortableDevice.h)

Para Windows 7, Windows Portable Devices admite los atributos siguientes para los eventos de un servicio de dispositivo. El método [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) devuelve estos atributos.




| Atributo                             | VarType         | Descripción                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **NOMBRE DEL ATRIBUTO \_ DE \_ EVENTO \_ WPD**       | **VT \_ LPWSTR**  | Cadena que especifica el nombre descriptivo del script del evento. Los caracteres válidos son alfanuméricos \[ a-zA-Z0-9 \] y \_ ''. |
| **OPCIONES DE ATRIBUTO \_ DE \_ EVENTO \_ WPD**    | **VT \_ UNKNOWN** | [**IPortableDeviceValues que**](iportabledevicevalues.md) contiene las opciones de evento.                               |
| **PARÁMETROS DE ATRIBUTO \_ DE \_ EVENTO WPD \_** | **VT \_ UNKNOWN** | [**IPortableDeviceKeyCollection que**](iportabledevicekeycollection.md) contiene los parámetros del evento.              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




