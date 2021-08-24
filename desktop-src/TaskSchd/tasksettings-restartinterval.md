---
title: Propiedad TaskSettings.RestartInterval
description: Para el scripting, obtiene o establece un valor que especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Propiedad RestartInterval Programador de tareas
- Propiedad RestartInterval Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad RestartInterval
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3293072fcec50b140a298887b12ed8f5dd1fb6a298c3b486069fe2e7eccaef00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681615"
---
# <a name="tasksettingsrestartinterval-property"></a>Propiedad TaskSettings.RestartInterval

Para el scripting, obtiene o establece un valor que especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Valor de propiedad

Valor que especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea. Si se establece esta propiedad, también se debe establecer la propiedad [**RestartCount.**](tasksettings-restartcount.md) El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, "PT5M" es 5 minutos, "PT1H" es 1 hora y "PT20M" es 20 minutos). El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es de 1 minuto.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento Interval**](taskschedulerschema-interval-restarttype-element.md) del Programador de tareas esquema.

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

 

 





