---
title: Propiedad IdleSettings. RestartOnIdle
description: En el caso de scripting, obtiene o establece un valor booleano que indica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Programador de tareas de la propiedad RestartOnIdle
- Programador de tareas de la propiedad RestartOnIdle, objeto IdleSettings
- Programador de tareas de objeto IdleSettings, propiedad RestartOnIdle
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686000"
---
# <a name="idlesettingsrestartonidle-property"></a>Propiedad IdleSettings. RestartOnIdle

En el caso de scripting, obtiene o establece un valor booleano que indica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.

## <a name="syntax"></a>Sintaxis


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Un valor booleano que indica si la tarea debe reiniciarse cuando el equipo se recorre en una condición de inactividad más de una vez. El valor predeterminado es False.

## <a name="remarks"></a>Observaciones

Esta propiedad solo se usa si la propiedad [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md) está establecida en true.

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) del esquema de programador de tareas.

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
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





