---
title: Propiedad TaskSettings.Compatibility
description: Para el scripting, obtiene o establece un valor entero que indica con qué versión de Programador de tareas una tarea es compatible.
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Propiedades de compatibilidad Programador de tareas
- Propiedad Compatibility Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad Compatibility
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
ms.openlocfilehash: 48cc560029400206d749ee7fc74fdf2330b02578ffd73fa4494d8d426951e5d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738245"
---
# <a name="tasksettingscompatibility-property"></a>Propiedad TaskSettings.Compatibility

Para el scripting, obtiene o establece un valor entero que indica con qué versión de Programador de tareas una tarea es compatible.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a>Valor de propiedad



| Value                                                                                                                                                                                                                                         | Significado                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <dt>**TASK \_ COMPATIBILIDAD \_ EN**</dt> <dt>0</dt> </dl> | La tarea es compatible con el comando AT.<br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <dt>**TASK \_ COMPATIBILIDAD \_ V1**</dt> <dt>1</dt> </dl> | La tarea es compatible con Programador de tareas 1.0.<br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <dt>**TASK \_ COMPATIBILIDAD \_ V2**</dt> <dt>2</dt> </dl> | La tarea es compatible con Programador de tareas 2.0.<br/> |



 

## <a name="remarks"></a>Comentarios

La compatibilidad de tareas, que se establece a través de la propiedad [**Compatibilidad,**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) solo debe establecerse en TASK COMPATIBILITY V1 si es necesario tener acceso a una tarea o modificarla desde un equipo \_ Windows \_ XP, Windows Server 2003 o Windows 2000. De lo contrario, se recomienda Programador de tareas compatibilidad con 2.0 porque la tarea tendrá más características.

Las tareas compatibles con el comando AT solo pueden tener un desencadenador de una vez.

Las tareas compatibles con Programador de tareas 1.0 solo pueden tener un desencadenador de hora, un desencadenador de inicio de sesión o un desencadenador de arranque, y la tarea solo puede tener una acción ejecutable.

Para obtener más información sobre la compatibilidad de tareas, vea [Novedades de Programador de tareas](what-s-new-in-task-scheduler.md) y [Tareas](tasks.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COMPATIBILIDAD DE \_ TAREAS**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





