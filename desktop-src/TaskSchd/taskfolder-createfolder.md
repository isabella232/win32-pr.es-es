---
title: Método TaskFolder.CreateFolder
description: Para el scripting, crea una carpeta para las tareas relacionadas.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- Método CreateFolder Programador de tareas
- Método CreateFolder Programador de tareas , objeto TaskFolder
- Objeto TaskFolder Programador de tareas , método CreateFolder
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5de913ccf98ee8369430425e423813168c083cbde737b5831917a5ee594e1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759025"
---
# <a name="taskfoldercreatefolder-method"></a>Método TaskFolder.CreateFolder

Para el scripting, crea una carpeta para las tareas relacionadas.

## <a name="syntax"></a>Sintaxis


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*folderName* \[ En\]
</dt> <dd>

Nombre que se usa para identificar la carpeta. Si se especifica "FolderName \\ SubFolder1 SubFolder2", se creará el árbol de carpetas completo si las carpetas \\ no existen. Este parámetro puede ser una ruta de acceso relativa a la instancia [**actual de TaskFolder.**](taskfolder.md) La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \\ ). Un ejemplo de una ruta de acceso de carpeta de tareas, en la carpeta de tareas raíz, \\ es MyTaskFolder. El carácter "." no se puede usar para especificar la carpeta de tareas actual y "..". no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

</dd> <dt>

*sddl* \[ En\]
</dt> <dd>

Descriptor de seguridad asociado a la carpeta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**TaskFolder**](taskfolder.md) que representa la nueva subcarpeta.

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
</dt> </dl>

 

 





