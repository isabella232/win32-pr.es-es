---
title: RegisteredTask. GetInstances, método
description: En el caso de scripting, devuelve todas las instancias de la tarea registrada actualmente en ejecución.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Método GetInstances Programador de tareas
- Método GetInstances Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método GetInstances
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150807"
---
# <a name="registeredtaskgetinstances-method"></a>RegisteredTask. GetInstances, método

En el caso de scripting, devuelve todas las instancias de la tarea registrada actualmente en ejecución.

> [!Note]  
> **RegisteredTask. GetInstances** solo devolverá las instancias de la tarea registrada actualmente en ejecución que se ejecutan en el contexto de seguridad de un usuario o debajo de él. Por ejemplo, para los miembros del grupo administradores, **GetInstances** devolverá todas las instancias de la tarea registrada actualmente en ejecución, pero para los miembros del grupo usuarios, **GetInstances** solo devolverá las instancias de la tarea registrada actualmente en ejecución que se ejecutan en el contexto de seguridad del grupo usuarios.

 

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

Este parámetro se reserva para uso futuro y debe establecerse en 0.

</dd> <dt>

*runningTasks* \[ enuncia\]
</dt> <dd>

Un objeto [**RunningTaskCollection**](runningtaskcollection.md) que contiene todas las instancias de la tarea que se están ejecutando actualmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

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

 

 





