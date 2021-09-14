---
title: Método RegisteredTask.GetSecurityDescriptor
description: Para el scripting, obtiene el descriptor de seguridad que se usa como credenciales para la tarea registrada.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- Método GetSecurityDescriptor Programador de tareas
- Método GetSecurityDescriptor Programador de tareas , objeto RegisteredTask
- Objeto RegisteredTask Programador de tareas método , GetSecurityDescriptor
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172997"
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

 

