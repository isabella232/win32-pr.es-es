---
title: Flujos de paquetes UDP
description: El orden en que se recorren las capas del motor de filtro de la plataforma de filtrado de Windows (WFP) durante una sesión UDP típica.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357430"
---
# <a name="udp-packet-flows"></a>Flujos de paquetes UDP

En esta sección se describe el orden en el que se recorren las capas del motor de filtro de la plataforma de filtrado de Windows (WFP) durante una sesión UDP típica.

> [!Note]  
> Los flujos de paquetes UDP para IPv6 siguen el mismo patrón que para IPv4.

 

> [!Note]  
> Todos los flujos de paquetes que no son TCP siguen el mismo patrón que los flujos de paquetes UDP.

 

## <a name="udp-connection-establishment"></a>Establecimiento de conexiones UDP

<dl> El servidor (receptor) realiza un abierto pasivo

-   enlace: \_ \_ redirección de enlace Ale V4 de nivel FWPM \_ \_ \_ (solo windows 7/Windows Server 2008 R2)
-   BIND: \_ asignación de \_ \_ recursos Ale \_ \_ V4 de capa FWPM

  
El cliente (remitente) realiza una apertura activa

-   enlace: \_ \_ redirección de enlace Ale V4 de nivel FWPM \_ \_ \_ (solo windows 7/Windows Server 2008 R2)
-   BIND: \_ asignación de \_ \_ recursos Ale \_ \_ V4 de capa FWPM
-   SendTo: FWPM \_ capa \_ de \_ conexión Ale \_ V4 de redirección \_ V4 (solo windows 7/Windows Server 2008 R2)
-   SendTo: FWPM \_ capa \_ de \_ autenticación \_ Ale \_ V4
-   \_Flujo ALE de capa de FWPM \_ \_ \_ establecido \_ V4
-   datos: \_ datos de \_ datagramas de nivel FWPM \_ \_ V4
-   Mensaje UDP: \_ transporte de salida de capa FWPM \_ \_ \_ V4
-   Datagramas IP: FWPM \_ de \_ salida de nivel \_ IPPACKET \_ V4

  
Servidor

-   Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4
-   Mensaje UDP: \_ transporte entrante de capa FWPM \_ \_ \_ V4
-   Mensaje UDP: \_ recepción de \_ \_ autenticación Ale \_ \_ de FWPM \_
-   \_Flujo ALE de capa de FWPM \_ \_ \_ establecido \_ V4
-   datos: \_ datos de \_ datagramas de nivel FWPM \_ \_ V4

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a>Se recibió un mensaje UDP que no está escuchando en el puerto o protocolo

Servidor (receptor)

-   Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4
-   Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4 \_
-   Destino ICMP inaccesible: error de \_ ICMP saliente de nivel FWPM \_ \_ \_ \_ V4
-   Destino ICMP inaccesible: transporte de \_ salida de capa FWPM \_ \_ \_ V4
-   No se puede tener acceso al destino ICMP: FWPM de \_ salida de nivel \_ \_ IPPACKET \_ V4

> [!Note]  
> UDP sin punto de conexión se indica en IPPACKET discard con una condición de error específica. Bloquee este paquete en IPPACKET discard para que la pila no envíe el evento correspondiente (error de ICMP).

 

## <a name="successful-reauthorization-of-a-udp-packet"></a>Reautorización correcta de un paquete UDP

Servidor (receptor)

-   Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4
-   Mensaje UDP: \_ transporte entrante de capa FWPM \_ \_ \_ V4
-   Mensaje UDP: \_ recepción de \_ \_ autenticación Ale \_ \_ de FWPM \_
-   Mensaje UDP: \_ datos de datagrama de nivel FWPM \_ \_ \_ V4 (entrante)

## <a name="failed-reauthorization-of-a-udp-packet"></a>No se pudo reautorizar un paquete UDP

Servidor (receptor)

-   Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4
-   Mensaje UDP: \_ transporte entrante de capa FWPM \_ \_ \_ V4
-   Mensaje UDP: \_ recepción de \_ \_ autenticación Ale \_ \_ de FWPM \_
-   Mensaje UDP: recepción de autenticación Ale de FWPM de \_ nivel de \_ \_ \_ recepción \_ aceptación \_ V4 \_ descartada

## <a name="udp-connection-termination"></a>Terminación de la conexión UDP

La terminación de la conexión UDP no se indica en ninguna capa WFP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtrado de identificadores de capas**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




