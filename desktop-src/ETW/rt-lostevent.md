---
description: Esta clase de tipo de evento se usa para indicar que los eventos se han perdido en una sesión en tiempo real. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: RT_LostEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541870"
---
# <a name="rt_lostevent-class"></a>RT \_ LostEvent (clase)

Esta clase de tipo de evento se usa para indicar que los eventos se han perdido en una sesión en tiempo real.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a>Miembros

La clase **RT \_ LostEvent** no define ningún miembro.

## <a name="remarks"></a>Observaciones

El tipo de evento RTLostEvent indica que se han perdido uno o varios eventos. El tipo de evento RTLostBuffer indica que se han perdido uno o más búferes. Los tipos de eventos RTLostEvent y RTLostBuffer se entregan antes de procesar los eventos del búfer.

RTLostFile indica que se perdió el archivo de copia de seguridad utilizado por el registrador automático para capturar eventos.

Perder eventos depende de la frecuencia con la que se registran los eventos y de cuánto tiempo dedica el consumidor a procesar los eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Evento perdido**](lost-event.md)
</dt> </dl>

 

 




