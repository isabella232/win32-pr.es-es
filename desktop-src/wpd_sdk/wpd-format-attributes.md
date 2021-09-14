---
description: Para Windows 7, Windows Portable Devices admite los atributos siguientes para los formatos de un servicio de dispositivo. El método IPortableDeviceServiceCapabilities::GetFormatAttributes devuelve estos atributos.
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Atributos de formato (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247052"
---
# <a name="format-attributes"></a>Atributos de formato

Para Windows 7, Windows Portable Devices admite los atributos siguientes para los formatos de un servicio de dispositivo. El método [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) devuelve estos atributos.




| **Atributo**                        | **VarType**    | **Descripción**                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| **ATRIBUTO DE \_ FORMATO \_ \_ WPD MIMETYPE** | **VT \_ LPWSTR** | El tipo MIME de formato.                                                                                                     |
| **NOMBRE DE ATRIBUTO \_ DE \_ FORMATO \_ WPD**     | **VT \_ LPWSTR** | Cadena que especifica el nombre descriptivo del script del formato. Los caracteres válidos son alfanuméricos \[ a-zA-Z0-9 \] y \_ ''. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




