---
title: Propiedad TaskSettings.RunOnlyIfIdle
description: Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición inactiva.
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
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160607"
---
# <a name="tasksettingsrunonlyifidle-property"></a>Propiedad TaskSettings.RunOnlyIfIdle

Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición inactiva.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, la propiedad indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición de inactividad. El valor predeterminado es False.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) del esquema Programador de tareas datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





