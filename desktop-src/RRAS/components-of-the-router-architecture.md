---
title: Componentes de la arquitectura del enrutador
description: La documentación de administración del enrutador hace referencia frecuente a los siguientes componentes del enrutador.
ms.assetid: 841a5728-39d6-4bd7-a41a-6543b4ed9985
keywords:
- enrutadores RRAS, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f39f104e001db99076dcd29d9d5b603d5cf9f3c526d54cd16e1ed0e4d10c575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791599"
---
# <a name="components-of-the-router-architecture"></a>Componentes de la arquitectura del enrutador

La documentación de administración del enrutador hace referencia frecuente a los siguientes componentes del enrutador.

Administrador de interfaces dinámicas (DIM)

Todas las funciones de administración del enrutador pasan a través de DIM. Según la naturaleza de la función, DIM puede pasar la llamada a uno de los administradores de enrutadores. DIM controla las funciones que solo se encargan de las interfaces. Si la función afecta a los protocolos de enrutamiento, DIM llamará al administrador de enrutadores para el transporte correspondiente a ese protocolo. Por ejemplo, si la función afecta al protocolo Open Shortest Path First (OSPF), DIM llamará al Administrador de enrutadores IP, ya que OSPF es un protocolo de enrutamiento IP.

Administradores de enrutadores

Cada transporte enrutable que se ajusta a la arquitectura del enrutador tiene su propio administrador de enrutadores. Actualmente existen administradores de enrutadores para los transportes IP e IPX. Los administradores de enrutadores administran protocolos de enrutador y otros tipos de clientes de enrutamiento que se ejecutan en interfaces en el equipo local.

Protocolos de enrutamiento y otros clientes

Los clientes son proveedores de servicios que funcionan dentro del marco de la arquitectura del enrutador. Los protocolos de enrutamiento son un tipo de cliente que es compatible con el enrutador.

Los clientes son específicos de un transporte enrutable determinado: IP o IPX. Los protocolos de enrutamiento para el transporte IP incluyen Open Shortest Path First (OSPF) y Protocolo de información de enrutamiento (RIP). Algunos ejemplos de protocolos de enrutamiento IPX son Service Advertising Protocol (SAP) y RIP para IPX. Un ejemplo de un cliente que no es un protocolo de enrutamiento es Traducción de direcciones de red (NAT) para IP.

La interfaz entre el administrador de enrutadores y un cliente se describe en la sección [Interfaz del protocolo de enrutamiento](about-routing-protocol-interface.md). Todos los clientes se ajustan a esta interfaz. Con esta interfaz, los proveedores pueden implementar sus propios clientes que son compatibles con el enrutador.

[Interfaces](interfaces.md)

Una interfaz es una conexión a una red externa. Cada interfaz se identifica mediante un índice de interfaz *único.* Las interfaces son entidades lógicas; Los clientes de enrutador, como NAT o OSPF, tratan con todos los tipos de interfaces de forma similar. Sin embargo, en términos de implementación, una interfaz puede representar una conexión dedicada (por ejemplo, a una red de área local (LAN)) o una conexión de acceso telefónico no dedicada (por ejemplo, una conexión PPP a una red de área extensa (WAN)).

En el caso de una interfaz LAN, la interfaz corresponde a un dispositivo físico real en el equipo, un adaptador LAN. En el caso de una interfaz WAN, la interfaz se asigna a un puerto en el momento en que se establece una conexión. El puerto podría ser un puerto COM, un puerto paralelo o un puerto virtual (para túneles como PPTP y L2TP).

Las interfaces WAN tienen la calidad adicional de que normalmente reciben una dirección de red solo en el momento en que se establece una conexión. Por ejemplo, una interfaz WAN que usa PPP recibe su dirección de capa de red del mismo nivel remoto durante el proceso de conexión. La recepción de una dirección de red como parte del proceso de conexión a veces se conoce como *enlace en tiempo de proceso.*

 

 




