---
title: Propiedad TaskSettings. AllowHardTerminate
description: Para scripting, obtiene o establece un valor booleano que indica que el servicio de Programador de tareas puede finalizar la tarea mediante TerminateProcess.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- Programador de tareas de la propiedad AllowHardTerminate
- Programador de tareas de la propiedad AllowHardTerminate, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad AllowHardTerminate
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
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802960"
---
# <a name="tasksettingsallowhardterminate-property"></a>Propiedad TaskSettings. AllowHardTerminate

Para scripting, obtiene o establece un valor booleano que indica que el servicio de Programador de tareas puede finalizar la tarea mediante [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). El servicio intentará cerrar la tarea en ejecución mediante el envío de la notificación de [**\_ cierre de WM**](../winmsg/wm-close.md) y, si la tarea no responde, la tarea se terminará solo si esta propiedad está establecida en true.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es true, la tarea se puede finalizar mediante [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Si es false, la tarea no se puede finalizar mediante **TerminateProcess**.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

