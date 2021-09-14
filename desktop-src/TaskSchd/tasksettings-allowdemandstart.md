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
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968552"
---
# <a name="tasksettingsallowdemandstart-property"></a>Propiedad TaskSettings.AllowDemandStart

Para el scripting, obtiene o establece un valor booleano que indica que la tarea se puede iniciar mediante el comando Ejecutar o el menú Contextual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, la tarea se puede ejecutar mediante el comando Ejecutar o el menú contextual. Si es False, la tarea no se puede ejecutar mediante el comando Ejecutar o el menú contextual. El valor predeterminado es True.

## <a name="remarks"></a>Observaciones

Cuando esta propiedad se establece en True, la tarea se puede iniciar independientemente de cuando cualquier desencadenador inicie la tarea.

Al leer o escribir XML para una tarea, esta configuración se especifica en el [elemento AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) del Programador de tareas esquema.

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

 

 





