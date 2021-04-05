---
title: Trigger. EndBoundary (propiedad)
description: En el caso de scripting, obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Programador de tareas de la propiedad EndBoundary
- Propiedad EndBoundary Programador de tareas, objeto desencadenador
- Programador de tareas de objeto desencadenador, propiedad EndBoundary
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
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079154"
---
# <a name="triggerendboundary-property"></a>Trigger. EndBoundary (propiedad)

En el caso de scripting, obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.

## <a name="syntax"></a>Sintaxis


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a>Valor de propiedad

Fecha y hora de desactivación del desencadenador. La fecha y la hora deben tener el formato siguiente: AAAA-MM-DDTHH: MM: SS (+-) HH: MM. Por ejemplo, la fecha 11 de octubre de 2005 a 1:21:17 en la zona horaria del Pacífico se escribiría como 2005-10-11T13:21:17-08:00. La sección (+-) HH: MM del formato describe la zona horaria como un número determinado de horas de antemano o detrás de la hora universal coordinada (hora del meridiano de Greenwich).

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, se especifica la propiedad Enabled mediante el elemento [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) del esquema de programador de tareas.

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

 

 





