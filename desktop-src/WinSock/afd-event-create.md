---
description: Evento de seguimiento de red winsock para una operación de creación de sockets.
ms.assetid: 59B9A570-5AEC-429D-AF71-AB6D8325C341
title: AFD_EVENT_CREATE evento
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
ms.openlocfilehash: 7ae6f50646ad863be711ab6d48e775aeac9023a053e29044f3921e1dee8c9948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121485"
---
# <a name="afd_event_create-event"></a>Evento AFD \_ EVENT \_ CREATE

El **evento AFD \_ EVENT \_ CREATE** es un evento de seguimiento de red winsock para una operación de creación de sockets.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CREATE = {0x3e8, 0x0, 0x10, 0x4, 0xa, 0x3e8, 0x8000000000000004};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EnterExit* 
</dt> <dd>

Información sobre este evento.

En la tabla siguiente se enumeran los valores posibles *para el parámetro EnterExit:*



| Value                                                                        | Significado                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Inicio de una solicitud winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Se completó la solicitud winsock.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | El controlador afd winsock realizó una acción interna (anulando una conexión, por ejemplo).<br/>      |
| <dl> <dt>3</dt> </dl> | El controlador TCP/IP provocó que se produjese este evento. Esto suele indicar una notificación de datos.<br/> |
| <dl> <dt>4</dt> </dl> | El controlador AFD winsock provocó que se produjese este evento (por ejemplo, al establecer una opción de socket).<br/> |



 

</dd> <dt>

*Ubicación* 
</dt> <dd>

Campo privado que se usa internamente.

</dd> <dt>

*Process* 
</dt> <dd>

Dirección [EPROCESS](/windows-hardware/drivers/kernel/eprocess) del proceso que posee el socket relacionado. Se trata de una estructura opaca que actúa como objeto de proceso para un proceso. Para más información, consulte la documentación Windows Driver Kit para la [estructura EPROCESS.](/windows-hardware/drivers/kernel/eprocess)

</dd> <dt>

*Punto de conexión* 
</dt> <dd>

Dirección DEL PUNTO DE CONEXIÓN DE AFD \_ del socket.

</dd> <dt>

*AddressFamily* 
</dt> <dd>

Especificación de la familia de direcciones para el socket. Los valores posibles para la familia de direcciones se definen en el *archivo de encabezado Ws2def.h.* Tenga en cuenta que el archivo de encabezado *Ws2def.h* se incluye automáticamente en *Winsock2.h* y nunca se debe usar directamente.

Los valores admitidos actualmente son AF INET o AF INET6, que son los formatos de familia de direcciones de Internet para \_ \_ IPv4 e IPv6. Se admiten otras opciones para la familia de direcciones (AF NETBIOS para su uso con NetBIOS, por ejemplo) si está instalado un proveedor de servicios Windows Sockets para la familia \_ de direcciones.

En la tabla siguiente se enumeran los valores comunes de la familia de direcciones, aunque muchos otros valores son posibles.



| Af                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AF_UNSPEC"></span><span id="af_unspec"></span><dl> <dt>**AF \_ UNSPEC**</dt> <dt>0</dt> </dl>           | La familia de direcciones no está especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>                 | La familia de direcciones IPv4 (Protocolo de Internet versión 4).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IPX"></span><span id="af_ipx"></span><dl> <dt>**AF \_ IPX**</dt> <dt>6</dt> </dl>                    | Familia de direcciones IPX/SPX. Esta familia de direcciones solo se admite si está instalado el protocolo de transporte compatible con NETBIOS DE NWLink IPX/SPX. <br/> Esta familia de direcciones no se admite en Windows Vista y versiones posteriores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_APPLETALK"></span><span id="af_appletalk"></span><dl> <dt>**AF \_ APPLETALK**</dt> <dt>16</dt> </dl> | Familia de direcciones de AppleTalk. Esta familia de direcciones solo se admite si está instalado el protocolo AppleTalk. <br/> Esta familia de direcciones no se admite en Windows Vista y versiones posteriores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_NETBIOS"></span><span id="af_netbios"></span><dl> <dt>**AF \_ NETBIOS**</dt> <dt>17</dt> </dl>       | Familia de direcciones NetBIOS. Esta familia de direcciones solo se admite si el Windows sockets para NetBIOS está instalado. <br/> El proveedor Windows Sockets para NetBIOS se admite en versiones de 32 bits de Windows. Este proveedor se instala de forma predeterminada en versiones de 32 bits de Windows. <br/> El proveedor Windows Sockets para NetBIOS no se admite en versiones de 64 bits de Windows. <br/> El Windows sockets para NetBIOS solo admite sockets donde el parámetro *de* tipo está establecido en **\_ SOCK DGRAM**.<br/> El proveedor Windows Sockets para NetBIOS no está directamente relacionado con la interfaz [de programación NetBIOS.](/previous-versions/windows/desktop/netbios/portal) La interfaz de programación NetBIOS no se admite en Windows Vista, Windows Server 2008 y versiones posteriores.<br/> |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl>             | La familia de direcciones IPv6 (Protocolo de Internet versión 6).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IRDA"></span><span id="af_irda"></span><dl> <dt>**AF \_ IRDA**</dt> <dt>26</dt> </dl>                | Familia de direcciones Protocolo de asociación de datos por infrarrojos (IrDA) (IrDA). <br/> Esta familia de direcciones solo se admite si el equipo tiene instalado un puerto y un controlador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="AF_BTH"></span><span id="af_bth"></span><dl> <dt>**AF \_ BTH**</dt> <dt>32</dt> </dl>                   | Familia Bluetooth de direcciones. <br/> Esta familia de direcciones solo se admite si el equipo tiene un Bluetooth y un controlador instalados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*SocketType* 
</dt> <dd>

Especificación de tipo para el nuevo socket. Los valores posibles para el tipo de socket se definen en el *archivo de encabezado Winsock2.h.*

En la tabla siguiente se enumeran los valores posibles para el *parámetro de* tipo admitido para Windows Sockets 2:



| Tipo                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SOCK_STREAM"></span><span id="sock_stream"></span><dl> <dt>**SOCK \_ STREAM**</dt> <dt>1</dt> </dl>          | Tipo de socket que proporciona secuencias de bytes basadas en conexiones secuenciadas, confiables y en dos sentidos con un mecanismo de transmisión de datos OOB. Este tipo de socket usa el Protocolo de control de transmisión (TCP) para la familia de direcciones de Internet (AF \_ INET o \_ AF INET6).<br/>                                                                                                                                |
| <span id="SOCK_DGRAM"></span><span id="sock_dgram"></span><dl> <dt>**SOCK \_ DGRAM**</dt> <dt>2</dt> </dl>             | Tipo de socket que admite datagramas, que son búferes sin conexión y no confiables de una longitud máxima fija (normalmente pequeña). Este tipo de socket usa el Protocolo de datagramas de usuario (UDP) para la familia de direcciones de Internet (AF \_ INET o AF \_ INET6).<br/>                                                                                                                                       |
| <span id="SOCK_RAW"></span><span id="sock_raw"></span><dl> <dt>**SOCK \_ RAW**</dt> <dt>3</dt> </dl>                   | Tipo de socket que proporciona un socket sin formato que permite a una aplicación manipular el siguiente encabezado de protocolo de capa superior. Para manipular el encabezado IPv4, la opción de socket [**\_ IP HDRINCL**](ipproto-ip-socket-options.md) debe establecerse en el socket. Para manipular el encabezado IPv6, se debe establecer la opción de socket [**\_ IPV6 HDRINCL**](ipproto-ipv6-socket-options.md) en el socket. <br/> |
| <span id="SOCK_RDM"></span><span id="sock_rdm"></span><dl> <dt>**SOCK \_ RDM**</dt> <dt>4</dt> </dl>                   | Tipo de socket que proporciona un datagrama de mensaje confiable. Un ejemplo de este tipo es la implementación del protocolo de multidifusión general pragmática (PGM) en Windows, a menudo denominada programación de [multidifusión confiable.](reliable-multicast-programming--pgm-.md) <br/> Este *valor* de tipo solo se admite si está instalado el Protocolo de multidifusión confiable.<br/>              |
| <span id="SOCK_SEQPACKET"></span><span id="sock_seqpacket"></span><dl> <dt>**SOCK \_ SEQPACKET**</dt> <dt>5</dt> </dl> | Tipo de socket que proporciona un paquete de pseudo streaming basado en datagramas. <br/>                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*Protocolo* 
</dt> <dd>

Protocolo que se va a usar. Las opciones posibles para el *parámetro protocol* son específicas de la familia de direcciones y el tipo de socket especificados. Los valores  posibles para el protocolo se definen en el archivo de *encabezado Wsrm.h* y el tipo de enumeración **IPPROTO** definido en el archivo de encabezado *Ws2def.h.* Tenga en cuenta que el archivo de encabezado *Ws2def.h* se incluye automáticamente en *Winsock2.h* y nunca se debe usar directamente.

Si se especifica un valor de 0, el autor de la llamada no desea especificar un protocolo y el proveedor de servicios elegirá el *protocolo* que se va a usar.

En la tabla siguiente se enumeran los valores comunes para *el protocolo, aunque* muchos otros valores son posibles.



| protocol                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IPPROTO_ICMP"></span><span id="ipproto_icmp"></span><dl> <dt>**IPPROTO \_ ICMP**</dt> <dt>1</dt> </dl>          | Protocolo de mensajes de control de Internet (ICMP). Este es un valor posible cuando el parámetro  *af* es AF **\_ UNSPEC,** AF **\_ INET** o AF **\_ INET6** y el parámetro de tipo es **SOCK \_ RAW** o no especificado.<br/>                                                                                               |
| <span id="IPPROTO_IGMP"></span><span id="ipproto_igmp"></span><dl> <dt>**IPPROTO \_ IGMP**</dt> <dt>2</dt> </dl>          | Protocolo de administración de grupos de Internet (IGMP). Este es un valor posible cuando el parámetro  *af* es AF **\_ UNSPEC,** AF **\_ INET** o AF **\_ INET6** y el parámetro de tipo es **SOCK \_ RAW** o no especificado.<br/>                                                                                              |
| <span id="BTHPROTO_RFCOMM"></span><span id="bthproto_rfcomm"></span><dl> <dt>**BTHPROTO \_ RFCOMM**</dt> <dt>3</dt> </dl> | El Bluetooth de radiofrecuencia (Bluetooth RFCOMM). Este es un valor posible cuando el *parámetro af* es **AF \_ BTH** y el *parámetro de tipo* es **SOCK \_ STREAM**. <br/>                                                                                                                 |
| <span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span><dl> <dt>**IPPROTO \_ TCP**</dt> <dt>6</dt> </dl>             | Protocolo de control de transmisión (TCP). Este es un valor posible cuando el parámetro *af* es **AF \_ INET** o **AF \_ INET6** y el parámetro *de* tipo **es SOCK \_ STREAM.**<br/>                                                                                                                                 |
| <span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span><dl> <dt>**IPPROTO \_ UDP**</dt> <dt>17</dt> </dl>            | Protocolo de datagramas de usuario (UDP). Este es un valor posible cuando el parámetro *af* es  **AF \_ INET** o **AF \_ INET6** y el parámetro de tipo **es SOCK \_ DGRAM.**<br/>                                                                                                                                         |
| <span id="IPPROTO_ICMPV6"></span><span id="ipproto_icmpv6"></span><dl> <dt>**IPPROTO \_ ICMPV6**</dt> <dt>58</dt> </dl>   | Protocolo de mensajes de control de Internet versión 6 (ICMPv6). Este es un valor posible cuando el parámetro  *af* es AF **\_ UNSPEC,** AF **\_ INET** o AF **\_ INET6** y el parámetro de tipo es **SOCK \_ RAW** o no especificado.<br/>                                                                                   |
| <span id="IPPROTO_RM"></span><span id="ipproto_rm"></span><dl> <dt>**IPPROTO \_ RM**</dt> <dt>113</dt> </dl>              | El protocolo PGM para multidifusión confiable. Este es un valor posible cuando el parámetro *af* es **AF \_ INET** y el parámetro *de* tipo **es \_ SOCK RDM**. Este protocolo también se denomina **IPPROTO \_ PGM.** <br/> Este *valor* de protocolo solo se admite si está instalado el protocolo de multidifusión confiable.<br/> |



 

</dd> <dt>

*ProcessId* 
</dt> <dd>

El identificador de proceso real o un indicador si el evento fue el resultado de la ejecución del código Winsock en un proceso del sistema o en un contexto de llamada a procedimiento diferido (DPC) (contextos fuera del proceso del usuario).

</dd> <dt>

*Estado* 
</dt> <dd>

Código NTSTATUS para la operación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Se hace un seguimiento del evento **\_ AFD EVENT \_ CREATE** para que una operación de red Winsock cree un socket. El canal para este evento es Winsock-AFD. El nivel de este evento es informativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control del seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**\_DESCRIPTOR DE EVENTOS**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalles del seguimiento de cambios del catálogo de Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

