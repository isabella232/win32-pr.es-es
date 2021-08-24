---
title: Flujos de paquetes TCP
description: El orden en el que se recorren las capas del motor de Windows de filtro de la Plataforma de filtrado automático (WFP) durante una sesión TCP típica.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d4836da7a1912a6e39358b54e2a3086dd80efe844d6a301d079014d4a5b209
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746635"
---
# <a name="tcp-packet-flows"></a>Flujos de paquetes TCP

En esta sección se describe el orden en el que se recorren las capas del motor de filtro Windows Filtering Platform (WFP) durante una sesión TCP típica.

> [!Note]  
> Los flujos de paquetes TCP para IPv6 siguen el mismo patrón que para IPv4.

 

> [!Note]  
> Los flujos de paquetes que no son TCP siguen el mismo patrón que los [flujos de paquetes UDP.](udp-packet-flows.md)

 

## <a name="tcp-connection-establishment"></a>Establecimiento de la conexión TCP

<dl> El servidor (receptor) realiza una apertura pasiva

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (solo Windows 7 /Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4
-   listen: FWPM \_ LAYER \_ ALE \_ AUTH \_ LISTEN \_ V4

  
El cliente (remitente) realiza la apertura activa

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (solo Windows 7 /Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4
-   connect: FWPM \_ LAYER \_ ALE \_ CONNECT REDIRECT \_ \_ V4 (solo Windows 7 /Windows Server 2008 R2)
-   connect: FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V4
-   SYN: TRANSPORTE SALIENTE DE CAPA FWPM \_ \_ \_ \_ V4
-   SYN: \_ \_ IPPACKET V4 DE SALIDA DE CAPA \_ FWPM \_

  
Servidor

-   SYN: \_ IPPACKET DE ENTRADA DE CAPA \_ \_ FWPM \_ V4
-   SYN: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   SYN: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   SYN-ACK: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   SYN-ACK: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Cliente

-   SYN-ACK: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   SYN-ACK: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   ACK: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   ACK: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Servidor

-   ACK: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   ACK: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   La escucha se completa. El servidor puede realizar una aceptación.

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a>TCP SYN recibido sin que nadie escuche en el puerto o protocolo

Servidor (receptor)

-   SYN: \_ IPPACKET DE ENTRADA DE CAPA \_ \_ FWPM \_ V4
-   SYN: DESCARTE DE TRANSPORTE ENTRANTE DE CAPA FWPM \_ \_ \_ \_ V4 \_
-   RST: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   RST: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

> [!Note]  
> TCP SYN sin punto de conexión se indica en Descarte de TRANSPORTE con una condición de error específica. Bloquee este paquete en EL DESCARTE DE TRANSPORTE para que la pila no envíe el evento correspondiente (RST). Para obtener un ejemplo de filtrado en modo sigiloso, vea [Preventing Port Scanning](preventing-port-scanning.md).

 

## <a name="data-transmitted-over-a-tcp-connection"></a>Datos transmitidos a través de una conexión TCP

<dl> Cliente (remitente)

-   Enviar
-   data: FWPM \_ LAYER \_ STREAM \_ V4
-   Segmentos TCP: FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V4
-   Datagramas IP: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Servidor (receptor)

-   Datagramas IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   Segmentos TCP: FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V4
-   data: FWPM \_ LAYER \_ STREAM \_ V4
-   Los datos están disponibles para leer.

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a>Reautorización correcta de un paquete TCP

Servidor (receptor)

-   Datagramas IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   Segmento TCP: FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V4
-   Segmento TCP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   data: FWPM \_ LAYER \_ STREAM \_ V4(INBOUND)

## <a name="failed-reauthorization-of-a-tcp-packet"></a>Error de reautorización de un paquete TCP

Servidor (receptor)

-   Datagramas IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   Segmento TCP: FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V4
-   Segmento TCP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   Segmento TCP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4 \_ DISCARD

## <a name="tcp-connection-termination"></a>Terminación de conexión TCP

La terminación de la conexión TCP no se indica en ninguna capa de WFP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtrar identificadores de capa**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




