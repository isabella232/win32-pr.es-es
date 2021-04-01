---
title: RegisteredTask. GetSecurityDescriptor, método
description: En el caso de scripting, obtiene el descriptor de seguridad que se usa como credenciales para la tarea registrada.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- Método GetSecurityDescriptor Programador de tareas
- Método GetSecurityDescriptor Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método GetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996852"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a>RegisteredTask. GetSecurityDescriptor, método

En el caso de scripting, obtiene el descriptor de seguridad que se usa como credenciales para la tarea registrada.

## <a name="syntax"></a>Sintaxis


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*securityInformation* 
</dt> <dd>

Información de seguridad de [**la \_ información de seguridad**](/windows/desktop/SecAuthZ/security-information).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Descriptor de seguridad de la tarea registrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

