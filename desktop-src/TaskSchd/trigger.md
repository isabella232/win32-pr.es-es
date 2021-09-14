---
title: Desencadenador de objeto
description: Objeto de scripting que proporciona las propiedades comunes heredadas por todos los objetos de desencadenador.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- desencadenadores Programador de tareas , objeto de desencadenador
- Desencadenador de objetos Programador de tareas
- Desencadenador de objetos Programador de tareas , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891396"
---
# <a name="trigger-object"></a>Desencadenador de objeto

Objeto de scripting que proporciona las propiedades comunes heredadas por todos los objetos de desencadenador.

## <a name="members"></a>Members

El **objeto Trigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Trigger** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Lectura y escritura<br/> | Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lectura y escritura<br/> | Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura y escritura<br/> | Obtiene o establece la cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse.<br/>                                         |
| [**Id**](trigger-id.md)<br/>                                 | Lectura y escritura<br/> | Obtiene o establece el identificador del desencadenador.<br/>                                                                                             |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura y escritura<br/> | Obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura y escritura<br/> | Obtiene o establece la fecha y hora en que se activa el desencadenador. El desencadenador puede iniciar la tarea después de activar el desencadenador.<br/>             |
| [**Tipo**](trigger-type.md)<br/>                             |                       | Obtiene el tipo del desencadenador.<br/>                                                                                                            |



 

## <a name="remarks"></a>Observaciones

El Programador de tareas proporciona los siguientes objetos individuales para los distintos desencadenadores que puede usar una tarea:

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

Al leer o escribir XML, los desencadenadores de una tarea se especifican en el [**elemento Triggers**](taskschedulerschema-triggers-tasktype-element.md) del Programador de tareas esquema.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea [Ejemplo de desencadenador de tiempo (scripting).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> </dl>

 

 





