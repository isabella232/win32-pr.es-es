---
title: Propiedad principal. GroupId
description: En el caso de scripting, obtiene o establece el identificador del grupo de usuarios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- Propiedad GroupId Programador de tareas
- Propiedad GroupId Programador de tareas, objeto principal
- Programador de tareas de objeto principal, propiedad GroupId
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686085"
---
# <a name="principalgroupid-property"></a>Propiedad principal. GroupId

En el caso de scripting, obtiene o establece el identificador del grupo de usuarios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.

## <a name="syntax"></a>Sintaxis


```VB
Principal.GroupId As String
```



## <a name="property-value"></a>Valor de propiedad

Identificador del grupo de usuarios que está asociado a esta entidad de seguridad.

## <a name="remarks"></a>Observaciones

No establezca esta propiedad si se especifica un identificador de usuario en la propiedad [**userid**](principal-userid.md) .

Al leer o escribir XML para una tarea, el identificador de grupo de una entidad de seguridad se especifica en el elemento [**GROUPID**](taskschedulerschema-groupid-principaltype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Deberían**](principal-userid.md)
</dt> <dt>

[**Principal**](principal.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





