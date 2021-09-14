---
title: Propiedad TaskSettings.StopIfGoingOnBatteries
description: Para el scripting, obtiene o establece un valor booleano que indica que la tarea se detendrán si el equipo se pone en baterías.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Propiedad StopIfGoingOnBatteries Programador de tareas
- Propiedad StopIfGoingOnBatteries Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad StopIfGoingOnBatteries
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160601"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a>Propiedad TaskSettings.StopIfGoingOnBatteries

Para el scripting, obtiene o establece un valor booleano que indica que la tarea se detendrán si el equipo se pone en baterías.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Valor booleano que indica que la tarea se detendrán si el equipo va a usar baterías. Si es True, la propiedad indica que la tarea se detendrán si el equipo va a usar baterías. Si es False, la propiedad indica que la tarea no se detendrán si el equipo va a usar baterías. El valor predeterminado es True. Consulte Comentarios para obtener más detalles.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) del esquema Programador de tareas datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





