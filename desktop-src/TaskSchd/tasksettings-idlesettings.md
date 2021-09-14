---
title: Propiedad TaskSettings.IdleSettings
description: Para el scripting, obtiene o establece la información que especifica cómo el Programador de tareas realiza tareas cuando el equipo está en una condición de inactividad.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- Propiedad IdleSettings Programador de tareas
- Propiedad IdleSettings Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas propiedad , IdleSettings
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968527"
---
# <a name="tasksettingsidlesettings-property"></a>Propiedad TaskSettings.IdleSettings

Para el scripting, obtiene o establece la información que especifica cómo el Programador de tareas realiza tareas cuando el equipo está en una condición de inactividad. Para obtener información sobre las condiciones de inactividad, vea [Task Idle Conditions](task-idle-conditions.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**IdleSettings**](idlesettings.md) que especifica cómo el Programador de tareas controla la tarea cuando el equipo entra en una condición de inactividad.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) del Programador de tareas esquema.

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

 

 





