---
title: Método RegisteredTask.GetInstances
description: Para el scripting, devuelve todas las instancias que se están ejecutando actualmente de la tarea registrada.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Método GetInstances Programador de tareas
- Método GetInstances Programador de tareas , objeto RegisteredTask
- Objeto RegisteredTask Programador de tareas método , GetInstances
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
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173002"
---
# <a name="registeredtaskgetinstances-method"></a>Método RegisteredTask.GetInstances

Para el scripting, devuelve todas las instancias que se están ejecutando actualmente de la tarea registrada.

> [!Note]  
> **RegisteredTask.GetInstances** solo devolverá instancias de la tarea registrada que se está ejecutando actualmente y que se ejecutan en el contexto de seguridad de un usuario o debajo de él. Por ejemplo, para los miembros del grupo Administradores, **GetInstances** devolverá todas las instancias de la tarea registrada actualmente en ejecución, pero para los miembros del grupo Usuarios, **GetInstances** solo devolverá instancias de la tarea registrada que se está ejecutando actualmente en el contexto de seguridad del grupo Usuarios.

 

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

Objeto [**RunningTaskCollection que**](runningtaskcollection.md) contiene todas las instancias en ejecución de la tarea.

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

 

 





