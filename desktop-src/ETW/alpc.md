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
ms.openlocfilehash: 2a4b09a8bab9280de8fb4c91368f5d6d93f7944a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063167"
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

## <a name="members"></a>Members

La **clase ALPC** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar eventos de llamada a procedimientos locales avanzados en una sesión de registro del kernel de NT, especifique la marca **\_ \_ \_ ALPC EVENT TRACE FLAG** en el miembro **EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos ALPC llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y [**especificando ALPCGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid.* Use los siguientes tipos de eventos para identificar el evento ALPC real al consumir eventos.



| Tipo de evento           | Descripción                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor del tipo de evento, 33 | Enviar evento de mensaje. La [**clase ALPC \_ Send \_ Message**](alpc-send-message.md) MOF define los datos de evento para este evento.                           |
| Valor del tipo de evento, 34 | Evento de recepción de mensajes. La [**clase ALPC \_ Receive \_ Message**](alpc-receive-message.md) MOF define los datos de evento para este evento.                  |
| Valor de tipo de evento, 35 | Espere al evento de respuesta. La [**clase ALPC \_ Wait For \_ \_ Reply**](alpc-wait-for-reply.md) MOF define los datos de evento para este evento.                    |
| Valor de tipo de evento, 36 | Espere a un nuevo evento de mensaje. La [**clase ALPC \_ Wait For \_ New \_ \_ Message**](alpc-wait-for-new-message.md) MOF define los datos de evento para este evento. |
| Valor de tipo de evento, 37 | Detener el evento de espera. La [**clase MOF ALPC \_ Unwait**](alpc-unwait.md) define los datos de evento para este evento.                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

