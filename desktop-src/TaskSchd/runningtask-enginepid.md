---
title: Propiedad RunningTask. EnginePID
description: En el caso de scripting, obtiene el identificador de proceso del motor (proceso) que está ejecutando la tarea.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Programador de tareas de la propiedad EnginePID
- Programador de tareas de la propiedad EnginePID, objeto RunningTask
- Programador de tareas de objeto RunningTask, propiedad EnginePID
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676830"
---
# <a name="runningtaskenginepid-property"></a>Propiedad RunningTask. EnginePID

En el caso de scripting, obtiene el identificador de proceso del motor (proceso) que está ejecutando la tarea.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>Valor de propiedad

IDENTIFICADOR de proceso del motor que ejecuta la tarea.

## <a name="remarks"></a>Observaciones

El ID. de proceso devuelto por esta propiedad no se puede anexar directamente a una cadena. El valor devuelto debe convertirse primero en un valor entero mediante una llamada a la función [cint](/previous-versions//fctcwhw9(v=vs.85)) en el valor devuelto.


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

