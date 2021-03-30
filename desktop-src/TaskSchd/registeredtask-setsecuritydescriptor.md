---
title: RegisteredTask. SetSecurityDescriptor, método
description: En el caso de scripting, establece el descriptor de seguridad que se usa como credenciales para la tarea registrada.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Método SetSecurityDescriptor Programador de tareas
- Método SetSecurityDescriptor Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método SetSecurityDescriptor
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150954"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a>RegisteredTask. SetSecurityDescriptor, método

En el caso de scripting, establece el descriptor de seguridad que se usa como credenciales para la tarea registrada.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SDDL* \[ de\]
</dt> <dd>

Descriptor de seguridad que se usa como credenciales para la tarea registrada.

> [!Note]  
> Si se deniega el acceso a la cuenta de sistema local a una tarea, el servicio de Programador de tareas puede generar resultados inesperados.

 

</dd> <dt>

*marcas* \[ de de\]
</dt> <dd>

Marcas que especifican cómo establecer el descriptor de seguridad. \_ \_ Se puede especificar la tarea no agregar \_ \_ marca de ACE principal (0x10) de la enumeración de [**\_ creación de tareas**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Puede especificar la lista de control de acceso (ACL) en el descriptor de seguridad de una tarea con el fin de permitir o denegar el acceso de determinados usuarios y grupos a una tarea.

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

 

 





