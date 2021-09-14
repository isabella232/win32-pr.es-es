---
description: En esta sección se describen las funciones, las estructuras de datos y los controles del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP).
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Anexo TCP/IP de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967216"
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

 

 



