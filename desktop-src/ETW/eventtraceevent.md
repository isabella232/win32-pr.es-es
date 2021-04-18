---
description: Clase primaria para los eventos de encabezado de registro. Esta clase siempre es la primera clase de seguimiento de eventos que se envía a un consumidor (este evento no se envía a los consumidores en tiempo real). La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: Clase EventTraceEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984495"
---
# <a name="eventtraceevent-class"></a>Clase EventTraceEvent

Clase primaria para los eventos de encabezado de registro. Esta clase siempre es la primera clase de seguimiento de eventos que se envía a un consumidor (este evento no se envía a los consumidores en tiempo real).

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **EventTraceEvent** no define ningún miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_Encabezado eventtracer**](eventtrace-header.md)
</dt> </dl>

 

 




