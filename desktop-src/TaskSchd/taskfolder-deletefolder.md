---
title: TaskFolder. DeleteFolder, método
description: En el caso de scripting, elimina una subcarpeta de la carpeta principal.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Método DeleteFolder Programador de tareas
- Método DeleteFolder Programador de tareas, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, método DeleteFolder
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea9b8aaa7da7710cedc49e10d6be2a203f62b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491374"
---
# <a name="taskfolderdeletefolder-method"></a>TaskFolder. DeleteFolder, método

En el caso de scripting, elimina una subcarpeta de la carpeta principal.

## <a name="syntax"></a>Sintaxis


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombrecarpeta* \[ de\]
</dt> <dd>

Nombre de la subcarpeta que se va a quitar. La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \) . Este parámetro puede ser una ruta de acceso relativa a la carpeta que desea eliminar. Un ejemplo de una ruta de carpeta de tareas, en la carpeta de tareas raíz, es \\ MyTaskFolder. No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. ' no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

</dd> <dt>

*marcas* \[ de de\]
</dt> <dd>

No se admite.

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

[**TaskFolder**](taskfolder.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





