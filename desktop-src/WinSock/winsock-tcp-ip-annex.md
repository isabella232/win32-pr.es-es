---
description: En esta sección se describen las funciones, las estructuras de datos y los controles del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP).
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Anexo TCP/IP de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a5cc403f0ff7f7e6b1daeb979ae9b7ec6ab3c3bed455843cec7ae4f43469975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822369"
---
# <a name="winsock-tcpip-annex"></a>Anexo TCP/IP de Winsock

En esta sección se describen las funciones, las estructuras de datos y los controles del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP).



| Elemento          | Descripción                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Nombres de protocolo | TCP, UDP                                                                                                                                    |
| Descripción      | Proporciona servicios de transporte a través de la capa de red IP: UDP para datagramas no confiables, TCP para flujos de bytes confiables y orientados a la conexión. |
| Familia de direcciones   | **AF \_ INET**, **AF \_ INET6**                                                                                                                 |
| Archivo de encabezado      | *Ws2tcpip.h*                                                                                                                                |



 

Se ofrecen dos tipos básicos de servicios de transporte: datagramas no confiables (UDP) y flujos de bytes orientados a conexiones confiables (TCP). Además, se admite opcionalmente un socket sin formato. Los sockets sin procesar permiten que una aplicación se comunique a través de protocolos distintos de TCP y UDP, como ICMP. Los sockets sin procesar se admiten en las familias de direcciones **\_ AF INET** y **AF \_ INET6** con algunas limitaciones.

En esta sección se tratan las extensiones de Winsock que son específicas de los protocolos TCP/IP. También se describen aspectos de las funciones base de Winsock que requieren una consideración especial o que pueden presentar un comportamiento único al usar TCP/IP.

 

 



