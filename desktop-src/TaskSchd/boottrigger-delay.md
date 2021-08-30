---
title: Propiedad BootTrigger.Delay
description: Para el scripting, obtiene o establece un valor que indica la cantidad de tiempo entre el momento en que se inicia el sistema y el momento en que se inicia la tarea.
ms.assetid: 4e1c4e6f-640a-4e7d-8197-914c58cfae90
keywords:
- Propiedad Delay Programador de tareas
- Propiedad Delay Programador de tareas , objeto BootTrigger
- Objeto BootTrigger Programador de tareas , propiedad Delay
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
ms.openlocfilehash: e286ce75fbcfab03f7e46cb6b58fda52343e3b9643f5d9eb462807d67b9c32c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034075"
---
# <a name="boottriggerdelay-property"></a>Propiedad BootTrigger.Delay

Para el scripting, obtiene o establece un valor que indica la cantidad de tiempo entre el momento en que se inicia el sistema y el momento en que se inicia la tarea.

## <a name="syntax"></a>Syntax


```VB
BootTrigger.Delay As String
```



## <a name="property-value"></a>Valor de propiedad

Valor que indica la cantidad de tiempo entre el momento en que se inicia el sistema y el momento en que se inicia la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="remarks"></a>Comentarios

Al leer o escribir su propio XML para una tarea, el retraso de arranque se especifica mediante el elemento [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) del Programador de tareas esquema.

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

[**BootTrigger**](boottrigger.md)
</dt> </dl>

 

 





