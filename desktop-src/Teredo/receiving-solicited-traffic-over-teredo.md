---
title: Recepción del tráfico solicitado a través de Teredo
description: Muchas aplicaciones como Microsoft Internet Explorer y Microsoft Outlook solo inician conexiones a Internet.
ms.assetid: bff5d65e-050d-4b09-9982-8024612ffa6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f003755f49d04113108f83c8d3eff67084364ad6dfcf8e9f40cf1bf7e142e0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001683"
---
# <a name="receiving-solicited-traffic-over-teredo"></a>Recepción del tráfico solicitado a través de Teredo

Muchas aplicaciones como Microsoft Internet Explorer y Microsoft Outlook solo inician conexiones a Internet. Para estas aplicaciones, [Teredo](about-teredo.md) puede proporcionar conectividad sin problemas a través de IPv6 en ausencia de otras interfaces IPv6. Además, se puede recibir tráfico solicitado a través de la interfaz de Teredo en las plataformas anteriores de Microsoft Windows XP con Service Pack 2 (SP2) y Windows Server 2003.

En la siguiente documentación se explica cómo estas aplicaciones logran la conectividad y las circunstancias en las que se usa Teredo.

## <a name="obtaining-a-destination-address"></a>Obtener una dirección de destino

Una aplicación intenta obtener la dirección de destino mediante varios métodos, como Sistema de nombres de dominio (DNS) o Protocolo de resolución de nombres del mismo nivel (PNRP). La aplicación puede obtener varias direcciones IP IPv4 e IPv6 mediante estos métodos. Las API típicas que se usan para obtener direcciones IP incluyen la API de Windows XP [**GetHostByName**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) y la nueva api Windows Vista API [**GetAddrInfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo). Por ejemplo, el uso de la API GetAddrInfo con el parámetro de la familia *ai \_* establecido en AF INET6, ya que la sugerencia addrinfo/protocol permite al usuario consultar específicamente las direcciones IPv6 de los servidores \_ DNS. La [**API DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) con el tipo DNS TYPE AAAA también se puede usar para consultar los registros AAAA de los servidores \_ \_ DNS.

## <a name="establishing-a-connection"></a>Establecer una conexión

Una conexión establecida con Teredo se describe como "sin problemas" porque se controla como cualquier otra conexión IPv6. La programación de una aplicación no requiere una consideración especial para poder usar la interfaz Teredo. Cuando se establece una conexión entre interfaces teredo, no se requiere un enrutador de retransmisión, típico de 6to4 y otras interfaces nativas. Sin embargo, Teredo está diseñado como una tecnología de transición de último recurso para la conectividad IPv6.

> [!Note]  
> Teredo no se utiliza si el nombre de host proporcionado se resuelve solo en direcciones IPv4.

 

Cuando una aplicación intenta conectarse a un destino mediante direcciones IPv6, se producirá lo siguiente:

-   La aplicación obtiene una lista de direcciones IPv6 mediante una llamada a la API [**GetAdaptersAddresses.**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) La Windows Vista devuelve una lista de todas las interfaces según el criterio de ordenación especificado en [RFC 3484](https://www.irt.org/rfc/rfc3484.htm). Como resultado, las interfaces IPv6 y 6to4 IPv6 se mostrarán antes que la interfaz Teredo. Sin embargo, cuando la conectividad IPv6 o 6to4 nativa no esté disponible, Teredo será la única interfaz compatible con IPv6 que se muestra.

    Es importante recordar que una aplicación puede usar cualquier interfaz proporcionada por la pila de Windows Vista; sin embargo, la ordenación de la lista de interfaces devuelta suele dar lugar a que Teredo se esté intentando en último lugar.

-   Antes Windows Vista intenta una conexión a través de la interfaz teredo, el sistema operativo garantiza que la dirección IPv6 se ha estabilizado. Esto se hace automáticamente para las conexiones salientes y no es una consideración fundamental para una aplicación. En caso de que la aplicación sea necesaria para garantizar la estabilidad de la dirección, se puede llamar a la API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) para asegurarse de que la dirección de Teredo es estable.

-   Una interfaz de Teredo intentará conectarse a otra interfaz de Teredo en el destino. Si no hay una interfaz teredo, se establece una conexión con una dirección de destino nativa o 6to4 a través de una retransmisión específica del host.

También es posible que las aplicaciones que inician conexiones a Internet reciban tráfico no solicitado. Para más información, [consulte Recepción de tráfico no solicitado a través de Teredo.](receiving-unsolicited-traffic-over-teredo.md)

## <a name="using-the-wsaconnectbyname-api"></a>Uso de la API WSAConnectByName

Al llamar a la API WSAConnectByName, es posible que una aplicación se conecte a un nombre de destino en lugar de especificar la dirección IP exacta. La Windows Vista prefiere IPv6 en lugar de IPv4 y, como resultado, primero se realizarán intentos de conexión a direcciones IPv6.

Al llamar a la API WSAConnectByName, se ordenarán todas las direcciones IP de destino obtenidas en el orden siguiente:

-   Dirección IPv6 nativa
-   Dirección IP 6to4
-   Dirección IPv4
-   Dirección Teredo

Una vez que las direcciones de destino se ordenan internamente, se intenta una conexión al destino en función de la mejor ruta disponible en el host local para la dirección de destino. Como se indica en el orden de las direcciones ordenadas, si el nombre de destino se resuelve en una dirección IPv4 y Teredo, se usará la dirección IPv4 para establecer la conexión.

La API WSAConnectByName funciona internamente para encontrar la mejor coincidencia entre direcciones. Este intento se basa en las rutas disponibles en el host local y en las direcciones de destino.

Debido a la ausencia actual de retransmisiones de Teredo en Internet, es poco probable que las conexiones a direcciones IPv6 nativas se produzcan correctamente a través de la interfaz Teredo. Si se llama a WSAConnectByName, Windows Vista no emitirá consultas AAAA cuando Teredo sea la única interfaz compatible con IPv6 disponible. Esto garantiza que las direcciones IPv6 nativas no se obtienen como destino y que las conexiones se intentan a través de IPv4, que tiene la mayor probabilidad de éxito. Para obtener direcciones IPv6 cuando Teredo es la única interfaz compatible con IPv6, una aplicación debe usar explícitamente la API DnsQuery para los registros AAAA.

 

 