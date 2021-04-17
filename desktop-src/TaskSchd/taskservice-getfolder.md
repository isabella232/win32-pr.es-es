---
title: TaskService. GetFolder, método
description: En el caso de scripting, obtiene una carpeta de tareas registradas.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- GetFolder (método) Programador de tareas
- Método GetFolder Programador de tareas, objeto TaskService
- Programador de tareas de objeto TaskService, método GetFolder
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74504e9cad124f8cbc9ec23e896ba4dec7d7f50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676989"
---
# <a name="taskservicegetfolder-method"></a>TaskService. GetFolder, método

En el caso de scripting, obtiene una carpeta de tareas registradas.

## <a name="syntax"></a>Sintaxis


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ruta de acceso* \[ de\]
</dt> <dd>

Ruta de acceso a la carpeta que se va a recuperar. No use una barra diagonal inversa después del nombre de la última carpeta en la ruta de acceso. La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \) . Un ejemplo de una ruta de carpeta de tareas, en la carpeta de tareas raíz, es \\ MyTaskFolder. No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. ' no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**TaskFolder**](taskfolder.md) para la carpeta solicitada.

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

 

 





