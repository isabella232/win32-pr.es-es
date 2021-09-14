---
title: Principal.RunLevel, propiedad
description: Para el scripting, obtiene o establece el identificador que se usa para especificar el nivel de privilegios necesario para ejecutar las tareas asociadas a la entidad de seguridad.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Propiedad RunLevel Programador de tareas
- Propiedad RunLevel Programador de tareas , objeto Principal
- Objeto principal Programador de tareas , propiedad RunLevel
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173029"
---
# <a name="principalrunlevel-property"></a>Principal.RunLevel, propiedad

Para el scripting, obtiene o establece el identificador que se usa para especificar el nivel de privilegios necesario para ejecutar las tareas asociadas a la entidad de seguridad.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a>Valor de propiedad

Identificador que se usa para especificar el nivel de privilegio necesario para ejecutar las tareas asociadas a la entidad de seguridad.



| Value                                                                                                                                                                                                                                         | Significado                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <dt>**TASK \_ RUNLEVEL \_ LUA**</dt> <dt>0</dt> </dl>             | Las tareas se ejecutarán con los privilegios mínimos (LUA).<br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <dt>**TASK \_ RUNLEVEL \_ HIGHEST**</dt> <dt>1</dt> </dl> | Las tareas se ejecutarán con los privilegios más altos.<br/>     |



 

## <a name="remarks"></a>Observaciones

Si una tarea se registra mediante la cuenta de administrador integrada o las cuentas de sistema local o servicio local, se omitirá la propiedad \\ **RunLevel.** El valor de propiedad también se omitirá si el Control de cuentas de usuario (UAC) está desactivado.

Si una tarea se registra mediante el grupo Administradores para el contexto de seguridad de la tarea, también debe establecer la propiedad [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) en **TASK \_ RUNLEVEL \_ HIGHEST** si desea ejecutar la tarea. Para obtener más información, vea [Contextos de seguridad para tareas](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Principal**](principal.md)
</dt> </dl>

 

 





