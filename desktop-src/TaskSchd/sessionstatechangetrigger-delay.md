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
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886524"
---
# <a name="sessionstatechangetriggerdelay-property"></a>Propiedad SessionStateChangeTrigger.Delay

Para el scripting, obtiene o establece un valor que indica cuánto tiempo tiene lugar un retraso antes de que se inicia una tarea después de que se detecte un cambio de estado de sesión de Terminal Server. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="syntax"></a>Sintaxis


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



 

 





