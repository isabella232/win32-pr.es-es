---
title: Propiedad principal. nivel
description: En el caso de scripting, obtiene o establece el identificador que se usa para especificar el nivel de privilegios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Programador de tareas de la propiedad nivel
- Propiedad nivel Programador de tareas, objeto principal
- Programador de tareas de objeto principal, propiedad nivel
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534293"
---
# <a name="principalrunlevel-property"></a>Propiedad principal. nivel

En el caso de scripting, obtiene o establece el identificador que se usa para especificar el nivel de privilegios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a>Valor de propiedad

El identificador que se usa para especificar el nivel de privilegios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.



| Value                                                                                                                                                                                                                                         | Significado                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <dt>**Tarea \_ de NIVEL \_ Lua**</dt> <dt>0</dt> </dl>             | Las tareas se ejecutarán con los privilegios mínimos (LUA).<br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <dt>**Tarea \_ de NIVEL \_ más alto**</dt> <dt>1</dt> </dl> | Las tareas se ejecutarán con los privilegios más altos.<br/>     |



 

## <a name="remarks"></a>Observaciones

Si una tarea se registra mediante la cuenta de \\ Administrador de Builtin o las cuentas de sistema local o de servicio local, se omitirá la propiedad **nivel** . También se omitirá el valor de propiedad si el control de cuentas de usuario (UAC) está desactivado.

Si una tarea se registra mediante el grupo de administradores para el contexto de seguridad de la tarea, también debe establecer la propiedad [**nivel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) en la **tarea \_ nivel \_ más alta** si desea ejecutar la tarea. Para obtener más información, vea [contextos de seguridad para tareas](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Principal**](principal.md)
</dt> </dl>

 

 





