---
title: Propiedad IdleSettings. IdleDuration
description: En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo que el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Programador de tareas de la propiedad IdleDuration
- Programador de tareas de la propiedad IdleDuration, objeto IdleSettings
- Programador de tareas de objeto IdleSettings, propiedad IdleDuration
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6eeed4fef540b3a9e13d0f52e3ce1934cb9e220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802990"
---
# <a name="idlesettingsidleduration-property"></a>Propiedad IdleSettings. IdleDuration

En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo que el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea.

## <a name="syntax"></a>Sintaxis


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a>Valor de propiedad

Valor que indica la cantidad de tiempo que el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). El valor mínimo es un minuto. Si este valor es **null**, el retraso se establecerá en el valor predeterminado de 10 minutos.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) del esquema de programador de tareas.

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

 

 





