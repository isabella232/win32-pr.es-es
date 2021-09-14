---
title: Método RegisteredTask.RunEx
description: Para el scripting, ejecuta la tarea registrada inmediatamente con marcas especificadas y un identificador de sesión.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- Método RunEx Programador de tareas
- Método RunEx Programador de tareas , objeto RegisteredTask
- RegisteredTask object Programador de tareas , runEx (método)
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172970"
---
# <a name="registeredtaskrunex-method"></a>Método RegisteredTask.RunEx

Para el scripting, ejecuta la tarea registrada inmediatamente con marcas especificadas y un identificador de sesión.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*params* \[ En\]
</dt> <dd>

Parámetros utilizados como valores en las acciones de tarea. Para no especificar ningún valor de parámetro para las acciones de tarea, establezca este parámetro en **Nothing**. De lo contrario, se puede especificar un valor de cadena único o una matriz de valores de cadena.

Los valores de cadena que especifique se emparejan con nombres y se almacenan como pares nombre-valor. Si especifica un valor de cadena único, Arg0 será el nombre asignado al valor. El valor se puede usar en la acción de tarea donde se usa la variable $(Arg0) en las propiedades de acción.

Si pasa valores como "0", "100" y "250" como una matriz de valores de cadena, "0" reemplazará las variables $(Arg0), "100" reemplazará las variables $(Arg1) y "250" reemplazará las variables $(Arg2) usadas en las propiedades de acción.

Se puede especificar un máximo de 32 valores de cadena.

Para obtener más información y una lista de las propiedades de acción que pueden usar $(Arg0), $(Arg1), ..., $(Arg32) variables en sus valores, vea Acciones de [tarea](task-actions.md).

</dd> <dt>

*flags* \[ En\]
</dt> <dd>

Constante [TASK \_ RUN \_ FLAGS](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) que define cómo se ejecuta la tarea.

</dd> <dt>

*sessionID* \[ En\]
</dt> <dd>

Sesión de terminal Server en la que desea iniciar la tarea.

Si la constante TASK RUN USE SESSION ID (0x4) no se pasa al parámetro \_ \_ \_ \_ *flags,* se omite el valor especificado en este parámetro. Si la constante TASK RUN USE SESSION ID se pasa al parámetro flags y el valor de sessionID es menor o igual que \_ \_ \_ \_ 0,  se devolverá un error de argumento no válido.

Si la constante TASK RUN USE SESSION ID se pasa al parámetro flags y el valor sessionID es un identificador de sesión válido mayor que 0 y si no se especifica ningún valor para el parámetro de usuario, el servicio Programador de tareas intentará iniciar la tarea de forma interactiva como el usuario que ha iniciado sesión en la \_ \_ sesión \_ \_ especificada.  

Si la constante TASK RUN USE SESSION ID se pasa al parámetro flags y el valor de sessionID es un identificador de sesión válido mayor que 0 y si se especifica un usuario en el parámetro de usuario, el servicio Programador de tareas intentará iniciar la tarea de forma interactiva como el usuario especificado en el parámetro \_ \_ \_ \_  *de* usuario. 

</dd> <dt>

*runningTask* \[ out\]
</dt> <dd>

Objeto [**RunningTask**](runningtask.md) que define la nueva instancia de la tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método devolverá sin errores, pero la tarea no se ejecutará si la propiedad [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) está establecida en false para la tarea registrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





