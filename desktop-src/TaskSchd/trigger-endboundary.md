---
title: Propiedad Trigger.EndBoundary
description: Para el scripting, obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- EndBoundary, propiedad Programador de tareas
- EndBoundary, propiedad Programador de tareas , objeto Trigger
- Desencadenador de objetos Programador de tareas , propiedad EndBoundary
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4f2b72100a7b981246788b38572c014a722c126115ab5a77d77eb7d96273f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010455"
---
# <a name="triggerendboundary-property"></a>Propiedad Trigger.EndBoundary

Para el scripting, obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.

## <a name="syntax"></a>Syntax


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a>Valor de propiedad

Fecha y hora en que se desactiva el desencadenador. La fecha y hora deben tener el formato siguiente: YYYY-MM-DDTHH:MM:SS(+-)HH:MM. Por ejemplo, la fecha del 11 de octubre de 2005 a las 1:21:17 en la zona horaria del Pacífico se escribiría como 2005-10-11T13:21:17-08:00. La sección (+-)HH:MM del formato describe la zona horaria como un número determinado de horas de antelación o detrás de la hora universal coordinada (hora media de Greenwich).

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, la propiedad enabled se especifica mediante el [**elemento EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) del Programador de tareas esquema.

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

 

 





