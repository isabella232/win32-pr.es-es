---
title: Objeto TimeTrigger (Windows.applicationmodel.background.h)
description: Objeto de scripting que representa un desencadenador que inicia una tarea en una fecha y hora específicas.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- desencadenador de tiempo Programador de tareas , objeto
- TimeTrigger object Programador de tareas
- Objeto TimeTrigger Programador de tareas , descrito
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f0fb6f5eaff5101f3cc1f5c4aeb2245335e4f65b27d2fafb364df2d05618ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771985"
---
# <a name="timetrigger-object"></a>Objeto TimeTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea en una fecha y hora específicas.

## <a name="members"></a>Miembros

El **objeto TimeTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto TimeTrigger** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Lectura/escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lectura/escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura/escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece la cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lectura/escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece el identificador del desencadenador.<br/>                                                                               |
| [**RandomDelay**](dailytrigger-randomdelay.md)<br/>          | Lectura/escritura<br/> | Obtiene o establece una hora de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.<br/>                                                                                    |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura/escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura/escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece la fecha y hora en que se activa el desencadenador. Este elemento es obligatorio.<br/>                                    |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Solo lectura<br/>  | Se hereda del [**desencadenador**](trigger.md). Obtiene el tipo del desencadenador.<br/>                                                                                              |



 

## <a name="remarks"></a>Comentarios

El [**elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores time y calendar [**(TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) [**y CalendarTrigger).**](taskschedulerschema-calendartrigger-triggergroup-element.md)

Al leer o escribir XML para una tarea, se especifica un desencadenador inactivo mediante el [**elemento TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) del Programador de tareas esquema.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea [Ejemplo de desencadenador de tiempo (scripting).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                             |
| Header<br/>                   | <dl> <dt>Windows.applicationmodel.background.h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl>                          |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**detonante**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





