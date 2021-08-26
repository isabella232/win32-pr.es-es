---
title: Propiedad TaskSettings.AllowDemandStart
description: Para el scripting, obtiene o establece un valor booleano que indica que la tarea se puede iniciar mediante el comando Ejecutar o el menú Contextual.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Propiedad AllowDemandStart Programador de tareas
- Propiedad AllowDemandStart Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad AllowDemandStart
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a48ecaf9010b4269ffff66b556d01cfccc057fd05207f619290af9e50f6c757f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959485"
---
# <a name="tasksettingsallowdemandstart-property"></a>Propiedad TaskSettings.AllowDemandStart

Para el scripting, obtiene o establece un valor booleano que indica que la tarea se puede iniciar mediante el comando Ejecutar o el menú Contextual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, la tarea se puede ejecutar mediante el comando Ejecutar o el menú contextual. Si es False, la tarea no se puede ejecutar mediante el comando Ejecutar o el menú contextual. El valor predeterminado es True.

## <a name="remarks"></a>Comentarios

Cuando esta propiedad se establece en True, la tarea se puede iniciar independientemente de cuando algún desencadenador inicia la tarea.

Al leer o escribir XML para una tarea, esta configuración se especifica en el [elemento AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





