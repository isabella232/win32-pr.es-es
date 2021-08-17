---
title: Método RegisteredTask.GetRunTimes
description: Para el scripting, obtiene las horas a las que está programada la ejecución de la tarea registrada durante un tiempo especificado.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Método GetRunTimes Programador de tareas
- Método GetRunTimes Programador de tareas , objeto RegisteredTask
- Objeto RegisteredTask Programador de tareas método , GetRunTimes
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
ms.openlocfilehash: 303dd08c576f31946207241b086fe945b3f1ac275c596496139d19f507670e30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759670"
---
# <a name="registeredtaskgetruntimes-method"></a>Método RegisteredTask.GetRunTimes

Para el scripting, obtiene las horas a las que está programada la ejecución de la tarea registrada durante un tiempo especificado.

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

*begin* \[ En\]
</dt> <dd>

Hora de inicio de la consulta.

</dd> <dt>

*end* \[ En\]
</dt> <dd>

Hora de finalización de la consulta.

</dd> <dt>

*count* \[ out\]
</dt> <dd>

Número de veces programadas que se ejecutará la tarea.

</dd> <dt>

*rgstTaskTimes* \[ out\]
</dt> <dd>

Las horas programadas que se ejecutará la tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si la tarea registrada contiene desencadenadores que están deshabilitados individualmente, estos desencadenadores seguirán afectando al siguiente tiempo de ejecución programado que se devuelve aunque estén deshabilitados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





