---
title: Objeto IdleTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando se produce una condición de inactividad.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- desencadenador inactivo Programador de tareas , objeto
- Objetos IdleTrigger Programador de tareas
- Objeto IdleTrigger Programador de tareas , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073437"
---
# <a name="idletrigger-object"></a>Objeto IdleTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea cuando se produce una condición de inactividad. Para obtener información sobre las condiciones de inactividad, vea [Task Idle Conditions](task-idle-conditions.md).

## <a name="members"></a>Members

El **objeto IdleTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto IdleTrigger** tiene estas propiedades.



| Propiedad.                                                            | Tipo de acceso           | Descripción                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                              |
| [EndBoundary](trigger-endboundary.md)<br/>                   | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la cantidad máxima de tiempo en la que el desencadenador puede iniciar la tarea.<br/>                                                 |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece el identificador del desencadenador.<br/>                                                                                             |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                                            |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Solo lectura<br/>  | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene el tipo del desencadenador.<br/>                                                                                                            |



 

## <a name="remarks"></a>Observaciones

Un desencadenador inactivo solo desencadenará una acción de tarea si el equipo entra en un estado de inactividad después del límite inicial del desencadenador.

Al leer o escribir XML para una tarea, se especifica un desencadenador inactivo mediante el elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) del Programador de tareas esquema.

Si un desencadenador inactivo desencadena una tarea, se omite la propiedad [**IdleSettings.WaitTimeout.**](idlesettings-waittimeout.md)

Si la instancia inicial de una tarea con un desencadenador inactivo todavía se está ejecutando, la tarea solo se inicia una vez sin repeticiones, aunque se definan varias repeticiones en la [**propiedad Repetición.**](trigger-repetition.md) Este comportamiento no se produce si la tarea se detiene por sí misma.

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
</dt> <dt>

[Programador de tareas objetos](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





