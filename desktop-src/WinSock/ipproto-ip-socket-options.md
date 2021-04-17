---
description: En las tablas siguientes \_ se describen las opciones de socket IP de IPPROTO que se aplican a los sockets creados para la familia de direcciones IPv4 (AF \_ inet). Consulte las páginas de referencia de la función getsockopt y el valor de My para obtener más información sobre cómo obtener y establecer las opciones de socket.
ms.assetid: 6b06a29e-59cd-4446-bd2f-131dc25bf571
title: Opciones de socket IPPROTO_IP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: b4c8daa18e7bd60e61473bdda1c885bbd163f0b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708658"
---
# <a name="ipproto_ip-socket-options"></a>\_Opciones de socket IP IPPROTO

En las tablas siguientes se describen **IPPROTO_IP** opciones de socket que se aplican a los sockets creados para la familia de direcciones IPv4 (AF \_ inet). Consulte las páginas de referencia de [**la función**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y el valor de My para obtener más información sobre cómo obtener y establecer las opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas de cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

Algunas opciones de socket requieren más explicación de lo que pueden transmitir estas tablas; Estas opciones contienen vínculos a páginas adicionales.

## <a name="options"></a>Opciones

| Opción | Obtener | Set | Tipo Optval | Descripción |
|-|-|-|-|-|
| IP_ADD_IFLIST | | sí | DWORD (IF_INDEX) | Agrega un índice de interfaz al IFLIST asociado a la opción **IP_IFLIST** . |
| IP_ADD_MEMBERSHIP | | sí | [**ip_mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Una el socket al grupo de multidifusión proporcionado en la interfaz especificada. |
| IP_ADD_SOURCE_MEMBERSHIP | | sí | [**\_origen de mreq IP \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Unir el grupo de multidifusión proporcionado en la interfaz especificada y aceptar los datos procedentes de la dirección de origen proporcionada. |
| \_origen de bloque de IP \_ | | sí | [**\_origen de mreq IP \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Quita el origen especificado como remitente del grupo de multidifusión y la interfaz proporcionados. |
| IP_DEL_IFLIST | | sí | DWORD (IF_INDEX) | Quita un índice de interfaz del IFLIST asociado a la opción **IP_IFLIST** . Solo la aplicación puede quitar las entradas, por lo que debe tener en cuenta que las entradas pueden quedar obsoletas una vez que se quita una interfaz. |
| \_DONTFRAGMENT IP | sí | sí | DWORD (booleano) | Indica que los datos no se deben fragmentar independientemente de la MTU local. Solo es válido para los protocolos orientados a mensajes. Los proveedores de Microsoft TCP/IP respetan esta opción para UDP e ICMP. |
| pertenencia de drop de IP \_ \_ | | sí | [**\_mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Deja el grupo de multidifusión especificado de la interfaz especificada. Los proveedores de servicios deben admitir esta opción cuando se admita la multidifusión. La compatibilidad se indica en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) devuelta por una llamada de función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) con lo siguiente: XPI admite MULTIpoint \_ \_ = 1, XP1 \_ Multipoint \_ control \_ Plane = 0, XP1 \_ Multipoint \_ Data \_ Plane = 0. |
| \_pertenencia \_ al origen de eliminación de IP \_ | | sí | [**\_origen de mreq IP \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Quita la pertenencia al grupo de multidifusión, la interfaz y la dirección de origen especificados. |
| IP_GET_IFLIST | sí | | DWORD [] (IF_INDEX []) | Obtiene el IFLIST actual asociado a la opción **IP_IFLIST** . Devuelve un error si **IP_IFLIST** no está habilitado. |
| \_HDRINCL IP | sí | sí | DWORD (booleano) | Cuando se establece en **true**, indica que la aplicación proporciona el encabezado IP. Solo se aplica a los \_ Sockets sin formato sock. El proveedor de servicios TCP/IP puede establecer el campo ID si el valor proporcionado por la aplicación es cero.  La \_ opción HDRINCL de IP solo se aplica al \_ tipo de protocolo sock RAW. Un proveedor de servicios TCP/IP que admita SOCK \_ raw debe admitir también \_ HDRINCL de IP.  |
| IP_IFLIST | sí | sí | DWORD (booleano) | Obtiene o establece el estado **IP_IFLIST** del socket. Cuando esta opción se establece en true, la recepción de datagramas se restringe a las interfaces que se encuentran en IFLIST. Se omiten los datagramas recibidos en otras interfaces. IFLIST se inicia vacío. Use **IP_ADD_IFLIST** y **IP_DEL_IFLIST** para editar IFLIST. |
| MTU de IP \_ | sí | | DWORD | Obtiene la estimación del sistema de la MTU de la ruta de acceso. Socket debe estar conectado. |
| \_detección de MTU de IP \_ | sí | sí | DWORD (**\_ Estado de PMTUD**) | Obtiene o establece el estado de detección de MTU de la ruta de acceso para el socket. El valor predeterminado es **IP \_ PMTUDISC \_ not \_ set**. En el caso de los sockets de secuencias, **\_ no se \_ \_ establece PMTUDISC de IP** y **PMTUDISC de IP \_ \_** realizará la detección de MTU. **Dirección IP \_ El \_** **\_ \_ sondeo** PMTUDISC no y PMTUDISC IP desactivará la detección de MTU de ruta de acceso. En el caso de los sockets de datagrama, las **\_ \_ PMTUDISC IP** obligarán a que todos los paquetes salientes tengan el bit de DF establecido y un intento de enviar paquetes mayores que la MTU de ruta de acceso producirá un error. **Dirección IP \_ PMTUDISC \_** no obligará a que todos los paquetes salientes tengan el bit DF sin establecer y los paquetes se fragmentarán según la MTU de la interfaz. **Dirección IP \_ El \_ sondeo PMTUDISC** obligará a que todos los paquetes salientes tengan el bit DF establecido y un intento de enviar paquetes mayores que la MTU de la interfaz producirá un error. |
| multidifusión IP \_ \_ si | sí | sí | DWORD | Obtiene o establece la interfaz de salida para enviar el tráfico de multidifusión IPv4. Esta opción no cambia la interfaz predeterminada para recibir tráfico IPv4 de multidifusión.  El valor de entrada para establecer esta opción es una dirección IPv4 de 4 bytes en el orden de bytes de la red. Este parámetro DWORD también puede ser un índice de interfaz en el orden de bytes de la red. Cualquier dirección IP en el bloque 0. x. x. x (primer octeto de 0), excepto la dirección IPv4 0.0.0.0, se trata como un índice de interfaz. Un índice de interfaz es un número de 24 bits y no se usa el bloque de direcciones IPv4 por 0.0.0.0/8 (este intervalo está reservado). El índice de interfaz se puede usar para especificar la interfaz predeterminada para el tráfico de multidifusión para IPv4. Si *optval* es cero, se especifica la interfaz predeterminada para recibir multidifusión para enviar el tráfico de multidifusión.  Al obtener esta opción, *optval* devuelve el índice de interfaz predeterminado actual para enviar tráfico IPv4 de multidifusión en el orden de bytes del host. |
| \_bucle de multidifusión IP \_ | sí | sí | DWORD (booleano) | Controla si los datos enviados por una aplicación en el equipo local (no necesariamente por el mismo socket) en una sesión de multidifusión se recibirán mediante un socket unido al grupo de destino de multidifusión en la interfaz de bucle invertido. Un valor de **true** hace que los datos de multidifusión enviados por una aplicación en el equipo local se entreguen a un socket de escucha en la interfaz de bucle invertido. Un valor de **false** evita que los datos de multidifusión enviados por una aplicación en el equipo local se entreguen a un socket de escucha en la interfaz de bucle invertido. De forma predeterminada, se habilita el **\_ \_ bucle invertido de multidifusión IP** . |
| \_TTL de multidifusión IP \_ | sí | sí | DWORD | Establece u obtiene el valor de TTL asociado al tráfico de multidifusión IP en el socket. |
| Opciones de IP \_ | sí | sí | Juegos \[\] | Especifica las opciones IP que se van a insertar en los paquetes salientes. Al establecer nuevas opciones se sobrescriben todas las opciones especificadas anteriormente. Si se establece optval en cero, se quitan todas las opciones especificadas anteriormente. \_No es necesaria la compatibilidad con las opciones de IP; para comprobar si \_ se admiten las opciones de IP, use [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para obtener las opciones actuales. Si **getsockopt** produce un error, \_ no se admiten las opciones de IP. |
| \_llegada original de IP \_ \_ si | sí | sí | DWORD (booleano) | Indica si la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) debe devolver datos de control opcionales que contengan la interfaz de llegada en la que se recibió el paquete para Sockets de datagrama. Esta opción permite que la interfaz IPv4 en la que se recibió el paquete se devuelva en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Esta opción solo es válida en los sockets de datagrama y sin formato (el tipo de socket debe ser SOCK \_ DGRAM o sock \_ raw). |
| [\_PKTINFO IP](ip-pktinfo.md) | sí | sí | DWORD | Indica que la función **WSARecvMsg** debe devolver información de paquetes. |
| \_difusión de recepción de IP \_ | sí | sí | DWORD (booleano) | Permite o bloquea la recepción de difusión. |
| \_RECVIF IP | sí | sí | DWORD (booleano) | Indica si la pila IP debe rellenar el búfer de control con detalles sobre la interfaz que ha recibido un paquete con un socket de datagrama. Cuando este valor es true, la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devolverá datos de control opcionales que contienen la interfaz en la que se recibió el paquete para Sockets de datagrama. Esta opción permite que la interfaz IPv4 en la que se recibió el paquete se devuelva en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Esta opción solo es válida en los sockets de datagrama y sin formato (el tipo de socket debe ser SOCK \_ DGRAM o sock \_ raw). |
| \_RECVTOS IP | sí | sí | DWORD (booleano) | Indica si la pila IP debe rellenar el búfer de control con un mensaje que contenga el campo de encabezado IPv4 del tipo de servicio (TOS) en un datagrama recibido. Cuando este valor es true, la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devolverá datos de control opcionales que contienen el valor del campo de encabezado IPv4 de tos del datagrama recibido.  Esta opción permite que el campo de encabezado IPv4 de TOS del datagrama recibido se devuelva en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) . El tipo de mensaje devuelto será el tos de IP \_ . Se devolverán todos los bits de DSCP y ECN del campo TOS.  Esta opción solo es válida en sockets de datagramas (el tipo de socket debe ser SOCK \_ DGRAM).  |
| \_RECVTTL IP | sí | sí | DWORD (booleano) | Indica que se debe devolver información de salto (TTL) en la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . Si *optval* se establece en **1** en la llamada a el [**valor de la opción, la**](/windows/desktop/api/winsock/nf-winsock-setsockopt)opción está habilitada. Si se establece en **0**, la opción está deshabilitada.  Esta opción solo es válida para los sockets de datagrama y sin formato (el tipo de socket debe ser SOCK \_ DGRAM o sock \_ raw). |
| TOS de IP \_ | sí | sí | DWORD (booleano) | No debe usarse. La configuración de tipo de servicio (TOS) solo debe establecerse mediante la API de calidad de servicio. Consulte [servicios diferenciados](/previous-versions/windows/desktop/qos/differentiated-services) en la sección Quality of Service del SDK de la plataforma para obtener más información. |
| TTL de IP \_ | sí | sí | DWORD (booleano) | Cambia el valor predeterminado establecido por el proveedor de servicios TCP/IP en el campo TTL del encabezado IP de los datagramas salientes. \_No es necesaria la compatibilidad con TTL de IP; para comprobar si \_ se admite TTL de IP, use [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para obtener las opciones actuales. Si **getsockopt** produce un error, \_ no se admite el TTL de IP. |
| \_origen de DESbloqueo de IP \_ | | sí | [**\_origen de mreq IP \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Agrega el origen especificado como remitente a la interfaz y al grupo de multidifusión proporcionado. |
| \_UNIDIFUSIÓN IP \_ si | sí | sí | DWORD (si es un \_ Índice) | Obtiene o establece la interfaz de salida para enviar el tráfico IPv4. Esta opción no cambia la interfaz predeterminada para recibir tráfico IPv4. Esta opción es importante para los equipos de host múltiple.  El valor de entrada para establecer esta opción es una dirección IPv4 de 4 bytes en el orden de bytes de la red. Este parámetro DWORD debe ser un índice de interfaz en el orden de bytes de la red. Cualquier dirección IP en el bloque 0. x. x. x (primer octeto de 0), excepto la dirección IPv4 0.0.0.0, se trata como un índice de interfaz. Un índice de interfaz es un número de 24 bits y no se usa el bloque de direcciones IPv4 por 0.0.0.0/8 (este intervalo está reservado). El índice de interfaz se puede usar para especificar la interfaz predeterminada para enviar tráfico para IPv4. La función [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) se puede usar para obtener la información del índice de la interfaz. Si *optval* es cero, la interfaz predeterminada para enviar tráfico está establecida en sin especificar.  Al obtener esta opción, *optval* devuelve el índice de interfaz predeterminado actual para enviar tráfico IPv4 en el orden de bytes del host. |
| IP_USER_MTU | sí | sí | DWORD | Obtiene o establece un límite superior en la MTU de nivel IP (en bytes) para el socket especificado. Si el valor es mayor que la estimación del sistema de la MTU de la ruta de acceso (que se puede recuperar en un socket conectado mediante una consulta a la opción de socket de **IP_MTU** ), la opción no tiene ningún efecto. Si el valor es menor, los paquetes salientes mayores que este se fragmentarán o no se enviarán, dependiendo del valor de **IP_DONTFRAGMENT**. El valor predeterminado es **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Para la seguridad de tipos, debe usar las funciones [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) y [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) en lugar de usar la opción socket directamente. |
| \_contexto de \_ redireccionamiento de WFP IP \_ | sí | sí | WSACMSGHDR con datos de control | Un tipo de datos auxiliar de socket de datagrama ( \_ tipo cmsg) para indicar el contexto de redirección para un socket UDP utilizado por un servicio de redireccionamiento de la plataforma de filtrado de Windows (WFP) en modo de usuario. |
| \_registros de \_ redirección de WFP de IP \_ | sí | sí | WSACMSGHDR con datos de control | Un tipo de datos auxiliar de socket de datagrama ( \_ tipo cmsg) para indicar el registro de redireccionamiento para un socket UDP utilizado por un servicio de redireccionamiento de la plataforma de filtrado de Windows (WFP) de modo de usuario. |

## <a name="windows-support-for-ip_proto-options"></a>Compatibilidad de Windows con \_ las opciones de IP proto

| Opción | Windows 10 | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|-|
| IP_ADD_IFLIST | A partir de Windows 10, versión 1803 | | | | | |
| \_agregar \_ pertenencia de IP | x | x | x | x | x | x |
| \_pertenencia \_ al origen de adición de IP \_ | x | x | x | x | x | x |
| \_origen de bloque de IP \_ | x | x | x | x | x | x |
| IP_DEL_IFLIST | A partir de Windows 10, versión 1803 | | | | | |
| \_DONTFRAGMENT IP | x | x | x | x | x | x |
| pertenencia de drop de IP \_ \_ | x | x | x | x | x | x |
| \_pertenencia \_ al origen de eliminación de IP \_ | x | x | x | x | x | x |
| IP_GET_IFLIST | A partir de Windows 10, versión 1803 | | | | | |
| \_HDRINCL IP | x | x | x | x | x | x |
| IP_IFLIST | A partir de Windows 10, versión 1803 | | | | | |
| multidifusión IP \_ \_ si | x | x | x | x | x | x |
| \_bucle de multidifusión IP \_ | x | x | x | x | x | x |
| \_TTL de multidifusión IP \_ | x | x | x | x | x | x |
| Opciones de IP \_ | x | x | x | x | x | x |
| \_llegada original de IP \_ \_ si | x | x | x | x | | |
| \_PKTINFO IP | x | x | x | x | x | x |
| \_difusión de recepción de IP \_ | x | x | x | x | x | x |
| \_RECVIF IP | A partir de Windows 10, versión 1703 | x | x | x | x | x |
| \_RECVTTL IP | x | | | | | |
| TOS de IP \_ | x | x | x | | | |
| TTL de IP \_ | x | x | x | x | x | x |
| \_origen de DESbloqueo de IP \_ | x | x | x | x | x | x |
| \_UNIDIFUSIÓN IP \_ si | x | x | x | x | x | x |
| \_contexto de \_ redireccionamiento de WFP IP \_ | x | x | x | | | |
| \_registros de \_ redirección de WFP de IP \_ | x | x | x | | | |

<br/>

| Opción | Windows Server 2003 | Windows XP |
|-|-|-|
| IP_ADD_IFLIST | | |
| \_agregar \_ pertenencia de IP | x | x |
| \_pertenencia \_ al origen de adición de IP \_ | x | x |
| \_origen de bloque de IP \_ | x | x |
| IP_DEL_IFLIST | | |
| \_DONTFRAGMENT IP | x | x |
| pertenencia de drop de IP \_ \_ | x | x |
| \_pertenencia \_ al origen de eliminación de IP \_ | x | x |
| IP_GET_IFLIST | | |
| \_HDRINCL IP | x | x |
| IP_IFLIST | | |
| multidifusión IP \_ \_ si | x | x |
| \_bucle de multidifusión IP \_ | x | x |
| \_TTL de multidifusión IP \_ | x | x |
| Opciones de IP \_ | x | x |
| \_llegada original de IP \_ \_ si | | |
| \_PKTINFO IP | x | x |
| \_difusión de recepción de IP \_ | x | x |
| \_RECVIF IP | | |
| \_RECVTTL IP | | |
| TOS de IP \_ | | |
| TTL de IP \_ | x | x |
| \_origen de DESbloqueo de IP \_ | x | x |
| \_UNIDIFUSIÓN IP \_ si | | |
| \_contexto de \_ redireccionamiento de WFP IP \_ | | |
| \_registros de \_ redirección de WFP de IP \_ | | |

## <a name="remarks"></a>Observaciones

En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y el nivel de **\_ IP IPPROTO** se define en el archivo de encabezado *Ws2def. h* que se incluye automáticamente en el archivo de encabezado *WinSock2. h* . Algunas de las opciones de socket **\_ IP de IPPROTO** se definen en el archivo de encabezado *Ws2ipdef. h* que se incluye automáticamente en el archivo de encabezado *Ws2tcpip. h* . Las demás opciones de socket **\_ IP de IPPROTO** se definen en el archivo de encabezado *Wsipv6ok. h* que se incluye automáticamente en el archivo de encabezado *WinSock2. h* . Los archivos de encabezado *Ws2def. h*, *Ws2ipdef. h* y *Wsipv6ok. h* nunca deben usarse directamente.

En el SDK de la plataforma publicado para Windows Server 2003 y Windows XP, el nivel de **\_ IP de IPPROTO** se define en el archivo de encabezado *WinSock2. h* . Algunas de las opciones de socket **\_ IP de IPPROTO** se definen en el archivo de encabezado *Ws2tcpip. h* . Las demás opciones de socket **\_ IP de IPPROTO** se definen en el archivo de encabezado *Wsipv6ok. h* que se incluye automáticamente en el archivo de encabezado *WinSock2. h* . El archivo de encabezado *Wsipv6ok. h* nunca debe usarse directamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | <dl> <dt>Ws2def. h (incluir WinSock2. h); </dt> <dt>Ws2ipdef. h (incluye Ws2tcpip. h); </dt> <dt>Wsipv6ok. h (incluir WinSock2. h)</dt> </dl> |
