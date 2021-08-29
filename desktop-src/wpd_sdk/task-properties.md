---
description: Windows Dispositivos portátiles admite las siguientes propiedades de tarea.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Propiedades de la tarea (PortableDevice.h)
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
ms.openlocfilehash: 06c45e348ce4e5100cdf5fc353c10d901bc9e98d454468ecf92f0c99d166415e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445495"
---
# <a name="task-properties"></a>Propiedades de la tarea

Windows Dispositivos portátiles admite las siguientes propiedades de tarea.



| Propiedad                         | VarType        | Descripción                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| **PROPIETARIO DE LA \_ TAREA \_ WPD**             | **VT \_ LPWSTR** | Propietario de la tarea.                                                                      |
| **PORCENTAJE DE TAREAS DE WPD \_ \_ \_ COMPLETADAS** | **VT \_ UI4**    | Número entre 0 y 100 que especifica lo completa que es la tarea.                         |
| **FECHA DEL RECORDATORIO \_ DE \_ LA TAREA \_ WPD**    | **VT \_ DATE**   | Valor que especifica cuándo se debe enviar un recordatorio para realizar la tarea, si no se completa. |
| **ESTADO DE LA \_ TAREA \_ WPD**            | **VT \_ LPWSTR** | Una descripción de cadena del estado de la tarea, por ejemplo, "En curso".                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




