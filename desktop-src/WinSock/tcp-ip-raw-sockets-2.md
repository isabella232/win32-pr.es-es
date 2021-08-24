---
description: Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente.
ms.assetid: 4cbe5505-75e7-454f-9e6b-f38bdc60bf6d
title: Sockets sin formato TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef8600c7b1a6c1bc5b2f7b5b210ca2d56f90069b0afce88c83ca45e9cfad8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733395"
---
# <a name="tcpip-raw-sockets"></a>Sockets sin formato TCP/IP

Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente. Este tema se centra solo en los sockets sin formato y los protocolos IPv4 e IPv6. Esto se debe a que la mayoría de los demás protocolos con la excepción de ATM no admiten sockets sin procesar. Para usar sockets sin procesar, una aplicación debe tener información detallada sobre el protocolo subyacente que se está utilizando.

Los proveedores de servicios Winsock para el protocolo IP pueden admitir un *tipo* de socket **de SOCK \_ RAW.** El Windows Sockets 2 para TCP/IP incluido en Windows admite este tipo de socket **\_ SOCK RAW.**

Hay dos tipos básicos de estos sockets sin procesar:

-   El primer tipo usa un tipo de protocolo conocido escrito en el encabezado IP que reconoce un proveedor de servicios Winsock. Un ejemplo del primer tipo de socket es un socket para el protocolo ICMP (tipo de protocolo IP = 1) o el protocolo ICMPv6 (tipo de procoiones IP = 58).
-   El segundo tipo permite especificar cualquier tipo de protocolo. Un ejemplo del segundo tipo sería un protocolo experimental que no es compatible directamente con el proveedor de servicios Winsock, como el Protocolo de transmisión de control de transmisiones (SCTP).

## <a name="determining-if-raw-sockets-are-supported"></a>Determinar si se admiten sockets sin formato

Si un proveedor de servicios Winsock admite sockets **SOCK \_ RAW** para las familias de direcciones AF INET o AF INET6, el tipo de socket de SOCK RAW debe incluirse en la estructura INFO de WSAPROTOCOL devuelta por la función \_ \_ [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) **\_** [**\_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para uno o varios de los proveedores de transporte disponibles.

El miembro **iAddressFamily** de la estructura [**INFO de \_ WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) debe especificar AF INET o AF INET6 y el miembro iSocketType de la estructura \_ \_ **\_ INFO WSAPROTOCOL**  debe especificar **SOCK \_ RAW** para uno de los proveedores de transporte.

El **miembro iProtocol** de la [**estructura \_ INFO de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) puede establecerse en **IPROTO \_ IP**. El **miembro iProtocol** de la estructura **INFO de WSAPROTOCOL \_** también puede establecerse en cero si el proveedor de servicios permite que una aplicación use un tipo de socket **SOCK \_ RAW** para otros protocolos de red distintos del protocolo de Internet para la familia de direcciones.

Los demás miembros de la estructura [**INFO de \_ WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) indican otras propiedades de la compatibilidad del protocolo con **SOCK \_ RAW** e indican cómo se debe tratar un socket de **SOCK \_ RAW.** Estos otros miembros de **WSAPROTOCOL \_ INFO** para **SOCK \_ RAW** normalmente especifican que el protocolo es sin conexión, orientado a mensajes, admite difusión o multidifusión (los bits XP1 CONNECTIONLESS, XP1 MESSAGE ORIENTED, XP1 SUPPORT BROADCAST y XP1 SUPPORT MULTIPOINT están establecidos en el miembro dwServiceFlags1) y pueden tener un tamaño máximo de mensaje de \_ \_ \_ \_ \_ \_ \_ 65 467 bytes.

En Windows XP y versiones posteriores, *se puede usarNetSh.exe* comando para determinar si se admiten sockets sin formato. El comando siguiente se ejecuta desde una ventana cmd y mostrará los datos del catálogo winsock en la consola:

**netsh winsock show catalog**

La salida incluirá una lista que contiene algunos de los datos de las estructuras info de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) admitidas en el equipo local. Busque el término RAW/IP o RAW/IPv6 en el campo Descripción para buscar los protocolos que admiten sockets sin formato.

## <a name="creating-a-raw-socket"></a>Creación de un socket sin formato

Para crear un socket de tipo **SOCK \_ RAW,** llame a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con el parámetro *af* (familia de direcciones) establecido en AF INET o \_ AF \_ INET6,   el parámetro de tipo establecido en **SOCK \_ RAW** y el parámetro de protocolo establecido en el número de protocolo necesario. El *parámetro protocol* se convierte en el valor de protocolo en el encabezado IP (SCTP es 132, por ejemplo).

> [!Note]  
> Es posible que una aplicación no  especifique cero (0) como parámetro de protocolo para las funciones  [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket), [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)y [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) si el parámetro de tipo está establecido en **SOCK \_ RAW.**

 

Los sockets sin procesar ofrecen la capacidad de manipular el transporte subyacente, por lo que se pueden usar con fines malintencionados que suponen una amenaza de seguridad. Por lo tanto, solo los miembros del grupo Administradores pueden crear sockets de tipo SOCK \_ RAW Windows 2000 y versiones posteriores.

## <a name="send-and-receive-operations"></a>Operaciones de envío y recepción

Una vez que una aplicación crea un socket de tipo **SOCK \_ RAW,** este socket se puede usar para enviar y recibir datos. Todos los paquetes enviados o recibidos en un socket de tipo **SOCK \_ RAW** se tratan como datagramas en un socket no desconectado.

Las reglas siguientes se aplican a las operaciones a través de sockets **SOCK \_ RAW:**

-   La [**función sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) [**o WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) se usa normalmente para enviar datos en un socket de tipo **SOCK \_ RAW.** La dirección de destino puede ser cualquier dirección válida en la familia de direcciones del socket, incluida una dirección de difusión o multidifusión. Para enviar a una dirección de difusión, una aplicación debe haber usado [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con SO \_ BROADCAST habilitado. De lo **contrario, sendto** **o WSASendTo** producirán un error con el código de error [WSAEACCES](windows-sockets-error-codes-2.md). Para IP, una aplicación puede enviar a cualquier dirección de multidifusión (sin convertirse en miembro del grupo).
-   Al enviar datos IPv4, una aplicación tiene la opción de especificar el encabezado IPv4 al frente del datagrama de salida para el paquete. Si la opción de socket **\_ IP HDRINCL** se establece en true para un socket IPv4 (familia de direcciones de AF INET), la aplicación debe proporcionar el encabezado IPv4 en los datos salientes para las operaciones de \_ envío. Si esta opción de socket es false (la configuración predeterminada), el encabezado IPv4 no debe incluir los datos salientes para las operaciones de envío.
-   Al enviar datos IPv6, una aplicación tiene la opción de especificar el encabezado IPv6 al frente del datagrama saliente para el paquete. Si la opción de socket **\_ IPV6 HDRINCL** se establece en true para un socket IPv6 (familia de direcciones de AF INET6), la aplicación debe proporcionar el encabezado IPv6 en los datos salientes para las operaciones de \_ envío. El valor predeterminado de esta opción es false. Si esta opción de socket es false (la configuración predeterminada), el encabezado IPv6 no debe incluirse en los datos salientes para las operaciones de envío. Para IPv6, no debe haber necesidad de incluir el encabezado IPv6. Si la información está disponible mediante funciones de socket, no se debe incluir el encabezado IPv6 para evitar problemas de compatibilidad en el futuro. Estos problemas se de abordan en RFC 3542 publicado por el IETF. No se recomienda usar la opción de socket **\_ IPV6 HDRINCL** y puede estar en desuso en el futuro.
-   La [**función recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) se usa normalmente para recibir datos en un socket de tipo **SOCK \_ RAW.** Ambas funciones tienen una opción para devolver la dirección IP de origen desde la que se envió el paquete. Los datos recibidos son un datagrama de un socket no desconectado.
-   Para IPv4 (familia de direcciones de AF INET), una aplicación recibe el encabezado IP al frente de cada datagrama recibido, independientemente de la opción de \_ socket **IP \_ HDRINCL.**
-   Para IPv6 (familia de direcciones de AF INET6), una aplicación recibe todo lo que hay después del último encabezado IPv6 en cada datagrama recibido, independientemente de la opción de socket \_ **\_ IPV6 HDRINCL.** La aplicación no recibe ningún encabezado IPv6 mediante un socket sin formato.
-   Los datagramas recibidos se copian en todos los sockets **SOCK \_ RAW** que cumplen las condiciones siguientes:

    -   El número de protocolo especificado en el parámetro *de* protocolo cuando se creó el socket debe coincidir con el número de protocolo del encabezado IP del datagrama recibido.
    -   Si se define una dirección IP local para el socket, debe corresponder a la dirección de destino especificada en el encabezado IP del datagrama recibido. Una aplicación puede especificar la dirección IP local llamando a la [**función bind.**](/windows/desktop/api/winsock/nf-winsock-bind) Si no se especifica ninguna dirección IP local para el socket, los datagramas se copian en el socket independientemente de la dirección IP de destino en el encabezado IP del datagrama recibido.
    -   Si se define una dirección externa para el socket, debe corresponder a la dirección de origen como se especifica en el encabezado IP del datagrama recibido. Una aplicación puede especificar la dirección IP externa llamando a la [**función connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) o [**WSAConnect.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) Si no se especifica ninguna dirección IP externa para el socket, los datagramas se copian en el socket independientemente de la dirección IP de origen en el encabezado IP del datagrama recibido.

Es importante comprender que algunos sockets de tipo **SOCK \_ RAW** pueden recibir muchos datagramas inesperados. Por ejemplo, un programa PING puede crear un socket de tipo **SOCK \_ RAW** para enviar solicitudes de eco ICMP y recibir respuestas. Aunque la aplicación espera respuestas de eco ICMP, todos los demás mensajes ICMP (como ICMP HOST UNREACHABLE) también se pueden entregar \_ a esta aplicación. Además, si hay varios sockets **SOCK \_ RAW** abiertos en un equipo al mismo tiempo, se pueden entregar los mismos datagramas a todos los sockets abiertos. Una aplicación debe tener un mecanismo para reconocer los datagramas de interés y omitir todos los demás. Para un programa PING, este mecanismo podría incluir la inspección del encabezado IP recibido en busca de identificadores únicos en el encabezado ICMP (por ejemplo, el identificador de proceso de la aplicación).

> [!Note]  
> Para usar un socket de tipo **SOCK \_ RAW** se requieren privilegios administrativos. Los usuarios que ejecutan aplicaciones winsock que usan sockets sin procesar deben ser miembros del grupo Administradores en el equipo local; de lo contrario, se producirá un error en las llamadas de socket sin procesar con un código de error [de WSAEACCES.](windows-sockets-error-codes-2.md) En Windows Vista y versiones posteriores, el acceso a los sockets sin formato se aplica durante la creación del socket. En versiones anteriores de Windows, el acceso a los sockets sin formato se aplica durante otras operaciones de socket.

 

## <a name="common-uses-of-raw-sockets"></a>Usos comunes de sockets sin formato

Un uso común de los sockets sin procesar son las aplicaciones de solución de problemas que necesitan examinar los encabezados y paquetes IP en detalle. Por ejemplo, se puede usar un socket sin formato con SIO RCVALL IOCTL para permitir que un socket reciba todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de \_ red. Para obtener más información, vea la [**referencia de SIO \_ RCVALL.**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85))

## <a name="limitations-on-raw-sockets"></a>Limitaciones de sockets sin procesar

En Windows 7, Windows Vista, Windows XP con Service Pack 2 (SP2) y Windows XP con Service Pack 3 (SP3), la capacidad de enviar tráfico a través de sockets sin procesar se ha restringido de varias maneras:

-   Los datos TCP no se pueden enviar a través de sockets sin formato.
-   Los datagramas UDP con una dirección de origen no válida no se pueden enviar a través de sockets sin formato. La dirección de origen IP de cualquier datagrama UDP saliente debe existir en una interfaz de red o se descarta el datagrama. Este cambio se realizó para limitar la capacidad de código malintencionado de crear ataques de denegación de servicio distribuidos y limita la capacidad de enviar paquetes suplantados (paquetes TCP/IP con una dirección IP de origen falsificado).
-   No se permite [**una llamada**](/windows/desktop/api/winsock/nf-winsock-bind) a la función de enlace con un socket sin procesar para el protocolo \_ TCP IPPROTO.
    > [!Note]  
    > La [**función bind**](/windows/desktop/api/winsock/nf-winsock-bind) con un socket sin formato se permite para otros protocolos \_ (IPPROTO IP, IPPROTO UDP o \_ IPPROTO \_ SCTP, por ejemplo).

     

Estas restricciones anteriores no se aplican a Windows Server 2008 R2, Windows Server 2008 , Windows Server 2003 ni a las versiones del sistema operativo anteriores a Windows XP con SP2.

> [!Note]  
> La implementación de Microsoft de TCP/IP en Windows es capaz de abrir un socket UDP o TCP sin procesar en función de las restricciones anteriores. Es posible que otros proveedores de Winsock no admitan el uso de sockets sin procesar.

 

Existen otras limitaciones para las aplicaciones que usan un socket de tipo **SOCK \_ RAW.** Por ejemplo, todas las aplicaciones que escuchan un protocolo específico recibirán todos los paquetes recibidos para este protocolo. Esto puede no ser lo que se desea para varias aplicaciones mediante un protocolo. Esto tampoco es adecuado para aplicaciones de alto rendimiento. Para evitar estos problemas, puede que sea necesario escribir un controlador Windows de protocolo de red (controlador de dispositivo) para el protocolo de red específico. En Windows Vista y versiones posteriores, Winsock Kernel (WSK), se puede usar una nueva interfaz de programación de red en modo kernel independiente del transporte para escribir un controlador de protocolo de red. En Windows Server 2003 y versiones anteriores, se puede escribir un proveedor de Interfaz de controlador de transporte (TDI) y un archivo DLL auxiliar de Winsock para admitir el protocolo de red. A continuación, el protocolo de red se agregaría al catálogo de Winsock como protocolo compatible. Esto permite que varias aplicaciones abran sockets para este protocolo específico y el controlador de dispositivo puede realizar un seguimiento de qué socket recibe paquetes y errores específicos. Para obtener información sobre cómo escribir un proveedor de protocolos de red, vea las secciones sobre WSK y TDI en Windows Driver Kit (WDK).

Las aplicaciones también deben ser conscientes del impacto que puede tener la configuración del firewall en el envío y la recepción de paquetes mediante sockets sin procesar.

 

 
