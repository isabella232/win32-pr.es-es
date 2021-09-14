---
title: Elemento Delay (sessionStateChangeTriggerType)
description: Contiene un valor que indica la longitud de retraso de una hora de inicio de una tarea, cuando se detecta un cambio de estado de sesión de Terminal Server.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
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
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073406"
---
# <a name="delay-sessionstatechangetriggertype-element"></a>Elemento Delay (sessionStateChangeTriggerType)

Contiene un valor que indica la longitud de retraso de una hora de inicio de una tarea, cuando se detecta un cambio de estado de sesión de Terminal Server. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). Para obtener más información sobre el tipo de duración, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

El tipo complejo [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) define el elemento **Delay.**

## <a name="parent-element"></a>Elemento primario



| Elemento                       | Derivado de                                                                                           | Descripción                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando una sesión de Terminal Server cambia de estado. <br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el retraso del desencadenador de cambio de estado de sesión se especifica mediante la [**propiedad SessionStateChangeTrigger.Delay.**](sessionstatechangetrigger-delay.md)

Para el desarrollo de C++, el retraso del desencadenador de cambio de estado de sesión se especifica mediante la [**propiedad Delay de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





