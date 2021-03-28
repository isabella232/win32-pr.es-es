---
description: Esta clase es la clase primaria para los eventos TCP/IP. La siguiente sintaxis se simplifica desde el código MOF.
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
ms.openlocfilehash: 6488ece2fd8df0670455ceea25560835c352b83e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984774"
---
# <a name="tcpip-class"></a>TcpIp (clase)

Esta clase es la clase primaria para los eventos TCP/IP.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **TCPIP** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar los eventos TCP/IP en una sesión de registro del kernel de NT, especifique la marca de **seguimiento de eventos de \_ \_ \_ red \_ TCPIP** Flag en el miembro **EnableFlags** de una estructura de propiedades de [**\_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos TCP/IP mediante una llamada a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**TcpIpGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar el evento de red (TCP/IP) real al consumir eventos.



| Tipo de evento                                                            | Descripción                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Tipo de seguimiento \_ \_ Accept**(el valor de tipo de evento es 15)<br/>     | Evento Accept para el protocolo IPv4. La clase MOF [**\_ TypeGroup2 de TCPIP**](tcpip-typegroup2.md) define los datos de evento para este evento.                                                            |
| **Evento \_ de Tipo de seguimiento \_ \_ Connect**(el valor de tipo de evento es 12)<br/>    | Evento de conexión para el protocolo IPv4. La clase MOF [**\_ TypeGroup2 de TCPIP**](tcpip-typegroup2.md) define los datos de evento para este evento.                                                           |
| **Evento \_ de Tipo de seguimiento \_ \_ Disconnect**(el valor del tipo de evento es 13)<br/> | Evento de desconexión del protocolo IPv4. La clase MOF [**\_ TypeGroup1 de TCPIP**](tcpip-typegroup1.md) define los datos de evento para este evento.                                                        |
| **Evento \_ de Tipo de seguimiento \_ \_ Receive**(el valor de tipo de evento es 11)<br/>    | Evento Receive para el protocolo IPv4. La clase MOF [**\_ TypeGroup1 de TCPIP**](tcpip-typegroup1.md) define los datos de evento para este evento.                                                           |
| **Evento \_ de Tipo de seguimiento \_ \_ reconnect**(el valor de tipo de evento es 16)<br/>  | Evento de reconexión para el protocolo IPv4. (Se produjo un error en un intento de conexión y se realiza otro intento). La clase MOF [**\_ TypeGroup1 de TCPIP**](tcpip-typegroup1.md) define los datos de evento para este evento. |
| **Evento \_ de Tipo de seguimiento \_ \_ retransmitir**(el valor del tipo de evento es 14)<br/> | Evento de retransmisión para el protocolo IPv4. La clase MOF [**\_ TypeGroup1 de TCPIP**](tcpip-typegroup1.md) define los datos de evento para este evento.                                                        |
| **Evento \_ de Tipo de seguimiento \_ \_ send**(el valor de tipo de evento es 10)<br/>       | Enviar evento para el protocolo IPv4. La clase MOF [**\_ SendIPV4 de TCPIP**](tcpip-sendipv4.md) define los datos de evento para este evento.                                                                  |
| Valor de tipo de evento, 17                                                  | Evento Fail. La clase de [**TCPIP \_ FAIL**](tcpip-fail.md) mof define los datos de evento para este evento.                                                                                            |
| Valor de tipo de evento, 18                                                  | Evento de copia TCP para el protocolo IPv4. La clase MOF [**\_ TypeGroup1 de TCPIP**](tcpip-typegroup1.md) define los datos de evento para este evento.                                                          |
| Valor del tipo de evento 26                                                  | Envía el evento para el protocolo IPv6. La clase MOF [**\_ SendIPV6 de TCPIP**](tcpip-sendipv6.md) define los datos de evento para este evento.                                                                  |
| Valor del tipo de evento 27                                                  | Evento Receive para el protocolo IPv6. La clase MOF [**\_ TypeGroup3 de TCPIP**](tcpip-typegroup3.md) define los datos de evento para este evento.                                                           |
| Valor del tipo de evento 28                                                  | Evento de conexión para el protocolo IPv6. La clase MOF [**\_ TypeGroup4 de TCPIP**](tcpip-typegroup4.md) define los datos de evento para este evento.                                                           |
| Valor de tipo de evento, 29                                                  | Evento de desconexión para el protocolo IPv6. La clase MOF [**\_ TypeGroup3 de TCPIP**](tcpip-typegroup3.md) define los datos de evento para este evento.                                                        |
| Valor de tipo de evento, 30                                                  | Evento de retransmisión para el protocolo IPv6. La clase MOF [**\_ TypeGroup3 de TCPIP**](tcpip-typegroup3.md) define los datos de evento para este evento.                                                        |
| Valor de tipo de evento, 31                                                  | Evento Accept para el protocolo IPv6. La clase MOF [**\_ TypeGroup4 de TCPIP**](tcpip-typegroup4.md) define los datos de evento para este evento.                                                            |
| Valor del tipo de evento, 32                                                  | Evento de reconexión para el protocolo IPv6. (Se produjo un error en un intento de conexión y se realiza otro intento). La clase MOF [**\_ TypeGroup3 de TCPIP**](tcpip-typegroup3.md) define los datos de evento para este evento. |
| Valor del tipo de evento, 34                                                  | Evento de copia TCP para el protocolo IPv6. La clase MOF [**\_ TypeGroup3 de TCPIP**](tcpip-typegroup3.md) define los datos de evento para este evento.                                                          |



 

Puede realizar un seguimiento de los eventos de red a un proceso de origen y de destino mediante la propiedad **ProcessId** . Dado que algunos eventos de red están registrados por subprocesos independientes, es posible que no pueda usar los miembros **ProcessId** y **ThreadId** del [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar el proceso o subproceso que originó las actividades de red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Error de TcpIp \_**](tcpip-fail.md)
</dt> <dt>

[**SendIPV4 de TcpIp \_**](tcpip-sendipv4.md)
</dt> <dt>

[**SendIPV6 de TcpIp \_**](tcpip-sendipv6.md)
</dt> <dt>

[**TypeGroup1 de TcpIp \_**](tcpip-typegroup1.md)
</dt> <dt>

[**TypeGroup2 de TcpIp \_**](tcpip-typegroup2.md)
</dt> <dt>

[**TypeGroup3 de TcpIp \_**](tcpip-typegroup3.md)
</dt> <dt>

[**TypeGroup4 de TcpIp \_**](tcpip-typegroup4.md)
</dt> <dt>

[**V0 de TcpIp \_**](tcpip-v0.md)
</dt> <dt>

[**TcpIp \_ v1**](tcpip-v1.md)
</dt> </dl>

 

 
