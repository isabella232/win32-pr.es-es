---
title: IdleSettings.IdleDuration, propiedad
description: Para el scripting, obtiene o establece un valor que indica la cantidad de tiempo que el equipo debe estar en estado inactivo antes de que se ejecute la tarea.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Propiedad IdleDuration Programador de tareas
- Propiedad IdleDuration Programador de tareas , objeto IdleSettings
- Objeto IdleSettings Programador de tareas propiedad , IdleDuration
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
ms.openlocfilehash: 30a78210202579d517410a2d82f1c5566d947f1ceb76cbd92538a0266b7b81ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002443"
---
# <a name="idlesettingsidleduration-property"></a>IdleSettings.IdleDuration, propiedad

Para el scripting, obtiene o establece un valor que indica la cantidad de tiempo que el equipo debe estar en estado inactivo antes de que se ejecute la tarea.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a>Valor de propiedad

Valor que indica la cantidad de tiempo que el equipo debe estar en estado inactivo antes de que se ejecute la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). El valor mínimo es un minuto. Si este valor es **NULL,** el retraso se establecerá en el valor predeterminado de 10 minutos.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) del Programador de tareas esquema.

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

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





