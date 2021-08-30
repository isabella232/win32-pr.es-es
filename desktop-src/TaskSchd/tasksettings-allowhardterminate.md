---
title: Propiedad TaskSettings.AllowHardTerminate
description: Para el scripting, obtiene o establece un valor booleano que indica que la tarea puede ser finalizada por el servicio Programador de tareas mediante TerminateProcess.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- Propiedad AllowHardTerminate Programador de tareas
- Propiedad AllowHardTerminate Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas propiedad , AllowHardTerminate
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f6886a43a3c63df80c392b04dc35aa4f3331af52048c0bbe9e86aaf4005f638
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099765"
---
# <a name="tasksettingsallowhardterminate-property"></a>Propiedad TaskSettings.AllowHardTerminate

Para el scripting, obtiene o establece un valor booleano que indica que la tarea puede ser finalizada por el servicio Programador de tareas mediante [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). El servicio intentará cerrar la tarea en ejecución mediante el envío de la notificación [**WM \_ CLOSE**](../winmsg/wm-close.md) y, si la tarea no responde, la tarea finalizará solo si esta propiedad está establecida en true.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, la tarea se puede finalizar mediante [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Si es False, la tarea no se puede finalizar mediante **TerminateProcess**.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, esta configuración se especifica en el [elemento AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) del esquema Programador de tareas datos.

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

 

