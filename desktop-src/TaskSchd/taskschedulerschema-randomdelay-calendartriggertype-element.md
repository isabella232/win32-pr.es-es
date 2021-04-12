---
title: Elemento RandomDelay (calendarTriggerType)
description: Contiene el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. | Elemento RandomDelay (calendarTriggerType)
ms.assetid: 497fab4e-ad63-43e6-a086-2d77b43662d9
keywords:
- Programador de tareas del elemento RandomDelay
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d71149bfeceeb6c17cafa27f56bb15bb184ead06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362275"
---
# <a name="randomdelay-calendartriggertype-element"></a>Elemento RandomDelay (calendarTriggerType)

Contiene el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

El elemento **RandomDelay** se define mediante el tipo complejo de [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                            | Derivado de                                                                       | Descripción                                                                                 |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**CalendarTrigger (triggerGroup)**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





