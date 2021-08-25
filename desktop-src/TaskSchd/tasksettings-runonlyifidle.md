---
title: Propiedad TaskSettings.RunOnlyIfIdle
description: Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición de inactividad.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Propiedad RunOnlyIfIdle Programador de tareas
- Propiedad RunOnlyIfIdle Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad RunOnlyIfIdle
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
ms.openlocfilehash: ed423dc4cd34a03bd3b76401284a4d6bfb98270e7c0d0feed0a45046a82e7d3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990825"
---
# <a name="tasksettingsrunonlyifidle-property"></a>Propiedad TaskSettings.RunOnlyIfIdle

Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición de inactividad.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, la propiedad indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición inactiva. El valor predeterminado es False.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) del Programador de tareas esquema.

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

 

 





