---
title: Propiedad TaskFolder. GetSecurityDescriptor
description: En el caso de scripting, obtiene el descriptor de seguridad de la carpeta.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- Programador de tareas de la propiedad GetSecurityDescriptor
- Programador de tareas de la propiedad GetSecurityDescriptor, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, propiedad GetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686105"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a>Propiedad TaskFolder. GetSecurityDescriptor

En el caso de scripting, obtiene el descriptor de seguridad de la carpeta.

## <a name="syntax"></a>Sintaxis


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskFolder.SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





