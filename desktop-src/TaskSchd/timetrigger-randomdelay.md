---
title: TimeTrigger.RandomDelay, propiedad
description: Para el scripting, obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. | TimeTrigger.RandomDelay, propiedad
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- Propiedades de RandomDelay Programador de tareas
- Propiedad RandomDelay Programador de tareas , objeto TimeTrigger
- Objeto TimeTrigger Programador de tareas , propiedad RandomDelay
topic_type:
- apiref
api_name:
- TimeTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdbe297ace4fd34c2b5bf88db132e0573afd208052b50331ab571881b85831f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354767"
---
# <a name="timetriggerrandomdelay-property"></a>TimeTrigger.RandomDelay, propiedad

Para el scripting, obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.

## <a name="syntax"></a>Syntax


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valor de propiedad

Tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





