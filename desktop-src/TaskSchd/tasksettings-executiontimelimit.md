---
title: Propiedad TaskSettings.ExecutionTimeLimit
description: Para el scripting, obtiene o establece la cantidad de tiempo que se permite completar la tarea.
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- Propiedad ExecutionTimeLimit Programador de tareas
- Propiedad ExecutionTimeLimit Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad ExecutionTimeLimit
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968528"
---
# <a name="tasksettingsexecutiontimelimit-property"></a>Propiedad TaskSettings.ExecutionTimeLimit

Para el scripting, obtiene o establece la cantidad de tiempo que se permite completar la tarea. De forma predeterminada, una tarea se detendrán 72 horas después de que empiece a ejecutarse. Puede cambiar esto cambiando esta configuración.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Valor de propiedad

Cantidad de tiempo que se permite completar la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). Un valor de PT0S permitirá que la tarea se ejecute indefinidamente. Cuando este parámetro se establece en Nothing, el límite de tiempo de ejecución es infinito.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) del Programador de tareas esquema.

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

 

 





