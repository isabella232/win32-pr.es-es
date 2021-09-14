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
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172830"
---
# <a name="runningtaskenginepid-property"></a>Propiedad RunningTask.EnginePID

Para el scripting, obtiene el identificador de proceso para el motor (proceso) que ejecuta la tarea.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>Valor de propiedad

Identificador de proceso del motor que ejecuta la tarea.

## <a name="remarks"></a>Observaciones

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



 

