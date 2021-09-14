---
title: Método RegisteredTask.SetSecurityDescriptor
description: Para el scripting, establece el descriptor de seguridad que se usa como credenciales para la tarea registrada.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Método SetSecurityDescriptor Programador de tareas
- Método SetSecurityDescriptor Programador de tareas , objeto RegisteredTask
- RegisteredTask object Programador de tareas , SetSecurityDescriptor method
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172965"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a>Método RegisteredTask.SetSecurityDescriptor

Para el scripting, establece el descriptor de seguridad que se usa como credenciales para la tarea registrada.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sddl* \[ En\]
</dt> <dd>

Descriptor de seguridad que se usa como credenciales para la tarea registrada.

> [!Note]  
> Si a la cuenta del sistema local se le deniega el acceso a una tarea, Programador de tareas servicio puede producir resultados inesperados.

 

</dd> <dt>

*flags* \[ En\]
</dt> <dd>

Marcas que especifican cómo establecer el descriptor de seguridad. Se puede \_ especificar la marca TASK DONT ADD PRINCIPAL ACE \_ \_ (0x10) de la \_ [**enumeración TASK \_ CREATION.**](/windows/desktop/api/taskschd/ne-taskschd-task_creation)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Puede especificar la lista de control de acceso (ACL) en el descriptor de seguridad de una tarea para permitir o denegar el acceso de determinados usuarios y grupos a una tarea.

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

 

 





