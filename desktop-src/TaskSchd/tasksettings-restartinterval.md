---
title: Propiedad TaskSettings. RestartInterval
description: En el caso de scripting, obtiene o establece un valor que especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Programador de tareas de la propiedad RestartInterval
- Programador de tareas de la propiedad RestartInterval, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad RestartInterval
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f511e43ebb1d61fd80f2fcab34aba092704b8338
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801466"
---
# <a name="tasksettingsrestartinterval-property"></a>Propiedad TaskSettings. RestartInterval

En el caso de scripting, obtiene o establece un valor que especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Valor de propiedad

Valor que especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea. Si se establece esta propiedad, también se debe establecer la propiedad [**RestartCount**](tasksettings-restartcount.md) . El formato de esta cadena es P <days> DT <hours> H <minutes> M <seconds> S (por ejemplo, "PT5M" es de 5 minutos, "PT1H" es 1 hora y "PT20M" es de 20 minutos). El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es 1 minuto.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) del esquema de programador de tareas.

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

 

 





