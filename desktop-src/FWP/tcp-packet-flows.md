---
title: Flujos de paquetes TCP
description: El orden en que se recorren las capas del motor de filtro de la plataforma de filtrado de Windows (WFP) durante una sesión TCP típica.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994399"
---
# <a name="tcp-packet-flows"></a>Flujos de paquetes TCP

En esta sección se describe el orden en el que se recorren las capas del motor de filtro de la plataforma de filtrado de Windows (WFP) durante una sesión TCP típica.

> [!Note]  
> Los flujos de paquetes TCP para IPv6 siguen el mismo patrón que para IPv4.

 

> [!Note]  
> Los flujos de paquetes que no son TCP siguen el mismo patrón que los [flujos de paquetes UDP](udp-packet-flows.md).

 

## <a name="tcp-connection-establishment"></a>Establecimiento de la conexión TCP

<dl> El servidor (receptor) realiza un abierto pasivo

-   enlace: \_ \_ redirección de enlace Ale V4 de nivel FWPM \_ \_ \_ (solo windows 7/Windows Server 2008 R2)
-   BIND: \_ asignación de \_ \_ recursos Ale \_ \_ V4 de capa FWPM
-   Listen: FWPM de la \_ autenticación Ale de capa de la \_ \_ \_ escucha \_ V4

  
El cliente (remitente) realiza una apertura activa

-   enlace: \_ \_ redirección de enlace Ale V4 de nivel FWPM \_ \_ \_ (solo windows 7/Windows Server 2008 R2)
-   BIND: \_ asignación de \_ \_ recursos Ale \_ \_ V4 de capa FWPM
-   Connect: \_ REdireccionamiento de la FWPM del nivel de \_ \_ conexión Ale \_ \_ V4 (solo windows 7/Windows Server 2008 R2)
-   conexión: FWPM \_ capa \_ de \_ autenticación \_ Ale \_ V4
-   SYN: \_ transporte de salida de capa FWPM \_ \_ \_ V4
-   SYN: FWPM de \_ nivel \_ saliente \_ IPPACKET \_ V4

  
Servidor

-   SYN: FWPM \_ Layer \_ entrante \_ IPPACKET \_ V4
-   SYN: \_ transporte de entrada de capa FWPM \_ \_ \_ V4
-   SYN: FWPM \_ capa \_ de \_ autenticación Ale de \_ recepción \_ aceptación \_ V4
-   SYN-ACK: \_ transporte de salida de capa FWPM \_ \_ \_ V4
-   SYN-ACK: FWPM de \_ salida de nivel de \_ \_ IPPACKET \_ V4

  
Remoto

-   SYN-ACK: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4
-   SYN-ACK: \_ transporte entrante de capa FWPM \_ \_ \_ V4
-   \_Flujo ALE de capa de FWPM \_ \_ \_ establecido \_ V4
-   CONFIRMACIÓN: transporte de salida de capa de FWPM \_ \_ \_ \_ V4
-   ACK: FWPM de \_ salida de nivel de \_ \_ IPPACKET \_ V4

  
Servidor

-   ACK: FWPM de \_ entrada de nivel de \_ \_ IPPACKET \_ V4
-   ACK: \_ transporte de entrada de capa FWPM \_ \_ \_ V4
-   \_Flujo ALE de capa de FWPM \_ \_ \_ establecido \_ V4
-   Se completa la escucha. El servidor puede realizar una aceptación.

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a>TCP SYN recibidos sin una escucha en el puerto o protocolo

Servidor (receptor)

-   SYN: FWPM \_ Layer \_ entrante \_ IPPACKET \_ V4
-   SYN: FWPM \_ capa de \_ entrada de \_ transporte \_ V4 \_ descartado
-   RST: \_ transporte de salida de capa FWPM \_ \_ \_ V4
-   RST: FWPM \_ de \_ salida de capa saliente \_ IPPACKET \_ V4

> [!Note]  
> TCP SYN sin extremo se indica en TRANSPORT discard con una condición de error específica. Bloquear este paquete en el transporte descartado para hacer que la pila no envíe el evento correspondiente (RST). Para obtener un ejemplo de filtrado de modo oculto, consulte [impedir el examen de puertos](preventing-port-scanning.md).

 

## <a name="data-transmitted-over-a-tcp-connection"></a>Datos transmitidos a través de una conexión TCP

<dl> Cliente (remitente)

-   Enviar
-   datos: \_ flujo de capa FWPM \_ \_ V4
-   Segmentos TCP: \_ transporte de salida de capa FWPM \_ \_ \_ V4
-   Datagramas IP: FWPM \_ de \_ salida de nivel \_ IPPACKET \_ V4

  
Servidor (receptor)

-   Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4
-   Segmentos TCP: \_ transporte de entrada de capa FWPM \_ \_ \_ V4
-   datos: \_ flujo de capa FWPM \_ \_ V4
-   Los datos están disponibles para leer.

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a>Reautorización correcta de un paquete TCP

Servidor (receptor)

-   Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4
-   Segmento TCP: \_ transporte entrante de capa FWPM \_ \_ \_ V4
-   Segmento TCP: aceptación de autenticación Ale de FWPM de capa de la \_ \_ \_ \_ recepción \_ \_ V4
-   datos: \_ flujo de capa FWPM \_ \_ V4 (entrante)

## <a name="failed-reauthorization-of-a-tcp-packet"></a>No se pudo reautorizar un paquete TCP

Servidor (receptor)

-   Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4
-   Segmento TCP: \_ transporte entrante de capa FWPM \_ \_ \_ V4
-   Segmento TCP: aceptación de autenticación Ale de FWPM de capa de la \_ \_ \_ \_ recepción \_ \_ V4
-   Segmento TCP: recepción de autenticación Ale de FWPM de \_ nivel de \_ \_ \_ recepción \_ aceptación \_ V4 \_ descartada

## <a name="tcp-connection-termination"></a>Terminación de la conexión TCP

La terminación de la conexión TCP no se indica en ninguna capa WFP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtrado de identificadores de capas**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




