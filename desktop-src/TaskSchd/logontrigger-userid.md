---
title: LogonTrigger. UserId (propiedad)
description: En el caso de scripting, obtiene o establece el identificador del usuario.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- Propiedad UserId Programador de tareas
- Propiedad UserId Programador de tareas, objeto LogonTrigger
- Programador de tareas de objeto LogonTrigger, propiedad UserId
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422037"
---
# <a name="logontriggeruserid-property"></a>LogonTrigger. UserId (propiedad)

En el caso de scripting, obtiene o establece el identificador del usuario.

## <a name="syntax"></a>Sintaxis


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a>Valor de propiedad

El identificador del usuario. Por ejemplo, "midominio \\ nombre" o para una cuenta local, "administrador".

Esta propiedad puede estar en uno de los siguientes formatos:

-   Nombre de usuario o SID: la tarea se inicia cuando el usuario inicia sesión en el equipo.
-   NULL: la tarea se inicia cuando cualquier usuario inicia sesión en el equipo.

## <a name="remarks"></a>Observaciones

Si desea que una tarea se desencadene cuando un miembro de un grupo inicia sesión en el equipo en lugar de cuando un usuario específico inicia sesión, no asigne un valor a la propiedad **LogonTrigger. userid** . En su lugar, cree un desencadenador Logon con una propiedad **LogonTrigger. userid** vacía y asigne un valor a la entidad de seguridad para la tarea mediante la propiedad [**principal. GROUPID**](principal-groupid.md) .

Al leer o escribir XML para una tarea, el identificador de usuario de inicio de sesión se especifica mediante el elemento [**userid**](taskschedulerschema-userid-logontriggertype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogonTrigger**](logontrigger.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





