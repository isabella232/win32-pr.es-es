---
title: Componentes de Teredo
ms.assetid: 95d83030-b1de-4f09-b9d0-f443d9672ca1
description: 'Más información sobre: Componentes de Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9bbf8c8f7ad244749d45b091bc52773bcbd9b307c5929fc2fcbfce370d8cfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942371"
---
# <a name="teredo-components"></a>Componentes de Teredo

La [infraestructura de Teredo](about-teredo.md) consta de los siguientes componentes:

## <a name="teredo-clients"></a>Clientes de Teredo

Un cliente de Teredo es un nodo IPv6/IPv4 que admite una interfaz de tunelización de Teredo a través de la cual los paquetes se tunelizaciónn a otros clientes o nodos de Teredo en Internet IPv6 (a través de una retransmisión de Teredo). Un cliente de Teredo se comunica con un servidor de Teredo para obtener un prefijo de dirección desde el que se configura o se usa una dirección IPv6 basada en Teredo para facilitar la comunicación con otros clientes o hosts de Teredo en Internet IPv6.

Windows XP con Service Pack 1 (SP1) con Advanced Networking Pack, Windows XP con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1), Windows Server 2003 con Service Pack 2 (SP2), Windows Vista y Windows Server 2008 incluyen el cliente de Teredo.

## <a name="teredo-servers"></a>Servidores de Teredo

Un servidor Teredo es un nodo IPv6/IPv4 que está conectado a Internet IPv4 e Internet IPv6, y admite una interfaz de tunelización de Teredo a través de la cual se reciben los paquetes. El rol general del servidor de Teredo es ayudar en la configuración de direcciones de los clientes de Teredo y facilitar la comunicación inicial entre los clientes de Teredo y otros clientes de Teredo o entre los clientes de Teredo y los hosts de solo IPv6. El servidor de Teredo escucha el tráfico de Teredo en el puerto UDP 3544.

A diferencia del cliente, el servidor teredo no se incluye con las plataformas operativas de Microsoft. Para facilitar la comunicación Windows equipos cliente de Teredo basados en dispositivos, Microsoft ha implementado servidores Teredo en Internet IPv4.

## <a name="teredo-relays"></a>Retransmisiones de Teredo

Una retransmisión de Teredo es un enrutador IPv6/IPv4 que puede reenviar paquetes entre clientes de Teredo en Internet IPv4 (mediante una interfaz de tunelización de Teredo) y hosts solo IPv6. En algunos casos, la retransmisión de Teredo interactúa con un servidor de Teredo para facilitar la comunicación inicial entre los clientes de Teredo y los hosts solo IPv6. La retransmisión de Teredo escucha el tráfico de Teredo en el puerto UDP 3544.

Al igual que el servidor de Teredo, las plataformas operativas de Microsoft no incluyen la funcionalidad de retransmisión de Teredo. Microsoft no planea actualmente implementar retransmisiones de Teredo en Internet IPv4. Las retransmisiones de Teredo no son necesarias para comunicarse con retransmisiones específicas del host de Teredo.

## <a name="teredo-host-specific-relays"></a>Retransmisiones de Host-Specific Teredo

La comunicación entre los clientes de Teredo y los hosts IPv6 configurados con una dirección global debe pasar por una retransmisión de Teredo. Esto es necesario para los hosts solo IPv6 conectados a Internet IPv6. Sin embargo, cuando el host IPv6 es compatible con IPv6 e IPv4 y está conectado a Internet IPv4 e Internet IPv6, la comunicación debe producirse entre el cliente de Teredo y el host IPv6 a través de Internet IPv4, en lugar de tener que atravesar Internet IPv6 y pasar por una retransmisión de Teredo.

Una retransmisión específica del host de Teredo es un nodo IPv6/IPv4 que tiene una interfaz y conectividad a Internet IPv4 e Internet IPv6 y puede comunicarse directamente con los clientes de Teredo a través de Internet IPv4, sin necesidad de una retransmisión de Teredo intermedia. La conectividad a Internet IPv4 puede ser a través de una dirección IPv4 pública o a través de una dirección IPv4 privada y una NAT vecino. La conectividad a Internet IPv6 puede realizarse a través de una conexión directa a Internet IPv6 o a través de una tecnología de transición IPv6 como 6to4, donde los paquetes IPv6 se tunelización a través de Internet IPv4. La retransmisión específica del host de Teredo escucha en el puerto UDP 3544 el tráfico de Teredo.

Windows XP con SP1 con Advanced Networking Pack, Windows XP con SP2, Windows Server 2003 con SP1, Windows Server 2003 con SP2, Windows Vista y Windows Server 2008 incluyen la funcionalidad de retransmisión específica del host de Teredo, que se habilita automáticamente si el equipo tiene asignada una dirección global. Una dirección global se asigna en un mensaje de anuncio de enrutador recibido desde un enrutador IPv6 nativo, un enrutador ISATAP o un enrutador 6to4. Si el equipo no tiene una dirección global, la funcionalidad de cliente de Teredo está habilitada.

La retransmisión específica del host de Teredo permite a los clientes de Teredo comunicarse eficazmente con hosts de 6to4, hosts IPv6 con un prefijo global distinto de 6to4 o hosts ISATAP o 6over4 dentro de organizaciones que usan un prefijo global para sus direcciones, siempre que ambos hosts usen una versión de Windows que admita Teredo.

 

 




