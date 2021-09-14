---
title: Método RegisteredTask.Stop
description: Para el scripting, detiene la tarea registrada inmediatamente.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Detener método Programador de tareas
- Método Stop Programador de tareas , objeto RegisteredTask
- RegisteredTask object Programador de tareas , Stop (Método)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172954"
---
# <a name="registeredtaskstop-method"></a>Método RegisteredTask.Stop

Para el scripting, detiene la tarea registrada inmediatamente.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flags* \[ En\]
</dt> <dd>

Reservado. Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función RegisteredTask.Stop** detiene todas las instancias de la tarea.

Los usuarios de la cuenta del sistema pueden detener una tarea, los usuarios con privilegios de grupo administrador pueden detener una tarea y, si un usuario tiene derechos para ejecutar y leer una tarea, el usuario puede detener la tarea. Un usuario puede detener las instancias de tarea que se ejecutan con las mismas credenciales que la cuenta de usuario. En todos los demás casos, se deniega al usuario el acceso para detener la tarea.

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
</dt> </dl>

 

 





