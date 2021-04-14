---
title: Propiedad TaskSettings. MultipleInstances
description: En el caso de scripting, obtiene o establece la Directiva que define el modo en que el Programador de tareas se encarga de varias instancias de la tarea.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Programador de tareas de la propiedad MultipleInstances
- Programador de tareas de la propiedad MultipleInstances, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad MultipleInstances
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
ms.openlocfilehash: 794ea07f1c01dabe957181bd327f8787f873917b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533855"
---
# <a name="tasksettingsmultipleinstances-property"></a>Propiedad TaskSettings. MultipleInstances

En el caso de scripting, obtiene o establece la Directiva que define el modo en que el Programador de tareas se encarga de varias instancias de la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a>Valor de propiedad

[**Tarea \_ de Constantes \_**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) de la Directiva de instancias.



| Value                                                                                                                                                                                                                                                               | Significado                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <dt>**Tarea \_ de INSTANCIAS en \_ paralelo**</dt> <dt>0</dt> </dl>                 | Inicia una nueva instancia de mientras se ejecuta una instancia existente de la tarea.<br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <dt>**Tarea \_ de \_Cola de instancias**</dt> <dt>1</dt> </dl>                          | Inicia una nueva instancia de la tarea después de que todas las demás instancias de la tarea se hayan completado.<br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <dt>**Tarea \_ de INSTANCIAS \_ omitir \_ nuevo**</dt> <dt>2</dt> </dl>          | No inicia una nueva instancia de si se está ejecutando una instancia existente de la tarea.<br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <dt>**Tarea \_ de LAS instancias se \_ detienen 3 \_ existentes**</dt> <dt></dt> </dl> | Detiene una instancia existente de la tarea antes de iniciar una nueva instancia.<br/>                 |



 

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Directiva de instancias de tarea \_**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





