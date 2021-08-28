---
title: Propiedad TaskSettings.Enabled
description: Para el scripting, obtiene o establece un valor booleano que indica que la tarea está habilitada. La tarea solo se puede realizar cuando esta configuración es True.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Propiedades habilitadas Programador de tareas
- Propiedad Enabled Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas propiedad , Enabled
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
ms.openlocfilehash: 0e7853177aecae963e4899a67d2ba5b39d1eaebdc75e25ce6e14523963a70c45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738166"
---
# <a name="tasksettingsenabled-property"></a>Propiedad TaskSettings.Enabled

Para el scripting, obtiene o establece un valor booleano que indica que la tarea está habilitada. La tarea solo se puede realizar cuando esta configuración es True.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, la tarea está habilitada. Si es False, la tarea no está habilitada.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) del Programador de tareas esquema.

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

 

 





