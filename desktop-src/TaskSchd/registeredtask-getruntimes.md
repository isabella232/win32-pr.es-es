---
title: RegisteredTask. GetRunTimes, método
description: En el caso de scripting, obtiene las veces que la tarea registrada está programada para ejecutarse durante un período de tiempo especificado.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Método GetRunTimes Programador de tareas
- Método GetRunTimes Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método GetRunTimes
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c15aba82c5515578a3c58a485e47718d09176483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534888"
---
# <a name="registeredtaskgetruntimes-method"></a>RegisteredTask. GetRunTimes, método

En el caso de scripting, obtiene las veces que la tarea registrada está programada para ejecutarse durante un período de tiempo especificado.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Inicio* \[ de de\]
</dt> <dd>

La hora de inicio de la consulta.

</dd> <dt>

*fin* \[ de de\]
</dt> <dd>

La hora de finalización de la consulta.

</dd> <dt>

*recuento* \[ enuncia\]
</dt> <dd>

El número de horas programadas que se ejecutará la tarea.

</dd> <dt>

*rgstTaskTimes* \[ enuncia\]
</dt> <dd>

Las horas programadas en las que se ejecutará la tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la tarea registrada contiene desencadenadores que se deshabilitan de forma individual, estos desencadenadores todavía afectarán a la siguiente hora de ejecución programada que se devuelva aunque estén deshabilitados.

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

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





