---
title: BootTrigger. Delay (propiedad)
description: En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo entre el momento en que se arranca el sistema y el momento en que se inicia la tarea.
ms.assetid: 4e1c4e6f-640a-4e7d-8197-914c58cfae90
keywords:
- Propiedad Delay Programador de tareas
- Propiedad Delay Programador de tareas, objeto BootTrigger
- Programador de tareas de objeto BootTrigger, propiedad Delay
topic_type:
- apiref
api_name:
- BootTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6be91f00b79f2c2a47235a389b82ffb9255d586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150615"
---
# <a name="boottriggerdelay-property"></a>BootTrigger. Delay (propiedad)

En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo entre el momento en que se arranca el sistema y el momento en que se inicia la tarea.

## <a name="syntax"></a>Sintaxis


```VB
BootTrigger.Delay As String
```



## <a name="property-value"></a>Valor de propiedad

Valor que indica la cantidad de tiempo entre el momento en que se arranca el sistema y el momento en que se inicia la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="remarks"></a>Observaciones

Al leer o escribir su propio XML para una tarea, el retraso de arranque se especifica mediante el elemento [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) del esquema de programador de tareas.

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

[**BootTrigger**](boottrigger.md)
</dt> </dl>

 

 





