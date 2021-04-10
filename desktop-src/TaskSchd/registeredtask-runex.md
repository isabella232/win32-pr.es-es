---
title: RegisteredTask. RunEx, método
description: En el caso de scripting, ejecuta la tarea registrada de inmediato usando las marcas especificadas y un identificador de sesión.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- Método RunEx Programador de tareas
- Método RunEx Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método RunEx
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150613"
---
# <a name="registeredtaskrunex-method"></a>RegisteredTask. RunEx, método

En el caso de scripting, ejecuta la tarea registrada de inmediato usando las marcas especificadas y un identificador de sesión.

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

*parámetros* \[ de\]
</dt> <dd>

Los parámetros usados como valores en las acciones de la tarea. Para no especificar ningún valor de parámetro para las acciones de tarea, establezca este parámetro en **Nothing**. De lo contrario, se puede especificar un valor de cadena único o una matriz de valores de cadena.

Los valores de cadena que especifique se emparejan con los nombres y se almacenan como pares de nombre y valor. Si especifica un valor de cadena único, Arg0 será el nombre asignado al valor. El valor se puede usar en la acción de tarea donde se usa la variable $ (Arg0) en las propiedades de acción.

Si pasa valores como "0", "100" y "250" como una matriz de valores de cadena, "0" reemplazará las variables $ (Arg0), "100" reemplazará las variables $ (arg1) y "250" reemplazará las variables $ (arg2) utilizadas en las propiedades de la acción.

Se puede especificar un máximo de 32 valores de cadena.

Para obtener más información y una lista de las propiedades de acción que pueden usar las variables $ (Arg0), $ (arg1),..., $ (Arg32) en sus valores, vea [acciones de tarea](task-actions.md).

</dd> <dt>

*marcas* \[ de de\]
</dt> <dd>

Una constante de [ \_ \_ marcadores de ejecución de tareas](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) que define cómo se ejecuta la tarea.

</dd> <dt>

*SessionID* \[ de\]
</dt> <dd>

La sesión de Terminal Server en la que desea iniciar la tarea.

Si la ejecución de la tarea \_ \_ usar la \_ \_ constante de ID. de sesión (0x4) no se pasa al parámetro *Flags* , se omite el valor especificado en este parámetro. Si la ejecución de la tarea \_ \_ usar el \_ ID. de sesión \_ se pasa al parámetro *Flags* y el valor de SessionID es menor o igual que 0, se devolverá un error de argumento no válido.

Si la ejecución de la tarea \_ \_ usar el \_ ID. de sesión \_ se pasa al parámetro *Flags* y el valor de SessionID es un identificador de sesión válido mayor que 0 y no se especifica ningún valor para el parámetro *User* , el servicio Programador de tareas intentará iniciar la tarea interactivamente como el usuario que ha iniciado sesión en la sesión especificada.

Si la ejecución de la tarea \_ \_ usar el \_ ID. de sesión \_ se pasa al parámetro *Flags* y el valor SessionID es un identificador de sesión válido mayor que 0 y se especifica un usuario en el parámetro *User* , el servicio Programador de tareas intentará iniciar la tarea interactivamente como el usuario especificado en el parámetro *User* .

</dd> <dt>

*runningTask* \[ enuncia\]
</dt> <dd>

Objeto [**RunningTask**](runningtask.md) que define la nueva instancia de la tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método devolverá sin errores, pero la tarea no se ejecutará si la propiedad [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) se establece en false para la tarea registrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





