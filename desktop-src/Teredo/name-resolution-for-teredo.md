---
title: Resolución de nombres para Teredo
ms.assetid: eb0cf6d5-f093-46f6-8995-d01971de8241
description: 'Más información acerca de: resolución de nombres para Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700b5d40fda0546c29bd7c47ee773977c374784c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678346"
---
# <a name="name-resolution-for-teredo"></a>Resolución de nombres para Teredo

La interfaz Teredo emplea actualmente los siguientes protocolos para la resolución de nombres:

## <a name="domain-name-system"></a>Sistema de nombres de dominio

El sistema de nombres de dominio (DNS) es actualmente la tecnología de resolución de nombres más prominente en Internet. La mayoría de los servidores web registran direcciones URL con servidores DNS. Sin embargo, las direcciones de una red doméstica no se registran con servidores DNS, ya que la mayoría de los usuarios domésticos obtienen direcciones IP a través del Protocolo de configuración dinámica de host (DHCP) desde su proveedor de servicios de Internet. Las concesiones DHCP son de una duración relativamente corta y tardan entre 48 y 72 horas en propagar un nombre a lo largo de la nube DNS. Como resultado, el DNS ha demostrado ser un método ineficaz de obtener la dirección IP pública de un usuario doméstico. Una dirección Teredo incluye la dirección IPv4 pública y, por lo tanto, hereda al menos la misma volatilidad de las direcciones IPv4. Por lo tanto, las direcciones Teredo no están registradas actualmente en DNS.

## <a name="peer-name-resolution-protocol"></a>Protocolo de resolución de nombres de mismo nivel

El protocolo de resolución de nombres de mismo nivel (PNRP) es una tecnología DNS distribuida que almacena direcciones IP en miles de equipos de usuario que forman parte de una nube PNRP. Con Windows Vista, cualquier usuario doméstico puede optar por convertirse en miembro de una nube PNRP y anunciar su dirección IPv6 Teredo en la red PNRP. A diferencia de las direcciones asignadas a los servidores DNS, las direcciones de la red PNRP suelen tardar menos de un minuto en propagarse. Dado que las direcciones Teredo pueden cambiar con frecuencia (la dirección IPv4 externa proporcionada por el ISP puede cambiar o el puerto externo que usa el dispositivo de puerta de enlace de Internet del usuario puede cambiar), PNRP ha demostrado ser un mecanismo eficaz para los usuarios domésticos. Los nombres de PNRP, las direcciones que terminan en ". pnrp.net" se basan en una única propiedad del sistema que no cambia. Como resultado, un nombre PNRP es una manera confiable de conectarse a un usuario doméstico. La API de [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) se puede usar para obtener la dirección IP mediante la tecnología PNRP (nombres DNS que terminan con ". PNRP.net") y establecer la conexión con otros hosts.

 

 
