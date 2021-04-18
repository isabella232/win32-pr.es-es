---
title: TaskFolder. CreateFolder, método
description: En el caso de los scripts, crea una carpeta para las tareas relacionadas.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- CreateFolder (método) Programador de tareas
- Método CreateFolder Programador de tareas, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, CreateFolder (método)
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
ms.openlocfilehash: 1ae66dadb0c943b1ca33be3e696ac1c8ca7d6234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676829"
---
# <a name="taskfoldercreatefolder-method"></a>TaskFolder. CreateFolder, método

En el caso de los scripts, crea una carpeta para las tareas relacionadas.

## <a name="syntax"></a>Sintaxis


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombrecarpeta* \[ de\]
</dt> <dd>

Nombre que se usa para identificar la carpeta. Si \\ se especifica "NombreCarpeta subcarpeta subfolder1 \\ SubFolder2", se creará el árbol de carpetas completo si las carpetas no existen. Este parámetro puede ser una ruta de acceso relativa a la instancia de [**TaskFolder**](taskfolder.md) actual. La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \) . Un ejemplo de una ruta de carpeta de tareas, en la carpeta de tareas raíz, es \\ MyTaskFolder. No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. ' no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

</dd> <dt>

*SDDL* \[ de\]
</dt> <dd>

Descriptor de seguridad asociado a la carpeta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**TaskFolder**](taskfolder.md) que representa la nueva subcarpeta.

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

 

 





