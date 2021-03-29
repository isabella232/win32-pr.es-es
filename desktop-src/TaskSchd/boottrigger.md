---
title: Objeto BootTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando se inicia el sistema.
ms.assetid: 9d5a7cf6-2e1d-44ae-bb45-66424770d61b
keywords:
- Programador de tareas de desencadenador de arranque, objeto
- Objeto BootTrigger Programador de tareas
- Programador de tareas de objeto BootTrigger, descrito
topic_type:
- apiref
api_name:
- BootTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346a4bc7b20606f59c26b131590b92593d40d07e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493133"
---
# <a name="boottrigger-object"></a>Objeto BootTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea cuando se inicia el sistema.

## <a name="members"></a>Miembros

El objeto **BootTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **BootTrigger** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay**](boottrigger-delay.md)<br/>                       |                       | Obtiene o establece un valor que indica la cantidad de tiempo entre el momento en el que se arranca el sistema y el momento en que se inicia la tarea.<br/>                                                           |
| [**habilitado**](trigger-enabled.md)<br/>                       | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.<br/>                           |
| [**Sesión**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece el identificador del desencadenador.<br/>                                                                               |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Solo lectura<br/>  | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene el tipo del desencadenador.<br/>                                                                                              |



 

## <a name="remarks"></a>Observaciones

El servicio de Programador de tareas se inicia cuando se inicia el sistema operativo y las tareas de desencadenador de arranque se establecen para iniciarse cuando se inicia el servicio Programador de tareas.

Solo un miembro del grupo administradores puede crear una tarea con un desencadenador de arranque.

Al crear su propio XML para una tarea, se especifica un desencadenador de arranque mediante el elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) del esquema de programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de arranque (scripting)](boot-trigger-example--scripting-.md).

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

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





