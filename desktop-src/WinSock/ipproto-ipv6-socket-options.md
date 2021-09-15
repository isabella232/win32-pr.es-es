---
description: En las tablas siguientes se describen las opciones de socket IPV6 de IPPROTO que se aplican a los sockets creados para la familia de \_ direcciones IPv6 \_ (AF INET6). Consulte las páginas de referencia de las funciones getsockopt y setsockopt para obtener más información sobre cómo obtener y establecer opciones de socket.
ms.assetid: 65f8f7a4-757b-43a3-9d47-b115754c89d6
title: Opciones de socket IPPROTO_IPV6
ms.topic: article
ms.date: 10/07/2019
ms.openlocfilehash: 86f8156f91e5f7e185319224e06d7bf54e87c6da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581289"
---
# <a name="ipproto_ipv6-socket-options"></a>Opciones de socket \_ IPV6 de IPPROTO

En las tablas siguientes se describen las opciones de socket **\_ IPV6 de IPPROTO** que se aplican a los sockets creados para la familia de direcciones IPv6 \_ (AF INET6). Consulte las [**páginas de referencia de la función getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obtener más información sobre cómo obtener y establecer opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas para cada protocolo instalado, use la función [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

Algunas opciones de socket requieren más explicaciones de las que pueden transmitir estas tablas. estas opciones contienen vínculos a información adicional.

## <a name="options"></a>Opciones

| Opción | get | set | Tipo optval | Descripción |
|-|-|-|-|-|
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | sí | sí | DWORD (booleano) | Indica si la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) debe devolver datos de control opcionales que contengan la interfaz de llegada original donde se recibió el paquete para los sockets de datagramas. Esta opción se usa con tecnologías de transición IPv6 (túneles 6to4, ISATAP y Teredo, por ejemplo) que proporcionan asignación de direcciones y tunelización automática de host a host para el tráfico IPv6 de unidifusión cuando los hosts IPv6 deben atravesar redes IP4 para llegar a otras redes IPv6. Los paquetes IPv6 se envían mediante túneles como paquetes IPv4. Esta opción permite que la interfaz IPv4 original donde se recibió el paquete se devuelva en la [**estructura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)  |
| IPV6_ADD_IFLIST | | sí | DWORD (IF_INDEX) | Agrega un índice de interfaz a IFLIST asociado a la **IP_IFLIST** predeterminada. |
| AGREGAR PERTENENCIA A IPV6 \_ \_ | | sí | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Una el socket al grupo de multidifusión proporcionado en la interfaz especificada.  Esta opción solo es válida en datagramas y sockets sin procesar (el tipo de socket debe ser SOCK \_ DGRAM o SOCK \_ RAW). |
| IPV6_DEL_IFLIST | | sí | DWORD (IF_INDEX) | Quita un índice de interfaz de IFLIST asociado a la **IP_IFLIST** predeterminada. Las entradas solo las puede quitar la aplicación, por lo que debe tener en cuenta que las entradas pueden estar obsoletas una vez que se quita una interfaz. |
| IPV6 \_ DROP \_ MEMBERSHIP | | sí | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Deje el grupo de multidifusión proporcionado desde la interfaz dada.  Esta opción solo es válida en datagramas y sockets sin procesar (el tipo de socket debe ser SOCK \_ DGRAM o SOCK \_ RAW). |
| IPV6_GET_IFLIST | sí | | DWORD[] (IF_INDEX[]) | Obtiene el IFLIST actual asociado a la **IP_IFLIST** predeterminada. Devuelve un error **si IP_IFLIST** está habilitado. |
| IPV6 \_ HDRINCL | sí | sí | DWORD(boolean) | Indica que la aplicación proporciona el encabezado IPv6 en todos los datos salientes. Si el *parámetro optval* se establece en **1 en** la llamada a [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), la opción está habilitada. Si *optval* se establece en **0,** la opción está deshabilitada. El valor predeterminado está deshabilitado. Esta opción solo es válida para datagramas y sockets sin procesar (el tipo de socket debe ser SOCK \_ DGRAM o SOCK \_ RAW). Un proveedor de servicios TCP/IP que admita SOCK \_ RAW también debe admitir IPV6 \_ HDRINCL. |
| IPV6 \_ HOPLIMIT | sí | sí | DWORD (booleano) | Indica que se debe devolver información de salto (TTL) en [**la LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Si *optval* se establece en **1 en** la llamada a [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), la opción está habilitada. Si se establece **en 0,** la opción está deshabilitada.  Esta opción solo es válida para datagramas y sockets sin procesar (el tipo de socket debe ser SOCK \_ DGRAM o SOCK \_ RAW). |
| IPV6_IFLIST | sí | sí | DWORD (booleano) | Obtiene o establece el **IP_IFLIST** del socket. Cuando esta opción se establece en true, la recepción de datagramas está restringida a las interfaces que se encuentran en IFLIST. Los datagramas recibidos en cualquier otra interfaz se omiten. IFLIST se inicia vacío. Use **IP_ADD_IFLIST** y **IP_DEL_IFLIST** para editar IFLIST. |
| IPV6 \_ JOIN \_ GROUP | | sí | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Igual que IPV6 \_ ADD \_ MEMBERSHIP |
| IPV6 \_ LEAVE \_ GROUP | | sí | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Igual que DROP MEMBERSHIP de IPV6 \_ \_ |
| MTU de IPV6 \_ | sí | | DWORD | Obtiene la estimación del sistema de la ruta de acceso MTU. El socket debe estar conectado. |
| IPV6 \_ MTU \_ DISCOVER | sí | sí | DWORD (**PMTUD \_ STATE**) | Obtiene o establece el estado de detección de MTU de la ruta de acceso para el socket. El valor predeterminado es **IP \_ PMTUDISC \_ NOT \_ SET.** Para los sockets de flujo, **IP \_ PMTUDISC \_ NOT \_ SET** e **IP \_ PMTUDISC \_ DO** realizarán la detección de MTU de ruta de acceso. **IP \_ PMTUDISC \_ DONT e** IP **\_ PMTUDISC \_ PROBE** desactivarán la detección de MTU de ruta de acceso. En el caso de los sockets de datagramas, si se establece en **IP \_ PMTUDISC \_ DO,** los intentos de enviar paquetes mayores que la ruta de acceso MTU producirán un error. Si se establece en **IP \_ PMTUDISC \_ DONT,** los paquetes se fragmentarán según la interfaz MTU. Si se establece en **IP \_ PMTUDISC \_ PROBE**, los intentos de enviar paquetes mayores que la interfaz MTU producirán un error.  |
| SALTOS DE \_ MULTIDIFUSIÓN IPV6 \_ | sí | sí | DWORD | Obtiene o establece el valor TTL asociado al tráfico de multidifusión IPv6 en el socket. No es válido establecer el TTL en un valor mayor que 255.  Esta opción solo es válida para datagramas y sockets sin procesar (el tipo de socket debe ser SOCK \_ DGRAM o SOCK \_ RAW). |
| MULTIDIFUSIÓN IPV6 \_ \_ SI | sí | sí | DWORD | Obtiene o establece la interfaz saliente para enviar tráfico de multidifusión IPv6. Esta opción no cambia la interfaz predeterminada para recibir tráfico de multidifusión IPv6. Esta opción es importante para los equipos de varios equipos locales.  El valor de entrada para establecer esta opción es un índice de interfaz de 4 bytes de la interfaz saliente deseada en el orden de bytes del host. La [**función GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) se puede usar para obtener la información del índice de interfaz. Si *optval* se establece en **NULL al** llamar a [**setsockopt,**](/windows/desktop/api/winsock/nf-winsock-setsockopt)se usa la interfaz IPv6 predeterminada. Si *optval* es cero, se especifica la interfaz predeterminada para recibir multidifusión para enviar tráfico de multidifusión.  Al obtener esta opción, el *optval* devuelve el índice de interfaz predeterminado actual para enviar tráfico IPv6 de multidifusión en el orden de bytes del host. |
| BUCLE DE MULTIDIFUSIÓN IPV6 \_ \_ | sí | sí | DWORD (booleano) | Indica que los datos de multidifusión enviados en el socket se mostrarán en el búfer de recepción de sockets si también están unidos en el grupo de multidifusión de destino. Si *optval* se establece en **1 en** la llamada a [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), la opción está habilitada. Si se establece **en 0,** la opción está deshabilitada.  Esta opción solo es válida para datagramas y sockets sin procesar (el tipo de socket debe ser SOCK \_ DGRAM o SOCK \_ RAW). |
| [IPV6 \_ PKTINFO](ipv6-pktinfo.md) | sí | sí | DWORD (booleano) | Indica que la información del paquete debe [**devolverla la LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) |
| [NIVEL DE PROTECCIÓN \_ IPV6 \_](ipv6-protection-level.md) | sí | sí | INT | Habilita la restricción de un socket a un ámbito especificado, como direcciones con el mismo prefijo local o de sitio de vínculo. Proporciona varios niveles de restricción y la configuración predeterminada. Vea [IPV6 \_ PROTECTION LEVEL \_ (NIVEL DE PROTECCIÓN de IPV6)](ipv6-protection-level.md) para obtener más información. |
| IPV6 \_ RECVIF | sí | sí | DWORD (booleano) | Indica si la pila IP debe rellenar el búfer de control con detalles sobre qué interfaz recibió un paquete con un socket de datagrama. Cuando este valor es true, la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devolverá datos de control opcionales que contienen la interfaz donde se recibió el paquete para sockets de datagrama. Esta opción permite que la interfaz IPv6 donde se recibió el paquete se devuelva en la [**estructura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)  Esta opción solo es válida para datagramas y sockets sin procesar (el tipo de socket debe ser SOCK \_ DGRAM o SOCK \_ RAW). |
| RECVTCLASS de IPV6 \_ | sí | sí | DWORD (booleano) | Indica si la pila IP debe rellenar el búfer de control con un mensaje que contiene el campo de encabezado Traffic Class IPv6 en un datagrama recibido. Cuando este valor es true, la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devolverá datos de control opcionales que contienen el valor del campo de encabezado IPv6 de clase de tráfico del datagrama recibido.  Esta opción permite devolver el campo de encabezado IPv6 de clase de tráfico del datagrama recibido en la [**estructura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) El tipo de mensaje devuelto será \_ TCLASS de IPV6. Se devolverán todos los bits DSCP y ECN del campo Clase de tráfico.  Esta opción solo es válida en sockets de datagramas (el tipo de socket debe ser SOCK \_ DGRAM).  |
| SALTOS \_ DE UNIDIFUSIÓN IPV6 \_ | sí | sí | DWORD | Obtiene o establece el valor TTL actual asociado al socket IPv6 para el tráfico de unidifusión. No es válido establecer el TTL en un valor mayor que 255. |
| IPV6 \_ UNICAST \_ IF | sí | sí | DWORD (IF \_ INDEX) | Obtiene o establece la interfaz saliente para enviar tráfico IPv6. Esta opción no cambia la interfaz predeterminada para recibir tráfico IPv6. Esta opción es importante para los equipos de varios equipos locales.  El valor de entrada para establecer esta opción es un índice de interfaz de 4 bytes de la interfaz saliente deseada en el orden de bytes del host. La [**función GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) se puede usar para obtener la información del índice de interfaz. Si *optval* es cero, la interfaz predeterminada para enviar tráfico IPv6 se establece en unspecified.  Al obtener esta opción, el *optval* devuelve el índice de interfaz predeterminado actual para enviar tráfico IPv6 en el orden de bytes del host. |
| IPV6_USER_MTU | sí | sí | DWORD | Obtiene o establece un límite superior en la MTU de la capa IP (en bytes) para el socket dado. Si el valor es mayor que la estimación del sistema de la ruta de acceso MTU (que puede recuperar en un socket conectado consultando la opción de socket **IPV6_MTU),** la opción no tiene ningún efecto. Si el valor es inferior, los paquetes salientes mayores que este se fragmentarán o no se enviarán, dependiendo del valor de **IPV6_DONTFRAG**. El valor predeterminado **es IP_UNSPECIFIED_USER_MTU** (MAXULONG). Para la seguridad de tipos, debe usar las funciones [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) y [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) en lugar de usar directamente la opción de socket. |
| IPV6 \_ V6ONLY | sí | sí | DWORD (booleano) | Indica si un socket creado para la familia de direcciones AF INET6 está restringido solo a \_ las comunicaciones IPv6. Los sockets creados para la familia de direcciones AF INET6 se pueden usar para las comunicaciones \_ IPv6 e IPv4. Es posible que algunas aplicaciones quieran restringir el uso de un socket creado para la familia de direcciones AF INET6 solo a \_ las comunicaciones IPv6. Cuando este valor es distinto de cero (el valor predeterminado en Windows), se puede usar un socket creado para la familia de direcciones AF INET6 para enviar y recibir solo paquetes \_ IPv6. Cuando este valor es cero, se puede usar un socket creado para la familia de direcciones AF INET6 para enviar y recibir paquetes hacia y desde una dirección IPv6 o una dirección \_ IPv4. Tenga en cuenta que la capacidad de interactuar con una dirección IPv4 exige el uso de direcciones asignadas IPv4. Esta opción de socket es compatible con Windows Vista o posterior. |

## <a name="windows-support-for-ipproto_ipv6-socket-options"></a>Windows compatibilidad con las opciones de socket IPV6 de IPPROTO \_

| Opción | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | x | x | x | | |
| IPV6_ADD_IFLIST | A partir Windows 10, versión 1803 | | | | |
| AGREGAR PERTENENCIA A IPV6 \_ \_ | x | x | x | x | x |
| IPV6_DEL_IFLIST | A partir Windows 10, versión 1803 | | | | |
| IPV6 \_ DROP \_ MEMBERSHIP | x | x | x | x | x |
| IPV6_GET_IFLIST | A partir Windows 10, versión 1803 | | | | |
| IPV6 \_ HDRINCL | x | x | x | x | x |
| IPV6 \_ HOPLIMIT | x | x | x | x | x |
| IPV6_IFLIST | A partir Windows 10, versión 1803 | | | | |
| IPV6 \_ JOIN \_ GROUP | x | x | x | x | x |
| IPV6 \_ LEAVE \_ GROUP | x | x | x | x | x |
| SALTOS DE \_ MULTIDIFUSIÓN IPV6 \_ | x | x | x | x | x |
| MULTIDIFUSIÓN IPV6 \_ \_ SI | x | x | x | x | x |
| BUCLE DE MULTIDIFUSIÓN IPV6 \_ \_ | x | x | x | x | x |
| IPV6 \_ PKTINFO | x | x | x | x | x |
| [NIVEL DE PROTECCIÓN \_ IPV6 \_](ipv6-protection-level.md) | x | x | x | x | x |
| IPV6 \_ RECVIF | x | x | x | x | x |
| SALTOS \_ DE UNIDIFUSIÓN IPV6 \_ | x | x | x | x | x |
| IPV6 \_ UNICAST \_ IF | x | x | x | x | x |
| IPV6 \_ V6ONLY | x | x | x | x | x |

<br/>

| Opción | Windows Server 2003 | Windows XP |
|-|-|-|
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | | |
| IPV6_ADD_IFLIST | | |
| AGREGAR PERTENENCIA A IPV6 \_ \_ | x | x |
| IPV6_DEL_IFLIST | | |
| IPV6 \_ DROP \_ MEMBERSHIP | x | x |
| IPV6_GET_IFLIST | | |
| IPV6 \_ HDRINCL x | x |
| IPV6 \_ HOPLIMIT x | x |
| IPV6_IFLIST | | |
| IPV6 \_ JOIN \_ GROUP | x | x |
| IPV6 \_ LEAVE \_ GROUP | x | x |
| SALTOS DE \_ MULTIDIFUSIÓN IPV6 \_ | x | x |
| MULTIDIFUSIÓN IPV6 \_ \_ SI | x | x |
| BUCLE DE MULTIDIFUSIÓN IPV6 \_ \_ | x | x |
| IPV6 \_ PKTINFO | x | x |
| [NIVEL DE PROTECCIÓN \_ IPV6 \_](ipv6-protection-level.md) | x | x |
| IPV6 \_ RECVIF | | |
| SALTOS \_ DE UNIDIFUSIÓN IPV6 \_ | x | x |
| IPV6 \_ UNICAST \_ IF | | |
| IPV6 \_ V6ONLY | | |

## <a name="remarks"></a>Observaciones

En el Kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y el nivel **\_ IPV6 de IPPROTO** se define en el archivo de encabezado *Ws2def.h* que se incluye automáticamente en el archivo de encabezado *Winsock2.h.* Las opciones de socket **\_ IPV6 de IPPROTO** se definen en el archivo de encabezado *Ws2ipdef.h* que se incluye automáticamente en el archivo de encabezado *Ws2tcpip.h.* Los *archivos de encabezado Ws2def.h* y *Ws2ipdef.h* nunca deben usarse directamente.

La opción de socket IP ORIGINAL ARRIVAL IF se admite \_ \_ en Windows Server \_ 2008 R2, así como en Windows 7.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | <dl> <dt>Ws2def.h (incluya Winsock2.h);</dt> <dt>Winsock2.h en Windows Server 2003 y Windows XP</dt> </dl> |
