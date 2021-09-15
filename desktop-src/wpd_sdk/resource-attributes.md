---
description: Windows Dispositivos portátiles admite los siguientes atributos de recursos.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Atributos de recursos (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571176"
---
# <a name="resource-attributes"></a>Atributos de recursos

Windows Dispositivos portátiles admite los siguientes atributos de recursos. Estos atributos los devuelven los métodos siguientes:

-   [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| Atributo                                                  | VarType      | Descripción                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **EL ATRIBUTO \_ DE RECURSO WPD \_ PUEDE \_ \_ ELIMINAR**                  | **VT \_ BOOL** | Valor booleano que especifica si un cliente tiene permiso para eliminar el recurso. Si no está presente, se supone que es false.                |
| **EL ATRIBUTO \_ DE RECURSO WPD \_ PUEDE \_ \_ LEER**                    | **VT \_ BOOL** | Valor booleano que especifica si un cliente tiene permiso para abrir el recurso para el acceso de lectura. Si está ausente, se supone que es False.  |
| **EL ATRIBUTO \_ DE RECURSO WPD \_ PUEDE \_ \_ ESCRIBIR**                   | **VT \_ BOOL** | Valor booleano que especifica si un cliente tiene permiso para abrir el recurso para el acceso de escritura. Si no está presente, se supone que es false. |
| **TAMAÑO ÓPTIMO DEL BÚFER DE LECTURA \_ DEL ATRIBUTO DE RECURSO \_ \_ \_ \_ \_ WPD**  | **VT \_ UI4**  | El tamaño de búfer recomendado que un autor de la llamada debe usar para las lecturas en búfer del recurso.                                                  |
| **TAMAÑO ÓPTIMO DEL BÚFER DE ESCRITURA \_ DEL ATRIBUTO DE RECURSO \_ \_ \_ \_ \_ WPD** | **VT \_ UI4**  | El tamaño de búfer recomendado que un autor de la llamada debe usar para las escrituras en búfer en el recurso.                                                   |
| **TAMAÑO TOTAL DEL \_ ATRIBUTO \_ DE RECURSO \_ \_ WPD**                  | **VT \_ UI8**  | Tamaño total de los datos del recurso, en bytes.                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades**](properties-and-attributes.md)
</dt> </dl>

 

 




