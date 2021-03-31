---
description: Evento de seguimiento de red Winsock para una operación de creación de Sockets.
ms.assetid: 59B9A570-5AEC-429D-AF71-AB6D8325C341
title: Evento AFD_EVENT_CREATE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CREATE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3216e1adccca6c7c7d64a22f77babe3cbb699c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907964"
---
# <a name="afd_event_create-event"></a>Evento de creación de \_ evento de AFD \_

El evento de **\_ \_ creación de eventos de AFD** es un evento de seguimiento de la red Winsock para una operación de creación de socket.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CREATE = {0x3e8, 0x0, 0x10, 0x4, 0xa, 0x3e8, 0x8000000000000004};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EnterExit* 
</dt> <dd>

Información sobre este evento.

En la tabla siguiente se enumeran los posibles valores para el parámetro *EnterExit* :



| Value                                                                        | Significado                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Inicio de una solicitud Winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Se completó la solicitud Winsock.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | El controlador Winsock AFD llevó a cabo una acción interna (anulando una conexión, por ejemplo).<br/>      |
| <dl> <dt>3</dt> </dl> | El controlador TCP/IP hizo que se produjera este evento. Normalmente, esto indica una notificación de datos.<br/> |
| <dl> <dt>4</dt> </dl> | El controlador Winsock AFD hizo que se produjera este evento (por ejemplo, si se establece una opción de socket).<br/> |



 

</dd> <dt>

*Ubicación* 
</dt> <dd>

Campo privado que se usa internamente.

</dd> <dt>

*Proceso* 
</dt> <dd>

La dirección [EPROCESS](/windows-hardware/drivers/kernel/eprocess) del proceso que posee el socket relacionado. Se trata de una estructura opaca que actúa como el objeto de proceso de un proceso. Para obtener más información, consulte la documentación del kit de controladores de Windows para la estructura [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .

</dd> <dt>

*Punto de conexión* 
</dt> <dd>

Dirección del \_ punto de conexión de AFD del socket.

</dd> <dt>

*AddressFamily* 
</dt> <dd>

Especificación de la familia de direcciones para el socket. Los valores posibles de la familia de direcciones se definen en el archivo de encabezado *Ws2def. h* . Tenga en cuenta que el archivo de encabezado *Ws2def. h* se incluye automáticamente en *WinSock2. h* y nunca se debe usar directamente.

Los valores admitidos actualmente son AF \_ inet o AF \_ inet6, que son los formatos de la familia de direcciones de Internet para IPv4 e IPv6. Otras opciones para la familia de direcciones (AF \_ NetBIOS para su uso con NetBIOS, por ejemplo) se admiten si se instala un proveedor de servicios de Windows Sockets para la familia de direcciones.

En la tabla siguiente se enumeran los valores comunes de la familia de direcciones, aunque son posibles muchos otros valores.



| AF                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AF_UNSPEC"></span><span id="af_unspec"></span><dl> <dt>**AF \_ No especificación**</dt> <dt>0</dt> </dl>           | No se especificó la familia de direcciones.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>                 | Familia de direcciones del Protocolo de Internet versión 4 (IPv4).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IPX"></span><span id="af_ipx"></span><dl> <dt>**AF \_ IPX**</dt> <dt>6</dt> </dl>                    | La familia de direcciones IPX/SPX. Esta familia de direcciones solo se admite si está instalado el protocolo de transporte compatible con NetBIOS IPX/SPX de NWLink. <br/> Esta familia de direcciones no es compatible con Windows Vista y versiones posteriores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_APPLETALK"></span><span id="af_appletalk"></span><dl> <dt>**AF \_ APPLETALK**</dt> <dt>16</dt> </dl> | Familia de direcciones AppleTalk. Esta familia de direcciones solo se admite si está instalado el protocolo AppleTalk. <br/> Esta familia de direcciones no es compatible con Windows Vista y versiones posteriores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_NETBIOS"></span><span id="af_netbios"></span><dl> <dt>**AF \_ NETBIOS**</dt> <dt>17</dt> </dl>       | La familia de direcciones NetBIOS. Esta familia de direcciones solo se admite si está instalado el proveedor de Windows Sockets para NetBIOS. <br/> El proveedor de Windows Sockets para NetBIOS es compatible con las versiones de 32 bits de Windows. Este proveedor se instala de manera predeterminada en las versiones de 32 bits de Windows. <br/> No se admite el proveedor de Windows Sockets para NetBIOS en las versiones de 64 bits de Windows. <br/> El proveedor de Windows Sockets para NetBIOS solo admite Sockets en los que el parámetro de *tipo* está establecido en **sock \_ DGRAM**.<br/> El proveedor de Windows Sockets para NetBIOS no está directamente relacionado con la interfaz de programación de [NetBIOS](/previous-versions/windows/desktop/netbios/portal) . La interfaz de programación de NetBIOS no es compatible con Windows Vista, Windows Server 2008 y versiones posteriores.<br/> |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl>             | La familia de direcciones del Protocolo de Internet versión 6 (IPv6).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IRDA"></span><span id="af_irda"></span><dl> <dt>**AF \_ IRDA**</dt> <dt>26</dt> </dl>                | La familia de direcciones de la Asociación de datos de infrarrojos (IrDA). <br/> Esta familia de direcciones solo se admite si el equipo tiene instalado un puerto de infrarrojos y un controlador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="AF_BTH"></span><span id="af_bth"></span><dl> <dt>**AF \_ BTH**</dt> <dt>32</dt> </dl>                   | La familia de direcciones de Bluetooth. <br/> Esta familia de direcciones solo se admite si el equipo tiene instalado un adaptador Bluetooth y un controlador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*SocketType* 
</dt> <dd>

Especificación de tipo para el nuevo socket. Los valores posibles para el tipo de socket se definen en el archivo de encabezado *WinSock2. h* .

En la tabla siguiente se enumeran los posibles valores para el parámetro de *tipo* compatible con Windows Sockets 2:



| Tipo                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SOCK_STREAM"></span><span id="sock_stream"></span><dl> <dt>**Sock \_ SECUENCIA**</dt> <dt>1</dt> </dl>          | Tipo de socket que proporciona secuencias de bytes secuenciadas, confiables y bidireccionales basadas en conexión con un mecanismo de transmisión de datos OOB. Este tipo de socket usa el protocolo de control de transmisión (TCP) para la familia de direcciones de Internet (AF \_ inet o AF \_ inet6).<br/>                                                                                                                                |
| <span id="SOCK_DGRAM"></span><span id="sock_dgram"></span><dl> <dt>**Sock \_ DGRAM**</dt> <dt>2</dt> </dl>             | Tipo de socket que admite datagramas, que son búferes sin conexión y no confiables de una longitud máxima fija (normalmente pequeña). Este tipo de socket usa el protocolo de datagramas de usuario (UDP) para la familia de direcciones de Internet (AF \_ inet o AF \_ inet6).<br/>                                                                                                                                       |
| <span id="SOCK_RAW"></span><span id="sock_raw"></span><dl> <dt>**Sock \_ Sin formato**</dt> <dt>3</dt> </dl>                   | Tipo de socket que proporciona un socket sin formato que permite a una aplicación manipular el siguiente encabezado de protocolo de nivel superior. Para manipular el encabezado IPv4, se debe establecer la opción de socket [**\_ HDRINCL de IP**](ipproto-ip-socket-options.md) en el socket. Para manipular el encabezado IPv6, se debe establecer la opción de socket [**\_ HDRINCL de IPv6**](ipproto-ipv6-socket-options.md) en el socket. <br/> |
| <span id="SOCK_RDM"></span><span id="sock_rdm"></span><dl> <dt>**Sock \_ RDM**</dt> <dt>4</dt> </dl>                   | Tipo de socket que proporciona un datagrama de mensaje confiable. Un ejemplo de este tipo es la implementación del Protocolo de multidifusión PGM (multidifusión general pragmática) en Windows, que a menudo se conoce como [programación confiable de multidifusión](reliable-multicast-programming--pgm-.md). <br/> Este valor de *tipo* solo se admite si se instala el protocolo de multidifusión confiable.<br/>              |
| <span id="SOCK_SEQPACKET"></span><span id="sock_seqpacket"></span><dl> <dt>**Sock \_ SEQPACKET**</dt> <dt>5</dt> </dl> | Tipo de socket que proporciona un paquete pseudo-Stream basado en datagramas. <br/>                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*Protocolo* 
</dt> <dd>

Protocolo que se va a usar. Las opciones posibles para el parámetro de *Protocolo* son específicas de la familia de direcciones y el tipo de socket especificados. Los valores posibles para el *Protocolo* se definen en el archivo de encabezado *WSRM. h* y en el tipo de enumeración **IPPROTO** definido en el archivo de encabezado *Ws2def. h* . Tenga en cuenta que el archivo de encabezado *Ws2def. h* se incluye automáticamente en *WinSock2. h* y nunca se debe usar directamente.

Si se especifica un valor de 0, el autor de la llamada no desea especificar un protocolo y el proveedor de servicios elegirá el *Protocolo* que se va a usar.

En la tabla siguiente se enumeran los valores comunes para el *Protocolo* , aunque es posible que haya muchos otros valores.



| protocol                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IPPROTO_ICMP"></span><span id="ipproto_icmp"></span><dl> <dt>**IPPROTO \_ ICMP**</dt> <dt>1</dt> </dl>          | Protocolo de mensajes de control de Internet (ICMP). Este es un valor posible cuando el parámetro *AF* es **AF \_ unspec**, **AF \_ inet** o **AF \_ inet6** y el parámetro de *tipo* es **sock \_ raw** o no se especifica.<br/>                                                                                               |
| <span id="IPPROTO_IGMP"></span><span id="ipproto_igmp"></span><dl> <dt>**IPPROTO \_ IGMP**</dt> <dt>2</dt> </dl>          | El protocolo de administración de grupos de Internet (IGMP). Este es un valor posible cuando el parámetro *AF* es **AF \_ unspec**, **AF \_ inet** o **AF \_ inet6** y el parámetro de *tipo* es **sock \_ raw** o no se especifica.<br/>                                                                                              |
| <span id="BTHPROTO_RFCOMM"></span><span id="bthproto_rfcomm"></span><dl> <dt>**BTHPROTO \_ RFCOMM**</dt> <dt>3</dt> </dl> | El protocolo de comunicaciones de radiofrecuencia de radio (Bluetooth RFCOMM) de Bluetooth. Este es un valor posible cuando el parámetro *AF* es **AF \_ BTH** y el parámetro de *tipo* es **sock \_ Stream**. <br/>                                                                                                                 |
| <span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span><dl> <dt>**IPPROTO \_ TCP**</dt> <dt>6</dt> </dl>             | El protocolo de control de transmisión (TCP). Este es un valor posible cuando el parámetro *AF* es **AF \_ inet** o **AF \_ inet6** y el parámetro de *tipo* es **sock \_ Stream**.<br/>                                                                                                                                 |
| <span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span><dl> <dt>**IPPROTO \_ UDP**</dt> <dt>17</dt> </dl>            | Protocolo de datagramas de usuario (UDP). Este es un valor posible cuando el parámetro *AF* es **AF \_ inet** o **AF \_ inet6** y el parámetro de *tipo* es **sock \_ DGRAM**.<br/>                                                                                                                                         |
| <span id="IPPROTO_ICMPV6"></span><span id="ipproto_icmpv6"></span><dl> <dt>**IPPROTO \_ ICMPV6**</dt> <dt>58</dt> </dl>   | El protocolo de mensajes de control de Internet versión 6 (ICMPv6). Este es un valor posible cuando el parámetro *AF* es **AF \_ unspec**, **AF \_ inet** o **AF \_ inet6** y el parámetro de *tipo* es **sock \_ raw** o no se especifica.<br/>                                                                                   |
| <span id="IPPROTO_RM"></span><span id="ipproto_rm"></span><dl> <dt>**IPPROTO \_ RM**</dt> <dt>113</dt> </dl>              | Protocolo PGM para multidifusión confiable. Este es un valor posible cuando el parámetro *AF* es **AF \_ inet** y el parámetro de *tipo* es **sock \_ RDM**. Este protocolo también se denomina **\_ PGM de IPPROTO**. <br/> Este valor de *Protocolo* solo se admite si se instala el protocolo de multidifusión confiable.<br/> |



 

</dd> <dt>

*ProcessId* 
</dt> <dd>

El ID. de proceso real o un indicador si el evento fue el resultado de la ejecución del código Winsock en un proceso del sistema o en un contexto de llamada a procedimiento diferida (DPC) (contextos fuera del proceso de usuario).

</dd> <dt>

*Estado* 
</dt> <dd>

Código NTSTATUS de la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se realiza un seguimiento del evento de **\_ \_ creación de eventos de AFD** para que una operación de red Winsock cree un socket. El canal de este evento es Winsock-AFD. El nivel de este evento es informativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**descriptor de eventos \_**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalles de seguimiento de cambios de catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

