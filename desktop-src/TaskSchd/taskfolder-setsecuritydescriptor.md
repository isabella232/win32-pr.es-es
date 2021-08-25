---
title: Propiedad TaskFolder.SetSecurityDescriptor
description: Para el scripting, establece el descriptor de seguridad de la carpeta.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- Propiedad SetSecurityDescriptor Programador de tareas
- Propiedad SetSecurityDescriptor Programador de tareas , objeto TaskFolder
- Objeto TaskFolder Programador de tareas , propiedad SetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8416e14a5415de86f8ad3f4a1181ce231ecfbdc875e36e9e3fd14014de8c4935
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033795"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a>Propiedad TaskFolder.SetSecurityDescriptor

Para el scripting, establece el descriptor de seguridad de la carpeta.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Puede especificar la lista de control de acceso (ACL) en el descriptor de seguridad de una carpeta de tareas para permitir o denegar el acceso de determinados usuarios y grupos a una carpeta de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**TaskFolder.GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





