---
title: Componentes de Teredo
ms.assetid: 95d83030-b1de-4f09-b9d0-f443d9672ca1
description: 'Más información acerca de: componentes de Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b4de66f38d5eb64b8321b6bb89e78fbb763e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677271"
---
# <a name="teredo-components"></a>Componentes de Teredo

La infraestructura de [Teredo](about-teredo.md) consta de los siguientes componentes:

## <a name="teredo-clients"></a>Clientes Teredo

Un cliente Teredo es un nodo IPv6/IPv4 que admite una interfaz de túnel Teredo a través de la cual los paquetes se tunelizan a otros clientes o nodos Teredo en Internet por IPv6 (a través de una retransmisión Teredo). Un cliente Teredo se comunica con un servidor Teredo para obtener un prefijo de dirección desde el que una dirección IPv6 basada en Teredo está configurada o se utiliza para facilitar la comunicación con otros clientes o hosts Teredo en Internet por IPv6.

Windows XP con Service Pack 1 (SP1) con Advanced Networking Pack, Windows XP con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1), Windows Server 2003 con Service Pack 2 (SP2), Windows Vista y Windows Server 2008 incluyen el cliente Teredo.

## <a name="teredo-servers"></a>Servidores Teredo

Un servidor Teredo es un nodo IPv6/IPv4 que está conectado a Internet IPv4 e Internet IPv6, y es compatible con una interfaz de túnel Teredo en la que se reciben los paquetes. El rol general del servidor Teredo es ayudarle en la configuración de la dirección de los clientes Teredo y para facilitar la comunicación inicial entre los clientes Teredo y otros clientes Teredo, o entre los clientes Teredo y los hosts solo IPv6. El servidor Teredo escucha en el puerto UDP 3544 para el tráfico Teredo.

A diferencia del cliente de, el servidor Teredo no está incluido en las plataformas operativas de Microsoft. Para facilitar la comunicación entre los equipos cliente Teredo basados en Windows, Microsoft ha implementado Servidores Teredo en Internet por IPv4.

## <a name="teredo-relays"></a>Retransmisiones Teredo

Una retransmisión Teredo es un enrutador IPv6/IPv4 que puede reenviar paquetes entre clientes Teredo en Internet por IPv4 (mediante una interfaz de túnel Teredo) y hosts solo IPv6. En algunos casos, la retransmisión Teredo interactúa con un servidor Teredo para facilitar la comunicación inicial entre los clientes Teredo y los hosts solo IPv6. La retransmisión Teredo escucha en el puerto UDP 3544 para el tráfico Teredo.

Al igual que el servidor Teredo, las plataformas operativas de Microsoft no incluyen la funcionalidad de retransmisión de Teredo. Microsoft no planea actualmente la implementación de retransmisiones Teredo en Internet por IPv4. No es necesario que las retransmisiones Teredo se comuniquen con retransmisiones específicas del host Teredo.

## <a name="teredo-host-specific-relays"></a>Retransmisiones de Host-Specific Teredo

La comunicación entre los clientes Teredo y los hosts IPv6 configurados con una dirección global debe pasar por una retransmisión Teredo. Esto es necesario para los hosts solo IPv6 conectados a Internet por IPv6. Sin embargo, cuando el host IPv6 es compatible con IPv4 y IPv4 y está conectado a Internet IPv4 e IPv6 Internet, se debe realizar la comunicación entre el cliente Teredo y el host IPv6 a través de Internet por IPv4, en lugar de tener que atravesar Internet IPv6 y pasar por una retransmisión Teredo.

Una retransmisión específica del host Teredo es un nodo IPv6/IPv4 que tiene una interfaz y conectividad con la red Internet IPv4 e IPv6, y puede comunicarse directamente con los clientes Teredo a través de Internet por IPv4, sin necesidad de una retransmisión Teredo intermedia. La conectividad a Internet IPv4 puede realizarse a través de una dirección IPv4 pública o a través de una dirección IPv4 privada y una NAT adyacente. La conectividad a Internet IPv6 puede realizarse a través de una conexión directa a Internet IPv6 o a través de una tecnología de transición IPv6 como 6to4, donde los paquetes IPv6 se tunelizan a través de Internet por IPv4. La retransmisión específica del host Teredo escucha en el puerto UDP 3544 para el tráfico Teredo.

Windows XP con SP1 con Advanced Networking Pack, Windows XP con SP2, Windows Server 2003 con SP1, Windows Server 2003 con SP2, Windows Vista y Windows Server 2008 incluyen la funcionalidad de retransmisión específica del host Teredo, que se habilita automáticamente si el equipo tiene asignada una dirección global. Se asigna una dirección global en un mensaje de anuncio de enrutador recibido de un enrutador IPv6 nativo, un enrutador ISATAP o un enrutador 6to4. Si el equipo no tiene una dirección global, la funcionalidad de cliente Teredo está habilitada.

La retransmisión específica del host Teredo permite a los clientes Teredo comunicarse de forma eficaz con hosts 6to4, hosts IPv6 con un prefijo global no 6to4 o hosts ISATAP o 6over4 dentro de organizaciones que usan un prefijo global para sus direcciones, siempre que ambos hosts usen una versión de Windows que admita Teredo.

 

 




