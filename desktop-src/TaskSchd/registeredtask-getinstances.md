---
title: Método RegisteredTask.GetInstances
description: Para el scripting, devuelve todas las instancias en ejecución de la tarea registrada.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Método GetInstances Programador de tareas
- Método GetInstances Programador de tareas , objeto RegisteredTask
- Método RegisteredTask Programador de tareas , GetInstances
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f9224922e70242304423950a67bf4acd866d1a551a90f4c9a6dadb94470ba1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126065"
---
# <a name="registeredtaskgetinstances-method"></a>Método RegisteredTask.GetInstances

Para el scripting, devuelve todas las instancias en ejecución de la tarea registrada.

> [!Note]  
> **RegisteredTask.GetInstances** solo devolverá instancias de la tarea registrada que se está ejecutando actualmente en o por debajo del contexto de seguridad de un usuario. Por ejemplo, para los miembros del grupo Administradores, **GetInstances** devolverá todas las instancias de la tarea registrada que se está ejecutando actualmente, pero para los miembros del grupo Usuarios, **GetInstances** solo devolverá instancias de la tarea registrada que se está ejecutando actualmente en el contexto de seguridad del grupo Usuarios.

 

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flags* 
</dt> <dd>

Este parámetro está reservado para uso futuro y debe establecerse en 0.

</dd> <dt>

*runningTasks* \[ out\]
</dt> <dd>

Objeto [**RunningTaskCollection**](runningtaskcollection.md) que contiene todas las instancias en ejecución de la tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

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

 

 





