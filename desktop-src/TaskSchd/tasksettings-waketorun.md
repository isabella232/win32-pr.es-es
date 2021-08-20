---
title: Propiedad TaskSettings.WakeToRun
description: Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas reactivará el equipo cuando llegue el momento de ejecutar la tarea.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Propiedad WakeToRun Programador de tareas
- Propiedad WakeToRun Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas propiedad , WakeToRun
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660aa9469d1146edcf40b480772ed2461cbc539688a10603c76b48b49b3749de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857068"
---
# <a name="tasksettingswaketorun-property"></a>Propiedad TaskSettings.WakeToRun

Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas reactivará el equipo cuando llegue el momento de ejecutar la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, la propiedad indica que el Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.

## <a name="remarks"></a>Comentarios

Cuando el Programador de tareas reactiva el equipo para ejecutar una tarea, la pantalla puede permanecer desactivada aunque el equipo ya no esté en modo de suspensión o hibernación. La pantalla se activará cuando Windows Vista detecte que un usuario ha vuelto a usar el equipo.

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





