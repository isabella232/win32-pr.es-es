---
title: Propiedad TaskSettings. StopIfGoingOnBatteries
description: En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea se detendrá si el equipo pasa a baterías.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Programador de tareas de la propiedad StopIfGoingOnBatteries
- Programador de tareas de la propiedad StopIfGoingOnBatteries, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aced436d653b6bbc02b4b36edea9046e3ac62392
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492245"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a>Propiedad TaskSettings. StopIfGoingOnBatteries

En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea se detendrá si el equipo pasa a baterías.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Un valor booleano que indica que la tarea se detendrá si el equipo pasa a baterías. Si es true, la propiedad indica que la tarea se detendrá si el equipo pasa a baterías. Si es false, la propiedad indica que la tarea no se detendrá si el equipo pasa a baterías. El valor predeterminado es True. Vea la sección Comentarios para obtener más detalles.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) del esquema de programador de tareas.

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

 

 





