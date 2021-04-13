---
title: Propiedad TaskSettings. Enabled
description: En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea está habilitada. La tarea solo se puede realizar cuando este valor es true.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Propiedad Enabled Programador de tareas
- Propiedad Enabled Programador de tareas, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad Enabled
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422437"
---
# <a name="tasksettingsenabled-property"></a>Propiedad TaskSettings. Enabled

En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea está habilitada. La tarea solo se puede realizar cuando este valor es true.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es true, la tarea está habilitada. Si es false, la tarea no está habilitada.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) del esquema de programador de tareas.

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

 

 





