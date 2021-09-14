---
title: Resolución de nombres para Teredo
ms.assetid: eb0cf6d5-f093-46f6-8995-d01971de8241
description: 'Más información sobre: Resolución de nombres para Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700b5d40fda0546c29bd7c47ee773977c374784c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073389"
---
# <a name="name-resolution-for-teredo"></a>Resolución de nombres para Teredo

La interfaz teredo utiliza actualmente los siguientes protocolos para la resolución de nombres:

## <a name="domain-name-system"></a>Sistema de nombres de dominio

El Sistema de nombres de dominio (DNS) es actualmente la tecnología de resolución de nombres más destacada en Internet. La mayoría de los servidores web registran direcciones URL con servidores DNS. Sin embargo, las direcciones de una red doméstica no se registran con servidores DNS, ya que la mayoría de los usuarios de origen obtienen direcciones IP a través del Protocolo de configuración dinámica de host (DHCP) de su proveedor de servicios de Internet. Las concesiones DHCP tienen una duración relativamente corta y pueden tardar entre 48 y 72 horas en propagar un nombre por toda la nube DNS. Como resultado, DNS ha demostrado ser un método ineficaz de obtener la dirección IP pública de un usuario principal. Una dirección Teredo incluye la dirección IPv4 pública y, por tanto, hereda al menos la misma inestabilidad de las direcciones IPv4. Por lo tanto, las direcciones de Teredo no están registradas actualmente en DNS.

## <a name="peer-name-resolution-protocol"></a>Protocolo de resolución de nombres de mismo nivel

El Protocolo de resolución de nombres del mismo nivel (PNRP) es una tecnología DNS distribuida que almacena direcciones IP en miles de máquinas de usuario que forman parte de una nube PNRP. Con Windows Vista, cualquier usuario principal puede optar por convertirse en miembro de una nube PNRP y anunciar su dirección IPv6 de Teredo en la red PNRP. A diferencia de las direcciones que se dan a los servidores DNS, las direcciones de la red PNRP suelen tardar menos de un minuto en propagarse. Dado que las direcciones de Teredo pueden cambiar con frecuencia (la dirección IPv4 externa proporcionada por el ISP puede cambiar o el puerto externo que usa el dispositivo de puerta de enlace de Internet del usuario puede cambiar), PNRP ha demostrado ser un mecanismo eficaz para los usuarios del hogar. Los nombres PNRP, las direcciones que terminan con ".pnrp.net" se basan en propiedades del sistema únicas que no cambian. Como resultado, un nombre PNRP es una manera confiable de conectarse a un usuario principal. La API [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) se puede usar para obtener la dirección IP mediante la tecnología PNRP (nombres DNS que terminan con ".pnrp.net") y establecer la conexión con otros hosts.

 

 
