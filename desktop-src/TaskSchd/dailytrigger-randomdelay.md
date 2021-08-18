---
title: DailyTrigger.RandomDelay, propiedad
description: Para el scripting, obtiene o establece una hora de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. | DailyTrigger.RandomDelay, propiedad
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- Propiedad RandomDelay Programador de tareas
- Propiedad RandomDelay Programador de tareas , objeto DailyTrigger
- Objeto DailyTrigger Programador de tareas , propiedad RandomDelay
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc3bfec997b50a1f9d802191387a2186576532ca027e1086fc311b31f0da5d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139478"
---
# <a name="dailytriggerrandomdelay-property"></a>DailyTrigger.RandomDelay, propiedad

Para el scripting, obtiene o establece una hora de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.

## <a name="syntax"></a>Syntax


```VB
DailyTrigger.RandomDelay As String
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

[**DailyTrigger**](dailytrigger.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





