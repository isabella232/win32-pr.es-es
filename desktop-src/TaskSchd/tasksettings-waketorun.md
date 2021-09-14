---
title: Propiedad TaskSettings.WakeToRun
description: Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas reactivará el equipo cuando llegue el momento de ejecutar la tarea.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Propiedad WakeToRun Programador de tareas
- Propiedad WakeToRun Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad WakeToRun
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
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073403"
---
# <a name="tasksettingswaketorun-property"></a>Propiedad TaskSettings.WakeToRun

Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas reactivará el equipo cuando llegue el momento de ejecutar la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, la propiedad indica que el Programador de tareas reactivará el equipo cuando llegue el momento de ejecutar la tarea.

## <a name="remarks"></a>Observaciones

Cuando el Programador de tareas reactiva el equipo para ejecutar una tarea, la pantalla puede permanecer desactivada aunque el equipo ya no esté en modo de suspensión o hibernación. La pantalla se activará cuando Windows Vista detecte que un usuario ha vuelto a usar el equipo.

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





