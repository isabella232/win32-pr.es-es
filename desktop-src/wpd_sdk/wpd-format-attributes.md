---
description: 'En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los formatos de un servicio de dispositivo. Estos atributos son devueltos por el método IPortableDeviceServiceCapabilities:: GetFormatAttributes.'
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Atributos de formato (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671010"
---
# <a name="format-attributes"></a>Atributos de formato

En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los formatos de un servicio de dispositivo. Estos atributos son devueltos por el método [**IPortableDeviceServiceCapabilities:: GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) .




| **Atributo**                        | **VarType**    | **Descripción**                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| **\_atributo de formato WPD \_ \_ Mimetype** | **VT \_ LPWStr** | El tipo MIME de formato.                                                                                                     |
| **\_nombre del \_ atributo de formato WPD \_**     | **VT \_ LPWStr** | Cadena que especifica el nombre descriptivo del script del formato. Los caracteres válidos son alfanuméricos a \[ -Za-z0-9 \] y ' \_ '. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




