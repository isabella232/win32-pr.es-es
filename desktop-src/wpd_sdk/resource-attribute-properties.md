---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de atributo de recurso.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Propiedades de los atributos de recursos (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718953"
---
# <a name="resource-attribute-properties"></a>Propiedades de atributo de recurso

Los dispositivos portátiles de Windows admiten las siguientes propiedades de atributo de recurso.



| Propiedad                                    | VarType         | Descripción                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_clave de \_ recurso de atributo de recurso WPD \_ \_** | **VT \_ desconocido** | Se trata de un [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contiene un valor único, que es la clave que identifica el recurso.                     |
| **\_formato de \_ atributo de recurso de WPD \_**        | **VT \_ CLSID**   | Valor GUID que especifica el formato del recurso. Vea [formatos de objeto](object-format-guids.md) para obtener una lista de formatos definidos por dispositivos portátiles de Windows. |
| **\_ \_ Tamaño total del atributo de recursos de \_ WPD \_**   | **VT \_ UI8**     | Tamaño total de los datos de recursos, en bytes.                                                                                                                            |



 

## <a name="remarks"></a>Observaciones

Estos atributos son devueltos por el método [**IPortableDeviceResources:: GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




