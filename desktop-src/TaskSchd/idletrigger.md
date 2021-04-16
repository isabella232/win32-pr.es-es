---
title: Objeto IdleTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando se produce una condición de inactividad.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- desencadenador inactivo Programador de tareas, objeto
- Objeto IdleTrigger Programador de tareas
- Programador de tareas de objeto IdleTrigger, descrito
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72288827fec34257bf4f54a152031ef37068790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686192"
---
# <a name="idletrigger-object"></a>Objeto IdleTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea cuando se produce una condición de inactividad. Para obtener información sobre las condiciones de inactividad, consulte [condiciones de inactividad de tareas](task-idle-conditions.md).

## <a name="members"></a>Miembros

El objeto **IdleTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **IdleTrigger** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                              |
| [EndBoundary](trigger-endboundary.md)<br/>                   | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.<br/>                                                 |
| [**Sesión**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece el identificador del desencadenador.<br/>                                                                                             |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                                            |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Solo lectura<br/>  | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene el tipo del desencadenador.<br/>                                                                                                            |



 

## <a name="remarks"></a>Observaciones

Un desencadenador inactivo solo desencadenará una acción de tarea si el equipo entra en un estado de inactividad después del límite de inicio del desencadenador.

Al leer o escribir XML para una tarea, se especifica un desencadenador inactivo mediante el elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) del esquema programador de tareas.

Si una tarea se desencadena mediante un desencadenador inactivo, se omite la propiedad [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) .

Si la instancia inicial de una tarea con un desencadenador idle todavía se está ejecutando, la tarea solo se inicia una vez sin repeticiones, aunque se hayan definido varias repeticiones en la propiedad [**repeticiones**](trigger-repetition.md) . Este comportamiento no se produce si la tarea se detiene por sí misma.

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
</dt> <dt>

[Objetos Programador de tareas](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





