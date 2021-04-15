---
title: RepetitionPattern. Duration (propiedad)
description: En el caso de scripting, obtiene o establece el tiempo que se repite el patrón.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Propiedad duration Programador de tareas
- Propiedad duration Programador de tareas, objeto RepetitionPattern
- Programador de tareas de objeto RepetitionPattern, propiedad duration
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686084"
---
# <a name="repetitionpatternduration-property"></a>RepetitionPattern. Duration (propiedad)

En el caso de scripting, obtiene o establece el tiempo que se repite el patrón.

## <a name="syntax"></a>Sintaxis


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a>Valor de propiedad

Cuánto tiempo se repite el patrón. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). El tiempo mínimo permitido es de un minuto.

Si no se especifica ningún valor para la duración, el patrón se repite indefinidamente.

## <a name="remarks"></a>Observaciones

Si especifica una duración de repetición para una tarea, también debe especificar el intervalo de repetición.

Al leer o escribir XML para una tarea, la duración de repetición se especifica en el elemento [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) del esquema de programador de tareas.

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

 

 





