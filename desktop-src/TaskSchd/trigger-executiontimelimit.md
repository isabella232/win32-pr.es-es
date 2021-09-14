---
title: Propiedad Trigger.ExecutionTimeLimit
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
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264908"
---
# <a name="triggerexecutiontimelimit-property"></a>Propiedad Trigger.ExecutionTimeLimit

Para el scripting, obtiene o establece la cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse.

## <a name="syntax"></a>Sintaxis


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Valor de propiedad

La cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el límite de tiempo de ejecución se especifica en el [**elemento ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) del esquema Programador de tareas ejecución.

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

 

 





