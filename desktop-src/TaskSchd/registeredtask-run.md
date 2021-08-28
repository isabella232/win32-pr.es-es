---
title: Método RegisteredTask.Run
description: Para el scripting, ejecuta la tarea registrada inmediatamente.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Ejecutar método Programador de tareas
- Ejecutar método Programador de tareas , objeto RegisteredTask
- RegisteredTask object Programador de tareas , Run method
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e747688ba80c08a39b0336fda126ae7d85a558f53c97aab230bc5d3d0113b360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681625"
---
# <a name="registeredtaskrun-method"></a>Método RegisteredTask.Run

Para el scripting, ejecuta la tarea registrada inmediatamente.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*params* \[ En\]
</dt> <dd>

Parámetros utilizados como valores en las acciones de tarea. Para no especificar ningún valor de parámetro para las acciones de tarea, establezca este parámetro en **Nothing**. De lo contrario, se puede especificar un valor de cadena único o una matriz de valores de cadena.

Los valores de cadena que especifique se emparejan con nombres y se almacenan como pares nombre-valor. Si especifica un valor de cadena único, Arg0 será el nombre asignado al valor. El valor se puede usar en la acción de tarea donde se usa la variable $(Arg0) en las propiedades de acción.

Si pasa valores como "0", "100" y "250" como una matriz de valores de cadena, "0" reemplazará las variables $(Arg0), "100" reemplazará a las variables $(Arg1) y "250" reemplazará las variables $(Arg2) usadas en las propiedades de acción.

Se puede especificar un máximo de 32 valores de cadena.

Para obtener más información y una lista de las propiedades de acción que pueden usar las variables $(Arg0), $(Arg1), ..., $(Arg32) en sus valores, vea Acciones de [tarea](task-actions.md).

</dd> <dt>

*ppRunningTask* \[ out\]
</dt> <dd>

Objeto [**RunningTask**](runningtask.md) que define la nueva instancia de la tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función RegisteredTask.Run** es equivalente a la [**función RegisteredTask.RunEx**](registeredtask-runex.md) con el parámetro flags igual a 0 y nada especificado para el parámetro de usuario.

Este método devolverá sin errores, pero la tarea no se ejecutará si la propiedad [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) está establecida en false para la tarea registrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





