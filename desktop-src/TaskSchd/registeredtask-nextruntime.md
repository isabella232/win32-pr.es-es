---
title: RegisteredTask.NextRunTime, propiedad
description: Para el scripting, obtiene la hora a la que se programa la siguiente ejecución de la tarea registrada.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Propiedad NextRunTime Programador de tareas
- Propiedad NextRunTime Programador de tareas , objeto RegisteredTask
- Objeto RegisteredTask Programador de tareas propiedad , NextRunTime
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172982"
---
# <a name="registeredtasknextruntime-property"></a>RegisteredTask.NextRunTime, propiedad

Para el scripting, obtiene la hora a la que se programa la siguiente ejecución de la tarea registrada.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>Valor de propiedad

Hora a la que se programa la siguiente ejecución de la tarea registrada.

## <a name="remarks"></a>Observaciones

Si la tarea registrada contiene desencadenadores que están deshabilitados individualmente, estos desencadenadores seguirán afectando al siguiente tiempo de ejecución programado que se devuelve aunque estén deshabilitados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





