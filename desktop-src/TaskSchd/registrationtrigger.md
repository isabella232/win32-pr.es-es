---
title: Objeto RegistrationTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando la tarea se registra o actualiza.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- desencadenador de registro Programador de tareas , objeto
- RegistrationTrigger object Programador de tareas
- Objeto RegistrationTrigger Programador de tareas , descrito
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85020e3c5a2d5c3167ac2ec6ed251a37c1bc98056dae867a5a07b63ee7148dae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759576"
---
# <a name="registrationtrigger-object"></a>Objeto RegistrationTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea cuando la tarea se registra o actualiza.

## <a name="members"></a>Miembros

El **objeto RegistrationTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto RegistrationTrigger** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay**](registrationtrigger-delay.md)<br/>               | Lectura/escritura<br/> | Obtiene o establece la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.<br/>                                                                                |
| [**habilitado**](trigger-enabled.md)<br/>                       | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece el identificador del desencadenador.<br/>                                                                               |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Solo lectura<br/>  | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene el tipo del desencadenador.<br/>                                                                                              |



 

## <a name="remarks"></a>Comentarios

Al crear su propio XML para una tarea, se especifica un desencadenador de registro mediante el [**elemento RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) del Programador de tareas esquema.

Si se registra una tarea con un desencadenador de registro retrasado y el equipo en el que está registrada la tarea se apaga o se reinicia durante el retraso, antes de que se ejecute la tarea, la tarea no se ejecutará y se perderá el retraso.

## <a name="examples"></a>Ejemplos

Para obtener más información y un ejemplo de código para este objeto de scripting, vea [Ejemplo de desencadenador de registro (scripting).](registration-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**detonante**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





