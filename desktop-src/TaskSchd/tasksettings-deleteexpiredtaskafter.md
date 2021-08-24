---
title: Propiedad TaskSettings.DeleteExpiredTaskAfter
description: Para el scripting, obtiene o establece la cantidad de tiempo que el Programador de tareas esperará antes de eliminar la tarea después de que expire.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Propiedad DeleteExpiredTaskAfter Programador de tareas
- Propiedad DeleteExpiredTaskAfter Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521f07a5712165c282a36bbfe2c3b66769239c53d652ae49a03fa6a50c19cb05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658455"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a>Propiedad TaskSettings.DeleteExpiredTaskAfter

Para el scripting, obtiene o establece la cantidad de tiempo que el Programador de tareas esperará antes de eliminar la tarea después de que expire. Si no se especifica ningún valor para esta propiedad, el Programador de tareas no eliminará la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena que obtiene o establece la cantidad de tiempo que el Programador de tareas esperará antes de eliminar la tarea después de que expire. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="remarks"></a>Comentarios

Una tarea expira después de que se haya superado el límite final para todos los desencadenadores asociados a la tarea. El límite final de un desencadenador se especifica mediante la [propiedad EndBoundary](trigger-endboundary.md) heredada por todos los objetos de desencadenador.

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





