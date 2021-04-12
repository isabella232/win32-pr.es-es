---
title: RegistrationTrigger. Delay (propiedad)
description: En el caso de scripting, obtiene o establece la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Propiedad Delay Programador de tareas
- Propiedad Delay Programador de tareas, objeto RegistrationTrigger
- Programador de tareas de objeto RegistrationTrigger, propiedad Delay
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534989"
---
# <a name="registrationtriggerdelay-property"></a>RegistrationTrigger. Delay (propiedad)

En el caso de scripting, obtiene o establece la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="syntax"></a>Sintaxis


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a>Valor de propiedad

La cantidad de tiempo entre el momento en que se registra el sistema y el momento en que se inicia la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el retraso de arranque se especifica mediante el elemento [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) del esquema de programador de tareas.

Si se registra una tarea con un desencadenador de registro retrasado y el equipo en el que se ha registrado la tarea se cierra o se reinicia durante el retraso, antes de que se ejecute la tarea, la tarea no se ejecutará y se perderá el retraso.

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
</dt> </dl>

 

 





