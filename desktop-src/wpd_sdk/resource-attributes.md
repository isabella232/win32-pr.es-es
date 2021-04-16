---
description: Los dispositivos portátiles de Windows admiten los siguientes atributos de recursos.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Atributos de recursos (PortableDevice. h)
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
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718952"
---
# <a name="resource-attributes"></a>Atributos de recursos

Los dispositivos portátiles de Windows admiten los siguientes atributos de recursos. Estos atributos se devuelven mediante los métodos siguientes:

-   [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| Atributo                                                  | VarType      | Descripción                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **el \_ atributo de recurso de WPD \_ \_ puede \_ eliminar**                  | **VT \_ bool** | Valor booleano que especifica si un cliente tiene permiso para eliminar el recurso. Si no está presente, se supone que es false.                |
| **el \_ atributo del recurso WPD \_ \_ puede \_ leer**                    | **VT \_ bool** | Valor booleano que especifica si un cliente tiene permiso para abrir el recurso para el acceso de lectura. Si no está presente, se supone que es false.  |
| **el \_ atributo del recurso WPD \_ \_ puede \_ escribir**                   | **VT \_ bool** | Valor booleano que especifica si un cliente tiene permiso para abrir el recurso para el acceso de escritura. Si no está presente, se supone que es false. |
| **\_tamaño de \_ \_ búfer de \_ lectura óptimo del \_ atributo \_ de recurso de WPD**  | **VT \_ UI4**  | Tamaño de búfer recomendado que un llamador debe utilizar para las lecturas almacenadas en búfer del recurso.                                                  |
| **\_tamaño de \_ \_ búfer de \_ escritura óptimo del \_ atributo \_ de recurso de WPD** | **VT \_ UI4**  | Tamaño de búfer recomendado que un llamador debe utilizar para las escrituras almacenadas en búfer en el recurso.                                                   |
| **\_ \_ Tamaño total del atributo de recursos de \_ WPD \_**                  | **VT \_ UI8**  | Tamaño total de los datos de recursos, en bytes.                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades**](properties-and-attributes.md)
</dt> </dl>

 

 




