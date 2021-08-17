---
title: Propiedad RunningTask.EnginePID
description: Para el scripting, obtiene el identificador de proceso para el motor (proceso) que ejecuta la tarea.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Propiedad EnginePID Programador de tareas
- Propiedad EnginePID Programador de tareas , objeto RunningTask
- Objeto RunningTask Programador de tareas , propiedad EnginePID
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed259ccc92e954ae1acde076f0cc09167d15071ea71a33039e7298479875b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759079"
---
# <a name="runningtaskenginepid-property"></a>Propiedad RunningTask.EnginePID

Para el scripting, obtiene el identificador de proceso para el motor (proceso) que ejecuta la tarea.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>Valor de propiedad

Identificador de proceso para el motor que ejecuta la tarea.

## <a name="remarks"></a>Comentarios

El identificador de proceso devuelto por esta propiedad no se puede anexar directamente a una cadena. El valor devuelto debe convertirse primero en un valor entero llamando a la [función CInt](/previous-versions//fctcwhw9(v=vs.85)) en el valor devuelto.


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

