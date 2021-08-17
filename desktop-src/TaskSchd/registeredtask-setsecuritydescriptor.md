---
title: Método RegisteredTask.SetSecurityDescriptor
description: Para el scripting, establece el descriptor de seguridad que se usa como credenciales para la tarea registrada.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Método SetSecurityDescriptor Programador de tareas
- Método SetSecurityDescriptor Programador de tareas , objeto RegisteredTask
- Objeto RegisteredTask Programador de tareas , método SetSecurityDescriptor
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
ms.openlocfilehash: c7ac6845624ab2032b9b90d742c1346081c3ba4719d0814cfd257d3787c2bf70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759596"
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
> Si se deniega el acceso a una tarea a la cuenta del sistema local, el Programador de tareas servicio puede producir resultados inesperados.

 

</dd> <dt>

*flags* \[ En\]
</dt> <dd>

Marcas que especifican cómo establecer el descriptor de seguridad. Se puede \_ especificar la marca TASK DONT ADD PRINCIPAL ACE (0x10) de la \_ \_ \_ [**enumeración TASK \_ CREATION.**](/windows/desktop/api/taskschd/ne-taskschd-task_creation)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

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

 

 





