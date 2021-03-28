---
description: Esta clase es la clase primaria para los eventos de llamada a procedimiento local avanzados. La siguiente sintaxis se simplifica desde el código MOF.
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984523"
---
# <a name="alpc-class"></a>ALPC (clase)

Esta clase es la clase primaria para los eventos de llamada a procedimiento local avanzados.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **ALPC** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar los eventos de llamada a procedimiento local avanzado en una sesión de registro del kernel de NT, especifique la marca de **seguimiento de eventos \_ \_ \_ ALPC** en el miembro **EnableFlags** de una estructura de propiedades de [**\_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos ALPC llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ALPCGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Use los siguientes tipos de eventos para identificar el evento ALPC real al consumir eventos.



| Tipo de evento           | Descripción                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor del tipo de evento, 33 | Enviar evento de mensaje. La clase MOF de [**\_ envío de \_ mensaje ALPC**](alpc-send-message.md) define los datos de evento para este evento.                           |
| Valor del tipo de evento, 34 | Evento Receive Message. La clase MOF de [**\_ recepción de \_ mensajes ALPC**](alpc-receive-message.md) define los datos de evento para este evento.                  |
| Valor del tipo de evento, 35 | Evento wait for reply. La clase del MOF [**\_ Wait \_ for \_ reply de ALPC**](alpc-wait-for-reply.md) define los datos de evento para este evento.                    |
| Valor del tipo de evento, 36 | Esperar un nuevo evento de mensaje. La clase MOF [**\_ Wait \_ for \_ New \_ Message**](alpc-wait-for-new-message.md) mof define los datos de evento para este evento. |
| Valor del tipo de evento, 37 | Detener evento en espera. La clase de MOF [**\_ unwait de ALPC**](alpc-unwait.md) define los datos de evento para este evento.                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

