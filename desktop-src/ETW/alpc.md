---
description: Esta clase es la clase primaria para eventos de llamada a procedimientos locales avanzados. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: ALPC (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 435b55c44f06b6be062653a45e14a1a890e026371d8bd8e649c87ce3542118c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070295"
---
# <a name="alpc-class"></a>ALPC (clase)

Esta clase es la clase primaria para eventos de llamada a procedimientos locales avanzados.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase ALPC** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar eventos de llamada a procedimientos locales avanzados en una sesión de registro del kernel de NT, especifique la marca **\_ EVENT TRACE FLAG \_ \_ ALPC** en el miembro **EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos ALPC llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ALPCGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid.* Use los siguientes tipos de eventos para identificar el evento ALPC real al consumir eventos.



| Tipo de evento           | Descripción                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor de tipo de evento, 33 | Evento de envío de mensajes. La [**clase MOF ALPC \_ Send \_ Message**](alpc-send-message.md) define los datos del evento para este evento.                           |
| Valor de tipo de evento, 34 | Evento de recepción de mensajes. La [**clase ALPC \_ Receive \_ Message**](alpc-receive-message.md) MOF define los datos de evento para este evento.                  |
| Valor de tipo de evento, 35 | Espere el evento de respuesta. La [**clase ALPC \_ Wait For \_ \_ Reply**](alpc-wait-for-reply.md) MOF define los datos de evento para este evento.                    |
| Valor de tipo de evento, 36 | Espere a que se produce un nuevo evento de mensaje. La [**clase MOF ALPC \_ Wait For New \_ \_ \_ Message**](alpc-wait-for-new-message.md) define los datos de evento para este evento. |
| Valor de tipo de evento, 37 | Detenga el evento en espera. La [**clase MOF ALPC \_ Unwait**](alpc-unwait.md) define los datos de evento para este evento.                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

