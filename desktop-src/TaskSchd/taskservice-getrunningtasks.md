---
title: Método TaskService.GetRunningTasks
description: Para el scripting, obtiene una colección de tareas en ejecución.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- Método GetRunningTasks Programador de tareas
- Método GetRunningTasks Programador de tareas , objeto TaskService
- Objeto TaskService Programador de tareas , método GetRunningTasks
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891468"
---
# <a name="taskservicegetrunningtasks-method"></a>Método TaskService.GetRunningTasks

Para el scripting, obtiene una colección de tareas en ejecución.

> [!Note]  
> **TaskService.GetRunningTasks** solo devolverá una colección de tareas en ejecución que se ejecutan en el contexto de seguridad de un usuario o debajo de él. Por ejemplo, para los miembros del grupo Administradores, **GetRunningTasks** devolverá una colección de todas las tareas en ejecución, pero para los miembros del grupo Usuarios, **GetRunningTasks** solo devolverá una colección de tareas que se ejecutan en el contexto de seguridad del grupo Usuarios.

 

## <a name="syntax"></a>Sintaxis


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flags* \[ En\]
</dt> <dd>

Pase 1 para devolver todas las tareas en ejecución, incluidas las tareas ocultas. Pase 0 para devolver una colección de tareas en ejecución que no son tareas ocultas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**RunningTaskCollection**](runningtaskcollection.md) que contiene las tareas que se están ejecutando actualmente.

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

 

 





