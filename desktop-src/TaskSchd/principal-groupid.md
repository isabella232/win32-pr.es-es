---
title: Principal.GroupId, propiedad
description: Para el scripting, obtiene o establece el identificador del grupo de usuarios necesario para ejecutar las tareas asociadas a la entidad de seguridad.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- Propiedad GroupId Programador de tareas
- Propiedad GroupId Programador de tareas , objeto Principal
- Objeto principal Programador de tareas , propiedad GroupId
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173037"
---
# <a name="principalgroupid-property"></a>Principal.GroupId, propiedad

Para el scripting, obtiene o establece el identificador del grupo de usuarios necesario para ejecutar las tareas asociadas a la entidad de seguridad.

## <a name="syntax"></a>Sintaxis


```VB
Principal.GroupId As String
```



## <a name="property-value"></a>Valor de propiedad

Identificador del grupo de usuarios asociado a esta entidad de seguridad.

## <a name="remarks"></a>Observaciones

No establezca esta propiedad si se especifica un identificador de usuario en la [**propiedad UserId.**](principal-userid.md)

Al leer o escribir XML para una tarea, el identificador de grupo de una entidad de seguridad se especifica en el [**elemento GroupId**](taskschedulerschema-groupid-principaltype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**UserId**](principal-userid.md)
</dt> <dt>

[**Principal**](principal.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





