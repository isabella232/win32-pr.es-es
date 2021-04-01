---
title: Propiedad TaskFolder. GetTask
description: En el caso de scripting, obtiene una tarea en una ubicación especificada de una carpeta.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Programador de tareas de la propiedad GetTask
- Programador de tareas de la propiedad GetTask, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, propiedad GetTask
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e813538cfcb995949cbe1fb8ec6a3b0d7772061c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801598"
---
# <a name="taskfoldergettask-property"></a>Propiedad TaskFolder. GetTask

En el caso de scripting, obtiene una tarea en una ubicación especificada de una carpeta.

## <a name="syntax"></a>Sintaxis


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a>Valor de propiedad

La ruta de acceso (ubicación) de la tarea en una carpeta. La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \) . Un ejemplo de una ruta de carpeta de tareas, en la carpeta de tareas raíz, es \\ MyTaskFolder. No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. ' no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

## <a name="error-codes"></a>Códigos de error

Tarea que se encuentra en la ubicación especificada. La tarea es un objeto [**RegisteredTask**](registeredtask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





