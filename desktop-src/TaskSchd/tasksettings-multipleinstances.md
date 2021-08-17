---
title: Propiedad TaskSettings.MultipleInstances
description: Para el scripting, obtiene o establece la directiva que define cómo el Programador de tareas trata con varias instancias de la tarea.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Propiedad MultipleInstances Programador de tareas
- Propiedad MultipleInstances Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas propiedad , MultipleInstances
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff0091b9051840fea4c37869b51902f0c5f4c7cfed43a47c4f3924b398fe3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059693"
---
# <a name="tasksettingsmultipleinstances-property"></a>Propiedad TaskSettings.MultipleInstances

Para el scripting, obtiene o establece la directiva que define cómo el Programador de tareas trata con varias instancias de la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a>Valor de propiedad

[**TASK \_ Constantes DE \_ INSTANCES POLICY.**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)



| Value                                                                                                                                                                                                                                                               | Significado                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <dt>**TASK \_ INSTANCES \_ PARALLEL**</dt> <dt>0</dt> </dl>                 | Inicia una nueva instancia mientras se ejecuta una instancia existente de la tarea.<br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <dt>**TASK \_ INSTANCES \_ QUEUE**</dt> <dt>1</dt> </dl>                          | Inicia una nueva instancia de la tarea una vez completadas todas las demás instancias de la tarea.<br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <dt>**TASK \_ LAS INSTANCIAS \_ \_ OMITEN NEW**</dt> <dt>2</dt> </dl>          | No inicia una nueva instancia si se está ejecutando una instancia existente de la tarea.<br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <dt>**TASK \_ INSTANCES \_ STOP \_ EXISTING**</dt> <dt>3</dt> </dl> | Detiene una instancia existente de la tarea antes de iniciar la nueva instancia.<br/>                 |



 

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DIRECTIVA \_ DE INSTANCIAS DE \_ TAREA**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





