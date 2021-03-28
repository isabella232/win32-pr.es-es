---
description: Esta clase es la clase primaria para los eventos UDP/IP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: Clase UdpIp
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
ms.openlocfilehash: 5116b5f97a4aa7e3bafa9da1c1208ce7ee9d5794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543075"
---
# <a name="udpip-class"></a>Clase UdpIp

Esta clase es la clase primaria para los eventos UDP/IP.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **UdpIp** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar los eventos UDP/IP en una sesión de registro del kernel de NT, especifique la marca de **seguimiento de eventos de \_ \_ \_ red \_ TCPIP** Flag en el miembro **EnableFlags** de una estructura de propiedades de [**\_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos UDP/IP mediante una llamada a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**UdpIpGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar el evento de red (UDP/IP) real al consumir eventos.



| Tipo de evento                                                         | Descripción                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Tipo de seguimiento \_ \_ Receive**(el valor de tipo de evento es 11)<br/> | Evento Receive para el protocolo IPv4. La clase MOF [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) define los datos de evento para este evento. |
| **Evento \_ de Tipo de seguimiento \_ \_ send**(el valor de tipo de evento es 10)<br/>    | Enviar evento para el protocolo IPv4. La clase MOF [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) define los datos de evento para este evento.    |
| Valor de tipo de evento, 17                                               | Evento Fail. La clase MOF [**\_ FAIL UdpIp**](udpip-fail.md) define los datos de evento para este evento.                                  |
| Valor del tipo de evento 26                                               | Envía el evento para el protocolo IPv6. La clase MOF [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) define los datos de evento para este evento.    |
| Valor del tipo de evento 27                                               | Evento Receive para el protocolo IPv6. La clase MOF [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) define los datos de evento para este evento. |



 

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

[**Error de UdpIp \_**](udpip-fail.md)
</dt> <dt>

[**UdpIp \_ TypeGroup1**](udpip-typegroup1.md)
</dt> <dt>

[**UdpIp \_ TypeGroup2**](udpip-typegroup2.md)
</dt> <dt>

[**UdpIp \_ v0**](udpip-v0.md)
</dt> <dt>

[**UdpIp \_ v1**](udpip-v1.md)
</dt> </dl>

 

 
