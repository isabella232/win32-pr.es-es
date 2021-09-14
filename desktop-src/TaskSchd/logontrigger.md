---
title: Objeto LogonTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando un usuario inicia sesión.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- desencadenador logon Programador de tareas , objeto
- Objeto LogonTrigger Programador de tareas
- Objeto LogonTrigger Programador de tareas , descrito
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9c4b2031b39a6dfd483b039023ad9114271b21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073429"
---
# <a name="logontrigger-object"></a>Objeto LogonTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea cuando un usuario inicia sesión. Cuando se Programador de tareas servicio, se enumeran todos los usuarios que han iniciado sesión y se ejecutan las tareas registradas con desencadenadores de inicio de sesión que coinciden con el usuario que ha iniciado sesión.

## <a name="members"></a>Members

El **objeto LogonTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto LogonTrigger** tiene estas propiedades.



| Propiedad.                                                            | Tipo de acceso           | Descripción                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay**](logontrigger-delay.md)<br/>                      | Lectura y escritura<br/> | Obtiene o establece un valor que indica la cantidad de tiempo entre el momento en que el usuario inicia sesión y el momento en que se inicia el trabajo.<br/>                                                                              |
| [**Enabled**](trigger-enabled.md)<br/>                       | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse.<br/>                                         |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece el identificador del desencadenador.<br/>                                                                                             |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                                            |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Solo lectura<br/>  | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene el tipo del desencadenador.<br/>                                                                                                            |
| [**Userid**](logontrigger-userid.md)<br/>                    | Lectura y escritura<br/> | Obtiene o establece el identificador del usuario.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Si desea que se desencadene una tarea cuando algún miembro de un grupo inicie sesión en el equipo en lugar de cuando un usuario específico inicie sesión, no asigne un valor a la propiedad [**LogonTrigger.UserId.**](logontrigger-userid.md) En su lugar, cree un desencadenador de inicio de sesión con una propiedad **LogonTrigger.UserId** vacía y asigne un valor a la entidad de seguridad para la tarea mediante la [**propiedad Principal.GroupId.**](principal-groupid.md)

Al leer o escribir XML para una tarea, se especifica un desencadenador de inicio de sesión mediante el elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) del Programador de tareas esquema.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea Ejemplo de desencadenador de inicio de [sesión (scripting).](logon-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Detonante**](trigger.md)
</dt> </dl>

 

 





