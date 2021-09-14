---
title: Propiedad RepetitionPattern.Interval
description: Para el scripting, obtiene o establece la cantidad de tiempo entre cada reinicio de la tarea.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Intervalo de propiedades Programador de tareas
- Propiedad Interval Programador de tareas , objeto RepetitionPattern
- Objeto RepetitionPattern Programador de tareas , propiedad Interval
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172861"
---
# <a name="repetitionpatterninterval-property"></a>Propiedad RepetitionPattern.Interval

Para el scripting, obtiene o establece la cantidad de tiempo entre cada reinicio de la tarea.

## <a name="syntax"></a>Sintaxis


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>Valor de propiedad

Cantidad de tiempo entre cada reinicio de la tarea. El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, "PT5M" es 5 minutos, "PT1H" es 1 hora y "PT20M" es 20 minutos). El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es de 1 minuto.

## <a name="remarks"></a>Observaciones

Si especifica una duración de repetición para una tarea, también debe especificar el intervalo de repetición.

Al leer o escribir XML para una tarea, el intervalo de repetición se especifica en el [**elemento Interval**](taskschedulerschema-interval-repetitiontype-element.md) del Programador de tareas esquema.

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

 

 





