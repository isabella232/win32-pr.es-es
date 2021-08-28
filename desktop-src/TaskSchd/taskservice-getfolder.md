---
title: Método TaskService.GetFolder
description: Para el scripting, obtiene una carpeta de tareas registradas.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Método GetFolder Programador de tareas
- Método GetFolder Programador de tareas , objeto TaskService
- Objeto TaskService Programador de tareas , método GetFolder
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
ms.openlocfilehash: 632595e462abd5d6bba5c2e91ebcd590f4ec9a7289092eaf56626e4586691be3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072435"
---
# <a name="taskservicegetfolder-method"></a>Método TaskService.GetFolder

Para el scripting, obtiene una carpeta de tareas registradas.

## <a name="syntax"></a>Sintaxis


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ruta de acceso* \[ En\]
</dt> <dd>

Ruta de acceso a la carpeta que se va a recuperar. No use una barra diagonal inversa después del nombre de la última carpeta en la ruta de acceso. La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \\ ). Un ejemplo de una ruta de acceso de carpeta de tareas, en la carpeta de tareas raíz, \\ es MyTaskFolder. El carácter "." no se puede usar para especificar la carpeta de tareas actual y "..". no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**TaskFolder**](taskfolder.md) para la carpeta solicitada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





