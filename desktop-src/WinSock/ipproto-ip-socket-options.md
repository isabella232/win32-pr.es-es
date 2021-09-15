---
description: En las tablas siguientes se describen las opciones de socket IPPROTO que se aplican a los sockets creados para la familia de \_ direcciones IPv4 \_ (AF INET). Consulte las páginas de referencia de función getsockopt y setsockopt para obtener más información sobre cómo obtener y establecer las opciones de socket.
ms.assetid: 6b06a29e-59cd-4446-bd2f-131dc25bf571
title: Opciones de socket IPPROTO_IP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: b4c8daa18e7bd60e61473bdda1c885bbd163f0b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476120"
---
# <a name="ipproto_ip-socket-options"></a>Opciones de \_ socket IPPROTO

En las tablas siguientes **se describen IPPROTO_IP** de sockets que se aplican a los sockets creados para la familia de direcciones IPv4 \_ (AF INET). Consulte las [**páginas de referencia de función getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obtener más información sobre cómo obtener y establecer opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas para cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

Algunas opciones de socket requieren más explicación de la que pueden transmitir estas tablas. estas opciones contienen vínculos a páginas adicionales.

## <a name="options"></a>Opciones

| Opción | Obtener | Set | Tipo optval | Descripción |
|-|-|-|-|-|
| IP_ADD_IFLIST | | sí | DWORD (IF_INDEX) | Agrega un índice de interfaz al IFLIST asociado a la **IP_IFLIST** predeterminada. |
| IP_ADD_MEMBERSHIP | | sí | [**ip_mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Una el socket al grupo de multidifusión proporcionado en la interfaz especificada. |
| IP_ADD_SOURCE_MEMBERSHIP | | sí | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Únase al grupo de multidifusión proporcionado en la interfaz especificada y acepte los datos procedentes de la dirección de origen proporcionada. |
| ORIGEN \_ DE BLOQUE DE \_ IP | | sí | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Quita el origen especificado como remitente del grupo de multidifusión y la interfaz proporcionados. |
| IP_DEL_IFLIST | | sí | DWORD (IF_INDEX) | Quita un índice de interfaz de IFLIST asociado a la **IP_IFLIST** predeterminada. Las entradas solo las puede quitar la aplicación, por lo que debe tener en cuenta que las entradas podrían querse obsoletas una vez que se quita una interfaz. |
| \_DONTFRAGMENT DE IP | sí | sí | DWORD (booleano) | Indica que los datos no deben fragmentarse independientemente de la MTU local. Solo es válido para protocolos orientados a mensajes. Los proveedores de TCP/IP de Microsoft respetan esta opción para UDP e ICMP. |
| DROP \_ MEMBERSHIP de IP \_ | | sí | [**ip \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Sale del grupo de multidifusión especificado de la interfaz especificada. Los proveedores de servicios deben admitir esta opción cuando se admite la multidifusión. La compatibilidad se indica en la estructura [**\_ INFO de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) devuelta por una llamada de función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) con lo siguiente: XPI \_ SUPPORT \_ MULTIPOINT=1, XP1 \_ MULTIPOINT \_ CONTROL \_ PLANE=0, XP1 \_ MULTIPOINT DATA \_ \_ PLANE=0. |
| PERTENENCIA AL \_ ORIGEN \_ DE DROP DE IP \_ | | sí | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Quita la pertenencia al grupo de multidifusión, la interfaz y la dirección de origen dados. |
| IP_GET_IFLIST | sí | | DWORD[] (IF_INDEX[]) | Obtiene el IFLIST actual asociado a la **IP_IFLIST** actual. Devuelve un error **si IP_IFLIST** no está habilitado. |
| IP \_ HDRINCL | sí | sí | DWORD (booleano) | Cuando se establece en **TRUE**, indica que la aplicación proporciona el encabezado IP. Solo se aplica a los \_ sockets SOCK RAW. El proveedor de servicios TCP/IP puede establecer el campo id. si el valor proporcionado por la aplicación es cero.  La opción \_ IP HDRINCL solo se aplica al tipo \_ DE PROTOCOLO SOCK RAW. Un proveedor de servicios TCP/IP que admita SOCK \_ RAW también debe admitir IP \_ HDRINCL.  |
| IP_IFLIST | sí | sí | DWORD (booleano) | Obtiene o establece el **IP_IFLIST** del socket. Cuando esta opción se establece en true, la recepción de datagramas se restringe a las interfaces que se encuentran en IFLIST. Los datagramas recibidos en cualquier otra interfaz se omiten. IFLIST se inicia vacío. Use **IP_ADD_IFLIST** y **IP_DEL_IFLIST** para editar IFLIST. |
| MTU \_ de IP | sí | | DWORD | Obtiene la estimación del sistema de la MTU de ruta de acceso. El socket debe estar conectado. |
| MTU \_ DISCOVER de IP \_ | sí | sí | DWORD (**PMTUD \_ STATE**) | Obtiene o establece el estado de detección de MTU de la ruta de acceso para el socket. El valor predeterminado es **IP \_ PMTUDISC \_ NOT \_ SET.** Para los sockets de secuencia, **IP \_ PMTUDISC \_ NOT \_ SET** e **IP \_ PMTUDISC \_ DO** realizarán la detección de MTU de ruta de acceso. **IP \_ PMTUDISC \_ DONT** e **IP \_ PMTUDISC \_ PROBE** desactivarán la detección de MTU de ruta de acceso. En el caso de los sockets de datagramas, **IP \_ PMTUDISC \_ DO** obligará a todos los paquetes salientes a tener el conjunto de bits DF y un intento de enviar paquetes mayores que la ruta de acceso MTU producirá un error. **IP \_ PMTUDISC \_ DONT** forzará que todos los paquetes salientes tengan el bit DF no establecido y los paquetes se fragmentarán según la MTU de interfaz. **IP \_ PMTUDISC \_ PROBE** forzará que todos los paquetes salientes tengan el conjunto de bits DF y un intento de enviar paquetes mayores que la MTU de interfaz producirá un error. |
| IP \_ MULTICAST \_ IF | sí | sí | DWORD | Obtiene o establece la interfaz saliente para enviar tráfico de multidifusión IPv4. Esta opción no cambia la interfaz predeterminada para recibir tráfico de multidifusión IPv4.  El valor de entrada para establecer esta opción es una dirección IPv4 de 4 bytes en orden de bytes de red. Este parámetro DWORD también puede ser un índice de interfaz en orden de bytes de red. Cualquier dirección IP del bloque 0.x.x.x (primer octeto de 0), excepto la dirección IPv4 0.0.0.0, se trata como un índice de interfaz. Un índice de interfaz es un número de 24 bits y no se usa el bloque de direcciones IPv4 0.0.0.0/8 (este intervalo está reservado). El índice de interfaz se puede usar para especificar la interfaz predeterminada para el tráfico de multidifusión para IPv4. Si *optval* es cero, se especifica la interfaz predeterminada para recibir multidifusión para enviar tráfico de multidifusión.  Al obtener esta opción, *optval* devuelve el índice de interfaz predeterminado actual para enviar tráfico IPv4 de multidifusión en orden de bytes del host. |
| BUCLE DE \_ MULTIDIFUSIÓN \_ IP | sí | sí | DWORD (booleano) | Controla si los datos enviados por una aplicación en el equipo local (no necesariamente por el mismo socket) de una sesión de multidifusión serán recibidos por un socket unido al grupo de destino de multidifusión en la interfaz de bucle atrás. Un valor **TRUE hace que** los datos de multidifusión enviados por una aplicación en el equipo local se entreguen a un socket de escucha en la interfaz de bucles bucles. Un valor **FALSE impide que** los datos de multidifusión enviados por una aplicación en el equipo local se entreguen a un socket de escucha en la interfaz de bucles bucles. De forma predeterminada, **EL \_ BUCLE DE \_ MULTIDIFUSIÓN DE IP** está habilitado. |
| TTL \_ de \_ MULTIDIFUSIÓN IP | sí | sí | DWORD | Establece o obtiene el valor TTL asociado al tráfico de multidifusión IP en el socket. |
| OPCIONES DE \_ IP | sí | sí | Char \[\] | Especifica las opciones de IP que se insertarán en los paquetes salientes. Al establecer nuevas opciones, se sobrescriben todas las opciones especificadas anteriormente. Si se establece optval en cero, se quitan todas las opciones especificadas anteriormente. No se requiere compatibilidad con IP OPTIONS; para comprobar si se admite \_ IP \_ OPTIONS, use [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para obtener las opciones actuales. Si **se produce un error en getsockopt,** no se admite IP \_ OPTIONS. |
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | sí | sí | DWORD (booleano) | Indica si la LPFN_WSARECVMSG [**(WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) debe devolver datos de control opcionales que contengan la interfaz de llegada donde se recibió el paquete para los sockets de datagramas. Esta opción permite que la interfaz IPv4 donde se recibió el paquete se devuelva en la [**estructura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)  Esta opción solo es válida en datagramas y sockets sin procesar (el tipo de socket debe ser SOCK \_ DGRAM o SOCK \_ RAW). |
| [IP \_ PKTINFO](ip-pktinfo.md) | sí | sí | DWORD | Indica que la función **WSARecvMsg** debe devolver la información del paquete. |
| DIFUSIÓN \_ DE RECEPCIÓN \_ DE IP | sí | sí | DWORD (booleano) | Permite o bloquea la recepción de difusión. |
| RECVIF de IP \_ | sí | sí | DWORD (booleano) | Indica si la pila ip debe rellenar el búfer de control con detalles sobre qué interfaz recibió un paquete con un socket de datagrama. Cuando este valor es true, la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devolverá datos de control opcionales que contienen la interfaz donde se recibió el paquete para los sockets de datagrama. Esta opción permite que la interfaz IPv4 donde se recibió el paquete se devuelva en la [**estructura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)  Esta opción solo es válida en datagramas y sockets sin procesar (el tipo de socket debe ser SOCK \_ DGRAM o SOCK \_ RAW). |
| \_RECVTOS DE IP | sí | sí | DWORD (booleano) | Indica si la pila ip debe rellenar el búfer de control con un mensaje que contiene el campo de encabezado IPv4 tipo de servicio (TOS) en un datagrama recibido. Cuando este valor es true, la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devolverá datos de control opcionales que contienen el valor del campo de encabezado IPv4 de TOS del datagrama recibido.  Esta opción permite que el campo de encabezado IPv4 de TOS del datagrama recibido se devuelva en la [**estructura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) El tipo de mensaje devuelto será IP \_ TOS. Se devolverán todos los bits DSCP y ECN del campo TOS.  Esta opción solo es válida en los sockets de datagramas (el tipo de socket debe ser SOCK \_ DGRAM).  |
| RECVTTL de IP \_ | sí | sí | DWORD (booleano) | Indica que se debe devolver información de salto (TTL) en [**la LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Si *optval* se establece en **1 en** la llamada a [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), la opción está habilitada. Si se establece en **0**, la opción está deshabilitada.  Esta opción solo es válida para datagramas y sockets sin procesar (el tipo de socket debe ser SOCK \_ DGRAM o SOCK \_ RAW). |
| IP \_ TOS | sí | sí | DWORD (booleano) | No debe usarse. La configuración del tipo de servicio (TOS) solo debe establecerse mediante la API de calidad de servicio. Consulte [Servicios diferenciados](/previous-versions/windows/desktop/qos/differentiated-services) en la sección Calidad de servicio del SDK de plataforma para obtener más información. |
| TTL de IP \_ | sí | sí | DWORD (booleano) | Cambia el valor predeterminado establecido por el proveedor de servicios TCP/IP en el campo TTL del encabezado IP en datagramas salientes. La compatibilidad con TTL de IP no es necesaria; para comprobar si se admite el TTL de \_ \_ IP, use [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para obtener las opciones actuales. Si **se produce un error en getsockopt,** no se admite el \_ TTL de IP. |
| ORIGEN \_ DE DESBLOQUEO DE \_ IP | | sí | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Agrega el origen especificado como remitente al grupo de multidifusión y la interfaz proporcionados. |
| IP \_ UNICAST \_ IF | sí | sí | DWORD (IF \_ INDEX) | Obtiene o establece la interfaz saliente para enviar tráfico IPv4. Esta opción no cambia la interfaz predeterminada para recibir tráfico IPv4. Esta opción es importante para los equipos de varios equipos de casa.  El valor de entrada para establecer esta opción es una dirección IPv4 de 4 bytes en orden de bytes de red. Este parámetro DWORD debe ser un índice de interfaz en orden de bytes de red. Cualquier dirección IP del bloque 0.x.x.x (primer octeto de 0), excepto la dirección IPv4 0.0.0.0, se trata como un índice de interfaz. Un índice de interfaz es un número de 24 bits y no se usa el bloque de direcciones IPv4 0.0.0.0/8 (este intervalo está reservado). El índice de interfaz se puede usar para especificar la interfaz predeterminada para enviar tráfico para IPv4. La [**función GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) se puede usar para obtener la información del índice de interfaz. Si *optval* es cero, la interfaz predeterminada para enviar tráfico se establece en unspecified.  Al obtener esta opción, el *optval* devuelve el índice de interfaz predeterminado actual para enviar tráfico IPv4 en el orden de bytes del host. |
| IP_USER_MTU | sí | sí | DWORD | Obtiene o establece un límite superior en la MTU de la capa IP (en bytes) para el socket dado. Si el valor es mayor que la estimación del sistema de la ruta de acceso MTU (que puede recuperar en un socket conectado consultando la opción de socket **IP_MTU),** la opción no tiene ningún efecto. Si el valor es inferior, los paquetes salientes mayores que este se fragmentarán o no se enviarán, dependiendo del valor de **IP_DONTFRAGMENT**. El valor predeterminado **es IP_UNSPECIFIED_USER_MTU** (MAXULONG). Para la seguridad de tipos, debe usar las funciones [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) y [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) en lugar de usar directamente la opción de socket. |
| CONTEXTO DE \_ REDIRECCIÓN DE WFP \_ DE \_ IP | sí | sí | WSACMSGHDR con datos de control | Un tipo de datos auxiliar de socket de datagrama (tipo cmsg) para indicar el contexto de redireccionamiento de un socket UDP usado por un modo de usuario Windows el servicio de redirección de la Plataforma de filtrado de datos \_ (WFP). |
| REGISTROS DE \_ REDIRECCIÓN DE WFP \_ DE \_ IP | sí | sí | WSACMSGHDR con datos de control | Tipo de datos auxiliar de socket de datagrama (tipo cmsg) para indicar el registro de redireccionamiento de un socket UDP usado por un modo de usuario Windows el servicio de redirección de la Plataforma de filtrado de datos \_ (WFP). |

## <a name="windows-support-for-ip_proto-options"></a>Windows compatibilidad con las opciones de \_ IP PROTO

| Opción | Windows 10 | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|-|
| IP_ADD_IFLIST | A partir Windows 10, versión 1803 | | | | | |
| AGREGAR \_ PERTENENCIA A \_ IP | x | x | x | x | x | x |
| PERTENENCIA \_ A ORIGEN DE \_ ADICIÓN DE \_ IP | x | x | x | x | x | x |
| ORIGEN \_ DEL BLOQUE \_ IP | x | x | x | x | x | x |
| IP_DEL_IFLIST | A partir Windows 10, versión 1803 | | | | | |
| \_DONTFRAGMENT DE IP | x | x | x | x | x | x |
| PERTENENCIA \_ A DROP DE IP \_ | x | x | x | x | x | x |
| PERTENENCIA AL \_ ORIGEN \_ DE COLOCACIÓN DE \_ IP | x | x | x | x | x | x |
| IP_GET_IFLIST | A partir Windows 10, versión 1803 | | | | | |
| IP \_ HDRINCL | x | x | x | x | x | x |
| IP_IFLIST | A partir Windows 10, versión 1803 | | | | | |
| IP \_ MULTICAST \_ IF | x | x | x | x | x | x |
| BUCLE DE \_ MULTIDIFUSIÓN \_ IP | x | x | x | x | x | x |
| TTL \_ de \_ MULTIDIFUSIÓN IP | x | x | x | x | x | x |
| OPCIONES DE \_ IP | x | x | x | x | x | x |
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | x | x | x | x | | |
| IP \_ PKTINFO | x | x | x | x | x | x |
| DIFUSIÓN \_ DE RECEPCIÓN \_ DE IP | x | x | x | x | x | x |
| RECVIF de IP \_ | A partir Windows 10, versión 1703 | x | x | x | x | x |
| RECVTTL de IP \_ | x | | | | | |
| IP \_ TOS | x | x | x | | | |
| TTL de IP \_ | x | x | x | x | x | x |
| ORIGEN \_ DE DESBLOQUEO DE \_ IP | x | x | x | x | x | x |
| IP \_ UNICAST \_ IF | x | x | x | x | x | x |
| CONTEXTO DE \_ REDIRECCIÓN DE WFP \_ DE \_ IP | x | x | x | | | |
| REGISTROS DE \_ REDIRECCIÓN DE WFP \_ DE \_ IP | x | x | x | | | |

<br/>

| Opción | Windows Server 2003 | Windows XP |
|-|-|-|
| IP_ADD_IFLIST | | |
| AGREGAR PERTENENCIA A IP \_ \_ | x | x |
| IP \_ ADD \_ SOURCE \_ MEMBERSHIP | x | x |
| ORIGEN \_ DE BLOQUE DE \_ IP | x | x |
| IP_DEL_IFLIST | | |
| \_DONTFRAGMENT DE IP | x | x |
| DROP \_ MEMBERSHIP de IP \_ | x | x |
| PERTENENCIA AL \_ ORIGEN \_ DE DROP DE IP \_ | x | x |
| IP_GET_IFLIST | | |
| IP \_ HDRINCL | x | x |
| IP_IFLIST | | |
| IP \_ MULTICAST \_ IF | x | x |
| BUCLE DE \_ MULTIDIFUSIÓN \_ IP | x | x |
| TTL \_ de \_ MULTIDIFUSIÓN IP | x | x |
| OPCIONES DE \_ IP | x | x |
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | | |
| IP \_ PKTINFO | x | x |
| DIFUSIÓN \_ DE RECEPCIÓN \_ DE IP | x | x |
| RECVIF de IP \_ | | |
| RECVTTL de IP \_ | | |
| IP \_ TOS | | |
| TTL de IP \_ | x | x |
| ORIGEN \_ DE DESBLOQUEO DE \_ IP | x | x |
| IP \_ UNICAST \_ IF | | |
| CONTEXTO DE \_ REDIRECCIÓN DE WFP \_ DE \_ IP | | |
| REGISTROS DE \_ REDIRECCIÓN DE WFP \_ DE \_ IP | | |

## <a name="remarks"></a>Observaciones

En el Kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y el nivel **\_ IP DE IPPROTO** se define en el archivo de encabezado *Ws2def.h* que se incluye automáticamente en el archivo de encabezado *Winsock2.h.* Algunas de las opciones de socket **IP DE \_ IPPROTO** se definen en el archivo de encabezado *Ws2ipdef.h,* que se incluye automáticamente en el archivo de encabezado *Ws2tcpip.h.* Las restantes opciones de socket **\_ IPPROTO se** definen en el archivo de encabezado *Wsipv6ok.h,* que se incluye automáticamente en el archivo de encabezado *Winsock2.h.* Los archivos de encabezado *Ws2def.h*, *Ws2ipdef.h y* *Wsipv6ok.h* nunca se deben usar directamente.

En el SDK de plataforma publicado para Windows Server 2003 y Windows XP, el nivel **\_ ip de IPPROTO** se define en el archivo de encabezado *Winsock2.h.* Algunas de las **opciones de socket IP DE \_ IPPROTO** se definen en el *archivo de encabezado Ws2tcpip.h.* Las restantes opciones de socket **\_ IPPROTO se** definen en el archivo de encabezado *Wsipv6ok.h,* que se incluye automáticamente en el archivo de encabezado *Winsock2.h.* El *archivo de encabezado Wsipv6ok.h* nunca se debe usar directamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | <dl> <dt>Ws2def.h (incluye Winsock2.h); </dt> <dt>Ws2ipdef.h (incluye Ws2tcpip.h); </dt> <dt>Wsipv6ok.h (incluye Winsock2.h)</dt> </dl> |
