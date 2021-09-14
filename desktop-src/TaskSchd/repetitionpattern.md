---
title: Objeto RepetitionPattern
description: Objeto de scripting que define la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- desencadenadores Programador de tareas , objeto de patrón de repetición
- patrón de repetición Programador de tareas , objeto
- Objeto RepetitionPattern Programador de tareas
- Objeto RepetitionPattern Programador de tareas , descrito
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172857"
---
# <a name="repetitionpattern-object"></a>Objeto RepetitionPattern

Objeto de scripting que define la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.

## <a name="members"></a>Members

El **objeto RepetitionPattern** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto RepetitionPattern** tiene estas propiedades.



| Propiedad                                                                    | Tipo de acceso           | Descripción                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](repetitionpattern-duration.md)<br/>                   | Lectura y escritura<br/> | Obtiene o establece cuánto tiempo se repite el patrón.<br/>                                                                                          |
| [**Intervalo**](repetitionpattern-interval.md)<br/>                   | Lectura y escritura<br/> | Obtiene o establece la cantidad de tiempo entre cada reinicio de la tarea.<br/>                                                                       |
| [**StopAtDurationEnd**](repetitionpattern-stopatdurationend.md)<br/> | Lectura y escritura<br/> | Obtiene o establece un valor booleano que indica si una instancia en ejecución de la tarea se detiene al final de la duración del patrón de repetición.<br/> |



 

## <a name="remarks"></a>Observaciones

Si especifica una duración de repetición para una tarea, también debe especificar el intervalo de repetición.

Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cinco veces. Las cinco repeticiones se pueden definir mediante el siguiente patrón.

1.  Una tarea se inicia al principio del primer minuto.
2.  La siguiente tarea se inicia al final del primer minuto.
3.  La siguiente tarea se inicia al final del segundo minuto.
4.  La siguiente tarea se inicia al final del tercer minuto.
5.  La siguiente tarea se inicia al final del cuarto minuto.

**Windows Server 2003, Windows XP y Windows 2000:** Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cuatro veces.

Al leer o escribir XML para una tarea, el patrón de repetición se especifica mediante el [**elemento Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) del Programador de tareas esquema.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para esta propiedad, vea [Ejemplo de desencadenador diario (scripting).](daily-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas objetos](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





