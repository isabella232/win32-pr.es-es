---
title: Propiedad RepetitionPattern.Duration
description: Para el scripting, obtiene o establece cuánto tiempo se repite el patrón.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Propiedad Duration Programador de tareas
- Propiedad Duration Programador de tareas , objeto RepetitionPattern
- Objeto RepetitionPattern Programador de tareas , propiedad Duration
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
ms.openlocfilehash: b649562d4d28f5427427e72c03172aecdc9cdac803b0239c020806673cb0bae8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759214"
---
# <a name="repetitionpatternduration-property"></a>Propiedad RepetitionPattern.Duration

Para el scripting, obtiene o establece cuánto tiempo se repite el patrón.

## <a name="syntax"></a>Syntax


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a>Valor de propiedad

Cuánto tiempo se repite el patrón. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). El tiempo mínimo permitido es de un minuto.

Si no se especifica ningún valor durante la duración, el patrón se repite indefinidamente.

## <a name="remarks"></a>Comentarios

Si especifica una duración de repetición para una tarea, también debe especificar el intervalo de repetición.

Al leer o escribir XML para una tarea, la duración de la repetición se especifica en el [**elemento Duration**](taskschedulerschema-duration-repetitiontype-element.md) del Programador de tareas esquema.

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
</dt> </dl>

 

 





