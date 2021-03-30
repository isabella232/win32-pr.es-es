---
title: RegisteredTask. STOP (método)
description: En el caso de scripting, detiene la tarea registrada inmediatamente.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Detener método Programador de tareas
- Método STOP Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método STOP
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422577"
---
# <a name="registeredtaskstop-method"></a>RegisteredTask. STOP (método)

En el caso de scripting, detiene la tarea registrada inmediatamente.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*marcas* \[ de de\]
</dt> <dd>

Reservado. Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **RegisteredTask. Stop** detiene todas las instancias de la tarea.

Los usuarios de la cuenta del sistema pueden detener una tarea, los usuarios con privilegios de grupo de administradores pueden detener una tarea y, si un usuario tiene derechos para ejecutar y leer una tarea, el usuario puede detener la tarea. Un usuario puede detener las instancias de tarea que se ejecutan con las mismas credenciales que la cuenta de usuario. En todos los demás casos, se deniega el acceso al usuario para detener la tarea.

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
</dt> </dl>

 

 





