---
description: 'Clase TcpIp: esta clase es la clase primaria para los eventos TCP/IP. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: TcpIp (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0782db83d5c92a0e39578bc4e0d46e2c1d41432feb418a08bceb2e3548a45b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069525"
---
# <a name="tcpip-class"></a>TcpIp (clase)

Esta clase es la clase primaria para los eventos TCP/IP.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase TcpIp** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar eventos TCP/IP en una sesión de registro del kernel de NT, especifique la marca **\_ \_ \_ \_ TCPIP EVENT TRACE FLAG NETWORK** en el miembro **EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos TCP/IP llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**TcpIpGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid.* Use los siguientes tipos de eventos para identificar el evento de red (TCP/IP) real al consumir eventos.



| Tipo de evento                                                            | Descripción                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ ACCEPT**(el valor del tipo de evento es 15)<br/>     | Acepte el evento para el protocolo IPv4. La [**clase MOF \_ TcpIp TypeGroup2**](tcpip-typegroup2.md) define los datos de evento para este evento.                                                            |
| **EVENT \_ TRACE \_ TYPE \_ CONNECT**(el valor del tipo de evento es 12)<br/>    | Conectar evento para el protocolo IPv4. La [**clase MOF \_ TcpIp TypeGroup2**](tcpip-typegroup2.md) define los datos de evento para este evento.                                                           |
| **EVENT \_ TRACE \_ TYPE \_ DISCONNECT**(el valor del tipo de evento es 13)<br/> | Evento de desconexión para el protocolo IPv4. La [**clase MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) define los datos de evento para este evento.                                                        |
| **EVENT \_ TRACE \_ TYPE \_ RECEIVE**(el valor del tipo de evento es 11)<br/>    | Evento de recepción para el protocolo IPv4. La [**clase MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) define los datos de evento para este evento.                                                           |
| **EVENT \_ TRACE \_ TYPE \_ RECONNECT**(el valor del tipo de evento es 16)<br/>  | Evento de reconexión para el protocolo IPv4. (Error en un intento de conexión y se realiza otro intento). La [**clase MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) define los datos de evento para este evento. |
| **EVENT \_ TRACE \_ TYPE \_ RETRANSMIT**(el valor del tipo de evento es 14)<br/> | Evento de retransmisión para el protocolo IPv4. La [**clase MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) define los datos de evento para este evento.                                                        |
| **EVENT \_ TRACE \_ TYPE \_ SEND**(el valor del tipo de evento es 10)<br/>       | Envío de eventos para el protocolo IPv4. La [**clase MOF TcpIp \_ SendIPV4**](tcpip-sendipv4.md) define los datos de evento para este evento.                                                                  |
| Valor de tipo de evento, 17                                                  | Evento de error. La [**clase MOF TcpIp \_ Fail**](tcpip-fail.md) define los datos de evento para este evento.                                                                                            |
| Valor de tipo de evento, 18                                                  | Evento de copia TCP para el protocolo IPv4. La [**clase MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) define los datos de evento para este evento.                                                          |
| Valor de tipo de evento, 26                                                  | Evento de envío para el protocolo IPv6. La [**clase MOF TcpIp \_ SendIPV6**](tcpip-sendipv6.md) define los datos de evento para este evento.                                                                  |
| Valor de tipo de evento, 27                                                  | Evento de recepción para el protocolo IPv6. La [**clase MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) define los datos de evento para este evento.                                                           |
| Valor de tipo de evento, 28                                                  | Conectar evento para el protocolo IPv6. La [**clase MOF \_ TcpIp TypeGroup4**](tcpip-typegroup4.md) define los datos de evento para este evento.                                                           |
| Valor de tipo de evento, 29                                                  | Evento de desconexión para el protocolo IPv6. La [**clase MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) define los datos de evento para este evento.                                                        |
| Valor de tipo de evento, 30                                                  | Evento de retransmisión para el protocolo IPv6. La [**clase MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) define los datos de evento para este evento.                                                        |
| Valor de tipo de evento, 31                                                  | Acepte el evento para el protocolo IPv6. La [**clase MOF \_ TcpIp TypeGroup4**](tcpip-typegroup4.md) define los datos de evento para este evento.                                                            |
| Valor de tipo de evento, 32                                                  | Evento de reconexión para el protocolo IPv6. (Error en un intento de conexión y se realiza otro intento). La [**clase MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) define los datos de evento para este evento. |
| Valor de tipo de evento, 34                                                  | Evento de copia TCP para el protocolo IPv6. La [**clase MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) define los datos de evento para este evento.                                                          |



 

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

[**Error \_ de TcpIp**](tcpip-fail.md)
</dt> <dt>

[**TcpIp \_ SendIPV4**](tcpip-sendipv4.md)
</dt> <dt>

[**TcpIp \_ SendIPV6**](tcpip-sendipv6.md)
</dt> <dt>

[**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md)
</dt> <dt>

[**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md)
</dt> <dt>

[**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md)
</dt> <dt>

[**TcpIp \_ TypeGroup4**](tcpip-typegroup4.md)
</dt> <dt>

[**TcpIp \_ V0**](tcpip-v0.md)
</dt> <dt>

[**TcpIp \_ V1**](tcpip-v1.md)
</dt> </dl>

 

 
