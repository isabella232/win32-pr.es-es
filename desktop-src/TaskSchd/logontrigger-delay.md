---
title: Propiedad LogonTrigger.Delay
description: Para el scripting, obtiene o establece un valor que indica la cantidad de tiempo entre el momento en que el usuario inicia sesión y el momento en que se inicia la tarea.
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- Retraso de la propiedad Programador de tareas
- Propiedad Delay Programador de tareas , objeto LogonTrigger
- Objeto LogonTrigger Programador de tareas , propiedad Delay
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073431"
---
# <a name="logontriggerdelay-property"></a>Propiedad LogonTrigger.Delay

Para el scripting, obtiene o establece un valor que indica la cantidad de tiempo entre el momento en que el usuario inicia sesión y el momento en que se inicia la tarea.

## <a name="syntax"></a>Sintaxis


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a>Valor de propiedad

Valor que indica la cantidad de tiempo entre el momento en que el usuario inicia sesión y el momento en que se inicia la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el retraso del desencadenador de inicio de sesión se especifica mediante el elemento [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) del esquema Programador de tareas inicio de sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogonTrigger**](logontrigger.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





