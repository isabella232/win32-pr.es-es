---
description: En esta sección se describen las funciones, estructuras de datos y controles del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP).
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Anexo TCP/IP de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275791"
---
# <a name="winsock-tcpip-annex"></a>Anexo TCP/IP de Winsock

En esta sección se describen las funciones, estructuras de datos y controles del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP).



| Elemento          | Descripción                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre (s) de protocolo | TCP, UDP                                                                                                                                    |
| Descripción      | Proporciona servicios de transporte a través del nivel de red IP: UDP para datagramas no confiables, TCP para flujos de bytes orientados a la conexión y confiables. |
| Familia de direcciones   | **AF \_ INET**, **AF \_ inet6**                                                                                                                 |
| Archivo de encabezado      | *Ws2tcpip. h*                                                                                                                                |



 

Se ofrecen dos tipos básicos de servicios de transporte: datagramas no confiables (UDP) y de conexión confiable orientados a secuencias de bytes (TCP). Además, se admite opcionalmente un socket sin formato. Los sockets sin formato permiten a una aplicación comunicarse a través de protocolos distintos de TCP y UDP, como ICMP. Los sockets sin formato se admiten en las familias de direcciones **AF \_ inetd** y **AF \_ inet6** con algunas limitaciones.

En esta sección se describen las extensiones de Winsock que son específicas de los protocolos TCP/IP. También describe aspectos de las funciones base de Winsock que requieren una consideración especial o que pueden presentar un comportamiento único cuando se usa TCP/IP.

 

 



