---
title: Elemento Delay (bootTriggerType)
description: Especifica la cantidad de tiempo entre el momento en que se inicia el sistema y el momento en que se inicia la tarea.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
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
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073413"
---
# <a name="delay-boottriggertype-element"></a>Elemento Delay (bootTriggerType)

Especifica la cantidad de tiempo entre el momento en que se inicia el sistema y el momento en que se inicia la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). Para obtener más información sobre el tipo de duración, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

El tipo complejo [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) define el elemento **Delay.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                     | Derivado de                                                               | Descripción                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando se arranca el sistema.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, la propiedad [**BootTrigger.Delay**](boottrigger-delay.md) especifica el retraso del desencadenador de eventos.

Para el desarrollo de C++, la propiedad [**IBootTrigger::D elay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) especifica el retraso del desencadenador de eventos.

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

 

 





