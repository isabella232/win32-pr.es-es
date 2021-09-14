---
title: RegistrationTrigger.Delay, propiedad
description: Para el scripting, obtiene o establece la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Retraso de la propiedad Programador de tareas
- Propiedad Delay Programador de tareas , objeto RegistrationTrigger
- Objeto RegistrationTrigger Programador de tareas , propiedad Delay
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172878"
---
# <a name="registrationtriggerdelay-property"></a>RegistrationTrigger.Delay, propiedad

Para el scripting, obtiene o establece la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="syntax"></a>Sintaxis


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a>Valor de propiedad

Cantidad de tiempo entre el momento en que se registra el sistema y el momento en que se inicia la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el retraso de arranque se especifica mediante el [**elemento Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) del Programador de tareas esquema.

Si se registra una tarea con un desencadenador de registro retrasado y el equipo en el que está registrada la tarea se apaga o se reinicia durante el retraso, antes de que se ejecute la tarea, la tarea no se ejecutará y se perderá el retraso.

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
</dt> </dl>

 

 





