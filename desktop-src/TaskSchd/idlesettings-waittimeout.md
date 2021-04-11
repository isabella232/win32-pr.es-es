---
title: Propiedad IdleSettings. WaitTimeout
description: En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- Programador de tareas de la propiedad WaitTimeout
- Programador de tareas de la propiedad WaitTimeout, objeto IdleSettings
- Programador de tareas de objeto IdleSettings, propiedad WaitTimeout
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079474"
---
# <a name="idlesettingswaittimeout-property"></a>Propiedad IdleSettings. WaitTimeout

En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad. Si no se especifica ningún valor para esta propiedad, el servicio Programador de tareas esperará indefinidamente a que se produzca una condición de inactividad.

## <a name="syntax"></a>Sintaxis


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a>Valor de propiedad

Valor que indica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). El tiempo mínimo permitido es 1 minuto. Si este valor es **null**, el retraso se establecerá en el valor predeterminado de 1 hora.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) del esquema de programador de tareas.

Si una tarea se desencadena mediante un desencadenador inactivo, se omite la propiedad **IdleSettings. WaitTimeout** .

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

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





