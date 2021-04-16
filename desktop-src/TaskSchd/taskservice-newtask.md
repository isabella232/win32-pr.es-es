---
title: TaskService. NewTask, método
description: En el caso de scripting, devuelve un objeto de definición de tarea vacía que se rellenará con la configuración y las propiedades y, a continuación, se registrará mediante el método TaskFolder. RegisterTaskDefinition.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Método NewTask Programador de tareas
- Método NewTask Programador de tareas, objeto TaskService
- Programador de tareas objeto TaskService, NewTask (método)
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686218"
---
# <a name="taskservicenewtask-method"></a>TaskService. NewTask, método

En el caso de scripting, devuelve un objeto de definición de tarea vacía que se rellenará con la configuración y las propiedades y, a continuación, se registrará mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .

## <a name="syntax"></a>Sintaxis


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*marcas* \[ de de\]
</dt> <dd>

Este parámetro se reserva para uso futuro y debe establecerse en 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La definición de tarea que especifica toda la información necesaria para crear una nueva tarea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





