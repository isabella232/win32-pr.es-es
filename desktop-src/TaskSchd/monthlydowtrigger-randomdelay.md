---
title: Propiedad MonthlyDOWTrigger.RandomDelay
description: Para el scripting, obtiene o establece una hora de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. | Propiedad MonthlyDOWTrigger.RandomDelay
ms.assetid: e5cb6c1d-8003-43f4-bf35-da490a6097f0
keywords:
- Propiedad RandomDelay Programador de tareas
- Propiedad RandomDelay Programador de tareas , objeto MonthlyDOWTrigger
- Objeto MonthlyDOWTrigger Programador de tareas , propiedad RandomDelay
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e781941e927547a4ea25935fb21299777c34b3ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073426"
---
# <a name="monthlydowtriggerrandomdelay-property"></a>Propiedad MonthlyDOWTrigger.RandomDelay

Para el scripting, obtiene o establece una hora de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.

## <a name="syntax"></a>Sintaxis


```VB
MonthlyDOWTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valor de propiedad

Tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, P2DT5S es un retraso de 2 días y 5 segundos).

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
</dt> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> </dl>

 

 





