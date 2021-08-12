---
title: Elemento RandomDelay (timeTriggerType)
description: Contiene el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. | Elemento RandomDelay (timeTriggerType)
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- Elemento RandomDelay Programador de tareas
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c4c9fde8a0f88ed7e87b5a0d3ccc252f141f6b677f535adf853ef0aca9499b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611512"
---
# <a name="randomdelay-timetriggertype-element"></a>Elemento RandomDelay (timeTriggerType)

Contiene el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). Para obtener más información sobre el tipo de duración, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

El elemento se define mediante el [**tipo complejo timeTriggerType.**](taskschedulerschema-timetriggertype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                    | Derivado de                                                               | Descripción                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**TimeTrigger (triggerGroup)**](taskschedulerschema-timetrigger-triggergroup-element.md) | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, [**vea RandomDelay Property of ITimeTrigger ( Propiedad RandomDelay de ITimeTrigger).**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay)

Para el desarrollo de scripts, [**consulte TimeTrigger.RandomDelay.**](timetrigger-randomdelay.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





