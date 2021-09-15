---
description: Windows Dispositivos portátiles admite las siguientes propiedades de atributo de recurso.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Propiedades del atributo de recurso (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572085"
---
# <a name="resource-attribute-properties"></a>Propiedades del atributo de recurso

Windows Dispositivos portátiles admite las siguientes propiedades de atributo de recurso.



| Propiedad                                    | VarType         | Descripción                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLAVE DE RECURSO \_ DEL ATRIBUTO DE RECURSO \_ \_ \_ WPD** | **VT \_ UNKNOWN** | Se trata de [**un objeto IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contiene un único valor, que es la clave que identifica el recurso.                     |
| **FORMATO DE ATRIBUTO \_ DE \_ RECURSO \_ WPD**        | **VT \_ CLSID**   | Valor GUID que especifica el formato del recurso. Vea [Formatos de](object-format-guids.md) objeto para obtener una lista de los formatos definidos por Windows portables. |
| **TAMAÑO TOTAL DEL \_ ATRIBUTO \_ DE RECURSO \_ WPD \_**   | **VT \_ UI8**     | Tamaño total de los datos del recurso, en bytes.                                                                                                                            |



 

## <a name="remarks"></a>Observaciones

El método [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) devuelve estos atributos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




