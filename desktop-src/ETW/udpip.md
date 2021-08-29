---
description: 'Clase UdpIp: esta clase es la clase primaria para eventos UDP/IP. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: UdpIp (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: a240b1cda5e9b25aeea15241b066bfe7cb9a583778043a5aee79faab69b2f75c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069355"
---
# <a name="udpip-class"></a>UdpIp (clase)

Esta clase es la clase primaria para los eventos UDP/IP.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase UdpIp** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar eventos UDP/IP en una sesión de registro del kernel de NT, especifique la marca **\_ \_ \_ \_ TCPIP EVENT TRACE FLAG NETWORK** en el miembro **EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos UDP/IP llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**UdpIpGuid**](nt-kernel-logger-constants.md) como *parámetro pGuid.* Use los siguientes tipos de eventos para identificar el evento de red (UDP/IP) real al consumir eventos.



| Tipo de evento                                                         | Descripción                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ RECEIVE**(el valor del tipo de evento es 11)<br/> | Evento de recepción para el protocolo IPv4. La [**clase MOF \_ UdpIp TypeGroup1**](udpip-typegroup1.md) define los datos de evento para este evento. |
| **EVENT \_ TRACE \_ TYPE \_ SEND**(el valor del tipo de evento es 10)<br/>    | Envío de eventos para el protocolo IPv4. La [**clase MOF \_ UdpIp TypeGroup1**](udpip-typegroup1.md) define los datos de evento para este evento.    |
| Valor de tipo de evento, 17                                               | Evento de error. La [**clase MOF UdpIp \_ Fail**](udpip-fail.md) define los datos de evento para este evento.                                  |
| Valor de tipo de evento, 26                                               | Evento de envío para el protocolo IPv6. La [**clase MOF UdpIp \_ TypeGroup2**](udpip-typegroup2.md) define los datos de evento para este evento.    |
| Valor de tipo de evento, 27                                               | Evento de recepción para el protocolo IPv6. La [**clase MOF UdpIp \_ TypeGroup2**](udpip-typegroup2.md) define los datos de evento para este evento. |



 

Puede realizar un seguimiento de los eventos de red a un proceso de origen y destino mediante la **propiedad ProcessId.** Dado que algunos eventos de red se registran mediante subprocesos independientes, es posible que no pueda usar los miembros **ProcessId** y **ThreadId** de [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar el proceso o subproceso que originó las actividades de red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemTrace de MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**Error \_ de UdpIp**](udpip-fail.md)
</dt> <dt>

[**UdpIp \_ TypeGroup1**](udpip-typegroup1.md)
</dt> <dt>

[**UdpIp \_ TypeGroup2**](udpip-typegroup2.md)
</dt> <dt>

[**UdpIp \_ V0**](udpip-v0.md)
</dt> <dt>

[**UdpIp \_ V1**](udpip-v1.md)
</dt> </dl>

 

 
