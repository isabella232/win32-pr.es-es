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
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968531"
---
# <a name="tasksettingsenabled-property"></a>Propiedad TaskSettings.Enabled

Para el scripting, obtiene o establece un valor booleano que indica que la tarea está habilitada. La tarea solo se puede realizar cuando esta configuración es True.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, la tarea está habilitada. Si es False, la tarea no está habilitada.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) del esquema Programador de tareas datos.

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

 

 





