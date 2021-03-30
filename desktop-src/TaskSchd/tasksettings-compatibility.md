---
title: TaskSettings. Compatibility (propiedad)
description: Para scripting, obtiene o establece un valor entero que indica la versión de Programador de tareas que una tarea es compatible con.
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Programador de tareas de propiedades de compatibilidad
- Propiedad Compatibility Programador de tareas, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad Compatibility
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801760"
---
# <a name="tasksettingscompatibility-property"></a>TaskSettings. Compatibility (propiedad)

Para scripting, obtiene o establece un valor entero que indica la versión de Programador de tareas que una tarea es compatible con.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a>Valor de propiedad



| Value                                                                                                                                                                                                                                         | Significado                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <dt>**Tarea \_ de COMPATIBILIDAD \_ en**</dt> <dt>0</dt> </dl> | La tarea es compatible con el comando AT.<br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <dt>**Tarea \_ de COMPATIBILIDAD \_ v1**</dt> <dt>1</dt> </dl> | La tarea es compatible con Programador de tareas 1,0.<br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <dt>**Tarea \_ de COMPATIBILIDAD \_ V2**</dt> <dt>2</dt> </dl> | La tarea es compatible con Programador de tareas 2,0.<br/> |



 

## <a name="remarks"></a>Observaciones

La compatibilidad de tareas, que se establece a través de la propiedad de [**compatibilidad**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , solo se debe establecer en compatibilidad de tareas \_ \_ v1 si es necesario tener acceso a una tarea o modificarla desde un equipo con Windows XP, Windows Server 2003 o Windows 2000. De lo contrario, se recomienda usar la compatibilidad con Programador de tareas 2,0 porque la tarea tendrá más características.

Las tareas compatibles con el comando AT solo pueden tener un desencadenador de una vez.

Las tareas compatibles con Programador de tareas 1,0 solo pueden tener un desencadenador de tiempo, un desencadenador de inicio de sesión o un desencadenador de arranque y la tarea solo puede tener una acción ejecutable.

Para obtener más información sobre la compatibilidad de tareas, vea [novedades de programador de tareas](what-s-new-in-task-scheduler.md) y [tareas](tasks.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**compatibilidad de tareas \_**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





