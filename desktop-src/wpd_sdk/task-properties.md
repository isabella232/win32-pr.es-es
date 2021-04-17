---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de tarea.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Propiedades de la tarea (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708670"
---
# <a name="task-properties"></a>Propiedades de la tarea

Los dispositivos portátiles de Windows admiten las siguientes propiedades de tarea.



| Propiedad                         | VarType        | Descripción                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| **propietario de la tarea de WPD \_ \_**             | **VT \_ LPWStr** | Propietario de la tarea.                                                                      |
| **\_ \_ porcentaje \_ completado de la tarea de WPD** | **VT \_ UI4**    | Un número entre 0 y 100 que especifica cómo se completa la tarea.                         |
| **\_fecha de \_ recordatorio de tarea de WPD \_**    | **fecha de VT \_**   | Valor que especifica cuándo se debe enviar un recordatorio para realizar la tarea, si no se ha completado. |
| **Estado de la tarea de WPD \_ \_**            | **VT \_ LPWStr** | Una descripción de cadena del estado de la tarea, por ejemplo, "en curso".                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




