---
description: Esta clase de tipo de evento se usa para indicar que los eventos se perdieron en una sesión en tiempo real. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: RT_LostEvent clase
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
ms.openlocfilehash: d0944b843c8deb38012242111b6c5057ccf7cb8557c69caefe9a87283d2ae418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328745"
---
# <a name="rt_lostevent-class"></a>RT \_ LostEvent (clase)

Esta clase de tipo de evento se usa para indicar que los eventos se perdieron en una sesión en tiempo real.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a>Miembros

La **clase \_ RT LostEvent** no define ningún miembro.

## <a name="remarks"></a>Comentarios

El tipo de evento RTLostEvent indica que se perdieron uno o varios eventos. El tipo de evento RTLostBuffer indica que se perdieron uno o varios búferes. Los tipos de eventos RTLostEvent y RTLostBuffer se entregan antes de procesar eventos desde el búfer.

RTLostFile indica que se perdió el archivo de respaldo utilizado por AutoLogger para capturar eventos.

La pérdida de eventos depende de la frecuencia con la que se registran los eventos y de cuánto tiempo dedica el consumidor a procesar los eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                      |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Evento \_ perdido**](lost-event.md)
</dt> </dl>

 

 




