---
title: Desencadenador (objeto)
description: Objeto de scripting que proporciona las propiedades comunes que heredan todos los objetos de desencadenador.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- desencadenadores Programador de tareas, objeto desencadenador
- Programador de tareas de objeto desencadenador
- Programador de tareas de objeto desencadenador, descrito
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905116"
---
# <a name="trigger-object"></a>Desencadenador (objeto)

Objeto de scripting que proporciona las propiedades comunes que heredan todos los objetos de desencadenador.

## <a name="members"></a>Miembros

El objeto **desencadenador** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **desencadenador** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lectura/escritura<br/> | Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura/escritura<br/> | Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.<br/>                                         |
| [**Sesión**](trigger-id.md)<br/>                                 | Lectura/escritura<br/> | Obtiene o establece el identificador del desencadenador.<br/>                                                                                             |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece la fecha y hora en que se activa el desencadenador. El desencadenador puede iniciar la tarea después de activar el desencadenador.<br/>             |
| [**Tipo**](trigger-type.md)<br/>                             |                       | Obtiene el tipo del desencadenador.<br/>                                                                                                            |



 

## <a name="remarks"></a>Observaciones

En el Programador de tareas se proporcionan los siguientes objetos individuales para los distintos desencadenadores que puede usar una tarea:

-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**SessionStateChangeTrigger**](sessionstatechangetrigger.md)

Al leer o escribir XML, los desencadenadores de una tarea se especifican en el elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) del esquema de programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> </dl>

 

 





