---
title: Trigger.Exepropiedad cutionTimeLimit
description: Para el scripting, obtiene o establece la cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse.
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- Propiedad ExecutionTimeLimit Programador de tareas
- Propiedad ExecutionTimeLimit Programador de tareas , objeto Trigger
- Desencadenador de objetos Programador de tareas , propiedad ExecutionTimeLimit
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724cc80a1d3bf35d00aff1eba220d657723ee8c5ed8ddb3c95474cf0534bff79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857078"
---
# <a name="triggerexecutiontimelimit-property"></a>Trigger.Exepropiedad cutionTimeLimit

Para el scripting, obtiene o establece la cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse.

## <a name="syntax"></a>Syntax


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Valor de propiedad

La cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, el límite de tiempo de ejecución se especifica en el [**elemento ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) del esquema Programador de tareas ejecución.

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

 

 





