---
title: Método RegisteredTask.GetSecurityDescriptor
description: Para el scripting, obtiene el descriptor de seguridad que se usa como credenciales para la tarea registrada.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- Método GetSecurityDescriptor Programador de tareas
- Método GetSecurityDescriptor Programador de tareas , objeto RegisteredTask
- RegisteredTask object Programador de tareas , GetSecurityDescriptor (método)
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
ms.openlocfilehash: a832413f6d5373a07a7201341d3b412843f3c8eba3414326eeaa8316a9caedd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118859134"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a>Método RegisteredTask.GetSecurityDescriptor

Para el scripting, obtiene el descriptor de seguridad que se usa como credenciales para la tarea registrada.

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

La información de seguridad de [**SECURITY \_ INFORMATION**](/windows/desktop/SecAuthZ/security-information).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Descriptor de seguridad de la tarea registrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder.GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

