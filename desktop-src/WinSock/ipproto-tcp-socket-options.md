---
description: En la tabla siguiente se describen las opciones de socket TCP de IPPROTO que se aplican a los sockets creados para las familias de direcciones IPv4 e IPv6 (AF INET e AF INET6) con el parámetro protocol para la función de socket especificada \_ \_ como TCP \_ (IPPROTO \_ TCP).
ms.assetid: 2a10498d-0a0b-4a2d-941e-9aa45a1a4428
title: Opciones de socket IPPROTO_TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153f3bdf2cbfa3cbdbc50214722c62b4ad2f75d65136f2f7370b73bdfa3bfc1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927583"
---
# <a name="ipproto_tcp-socket-options"></a>Opciones de socket TCP de IPPROTO \_

En la tabla siguiente se describen las opciones de socket TCP de **IPPROTO \_** que se aplican a los sockets creados para las familias de direcciones IPv4 e IPv6 (AF INET e AF INET6) con el parámetro protocol para la función de socket especificada \_ como TCP \_ (IPPROTO  [](/windows/desktop/api/Winsock2/nf-winsock2-socket) \_ TCP). Consulte las [**páginas de referencia de la función getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obtener más información sobre cómo obtener y establecer opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas para cada protocolo instalado, use la función [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

## <a name="options"></a>Opciones

<table>
<colgroup>
<col/>
<col/>
<col/>
<col/>
<col/>
</colgroup>
<thead>
<tr class="header">
<th>Opción</th>
<th>Obtener</th>
<th>Set</th>
<th>Tipo optval</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>TCP_BSDURGENT</td>
<td>Sí</td>
<td>Sí</td>
<td>DWORD (booleano)</td>
<td>Si <strong>es TRUE,</strong>el proveedor de servicios implementa el estilo de distribución de software de Berkeley (BSD) (valor predeterminado) para controlar los datos acelerados. Esta opción es la inversa de la TCP_EXPEDITED_1122 predeterminada. Esta opción se puede establecer en la conexión solo una vez. Una vez que esta opción está activada, esta opción no se puede desactivar. Esta opción no es necesaria para que la implementen los proveedores de servicios. La opción está habilitada (se establece en <strong>TRUE)</strong>de forma predeterminada.</td>
</tr>
<tr>
<td>TCP_EXPEDITED_1122</td>
<td>Sí</td>
<td>Sí</td>
<td>DWORD (booleano)</td>
<td>Si <strong>es TRUE,</strong>el proveedor de servicios implementa los datos rápidos tal y como se especifica en RFC-1222. De lo contrario, se usa el estilo de distribución de software de Berkeley (BSD) (valor predeterminado). Esta opción se puede establecer en la conexión solo una vez. Una vez que esta opción está activada, esta opción no se puede desactivar. Esta opción no es necesaria para que la implementen los proveedores de servicios.</td>
</tr>
<tr>
<td>TCP_FAIL_CONNECT_ON_ICMP_ERROR</td>
<td>Sí</td>
<td>Sí</td>
<td>DWORD (booleano)</td>
<td>Si <strong>es TRUE,</strong>se devolverá una llamada API de conexión tras la recepción de un error ICMP con el valor WSAEHOSTUNREACH. La dirección de origen del error estará disponible a través de la opción TCP_ICMP_ERROR_INFO socket. Si <strong>es FALSE,</strong>el socket se comporta normalmente. El valor predeterminado está deshabilitado (se establece en <strong>FALSE).</strong> Para la seguridad de tipos, debe usar las funciones <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror">WSAGetFailConnectOnIcmpError</a> y <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror">WSASetFailConnectOnIcmpError</a> en lugar de usar directamente la opción de socket.</td>
</tr>
<tr>
<td>TCP_ICMP_ERROR_INFO</td>
<td>Sí</td>
<td>No</td>
<td><a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a></td>
<td>Recupera la información de un error ICMP recibido por el socket TCP durante una llamada de conexión con errores. Solo es válido en un socket TCP TCP_FAIL_CONNECT_ON_ICMP_ERROR se ha habilitado previamente y <strong>connect</strong> ha devuelto WSAEHOSTUNREACH. La consulta no es de bloqueo. Si se consulta correctamente y el valor de optlen devuelto es 0, no se ha recibido ningún error ICMP desde la última llamada de conexión. Si se recibió un error ICMP, su información estará disponible hasta que se <strong>vuelva</strong> a llamar a la conexión. La información se devuelve como una <a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">estructura ICMP_ERROR_INFO</a> datos. Para la seguridad de tipos, debe usar la función <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo">WSAGetIcmpErrorInfo</a> en lugar de usar directamente la opción de socket.</td>
</tr>
<tr>
<td>TCP_KEEPCNT</td>
<td>Sí</td>
<td>Sí</td>
<td>DWORD</td>
<td>Obtiene o establece el número de sondeos tcp keep alive que se enviarán antes de que finalice la conexión. No es válido establecer TCP_KEEPCNT en un valor mayor que 255.</td>
</tr>
<tr>
<td>TCP_MAXRT</td>
<td>Sí</td>
<td>Sí</td>
<td>DWORD</td>
<td>Si este valor no es negativo, representa el tiempo de espera de conexión deseado en segundos. Si es -1, representa una solicitud para deshabilitar el tiempo de espera de conexión (es decir, la conexión se retransmitirá indefinidamente). Si se deshabilita el tiempo de espera de conexión, el tiempo de espera de retransmisión aumenta exponencialmente para cada retransmisión hasta su valor máximo de 60 s y, a continuación, permanece allí.</td>
</tr>
<tr>
<td>TCP_NODELAY</td>
<td>Sí</td>
<td>Sí</td>
<td>DWORD (booleano)</td>
<td>Habilita o deshabilita el algoritmo nagle para sockets TCP. Esta opción está deshabilitada (se establece en FALSE) de forma predeterminada.</td>
</tr>
<tr>
<td>TCP_TIMESTAMPS</td>
<td>Sí</td>
<td>Sí</td>
<td>DWORD (booleano)</td>
<td>Habilita o deshabilita las marcas de tiempo rfc 1323. Tenga en cuenta que también hay una configuración global para las marcas de tiempo (el valor predeterminado es off), &quot; Timestamps &quot; in (set/get)-nettcpsetting. Establecer esta opción de socket invalida esa configuración global.</td>
</tr>
<tr>
<td>TCP_FASTOPEN</td>
<td>Sí</td>
<td>Sí</td>
<td>DWORD (booleano)</td>
<td>Habilita o deshabilita <a href="https://tools.ietf.org/html/rfc7413">RFC 7413</a> TCP Fast Open, lo que le permite empezar a enviar datos durante la fase de protocolo de enlace triple de apertura de una conexión. Tenga en cuenta que para usar las aperturas rápidas, debe usar <a href="/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex"><strong>ConnectEx</strong></a> para realizar la conexión inicial y especificar los datos del parámetro <em>lpSendBuffer</em> de esa función que se transferirán durante el proceso de protocolo de enlace. Algunos de los datos de <em>lpSendBuffer</em> se transferirán en el protocolo Fast Open.</td>
</tr>
<tr>
<td>TCP_KEEPIDLE</td>
<td>Sí</td>
<td>Sí</td>
<td>DWORD</td>
<td>Obtiene o establece el número de segundos que una conexión TCP permanecerá inactiva antes de que los sondeos keepalive se envíen al remoto.
<blockquote>
[!Note]<br />
Esta opción está disponible a partir de Windows 10, versión 1709.
</blockquote>
<br/></td>
</tr>
<tr>
<td>TCP_KEEPINTVL</td>
<td>Sí</td>
<td>Sí</td>
<td>DWORD</td>
<td>Obtiene o establece el número de segundos que una conexión TCP esperará una respuesta keepalive antes de enviar otro sondeo keepalive.
<blockquote>
[!Note]<br />
Esta opción está disponible a partir de Windows 10, versión 1709.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>

## <a name="windows-support-for-ipproto_tcp-options"></a>Windows compatibilidad con las opciones TCP de IPPROTO \_

| Opción | Windows 10 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|
| TCP \_ BSDURGENT | x | x | x | x |
| TCP \_ EXPEDITED \_ 1122 | x | x | x | x |
| TCP \_ KEEPCNT | A partir Windows 10, versión 1703 | | | |
| TCP \_ MAXRT | x | x | x | x |
| TCP \_ NODELAY | x | x | x | x |
| MARCAS \_ DE TIEMPO TCP | x | x | x | x |
| TCP \_ FASTOPEN | A partir Windows 10, versión 1607 | | | |

<br/>

 | Opción | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-|-|-|-|-|-|
| TCP \_ BSDURGENT | x | x | x | x | |
| TCP \_ EXPEDITED \_ 1122 | x | x | x | | |
| TCP \_ KEEPCNT | | | | | |
| TCP \_ MAXRT | | | | | |
| TCP \_ NODELAY | x | x | x | x | |
| MARCAS \_ DE TIEMPO TCP | | | | | |
| TCP \_ FASTOPEN | | | | | |

## <a name="remarks"></a>Comentarios

En el Kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y el nivel TCP de **IPPROTO \_** se define en el archivo de encabezado *Ws2def.h* que se incluye automáticamente en el archivo de encabezado *Winsock2.h.* Las opciones de socket TCP de **IPPROTO, \_** a excepción de **TCP \_ BSDURGENT,** se definen en el archivo de encabezado *Ws2ipdef.h* que se incluye automáticamente en el archivo de encabezado *Ws2tcpip.h.* La **opción TCP \_ BSDURGENT** por motivos históricos se define en el archivo de encabezado *Mswsock.h.* Los *archivos de encabezado Ws2def.h* y *Ws2ipdef.h* nunca deben usarse directamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | <dl> <dt>Ws2def.h (incluye Winsock2.h);</dt> <dt>Winsock2.h en Windows Server 2003, Windows XP y Windows 2000</dt> </dl> |
