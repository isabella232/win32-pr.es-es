---
description: 'En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los eventos de un servicio de dispositivo. Estos atributos son devueltos por el método IPortableDeviceServiceCapabilities:: GetEventAttributes.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Atributos de evento (PortableDevice. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698524"
---
# <a name="event-attributes-portabledeviceh"></a>Atributos de evento (PortableDevice. h)

En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los eventos de un servicio de dispositivo. Estos atributos son devueltos por el método [**IPortableDeviceServiceCapabilities:: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .




| Atributo                             | VarType         | Descripción                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **\_nombre del \_ atributo de evento WPD \_**       | **VT \_ LPWStr**  | Cadena que especifica el nombre descriptivo del script del evento. Los caracteres válidos son alfanuméricos a \[ -Za-z0-9 \] y ' \_ '. |
| **\_Opciones del \_ atributo de evento WPD \_**    | **VT \_ desconocido** | [**IPortableDeviceValues**](iportabledevicevalues.md) que contiene las opciones de evento.                               |
| **\_parámetros del \_ atributo de evento WPD \_** | **VT \_ desconocido** | [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contiene los parámetros de evento.              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




