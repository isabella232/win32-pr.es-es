---
title: Propiedad SessionStateChangeTrigger.Delay
description: Para el scripting, obtiene o establece un valor que indica cuánto tiempo tiene lugar un retraso antes de que se inicia una tarea después de que se detecte un cambio de estado de sesión de Terminal Server.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Retraso de la propiedad Programador de tareas
- Propiedad Delay Programador de tareas , objeto SessionStateChangeTrigger
- Objeto SessionStateChangeTrigger Programador de tareas , propiedad Delay
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26767aeca55af5ae208791f42b5973fa38df507a84f08f3d2d1fe8db28965b52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139358"
---
# <a name="sessionstatechangetriggerdelay-property"></a>Propiedad SessionStateChangeTrigger.Delay

Para el scripting, obtiene o establece un valor que indica cuánto tiempo tiene lugar un retraso antes de que se inicia una tarea después de que se detecte un cambio de estado de sesión de Terminal Server. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="syntax"></a>Syntax


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a>Valor de propiedad

Retraso que tiene lugar antes de que se inicia una tarea después de detectar un cambio de estado de sesión de Terminal Server.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





