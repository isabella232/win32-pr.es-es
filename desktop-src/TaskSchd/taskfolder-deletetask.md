---
title: TaskFolder. DeleteTask, método
description: En el caso de scripting, elimina una tarea de la carpeta.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- Método DeleteTask Programador de tareas
- Método DeleteTask Programador de tareas, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, método DeleteTask
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802780"
---
# <a name="taskfolderdeletetask-method"></a>TaskFolder. DeleteTask, método

En el caso de scripting, elimina una tarea de la carpeta.

## <a name="syntax"></a>Sintaxis


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ de de\]
</dt> <dd>

El nombre de la tarea que se especifica cuando se registró la tarea. No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. ' no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

</dd> <dt>

*marcas* \[ de de\]
</dt> <dd>

No se admite. El valor es 0

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
</dt> </dl>

 

 





