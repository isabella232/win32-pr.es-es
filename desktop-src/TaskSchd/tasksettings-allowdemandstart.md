---
title: Propiedad TaskSettings. AllowDemandStart
description: En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea se puede iniciar con el comando ejecutar o el menú contextual.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Programador de tareas de la propiedad AllowDemandStart
- Programador de tareas de la propiedad AllowDemandStart, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad AllowDemandStart
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422029"
---
# <a name="tasksettingsallowdemandstart-property"></a>Propiedad TaskSettings. AllowDemandStart

En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea se puede iniciar con el comando ejecutar o el menú contextual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es true, la tarea se puede ejecutar con el comando ejecutar o el menú contextual. Si es false, la tarea no se puede ejecutar con el comando ejecutar o el menú contextual. El valor predeterminado es True.

## <a name="remarks"></a>Observaciones

Cuando esta propiedad se establece en true, la tarea puede iniciarse de forma independiente cuando algún desencadenador inicia la tarea.

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) del esquema de programador de tareas.

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

 

 





