---
title: Método TaskService.NewTask
description: Para el scripting, devuelve un objeto de definición de tarea vacío que se va a rellenar con valores y propiedades y, a continuación, se registra mediante el método TaskFolder.RegisterTaskDefinition.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Método NewTask Programador de tareas
- Método NewTask Programador de tareas , objeto TaskService
- Objeto TaskService Programador de tareas método , NewTask
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
ms.openlocfilehash: e22da6f62f59bf24ded0eed9dea21e3a1a9d1c3e7ecc36fb6f425f58124aee71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990935"
---
# <a name="taskservicenewtask-method"></a>Método TaskService.NewTask

Para el scripting, devuelve un objeto de definición de tarea vacío que se va a rellenar con valores y propiedades y, a continuación, se registra mediante el [**método TaskFolder.RegisterTaskDefinition.**](taskfolder-registertaskdefinition.md)

## <a name="syntax"></a>Sintaxis


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flags* \[ En\]
</dt> <dd>

Este parámetro está reservado para uso futuro y debe establecerse en 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Definición de tarea que especifica toda la información necesaria para crear una nueva tarea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





