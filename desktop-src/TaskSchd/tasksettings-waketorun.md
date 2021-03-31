---
title: Propiedad TaskSettings. WakeToRun
description: En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas reactivará el equipo cuando llega el momento de ejecutar la tarea.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Programador de tareas de la propiedad WakeToRun
- Programador de tareas de la propiedad WakeToRun, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad WakeToRun
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801753"
---
# <a name="tasksettingswaketorun-property"></a>Propiedad TaskSettings. WakeToRun

En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas reactivará el equipo cuando llega el momento de ejecutar la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es true, la propiedad indica que el Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.

## <a name="remarks"></a>Observaciones

Cuando el servicio de Programador de tareas reactiva el equipo para ejecutar una tarea, es posible que la pantalla permanezca desactivada aunque el equipo ya no esté en modo de suspensión o hibernación. La pantalla se activará cuando Windows Vista detecte que un usuario ha vuelto a usar el equipo.

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) del esquema de programador de tareas.

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

 

 





