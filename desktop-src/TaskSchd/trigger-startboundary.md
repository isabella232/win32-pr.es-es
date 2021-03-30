---
title: Trigger. StartBoundary (propiedad)
description: En el caso de scripting, obtiene o establece la fecha y hora en que se activa el desencadenador.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- Programador de tareas de la propiedad StartBoundary
- Propiedad StartBoundary Programador de tareas, objeto desencadenador
- Programador de tareas de objeto desencadenador, propiedad StartBoundary
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
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801747"
---
# <a name="triggerstartboundary-property"></a>Trigger. StartBoundary (propiedad)

En el caso de scripting, obtiene o establece la fecha y hora en que se activa el desencadenador.

## <a name="syntax"></a>Sintaxis


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a>Valor de propiedad

Fecha y hora en que se activa el desencadenador. La fecha y la hora deben tener el formato siguiente: AAAA-MM-DDTHH: MM: SS (+-) HH: MM. Por ejemplo, la fecha 11 de octubre de 2005 a 1:21:17 en la zona horaria del Pacífico se escribiría como 2005-10-11T13:21:17-08:00. La sección (+-) HH: MM del formato describe la zona horaria como un número determinado de horas de antemano o detrás de la hora universal coordinada (hora del meridiano de Greenwich).

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el límite de inicio del desencadenador se especifica en el elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) del esquema de programador de tareas.

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

 

 





