---
description: Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente.
ms.assetid: 4cbe5505-75e7-454f-9e6b-f38bdc60bf6d
title: Sockets sin formato de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25cc08d59d80089a4e655f363e4a899edac8d2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715853"
---
# <a name="tcpip-raw-sockets"></a>Sockets sin formato de TCP/IP

Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente. Este tema se centra únicamente en los sockets sin formato y los protocolos IPv4 e IPv6. Esto se debe a que la mayoría de los demás protocolos con la excepción de ATM no admiten Sockets sin formato. Para usar sockets sin formato, una aplicación debe tener información detallada sobre el protocolo subyacente que se está usando.

Los proveedores de servicios Winsock para el protocolo IP pueden admitir un *tipo* de socket de **sock \_ raw**. El proveedor de Windows Sockets 2 para TCP/IP incluido en Windows es compatible con este tipo de socket **\_ sin formato sock** .

Existen dos tipos básicos de estos Sockets sin formato:

-   El primer tipo utiliza un tipo de protocolo conocido escrito en el encabezado IP reconocido por un proveedor de servicios Winsock. Un ejemplo del primer tipo de socket es un socket para el protocolo ICMP (protocolo IP tipo = 1) o el protocolo ICMPv6 (IP Procotol Type = 58).
-   El segundo tipo permite especificar cualquier tipo de protocolo. Un ejemplo del segundo tipo sería un protocolo experimental que no es directamente compatible con el proveedor de servicios Winsock como el protocolo de transmisión de control de transmisión (SCTP).

## <a name="determining-if-raw-sockets-are-supported"></a>Determinar si se admiten Sockets sin formato

Si un proveedor de servicios Winsock admite Sockets **\_ sin formato de sock** para las \_ familias de direcciones AF inet o AF \_ inet6, el tipo de socket de **sock \_ raw** debe estar incluido en la estructura [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) devuelta por la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) para uno o varios de los proveedores de transporte disponibles.

El miembro **iAddressFamily** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) debe especificar AF \_ inet o AF \_ inet6 y el miembro **ISocketType** de la estructura **WSAPROTOCOL \_ info** debe especificar **sock \_ raw** para uno de los proveedores de transporte.

El miembro **iProtocol** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) se puede establecer en **IPROTO \_ IP**. El miembro **iProtocol** de la estructura de **\_ información de WSAPROTOCOL** también se puede establecer en cero si el proveedor de servicios permite que una aplicación use un tipo de socket **\_ sin formato sock** para otros protocolos de red distintos del Protocolo de Internet para la familia de direcciones.

Los demás miembros de la estructura [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) indican otras propiedades de la compatibilidad con el protocolo para **sock \_ raw** e indican cómo se debe tratar un socket de **sock \_ raw** . Estos otros miembros de la **\_ información de WSAPROTOCOL** para **sock \_ raw** normalmente especifican que el protocolo es sin conexión, orientado a mensajes, admite difusión/multidifusión (el XP1 \_ de conexión sin conexión, XP1 \_ , de compatibilidad con XP1, y XP1 admiten \_ \_ \_ \_ \_ bits Multipoint se establecen en el miembro dwServiceFlags1) y pueden tener un tamaño máximo de mensaje de 65.467 bytes.

En Windows XP y versiones posteriores, se puede usar el comando *NetSh.exe* para determinar si se admiten Sockets sin formato. El siguiente comando que se ejecuta desde una ventana de CMD mostrará los datos del catálogo de Winsock en la consola de:

**netsh winsock show Catalog**

El resultado incluirá una lista que contiene algunos de los datos de las estructuras de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) admitidas en el equipo local. Busque el término RAW/IP o RAW/IPv6 en el campo Descripción para encontrar los protocolos que admiten Sockets sin formato.

## <a name="creating-a-raw-socket"></a>Creación de un socket sin formato

Para crear un socket de tipo **sock \_ raw**, llame a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con el parámetro *AF* (Family Address) establecido en AF \_ inet o AF \_ inet6, el parámetro de *tipo* establecido en **sock \_ raw** y el parámetro *Protocol* establecido en el número de protocolo requerido. El parámetro de *Protocolo* se convierte en el valor de protocolo del encabezado IP (SCTP es 132, por ejemplo).

> [!Note]  
> Una aplicación no puede especificar cero (0) como parámetro de *Protocolo* para las funciones [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket), [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)y [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) si el parámetro de *tipo* se establece en **sock \_ raw**.

 

Los sockets sin formato ofrecen la capacidad de manipular el transporte subyacente, por lo que se pueden utilizar con fines malintencionados que supongan una amenaza para la seguridad. Por lo tanto, solo los miembros del grupo administradores pueden crear sockets de tipo SOCK \_ raw en Windows 2000 y versiones posteriores.

## <a name="send-and-receive-operations"></a>Operaciones de envío y recepción

Una vez que una aplicación crea un socket de tipo **sock \_ raw**, este socket se puede usar para enviar y recibir datos. Todos los paquetes enviados o recibidos en un socket de tipo **sock \_ raw** se tratan como datagramas en un socket no conectado.

Las siguientes reglas se aplican a las operaciones a través de sockets **\_ sin formato de sock** :

-   Normalmente, la función [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) o [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) se usa para enviar datos en un socket de tipo **sock \_ raw**. La dirección de destino puede ser cualquier dirección válida en la familia de direcciones del socket, incluida una dirección de difusión o multidifusión. Para enviar a una dirección de difusión, una aplicación debe haber [**usado la**](/windows/desktop/api/winsock/nf-winsock-setsockopt) opción de r con la \_ difusión habilitada. De lo contrario, se producirá un error en **SendTo** o **WSASendTo** con el código de error [WSAEACCES](windows-sockets-error-codes-2.md). Para IP, una aplicación puede enviar a cualquier dirección de multidifusión (sin convertirse en miembro del grupo).
-   Al enviar datos IPv4, una aplicación tiene la opción de especificar el encabezado IPv4 al principio del datagrama saliente para el paquete. Si la opción de socket **\_ HDRINCL de IP** está establecida en true para un socket IPv4 (familia de direcciones de AF \_ inet), la aplicación debe proporcionar el encabezado IPv4 en los datos salientes para las operaciones de envío. Si esta opción de socket es false (el valor predeterminado), el encabezado IPv4 no debe incluir los datos salientes para las operaciones de envío.
-   Al enviar datos IPv6, una aplicación tiene la opción de especificar el encabezado IPv6 al principio del datagrama saliente para el paquete. Si la opción de socket **\_ HDRINCL de IPv6** está establecida en true para un socket IPv6 (familia de direcciones de AF \_ inet6), la aplicación debe proporcionar el encabezado IPv6 en los datos salientes para las operaciones de envío. El valor predeterminado de esta opción es false. Si esta opción de socket es false (el valor predeterminado), el encabezado IPv6 no debe incluirse en los datos salientes para las operaciones de envío. En el caso de IPv6, no es necesario incluir el encabezado IPv6. Si la información está disponible mediante las funciones de socket, el encabezado IPv6 no debe incluirse para evitar problemas de compatibilidad en el futuro. Estos problemas se describen en RFC 3542 publicado por IETF. No se recomienda usar la opción de socket **\_ HDRINCL de IPv6** y puede estar en desuso en el futuro.
-   La función [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) se usa normalmente para recibir datos en un socket de tipo **sock \_ raw**. Ambas funciones tienen una opción para devolver la dirección IP de origen desde la que se envió el paquete. Los datos recibidos son un datagrama de un socket no conectado.
-   En el caso de IPv4 (familia de direcciones de AF \_ inet), una aplicación recibe el encabezado IP al principio de cada datagrama recibido, con independencia de la opción de socket **\_ HDRINCL de IP** .
-   Para IPv6 (familia de direcciones de AF \_ inet6), una aplicación recibe todo después del último encabezado IPv6 en cada datagrama recibido, con independencia de la opción de socket **\_ HDRINCL de IPv6** . La aplicación no recibe ningún encabezado IPv6 que use un socket sin formato.
-   Los datagramas recibidos se copian en todos los sockets **\_ sin formato de sock** que cumplen las condiciones siguientes:

    -   El número de protocolo especificado en el parámetro *Protocol* cuando se creó el socket debe coincidir con el número de protocolo del encabezado IP del datagrama recibido.
    -   Si se define una dirección IP local para el socket, debe corresponderse con la dirección de destino especificada en el encabezado IP del datagrama recibido. Una aplicación puede especificar la dirección IP local llamando a la función [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) . Si no se especifica ninguna dirección IP local para el socket, los datagramas se copian en el socket sin tener en consideración la dirección IP de destino en el encabezado IP del datagrama recibido.
    -   Si se define una dirección externa para el socket, debe corresponderse con la dirección de origen tal y como se especifica en el encabezado IP del datagrama recibido. Una aplicación puede especificar la dirección IP externa mediante una llamada a la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) o [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) . Si no se especifica ninguna dirección IP externa para el socket, los datagramas se copian en el socket sin tener en consideración la dirección IP de origen en el encabezado IP del datagrama recibido.

Es importante comprender que algunos sockets de tipo **sock \_ raw** pueden recibir muchos datagramas inesperados. Por ejemplo, un programa PING puede crear un socket de tipo **sock \_ raw** para enviar solicitudes de eco ICMP y recibir respuestas. Mientras la aplicación espera respuestas de eco ICMP, \_ es posible que también se entreguen a esta aplicación todos los demás mensajes ICMP (como el host ICMP inaccesible). Además, si hay varios Sockets **\_ sin formato de sock** abiertos en un equipo al mismo tiempo, se pueden entregar los mismos datagramas a todos los sockets abiertos. Una aplicación debe tener un mecanismo para reconocer los datagramas de interés y omitir todos los demás. En el caso de un programa PING, tal mecanismo podría incluir inspeccionar el encabezado IP recibido para los identificadores únicos en el encabezado ICMP (el identificador de proceso de la aplicación, por ejemplo).

> [!Note]  
> Para usar un socket de tipo **sock \_ raw** , es necesario disponer de privilegios administrativos. Los usuarios que ejecutan aplicaciones Winsock que utilizan Sockets sin formato deben ser miembros del grupo administradores en el equipo local; de lo contrario, las llamadas de socket sin formato producirán un error con el código [WSAEACCES](windows-sockets-error-codes-2.md). En Windows Vista y versiones posteriores, el acceso a los sockets sin formato se aplica al crear el socket. En versiones anteriores de Windows, el acceso a los sockets sin formato se aplica durante otras operaciones de socket.

 

## <a name="common-uses-of-raw-sockets"></a>Usos comunes de los sockets sin formato

Un uso común de los sockets sin formato es la solución de problemas de las aplicaciones que necesitan examinar los paquetes IP y los encabezados en detalle. Por ejemplo, se puede usar un socket sin formato con el \_ ioctl SiO RCVALL para permitir que un socket reciba todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red. Para obtener más información, consulte la referencia de [**SiO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) .

## <a name="limitations-on-raw-sockets"></a>Limitaciones de los sockets sin formato

En Windows 7, Windows Vista, Windows XP con Service Pack 2 (SP2) y Windows XP con Service Pack 3 (SP3), la capacidad de enviar tráfico a través de sockets sin formato se ha restringido de varias maneras:

-   No se pueden enviar datos TCP a través de sockets sin formato.
-   Los datagramas UDP con una dirección de origen no válida no se pueden enviar a través de sockets sin formato. La dirección de origen IP de cualquier datagrama UDP saliente debe existir en una interfaz de red o se debe quitar el datagrama. Este cambio se realizó para limitar la capacidad de código malintencionado para crear ataques de denegación de servicio distribuidos y limita la capacidad de enviar paquetes suplantados (paquetes TCP/IP con una dirección IP de origen falsificada).
-   No se permite una llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) con un socket sin formato para el \_ protocolo TCP IPPROTO.
    > [!Note]  
    > La función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) con un socket sin formato se permite para otros protocolos ( \_ por ejemplo, IPPROTO IP, IPPROTO \_ UDP o IPPROTO \_ SCTP).

     

Estas restricciones anteriores no se aplican a Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 ni a las versiones del sistema operativo anteriores a Windows XP con SP2.

> [!Note]  
> La implementación de Microsoft de TCP/IP en Windows es capaz de abrir un socket UDP o TCP sin formato en función de las restricciones anteriores. Es posible que otros proveedores Winsock no admitan el uso de sockets sin formato.

 

Existen otras limitaciones para las aplicaciones que usan un socket de tipo **sock \_ raw**. Por ejemplo, todas las aplicaciones que escuchan un protocolo específico recibirán todos los paquetes recibidos para este protocolo. Es posible que esto no sea lo que se desea para varias aplicaciones que usan un protocolo. Esto tampoco es adecuado para las aplicaciones de alto rendimiento. Para solucionar estos problemas, puede que sea necesario escribir un controlador de protocolo de red de Windows (controlador de dispositivo) para el protocolo de red específico. En Windows Vista y versiones posteriores, Winsock kernel (WSK), se puede usar una nueva interfaz de programación de red en modo kernel independiente del transporte para escribir un controlador de protocolo de red. En Windows Server 2003 y versiones anteriores, se puede escribir un proveedor de Interfaz de controlador de transporte (TDI) y una DLL de aplicación auxiliar de Winsock para admitir el protocolo de red. Después, el protocolo de red se agregaría al catálogo Winsock como un protocolo admitido. Esto permite que varias aplicaciones abran Sockets para este protocolo específico y el controlador del dispositivo puede realizar un seguimiento de qué socket recibe paquetes y errores específicos. Para obtener información sobre cómo escribir un proveedor de protocolo de red, vea las secciones sobre WSK y TDI en el kit de controladores de Windows (WDK).

Las aplicaciones también deben tener en cuenta el impacto que la configuración de Firewall puede tener al enviar y recibir paquetes mediante Sockets sin formato.

 

 
