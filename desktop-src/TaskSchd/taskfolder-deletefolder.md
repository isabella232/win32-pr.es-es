---
title: Método TaskFolder.DeleteFolder
description: Para el scripting, elimina una subcarpeta de la carpeta primaria.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Método DeleteFolder Programador de tareas
- Método DeleteFolder Programador de tareas , objeto TaskFolder
- TaskFolder object Programador de tareas , DeleteFolder (método)
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
ms.openlocfilehash: 31080f017329cde376b646befd4b7e12ba02926b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387044"
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

Nombre de la subcarpeta que se va a quitar. La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \\ ). Este parámetro puede ser una ruta de acceso relativa a la carpeta que desea eliminar. Un ejemplo de una ruta de acceso de carpeta de tareas, en la carpeta de tareas raíz, \\ es MyTaskFolder. No se puede usar el carácter '.' para especificar la carpeta de tareas actual y '..'. no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

</dd> <dt>

*flags* \[ En\]
</dt> <dd>

No compatible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskFolder**](taskfolder.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





