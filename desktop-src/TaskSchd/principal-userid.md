---
title: Propiedad Principal.UserId
description: Para el scripting, obtiene o establece el identificador de usuario necesario para ejecutar las tareas asociadas a la entidad de seguridad.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- Propiedad UserId Programador de tareas
- Propiedad UserId Programador de tareas , objeto Principal
- Objeto principal Programador de tareas , propiedad UserId
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9501184f3316e464aa26f42d51e0b4c27eccaeb72d447faa91edaa33b0b4774c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060033"
---
# <a name="principaluserid-property"></a>Propiedad Principal.UserId

Para el scripting, obtiene o establece el identificador de usuario necesario para ejecutar las tareas asociadas a la entidad de seguridad.

## <a name="syntax"></a>Syntax


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Valor de propiedad

Identificador de usuario necesario para ejecutar la tarea.

## <a name="remarks"></a>Comentarios

No establezca esta propiedad si se especifica un identificador de grupo en la [**propiedad GroupId.**](principal-groupid.md)

Al leer o escribir XML para una tarea, el identificador de usuario de la entidad de seguridad se especifica mediante el [**elemento UserId**](taskschedulerschema-userid-principaltype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**Principal**](principal.md)
</dt> <dt>

[**Principal.GroupId**](principal-groupid.md)
</dt> </dl>

 

 





