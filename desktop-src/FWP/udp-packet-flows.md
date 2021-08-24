---
title: Flujos de paquetes UDP
description: El orden en el que se recorren las capas del motor Windows filtro de la Plataforma de filtrado automático (WFP) durante una sesión UDP típica.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e850f67bce9a001d41ebb54b17d3d0d86b94b22f083529e4589d6b69841b7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746645"
---
# <a name="udp-packet-flows"></a>Flujos de paquetes UDP

En esta sección se describe el orden en el que se recorren las capas del motor de filtro Windows Filtering Platform (WFP) durante una sesión UDP típica.

> [!Note]  
> Los flujos de paquetes UDP para IPv6 siguen el mismo patrón que para IPv4.

 

> [!Note]  
> Todos los flujos de paquetes que no son TCP siguen el mismo patrón que los flujos de paquetes UDP.

 

## <a name="udp-connection-establishment"></a>Establecimiento de la conexión UDP

<dl> El servidor (receptor) realiza una apertura pasiva

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (solo Windows 7 /Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4

  
El cliente (remitente) realiza la apertura activa

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (solo Windows 7 /Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4
-   sendto: FWPM \_ LAYER \_ ALE \_ CONNECT REDIRECT \_ \_ V4 (solo Windows 7 /Windows Server 2008 R2)
-   sendto: FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   data: FWPM \_ LAYER \_ DATAGRAM \_ DATA \_ V4
-   Mensaje UDP: FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V4
-   Datagramas IP: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Servidor

-   Datagramas IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   Mensaje UDP: FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V4
-   Mensaje UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   data: FWPM \_ LAYER \_ DATAGRAM \_ DATA \_ V4

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a>Mensaje UDP recibido sin que nadie escuche en el puerto o protocolo

Servidor (receptor)

-   Datagramas IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   Datagramas IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4 \_ DISCARD
-   Icmp Dest Unst Unreachable: FWPM \_ LAYER OUTBOUND ICMP ERROR \_ \_ \_ \_ V4
-   Icmp Dest Unst Unreachable: FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V4
-   Icmp Dest Unst Unreachable: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

> [!Note]  
> UDP sin punto de conexión se indica en Descarte de IPPACKET con una condición de error específica. Bloquee este paquete en el descarte de IPPACKET para que la pila no envíe el evento correspondiente (error ICMP).

 

## <a name="successful-reauthorization-of-a-udp-packet"></a>Reautorización correcta de un paquete UDP

Servidor (receptor)

-   Datagramas IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   Mensaje UDP: FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V4
-   Mensaje UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   Mensaje UDP: FWPM \_ LAYER \_ DATAGRAM \_ DATA \_ V4(INBOUND)

## <a name="failed-reauthorization-of-a-udp-packet"></a>Error de reautorización de un paquete UDP

Servidor (receptor)

-   Datagramas IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   Mensaje UDP: FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V4
-   Mensaje UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   Mensaje UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4 \_ DISCARD

## <a name="udp-connection-termination"></a>Terminación de conexión UDP

La terminación de la conexión UDP no se indica en ninguna capa de WFP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtrar identificadores de capa**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




