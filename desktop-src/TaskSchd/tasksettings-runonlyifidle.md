---
title: Propiedad TaskSettings. RunOnlyIfIdle
description: En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición de inactividad.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Programador de tareas de la propiedad RunOnlyIfIdle
- Programador de tareas de la propiedad RunOnlyIfIdle, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad RunOnlyIfIdle
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422155"
---
# <a name="tasksettingsrunonlyifidle-property"></a>Propiedad TaskSettings. RunOnlyIfIdle

En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición de inactividad.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es true, la propiedad indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición de inactividad. El valor predeterminado es False.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) del esquema de programador de tareas.

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

 

 





