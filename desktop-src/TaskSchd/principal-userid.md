---
title: Propiedad principal. UserId
description: En el caso de scripting, obtiene o establece el identificador de usuario necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- Propiedad UserId Programador de tareas
- Propiedad UserId Programador de tareas, objeto principal
- Programador de tareas de objeto principal, propiedad UserId
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
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150511"
---
# <a name="principaluserid-property"></a>Propiedad principal. UserId

En el caso de scripting, obtiene o establece el identificador de usuario necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.

## <a name="syntax"></a>Sintaxis


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Valor de propiedad

Identificador de usuario necesario para ejecutar la tarea.

## <a name="remarks"></a>Observaciones

No establezca esta propiedad si se especifica un identificador de grupo en la propiedad [**GROUPID**](principal-groupid.md) .

Al leer o escribir XML para una tarea, el identificador de usuario de la entidad de seguridad se especifica mediante el elemento [**userid**](taskschedulerschema-userid-principaltype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**Principal**](principal.md)
</dt> <dt>

[**Entidad de seguridad. GroupId**](principal-groupid.md)
</dt> </dl>

 

 





