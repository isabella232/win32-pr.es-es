---
title: Objeto LogonTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando un usuario inicia sesión.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- Programador de tareas de desencadenador de inicio de sesión, objeto
- Objeto LogonTrigger Programador de tareas
- Programador de tareas de objeto LogonTrigger, descrito
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996690"
---
# <a name="logontrigger-object"></a>Objeto LogonTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea cuando un usuario inicia sesión. Cuando se inicia el servicio Programador de tareas, se enumeran todos los usuarios que han iniciado sesión y se ejecutan las tareas registradas con desencadenadores Logon que coinciden con el usuario que ha iniciado sesión.

## <a name="members"></a>Miembros

El objeto **LogonTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **LogonTrigger** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay**](logontrigger-delay.md)<br/>                      | Lectura/escritura<br/> | Obtiene o establece un valor que indica la cantidad de tiempo entre el momento en el que el usuario inicia sesión y el momento en que se inicia el trabajo.<br/>                                                                              |
| [**habilitado**](trigger-enabled.md)<br/>                       | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.<br/>                                         |
| [**Sesión**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece el identificador del desencadenador.<br/>                                                                                             |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                                            |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Solo lectura<br/>  | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene el tipo del desencadenador.<br/>                                                                                                            |
| [**Deberían**](logontrigger-userid.md)<br/>                    | Lectura/escritura<br/> | Obtiene o establece el identificador del usuario.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Si desea que una tarea se desencadene cuando un miembro de un grupo inicia sesión en el equipo en lugar de cuando un usuario específico inicia sesión, no asigne un valor a la propiedad [**LogonTrigger. userid**](logontrigger-userid.md) . En su lugar, cree un desencadenador Logon con una propiedad **LogonTrigger. userid** vacía y asigne un valor a la entidad de seguridad para la tarea mediante la propiedad [**principal. GROUPID**](principal-groupid.md) .

Al leer o escribir XML para una tarea, se especifica un desencadenador Logon mediante el elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) del esquema programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de inicio de sesión (scripting)](logon-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Activado**](trigger.md)
</dt> </dl>

 

 





