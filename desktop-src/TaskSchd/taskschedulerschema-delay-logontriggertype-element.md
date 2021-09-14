---
title: Elemento Delay (logonTriggerType)
description: Cantidad de tiempo entre el momento en que el usuario inicia sesión y el momento en que se inicia la tarea.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
keywords:
- Delay, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a820bad3d68cfb0a697f795a9fd7326c9e52abe9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073409"
---
# <a name="delay-logontriggertype-element"></a>Elemento Delay (logonTriggerType)

Cantidad de tiempo entre el momento en que el usuario inicia sesión y el momento en que se inicia la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). Para obtener más información sobre el tipo de duración, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

El tipo complejo [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) define el elemento **Delay.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                       | Derivado de                                                                 | Descripción                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el retraso del desencadenador de inicio de sesión se especifica mediante la [**propiedad LogonTrigger.Delay.**](logontrigger-delay.md)

Para el desarrollo de C++, el identificador de usuario para el desencadenador logon se especifica mediante la [**propiedad ILogonTrigger::D elay.**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





