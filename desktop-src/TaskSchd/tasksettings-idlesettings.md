---
title: Propiedad TaskSettings. IdleSettings
description: En el caso de scripting, obtiene o establece la información que especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en una condición de inactividad.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- Programador de tareas de la propiedad IdleSettings
- Programador de tareas de la propiedad IdleSettings, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad IdleSettings
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676849"
---
# <a name="tasksettingsidlesettings-property"></a>Propiedad TaskSettings. IdleSettings

En el caso de scripting, obtiene o establece la información que especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en una condición de inactividad. Para obtener información sobre las condiciones de inactividad, consulte [condiciones de inactividad de tareas](task-idle-conditions.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**IdleSettings**](idlesettings.md) que especifica cómo el programador de tareas controla la tarea cuando el equipo entra en una condición de inactividad.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) del esquema de programador de tareas.

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

 

 





