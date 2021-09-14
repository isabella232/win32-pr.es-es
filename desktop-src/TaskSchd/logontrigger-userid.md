---
title: Propiedad LogonTrigger.UserId
description: Para el scripting, obtiene o establece el identificador del usuario.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- UserId, propiedad Programador de tareas
- Propiedad UserId Programador de tareas , objeto LogonTrigger
- Objeto LogonTrigger Programador de tareas , propiedad UserId
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073433"
---
# <a name="logontriggeruserid-property"></a>Propiedad LogonTrigger.UserId

Para el scripting, obtiene o establece el identificador del usuario.

## <a name="syntax"></a>Sintaxis


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a>Valor de propiedad

El identificador del usuario. Por ejemplo, "MyDomain \\ MyName" o para una cuenta local, "Administrador".

Esta propiedad puede tener uno de los formatos siguientes:

-   Nombre de usuario o SID: la tarea se inicia cuando el usuario inicia sesión en el equipo.
-   NULL: la tarea se inicia cuando cualquier usuario inicia sesión en el equipo.

## <a name="remarks"></a>Observaciones

Si desea que se desencadene una tarea cuando algún miembro de un grupo inicie sesión en el equipo en lugar de cuando un usuario específico inicie sesión, no asigne un valor a la propiedad **LogonTrigger.UserId.** En su lugar, cree un desencadenador de inicio de sesión con una propiedad **LogonTrigger.UserId** vacía y asigne un valor a la entidad de seguridad para la tarea mediante la [**propiedad Principal.GroupId.**](principal-groupid.md)

Al leer o escribir XML para una tarea, el identificador de usuario de inicio de sesión se especifica mediante el [**elemento UserId**](taskschedulerschema-userid-logontriggertype-element.md) del esquema Programador de tareas inicio de sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogonTrigger**](logontrigger.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





