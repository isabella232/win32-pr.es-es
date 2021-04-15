---
title: Propiedad DailyTrigger. DaysInterval
description: En el caso de scripting, obtiene o establece el intervalo entre los días de la programación.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Programador de tareas de la propiedad DaysInterval
- Programador de tareas de la propiedad DaysInterval, objeto DailyTrigger
- Programador de tareas de objeto DailyTrigger, propiedad DaysInterval
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534300"
---
# <a name="dailytriggerdaysinterval-property"></a>Propiedad DailyTrigger. DaysInterval

En el caso de scripting, obtiene o establece el intervalo entre los días de la programación.

## <a name="syntax"></a>Sintaxis


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Valor de propiedad

Intervalo entre los días de la programación.

## <a name="remarks"></a>Observaciones

Un intervalo de 1 genera una programación diaria. Un intervalo de 2 genera una programación de todos los días.

Al leer o escribir su propio XML para una tarea, el intervalo de una programación diaria se especifica mediante el elemento [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) del esquema de programador de tareas.

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
</dt> <dt>

[**DailyTrigger**](dailytrigger.md)
</dt> </dl>

 

 





