---
description: En la tabla siguiente se describen \_ las opciones de socket TCP de IPPROTO que se aplican a los sockets creados para las familias de direcciones IPv4 e IPv6 (AF \_ inet y AF \_ inet6) con el parámetro Protocol a la función socket especificada como TCP (IPPROTO \_ TCP).
ms.assetid: 2a10498d-0a0b-4a2d-941e-9aa45a1a4428
title: Opciones de socket IPPROTO_TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d261a639c10faa8c8ef52ba1ae88a0fbc52a16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708775"
---
# <a name="ipproto_tcp-socket-options"></a>\_Opciones de socket TCP de IPPROTO

En la tabla siguiente se describen las opciones de socket **\_ TCP de IPPROTO** que se aplican a los sockets creados para las familias de direcciones IPv4 e IPv6 (AF \_ inet y AF \_ inet6) con el parámetro *Protocol* a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) especificada como TCP (IPPROTO \_ TCP). Consulte las páginas de referencia de [**la función**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y el valor de My para obtener más información sobre cómo obtener y establecer las opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas de cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

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
<th>Tipo Optval</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td>TCP_BSDURGENT</td>
<td>sí</td>
<td>sí</td>
<td>DWORD (booleano)</td>
<td>Si <strong>es true</strong>, el proveedor de servicios implementa el estilo de distribución de software Berkeley (BSD) (valor predeterminado) para controlar los datos inmediatos. Esta opción es la inversa de la opción TCP_EXPEDITED_1122. Esta opción solo se puede establecer en la conexión una vez. Una vez que esta opción está establecida en ON, esta opción no se puede desactivar. No es necesario que los proveedores de servicios implementen esta opción. De forma predeterminada, la opción está habilitada (establecida en <strong>true</strong>).</td>
</tr>
<tr>
<td>TCP_EXPEDITED_1122</td>
<td>sí</td>
<td>sí</td>
<td>DWORD (booleano)</td>
<td>Si <strong>es true</strong>, el proveedor de servicios implementa los datos expedidos tal y como se especifica en RFC-1222. De lo contrario, se usa el estilo de distribución de software Berkeley (BSD) (predeterminado). Esta opción solo se puede establecer en la conexión una vez. Una vez que esta opción está establecida en ON, esta opción no se puede desactivar. No es necesario que los proveedores de servicios implementen esta opción.</td>
</tr>
<tr>
<td>TCP_FAIL_CONNECT_ON_ICMP_ERROR</td>
<td>sí</td>
<td>sí</td>
<td>DWORD (booleano)</td>
<td>Si <strong>es true</strong>, se devolverá una llamada de API de conexión tras la recepción de un error de ICMP con el valor WSAEHOSTUNREACH. La dirección de origen del error estará disponible a continuación a través de la opción socket de TCP_ICMP_ERROR_INFO. Si <strong>es false</strong>, el socket se comporta normalmente. El valor predeterminado es deshabilitado (establecido en <strong>false</strong>). Para la seguridad de tipos, debe usar las funciones <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror">WSAGetFailConnectOnIcmpError</a> y <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror">WSASetFailConnectOnIcmpError</a> en lugar de usar la opción socket directamente.</td>
</tr>
<tr>
<td>TCP_ICMP_ERROR_INFO</td>
<td>sí</td>
<td>no</td>
<td><a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a></td>
<td>Recupera la información de un error ICMP recibido por el socket TCP durante una llamada de conexión errónea. Solo es válido en un socket TCP donde se ha habilitado anteriormente TCP_FAIL_CONNECT_ON_ICMP_ERROR y <strong>Connect</strong> ha devuelto WSAEHOSTUNREACH. La consulta no está bloqueada. Si se consulta correctamente y el valor devuelto de optlen es 0, no se ha recibido ningún error ICMP desde la última llamada de conexión. Si se ha recibido un error ICMP, su información estará disponible hasta que se vuelva a llamar a la <strong>conexión</strong> . La información se devuelve como una estructura de <a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a> . Para la seguridad de tipos, debe usar la función <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo">WSAGetIcmpErrorInfo</a> en lugar de usar la opción socket directamente.</td>
</tr>
<tr>
<td>TCP_KEEPCNT</td>
<td>sí</td>
<td>sí</td>
<td>DWORD</td>
<td>Obtiene o establece el número de sondeos de mantenimiento de conexiones TCP que se enviarán antes de que finalice la conexión. No es válido establecer TCP_KEEPCNT en un valor mayor que 255.</td>
</tr>
<tr>
<td>TCP_MAXRT</td>
<td>sí</td>
<td>sí</td>
<td>DWORD</td>
<td>Si este valor no es negativo, representa el tiempo de espera de conexión deseado en segundos. Si es-1, representa una solicitud para deshabilitar el tiempo de espera de conexión (es decir, la conexión se retransmitirá de forma indefinida). Si el tiempo de espera de la conexión está deshabilitado, el tiempo de espera de retransmisión aumenta exponencialmente para cada retransmisión hasta su valor máximo de 60sec y, a continuación, permanece allí.</td>
</tr>
<tr>
<td>TCP_NODELAY</td>
<td>sí</td>
<td>sí</td>
<td>DWORD (booleano)</td>
<td>Habilita o deshabilita el algoritmo de Nagle para Sockets TCP. Esta opción está deshabilitada (establecida en FALSE) de forma predeterminada.</td>
</tr>
<tr>
<td>TCP_TIMESTAMPS</td>
<td>sí</td>
<td>sí</td>
<td>DWORD (booleano)</td>
<td>Habilita o deshabilita las marcas de tiempo de RFC 1323. Tenga en cuenta que también hay una configuración global para las marcas de tiempo (el valor predeterminado es OFF), las &quot; marcas &quot; de tiempo de (Set/Get)-nettcpsetting. Al establecer esta opción de socket, se invalida la opción de configuración global.</td>
</tr>
<tr>
<td>TCP_FASTOPEN</td>
<td>sí</td>
<td>sí</td>
<td>DWORD (booleano)</td>
<td>Habilita o deshabilita <a href="https://tools.ietf.org/html/rfc7413">RFC 7413</a> TCP Fast Open, que le permite empezar a enviar datos durante la fase de protocolo de enlace de tres vías en la que se abre una conexión. Tenga en cuenta que para hacer uso de aperturas rápidas, debe utilizar <a href="/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex"><strong>ConnectEx</strong></a> para establecer la conexión inicial y especificar los datos en el parámetro <em>lpSendBuffer</em> de la función que se va a transferir durante el proceso del Protocolo de enlace. Algunos de los datos de <em>lpSendBuffer</em> se transferirán en el protocolo de apertura rápida.</td>
</tr>
<tr>
<td>TCP_KEEPIDLE</td>
<td>sí</td>
<td>sí</td>
<td>DWORD</td>
<td>Obtiene o establece el número de segundos que una conexión TCP permanecerá inactiva antes de que se envíen sondeos keepalive al remoto.
<blockquote>
[!Note]<br />
Esta opción está disponible a partir de Windows 10, versión 1709.
</blockquote>
<br/></td>
</tr>
<tr>
<td>TCP_KEEPINTVL</td>
<td>sí</td>
<td>sí</td>
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

## <a name="windows-support-for-ipproto_tcp-options"></a>Compatibilidad de Windows con \_ las opciones de TCP de IPPROTO

| Opción | Windows 10 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|
| \_BSDURGENT TCP | x | x | x | x |
| TCP \_ acelerado \_ 1122 | x | x | x | x |
| \_KEEPCNT TCP | A partir de Windows 10, versión 1703 | | | |
| \_MAXRT TCP | x | x | x | x |
| retardo de TCP \_ | x | x | x | x |
| marcas de tiempo TCP \_ | x | x | x | x |
| \_FASTOPEN TCP | A partir de Windows 10, versión 1607 | | | |

<br/>

 | Opción | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/me |
|-|-|-|-|-|-|
| \_BSDURGENT TCP | x | x | x | x | |
| TCP \_ acelerado \_ 1122 | x | x | x | | |
| \_KEEPCNT TCP | | | | | |
| \_MAXRT TCP | | | | | |
| retardo de TCP \_ | x | x | x | x | |
| marcas de tiempo TCP \_ | | | | | |
| \_FASTOPEN TCP | | | | | |

## <a name="remarks"></a>Observaciones

En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y el nivel **\_ TCP de IPPROTO** se define en el archivo de encabezado *Ws2def. h* que se incluye automáticamente en el archivo de encabezado *WinSock2. h* . Las opciones de socket **\_ TCP IPPROTO** , con la excepción de **TCP \_ BSDURGENT**, se definen en el archivo de encabezado *Ws2ipdef. h* que se incluye automáticamente en el archivo de encabezado *Ws2tcpip. h* . La **opción \_ BSDURGENT de TCP** para los motivos históricos se define en el archivo de encabezado *mswsock. h* . Los archivos de encabezado *Ws2def. h* y *Ws2ipdef. h* nunca deben usarse directamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | <dl> <dt>Ws2def. h (incluir WinSock2. h); </dt> <dt>WinSock2. h en Windows Server 2003, Windows XP y windows 2000</dt> </dl> |
