---
title: Propiedad Trigger.StartBoundary
description: Para el scripting, obtiene o establece la fecha y hora en que se activa el desencadenador.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- Propiedad StartBoundary Programador de tareas
- Propiedad StartBoundary Programador de tareas , objeto Trigger
- Desencadenador de objeto Programador de tareas , propiedad StartBoundary
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b49fa865c215c3190b2d081390c98eec1336ffb00a4bf1e9dd9d94226105e96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002083"
---
# <a name="triggerstartboundary-property"></a>Propiedad Trigger.StartBoundary

Para el scripting, obtiene o establece la fecha y hora en que se activa el desencadenador.

## <a name="syntax"></a>Syntax


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a>Valor de propiedad

Fecha y hora en que se activa el desencadenador. La fecha y hora deben tener el formato siguiente: YYYY-MM-DDTHH:MM:SS(+-)HH:MM. Por ejemplo, la fecha del 11 de octubre de 2005 a las 1:21:17 en la zona horaria del Pacífico se escribiría como 2005-10-11T13:21:17-08:00. La sección (+-)HH:MM del formato describe la zona horaria como un número determinado de horas de antelación o detrás de la hora universal coordinada (hora media de Greenwich).

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, el límite inicial del desencadenador se especifica en el [**elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) del Programador de tareas esquema.

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

 

 





