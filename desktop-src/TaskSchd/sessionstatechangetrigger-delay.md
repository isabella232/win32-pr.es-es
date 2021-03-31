---
title: SessionStateChangeTrigger. Delay (propiedad)
description: En el caso de scripting, obtiene o establece un valor que indica cuánto tiempo se produce un retraso antes de que se inicie una tarea después de que se detecte un cambio de estado de sesión Terminal Server.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Propiedad Delay Programador de tareas
- Propiedad Delay Programador de tareas, objeto SessionStateChangeTrigger
- Programador de tareas de objeto SessionStateChangeTrigger, propiedad Delay
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150048"
---
# <a name="sessionstatechangetriggerdelay-property"></a>SessionStateChangeTrigger. Delay (propiedad)

En el caso de scripting, obtiene o establece un valor que indica cuánto tiempo se produce un retraso antes de que se inicie una tarea después de que se detecte un cambio de estado de sesión Terminal Server. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="syntax"></a>Sintaxis


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a>Valor de propiedad

Retraso que tiene lugar antes de que se inicie una tarea después de que se detecte un cambio de estado de sesión Terminal Server.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





