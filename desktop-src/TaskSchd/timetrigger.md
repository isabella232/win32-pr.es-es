---
title: Objeto TimeTrigger (Windows.applicationmodel.background.h)
description: Objeto de scripting que representa un desencadenador que inicia una tarea en una fecha y hora específicas.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- time trigger Programador de tareas , object
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
ms.openlocfilehash: 1a8403b93e1c5292ade9f6f402b7e41994339140
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264919"
---
# <a name="timetrigger-object"></a>Objeto TimeTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea en una fecha y hora específicas.

## <a name="members"></a>Members

El **objeto TimeTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto TimeTrigger** tiene estas propiedades.



| Propiedad.                                                            | Tipo de acceso           | Descripción                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Lectura y escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lectura y escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura y escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece la cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lectura y escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece el identificador del desencadenador.<br/>                                                                               |
| [**RandomDelay**](dailytrigger-randomdelay.md)<br/>          | Lectura y escritura<br/> | Obtiene o establece una hora de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.<br/>                                                                                    |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura y escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura y escritura<br/> | Se hereda del [**desencadenador**](trigger.md). Obtiene o establece la fecha y hora en que se activa el desencadenador. Este elemento es obligatorio.<br/>                                    |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Solo lectura<br/>  | Se hereda del [**desencadenador**](trigger.md). Obtiene el tipo del desencadenador.<br/>                                                                                              |



 

## <a name="remarks"></a>Observaciones

El [**elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores time y calendar [**(TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) [**y CalendarTrigger).**](taskschedulerschema-calendartrigger-triggergroup-element.md)

Al leer o escribir XML para una tarea, se especifica un desencadenador inactivo mediante el [**elemento TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) del Programador de tareas esquema.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea [Ejemplo de desencadenador de tiempo (scripting).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                             |
| Encabezado<br/>                   | <dl> <dt>Windows.applicationmodel.background.h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl>                          |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Detonante**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





