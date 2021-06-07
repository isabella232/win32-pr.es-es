---
title: Propiedad TaskFolder.GetTask
description: Para el scripting, obtiene una tarea en una ubicación especificada de una carpeta.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Propiedad GetTask Programador de tareas
- Propiedad GetTask Programador de tareas , objeto TaskFolder
- Objeto TaskFolder Programador de tareas , propiedad GetTask
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
ms.openlocfilehash: b697b8fa2d0715dcf0282c5f32490bfccec79fec
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387681"
---
# <a name="taskfoldergettask-property"></a>Propiedad TaskFolder.GetTask

Para el scripting, obtiene una tarea en una ubicación especificada de una carpeta.

## <a name="syntax"></a>Sintaxis


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso (ubicación) a la tarea en una carpeta. La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \\ ). Un ejemplo de una ruta de acceso de carpeta de tareas, en la carpeta de tareas raíz, \\ es MyTaskFolder. El carácter "." no se puede usar para especificar la carpeta de tareas actual y "..". no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

## <a name="error-codes"></a>Códigos de error

Tarea en la ubicación especificada. La tarea es un [**objeto RegisteredTask.**](registeredtask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





