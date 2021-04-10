---
title: Propiedad TaskFolder. SetSecurityDescriptor
description: Para el scripting, establece el descriptor de seguridad de la carpeta.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- Programador de tareas de la propiedad SetSecurityDescriptor
- Programador de tareas de la propiedad SetSecurityDescriptor, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, propiedad SetSecurityDescriptor
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
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996159"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a>Propiedad TaskFolder. SetSecurityDescriptor

Para el scripting, establece el descriptor de seguridad de la carpeta.

## <a name="syntax"></a>Sintaxis


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Puede especificar la lista de control de acceso (ACL) en el descriptor de seguridad para una carpeta de tareas con el fin de permitir o denegar el acceso de determinados usuarios y grupos a una carpeta de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





