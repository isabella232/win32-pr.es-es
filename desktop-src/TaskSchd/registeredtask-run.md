---
title: RegisteredTask. Run (método)
description: En el caso de scripting, ejecuta la tarea registrada inmediatamente.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Ejecutar método Programador de tareas
- Método Run Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, Run (método)
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
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686127"
---
# <a name="registeredtaskrun-method"></a>RegisteredTask. Run (método)

En el caso de scripting, ejecuta la tarea registrada inmediatamente.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
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

*ppRunningTask* \[ enuncia\]
</dt> <dd>

Objeto [**RunningTask**](runningtask.md) que define la nueva instancia de la tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **RegisteredTask. Run** es equivalente a la función [**RegisteredTask. RunEx**](registeredtask-runex.md) con el parámetro flags igual a 0 y no se ha especificado ningún valor para el parámetro user.

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

 

 





