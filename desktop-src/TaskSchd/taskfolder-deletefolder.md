---
title: Método TaskFolder.DeleteFolder
description: Para el scripting, elimina una subcarpeta de la carpeta primaria.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Método DeleteFolder Programador de tareas
- Método DeleteFolder Programador de tareas , objeto TaskFolder
- Objeto TaskFolder Programador de tareas método , DeleteFolder
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
ms.openlocfilehash: a73dfe168b599de6e09d5437d0be4ec7a851d246f9fcbce0f79f662b62c56212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974905"
---
# <a name="taskfolderdeletefolder-method"></a>Método TaskFolder.DeleteFolder

Para el scripting, elimina una subcarpeta de la carpeta primaria.

## <a name="syntax"></a>Sintaxis


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*folderName* \[ En\]
</dt> <dd>

Nombre de la subcarpeta que se va a quitar. La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \\ ). Este parámetro puede ser una ruta de acceso relativa a la carpeta que desea eliminar. Un ejemplo de una ruta de acceso de carpeta de tareas, en la carpeta de tareas raíz, \\ es MyTaskFolder. El carácter "." no se puede usar para especificar la carpeta de tareas actual y "..". no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

</dd> <dt>

*flags* \[ En\]
</dt> <dd>

No compatible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskFolder**](taskfolder.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





