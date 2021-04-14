---
title: Recibir tráfico solicitado a través de Teredo
description: Muchas aplicaciones, como Microsoft Internet Explorer y Microsoft Outlook, solo inician conexiones a Internet.
ms.assetid: bff5d65e-050d-4b09-9982-8024612ffa6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035d067afeb9c62795efb5acd0bb28adc3afcb16
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104533562"
---
# <a name="receiving-solicited-traffic-over-teredo"></a>Recibir tráfico solicitado a través de Teredo

Muchas aplicaciones, como Microsoft Internet Explorer y Microsoft Outlook, solo inician conexiones a Internet. Para estas aplicaciones, [Teredo](about-teredo.md) puede proporcionar conectividad fluida a través de IPv6 en ausencia de otras interfaces IPv6. Además, se puede recibir tráfico solicitado a través de la interfaz Teredo en las plataformas anteriores de Microsoft Windows XP con Service Pack 2 (SP2) y Windows Server 2003.

En la siguiente documentación se explica cómo estas aplicaciones consiguen la conectividad y las circunstancias en las que se utiliza Teredo.

## <a name="obtaining-a-destination-address"></a>Obtención de una dirección de destino

Una aplicación intenta obtener la dirección de destino mediante varios métodos como el sistema de nombres de dominio (DNS) o el protocolo de resolución de nombres de mismo nivel (PNRP). Es posible que la aplicación obtenga varias direcciones IP IPv4 e IPv6 mediante estos métodos. Las API típicas que se usan para obtener direcciones IP incluyen la API de Windows XP [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) y la nueva API de Windows Vista [**función getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo). Por ejemplo, si se usa la API función getaddrinfo con el parámetro de la *\_ familia AI* establecido en AF \_ inet6 como la sugerencia addrinfo/Protocol, el usuario puede consultar los servidores DNS para las direcciones IPv6 específicamente. La API de [**DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) con el tipo DNS \_ Type \_ AAAA también puede usarse para consultar los registros AAAA en los servidores DNS.

## <a name="establishing-a-connection"></a>Establecer una conexión

Una conexión establecida con Teredo se describe como "fluida" porque se trata como cualquier otra conexión IPv6. La programación de una aplicación no requiere una consideración especial para poder usar la interfaz Teredo. Cuando se establece una conexión entre las interfaces de Teredo, no es necesario un enrutador de retransmisión, típico de 6to4 y otras interfaces nativas. Sin embargo, Teredo está diseñado como tecnología de transición de último recurso para la conectividad IPv6.

> [!Note]  
> Teredo no se usará si el nombre de host proporcionado se resuelve solo en direcciones IPv4.

 

Cuando una aplicación intenta conectarse a un destino mediante direcciones IPv6, ocurrirá lo siguiente:

-   La aplicación obtiene una lista de direcciones IPv6 mediante una llamada a la API [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) . La pila de Windows Vista devuelve una lista de todas las interfaces según el criterio de ordenación especificado en [RFC 3484](https://www.irt.org/rfc/rfc3484.htm). Como resultado, las interfaces IPv6 e IPv6 6to4 se enumerarán antes que la interfaz Teredo. Sin embargo, cuando la conectividad IPv6 o 6to4 nativa no está disponible, Teredo será la única interfaz compatible con IPv6 que se muestra.

    Es importante recordar que una aplicación puede usar cualquier interfaz proporcionada por la pila de Windows Vista; sin embargo, la ordenación de la lista de interfaces devuelta normalmente hará que se intente usar Teredo en último lugar.

-   Antes de que Windows Vista intente una conexión a través de la interfaz Teredo, el sistema operativo garantiza que la dirección IPv6 esté estabilizada. Esto se hace automáticamente para las conexiones salientes y no es una consideración fundamental para una aplicación. En el caso de que la aplicación sea necesaria para garantizar la estabilidad de la dirección, se puede llamar a la API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) para asegurarse de que la dirección Teredo es estable.

-   Una interfaz Teredo intentará conectarse a otra interfaz Teredo en el destino. Si no hay una interfaz Teredo, se establece una conexión con una dirección de destino nativa o 6to4 a través de una retransmisión específica del host.

También es posible que las aplicaciones que inician conexiones a Internet reciban tráfico no solicitado. Para obtener más información, consulte [recibir tráfico no solicitado a través de Teredo](receiving-unsolicited-traffic-over-teredo.md).

## <a name="using-the-wsaconnectbyname-api"></a>Uso de la API de WSAConnectByName

Al llamar a la API WSAConnectByName, es posible que una aplicación se conecte a un nombre de destino en lugar de especificar la dirección IP exacta. La pila de Windows Vista prefiere IPv6 a través de IPv4 y, como resultado, los intentos de conexión se realizarán primero en las direcciones IPv6.

Al llamar a la API WSAConnectByName se ordenarán todas las direcciones IP de destino obtenidas en el siguiente orden:

-   Dirección IPv6 nativa
-   Dirección IP 6to4
-   Dirección IPv4
-   Dirección Teredo

Una vez que las direcciones de destino se ordenan internamente, se intenta establecer una conexión con el destino en función de la mejor ruta disponible en el host local para la dirección de destino. Como se indica en el orden de las direcciones ordenadas, si el nombre de destino se resuelve en una dirección IPv4 y Teredo, se usará la dirección IPv4 para establecer la conexión.

La API de WSAConnectByName funciona internamente para encontrar la mejor coincidencia entre las direcciones. Este intento se basa en las rutas disponibles en el host local y en las direcciones de destino.

Debido a la ausencia actual de retransmisiones Teredo en Internet, es poco probable que las conexiones a direcciones IPv6 nativas se realicen correctamente a través de la interfaz Teredo. Si se llama a WSAConnectByName, Windows Vista no emitirá consultas AAAA cuando Teredo sea la única interfaz compatible con IPv6 disponible. Esto garantiza que las direcciones IPv6 nativas no se obtienen como destino y que se intentan las conexiones a través de IPv4, lo que tiene la mayor probabilidad de éxito. Con el fin de obtener direcciones IPv6 cuando Teredo es la única interfaz compatible con IPv6, una aplicación debe usar explícitamente la API DnsQuery para registros AAAA.

 

 