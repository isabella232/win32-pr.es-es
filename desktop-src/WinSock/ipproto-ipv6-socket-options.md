---
description: En las tablas siguientes \_ se describen las opciones de socket de IPv6 de IPPROTO que se aplican a los sockets creados para la familia de direcciones IPv6 (AF \_ inet6). Consulte las páginas de referencia de la función getsockopt y el valor de My para obtener más información sobre cómo obtener y establecer las opciones de socket.
ms.assetid: 65f8f7a4-757b-43a3-9d47-b115754c89d6
title: Opciones de socket IPPROTO_IPV6
ms.topic: article
ms.date: 10/07/2019
ms.openlocfilehash: 1ceaf08c2a59a24b9ff694ac9ff42b28fbf18480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718747"
---
# <a name="ipproto_ipv6-socket-options"></a>Opciones de socket de IPv6 de IPPROTO \_

En las tablas siguientes se describen las opciones de socket de **\_ IPv6 de IPPROTO** que se aplican a los sockets creados para la familia de direcciones IPv6 (AF \_ inet6). Consulte las páginas de referencia de [**la función**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y el valor de My para obtener más información sobre cómo obtener y establecer las opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas de cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

Algunas opciones de socket requieren más explicación de lo que pueden transmitir estas tablas; Estas opciones contienen vínculos a información adicional.

## <a name="options"></a>Opciones

| Opción | get | set | Tipo Optval | Descripción |
|-|-|-|-|-|
| \_llegada original de IP \_ \_ si | sí | sí | DWORD (booleano) | Indica si la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) debe devolver datos de control opcionales que contengan la interfaz de llegada original en la que se recibió el paquete para Sockets de datagrama. Esta opción se usa con tecnologías de transición IPv6 (túneles 6to4, ISATAP y Teredo, por ejemplo) que proporcionan la asignación de direcciones y la tunelización automática de host a host para el tráfico IPv6 de unidifusión cuando los hosts IPv6 deben atravesar redes IP4 para llegar a otras redes IPv6. Los paquetes IPv6 se envían mediante túneles como paquetes IPv4. Esta opción permite que la interfaz IPv4 original en la que se recibió el paquete se devuelva en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  |
| IPV6_ADD_IFLIST | | sí | DWORD (IF_INDEX) | Agrega un índice de interfaz al IFLIST asociado a la opción **IP_IFLIST** . |
| IPV6 \_ agregar \_ pertenencia | | sí | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Una el socket al grupo de multidifusión proporcionado en la interfaz especificada.  Esta opción solo es válida en los sockets de datagrama y sin formato (el tipo de socket debe ser SOCK \_ DGRAM o sock \_ raw). |
| IPV6_DEL_IFLIST | | sí | DWORD (IF_INDEX) | Quita un índice de interfaz del IFLIST asociado a la opción **IP_IFLIST** . Solo la aplicación puede quitar las entradas, por lo que debe tener en cuenta que las entradas pueden quedar obsoletas una vez que se quita una interfaz. |
| \_Eliminación de \_ PERtenencia IPv6 | | sí | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Deje el grupo de multidifusión proporcionado de la interfaz especificada.  Esta opción solo es válida en los sockets de datagrama y sin formato (el tipo de socket debe ser SOCK \_ DGRAM o sock \_ raw). |
| IPV6_GET_IFLIST | sí | | DWORD [] (IF_INDEX []) | Obtiene el IFLIST actual asociado a la opción **IP_IFLIST** . Devuelve un error si **IP_IFLIST** no está habilitado. |
| \_HDRINCL IPv6 | sí | sí | DWORD (booleano) | Indica que la aplicación proporciona el encabezado IPv6 en todos los datos salientes. Si el parámetro *optval* se establece en **1** en la llamada a la opción-i [**, la**](/windows/desktop/api/winsock/nf-winsock-setsockopt)opción está habilitada. Si *optval* se establece en **0**, la opción está deshabilitada. El valor predeterminado está deshabilitado. Esta opción solo es válida para los sockets de datagrama y sin formato (el tipo de socket debe ser SOCK \_ DGRAM o sock \_ raw). Un proveedor de servicios TCP/IP que admita SOCK \_ raw debe admitir también \_ HDRINCL de IPv6. |
| \_HOPLIMIT IPv6 | sí | sí | DWORD (booleano) | Indica que se debe devolver información de salto (TTL) en la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . Si *optval* se establece en **1** en la llamada a el [**valor de la opción, la**](/windows/desktop/api/winsock/nf-winsock-setsockopt)opción está habilitada. Si se establece en **0**, la opción está deshabilitada.  Esta opción solo es válida para los sockets de datagrama y sin formato (el tipo de socket debe ser SOCK \_ DGRAM o sock \_ raw). |
| IPV6_IFLIST | sí | sí | DWORD (booleano) | Obtiene o establece el estado **IP_IFLIST** del socket. Cuando esta opción se establece en true, la recepción de datagramas se restringe a las interfaces que se encuentran en IFLIST. Se omiten los datagramas recibidos en otras interfaces. IFLIST se inicia vacío. Use **IP_ADD_IFLIST** y **IP_DEL_IFLIST** para editar IFLIST. |
| \_Grupo de combinación IPv6 \_ | | sí | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Igual que IPV6 \_ agregar \_ pertenencia |
| \_Grupo de abandonar IPv6 \_ | | sí | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Igual que la \_ \_ pertenencia a un destino IPv6 |
| MTU de IPV6 \_ | sí | | DWORD | Obtiene la estimación del sistema de la MTU de la ruta de acceso. Socket debe estar conectado. |
| \_Detección de MTU de IPv6 \_ | sí | sí | DWORD (**\_ Estado de PMTUD**) | Obtiene o establece el estado de detección de MTU de la ruta de acceso para el socket. El valor predeterminado es **IP \_ PMTUDISC \_ not \_ set**. En el caso de los sockets de secuencias, **\_ no se \_ \_ establece PMTUDISC de IP** y **PMTUDISC de IP \_ \_** realizará la detección de MTU. **Dirección IP \_ El \_** **\_ \_ sondeo** PMTUDISC no y PMTUDISC IP desactivará la detección de MTU de ruta de acceso. En el caso de los sockets de datagrama, si se establece en **IP \_ PMTUDISC \_** , los intentos de enviar paquetes mayores que la MTU de ruta de acceso producirán un error. Si se establece en **IP \_ PMTUDISC \_**, los paquetes se fragmentarán según la MTU de la interfaz. Si se establece en el **\_ \_ sondeo de PMTUDISC IP**, los intentos de envío de paquetes mayores que la MTU de interfaz producirán un error.  |
| \_Saltos de multidifusión IPv6 \_ | sí | sí | DWORD | Obtiene o establece el valor de TTL asociado al tráfico de multidifusión IPv6 en el socket. No es válido establecer el TTL en un valor mayor que 255.  Esta opción solo es válida para los sockets de datagrama y sin formato (el tipo de socket debe ser SOCK \_ DGRAM o sock \_ raw). |
| Multidifusión IPV6 \_ \_ si | sí | sí | DWORD | Obtiene o establece la interfaz de salida para enviar el tráfico de multidifusión IPv6. Esta opción no cambia la interfaz predeterminada para recibir tráfico IPv6 de multidifusión. Esta opción es importante para los equipos de host múltiple.  El valor de entrada para establecer esta opción es un índice de interfaz de 4 bytes de la interfaz de salida deseada en el orden de bytes del host. La función [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) se puede usar para obtener la información del índice de la interfaz. Si *optval* se establece en **null** cuando se llama a la [**opción de llamada a la**](/windows/desktop/api/winsock/nf-winsock-setsockopt)interfaz, se usa la interfaz predeterminada de IPv6. Si *optval* es cero, se especifica la interfaz predeterminada para recibir multidifusión para enviar el tráfico de multidifusión.  Al obtener esta opción, *optval* devuelve el índice de interfaz predeterminado actual para enviar tráfico IPv6 de multidifusión en el orden de bytes del host. |
| \_Bucle de multidifusión IPv6 \_ | sí | sí | DWORD (booleano) | Indica que los datos de multidifusión enviados en el socket se devolverán al búfer de recepción de sockets si también se unen en el grupo de multidifusión de destino. Si *optval* se establece en **1** en la llamada a el [**valor de la opción, la**](/windows/desktop/api/winsock/nf-winsock-setsockopt)opción está habilitada. Si se establece en **0**, la opción está deshabilitada.  Esta opción solo es válida para los sockets de datagrama y sin formato (el tipo de socket debe ser SOCK \_ DGRAM o sock \_ raw). |
| [\_PKTINFO IPv6](ipv6-pktinfo.md) | sí | sí | DWORD (booleano) | Indica que la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) debe devolver información de paquetes. |
| [\_Nivel de protección IPv6 \_](ipv6-protection-level.md) | sí | sí | INT | Habilita la restricción de un socket a un ámbito especificado, como direcciones con el mismo prefijo local de vínculo o sitio. Proporciona diversos niveles de restricción y valores predeterminados. Para obtener más información, consulte [ \_ \_ nivel de protección de IPv6](ipv6-protection-level.md) . |
| \_RECVIF IPv6 | sí | sí | DWORD (booleano) | Indica si la pila IP debe rellenar el búfer de control con detalles sobre la interfaz que ha recibido un paquete con un socket de datagrama. Cuando este valor es true, la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devolverá datos de control opcionales que contienen la interfaz en la que se recibió el paquete para Sockets de datagrama. Esta opción permite que la interfaz IPv6 en la que se recibió el paquete se devuelva en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Esta opción solo es válida para los sockets de datagrama y sin formato (el tipo de socket debe ser SOCK \_ DGRAM o sock \_ raw). |
| \_RECVTCLASS IPv6 | sí | sí | DWORD (booleano) | Indica si la pila IP debe rellenar el búfer de control con un mensaje que contenga el campo de encabezado IPv6 de la clase de tráfico en un datagrama recibido. Cuando este valor es true, la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devolverá datos de control opcionales que contienen el valor del campo de encabezado IPv6 de clase de tráfico del datagrama recibido.  Esta opción permite que el campo de encabezado IPv6 de clase de tráfico del datagrama recibido se devuelva en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) . El tipo de mensaje devuelto será \_ TCLASS IPv6. Se devolverán todos los bits de DSCP y ECN del campo de clase de tráfico.  Esta opción solo es válida en sockets de datagramas (el tipo de socket debe ser SOCK \_ DGRAM).  |
| \_Saltos de UNIDIFUSIÓN IPv6 \_ | sí | sí | DWORD | Obtiene o establece el valor de TTL actual asociado al socket IPv6 para el tráfico de unidifusión. No es válido establecer el TTL en un valor mayor que 255. |
| \_UNIDIFUSIÓN IPv6 \_ si | sí | sí | DWORD (si es un \_ Índice) | Obtiene o establece la interfaz de salida para enviar el tráfico IPv6. Esta opción no cambia la interfaz predeterminada para recibir tráfico IPv6. Esta opción es importante para los equipos de host múltiple.  El valor de entrada para establecer esta opción es un índice de interfaz de 4 bytes de la interfaz de salida deseada en el orden de bytes del host. La función [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) se puede usar para obtener la información del índice de la interfaz. Si *optval* es cero, la interfaz predeterminada para enviar tráfico IPv6 está establecida en sin especificar.  Al obtener esta opción, *optval* devuelve el índice de interfaz predeterminado actual para enviar tráfico IPv6 en el orden de bytes del host. |
| IPV6_USER_MTU | sí | sí | DWORD | Obtiene o establece un límite superior en la MTU de nivel IP (en bytes) para el socket especificado. Si el valor es mayor que la estimación del sistema de la MTU de la ruta de acceso (que se puede recuperar en un socket conectado mediante una consulta a la opción de socket de **IPV6_MTU** ), la opción no tiene ningún efecto. Si el valor es menor, los paquetes salientes mayores que este se fragmentarán o no se enviarán, dependiendo del valor de **IPV6_DONTFRAG**. El valor predeterminado es **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Para la seguridad de tipos, debe usar las funciones [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) y [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) en lugar de usar la opción socket directamente. |
| \_V6ONLY IPv6 | sí | sí | DWORD (booleano) | Indica si un socket creado para la \_ familia de direcciones AF inet6 está restringido únicamente a las comunicaciones IPv6. Los sockets creados para la \_ familia de direcciones AF inet6 se pueden usar para las comunicaciones IPv6 e IPv4. Es posible que algunas aplicaciones deseen restringir el uso de un socket creado para la familia de direcciones de AF \_ inet6 solo a las comunicaciones IPv6. Cuando este valor es distinto de cero (el valor predeterminado en Windows), un socket creado para la \_ familia de direcciones AF inet6 se puede usar para enviar y recibir paquetes IPv6 únicamente. Cuando este valor es cero, un socket creado para la \_ familia de direcciones AF inet6 se puede usar para enviar y recibir paquetes a y desde una dirección IPv6 o una dirección IPv4. Tenga en cuenta que la capacidad de interactuar con una dirección IPv4 exige el uso de direcciones asignadas IPv4. Esta opción de socket es compatible con Windows Vista o posterior. |

## <a name="windows-support-for-ipproto_ipv6-socket-options"></a>Compatibilidad de Windows con \_ Opciones de socket de IPv6 de IPPROTO

| Opción | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|
| \_llegada original de IP \_ \_ si | x | x | x | | |
| IPV6_ADD_IFLIST | A partir de Windows 10, versión 1803 | | | | | |
| IPV6 \_ agregar \_ pertenencia | x | x | x | x | x |
| IPV6_DEL_IFLIST | A partir de Windows 10, versión 1803 | | | | | |
| \_Eliminación de \_ PERtenencia IPv6 | x | x | x | x | x |
| IPV6_GET_IFLIST | A partir de Windows 10, versión 1803 | | | | | |
| \_HDRINCL IPv6 | x | x | x | x | x |
| \_HOPLIMIT IPv6 | x | x | x | x | x |
| IPV6_IFLIST | A partir de Windows 10, versión 1803 | | | | | |
| \_Grupo de combinación IPv6 \_ | x | x | x | x | x |
| \_Grupo de abandonar IPv6 \_ | x | x | x | x | x |
| \_Saltos de multidifusión IPv6 \_ | x | x | x | x | x |
| Multidifusión IPV6 \_ \_ si | x | x | x | x | x |
| \_Bucle de multidifusión IPv6 \_ | x | x | x | x | x |
| \_PKTINFO IPv6 | x | x | x | x | x |
| [\_Nivel de protección IPv6 \_](ipv6-protection-level.md) | x | x | x | x | x |
| \_RECVIF IPv6 | x | x | x | x | x |
| \_Saltos de UNIDIFUSIÓN IPv6 \_ | x | x | x | x | x |
| \_UNIDIFUSIÓN IPv6 \_ si | x | x | x | x | x |
| \_V6ONLY IPv6 | x | x | x | x | x |

<br/>

| Opción | Windows Server 2003 | Windows XP |
|-|-|-|
| \_llegada original de IP \_ \_ si | | |
| IPV6_ADD_IFLIST | | |
| IPV6 \_ agregar \_ pertenencia | x | x |
| IPV6_DEL_IFLIST | | |
| \_Eliminación de \_ PERtenencia IPv6 | x | x |
| IPV6_GET_IFLIST | | |
| \_HDRINCL IPv6 x | x |
| \_HOPLIMIT IPv6 x | x |
| IPV6_IFLIST | | |
| \_Grupo de combinación IPv6 \_ | x | x |
| \_Grupo de abandonar IPv6 \_ | x | x |
| \_Saltos de multidifusión IPv6 \_ | x | x |
| Multidifusión IPV6 \_ \_ si | x | x |
| \_Bucle de multidifusión IPv6 \_ | x | x |
| \_PKTINFO IPv6 | x | x |
| [\_Nivel de protección IPv6 \_](ipv6-protection-level.md) | x | x |
| \_RECVIF IPv6 | | |
| \_Saltos de UNIDIFUSIÓN IPv6 \_ | x | x |
| \_UNIDIFUSIÓN IPv6 \_ si | | |
| \_V6ONLY IPv6 | | |

## <a name="remarks"></a>Observaciones

En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y el nivel de **\_ IPv6 IPPROTO** se define en el archivo de encabezado *Ws2def. h* que se incluye automáticamente en el archivo de encabezado *WinSock2. h* . Las opciones de socket **\_ IPv6 de IPPROTO** se definen en el archivo de encabezado *Ws2ipdef. h* que se incluye automáticamente en el archivo de encabezado *Ws2tcpip. h* . Los archivos de encabezado *Ws2def. h* y *Ws2ipdef. h* nunca deben usarse directamente.

La opción de la \_ llegada original de IP \_ si el \_ socket es compatible con Windows Server 2008 R2 y con Windows 7.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | <dl> <dt>Ws2def. h (incluir WinSock2. h); </dt> <dt>WinSock2. h en Windows Server 2003 y Windows XP</dt> </dl> |
