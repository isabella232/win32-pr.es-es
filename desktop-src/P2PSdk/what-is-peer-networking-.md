---
description: Las redes punto a punto son una tecnología de red sin servidor que permite que varios dispositivos de red compartan recursos y se comuniquen directamente entre sí.
ms.assetid: d2a43d3b-2782-4777-8c65-05e2c52930d0
title: ¿Qué son las redes del mismo nivel?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f6ce2175aa32e37c80c4cde5c231540a48c448360974ecbd022c21eb552ccdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034105"
---
# <a name="what-is-peer-networking"></a>¿Qué son las redes del mismo nivel?

Las redes punto a punto son una tecnología de red sin servidor que permite que varios dispositivos de red compartan recursos y se comuniquen directamente entre sí. Esta tecnología está disponible para Windows XP con Service Pack 1 (SP1) y clientes posteriores que ejecutan Advanced Networking Pack para la infraestructura punto a punto.

La infraestructura punto a punto es un conjunto de API de red que le ayudan a desarrollar aplicaciones de red descentralizadas que usan la potencia colectiva de los equipos en una red. Por ejemplo, las aplicaciones punto a punto pueden ser comunicaciones de colaboración, tecnologías de distribución de contenido, entre otras.

La infraestructura punto a punto proporciona una infraestructura de red sólida para que pueda concentrarse en el desarrollo de aplicaciones, ya que la infraestructura se desarrolla en su lugar.

La infraestructura punto a punto incluye los siguientes componentes principales:

-   [Resolución de nombres del mismo nivel escalable y segura](#scalable-and-secure-peer-name-resolution)
-   [Comunicación multipunto eficaz](#efficient-multipoint-communication)
-   [Administración de datos distribuidos](#distributed-data-management)
-   [Proteger identidades del mismo nivel](#secure-peer-identities)
-   [Proteger grupos punto a punto](#secure-peer-to-peer-groups)

## <a name="scalable-and-secure-peer-name-resolution"></a>Resolución de nombres del mismo nivel escalable y segura

La API del proveedor de espacios de nombres del Protocolo de resolución de nombres del mismo nivel [(PNRP)](pnrp-namespace-provider-api.md) es un protocolo de resolución de nombre a IP. El ámbito o contexto IPv6 que incluye todos los pares participantes se denomina [nube](clouds.md). PNRP permite a los elementos del mismo nivel interactuar entre sí dentro de una nube.

## <a name="efficient-multipoint-communication"></a>Comunicación multipunto eficaz

La infraestructura punto a punto incluye [Graphing API](graphing-api.md) que proporciona una comunicación multipunto eficaz. Al igual que PNRP, el grafo punto a punto permite que un conjunto de nodos interactúe y pase datos entre sí en forma de [registro.](records.md) Cada registro que un elemento del mismo nivel genera o actualiza se envía a todos los nodos de un gráfico.

## <a name="distributed-data-management"></a>Distribución Administración de datos

La administración de datos distribuida almacena automáticamente todos los registros enviados a un gráfico punto a punto hasta la hora de expiración especificada para cada registro. Las redes punto a punto garantizan que cada nodo de un gráfico punto a punto tiene una vista similar de la base de datos de registros. Si un gráfico punto a punto tiene asociado un modelo de seguridad, el gráfico contiene la siguiente información:

-   Quién y no se puede conectar a un grafo
-   Quién proteger y validar registros en función de criterios definidos externamente

## <a name="secure-peer-identities"></a>Proteger identidades del mismo nivel

La infraestructura punto a punto proporciona una [API](identity-manager-api.md) de Identity Manager punto a punto que permite crear, administrar y manipular las identidades del mismo nivel. Las identidades del mismo nivel se usan para definir nombres para puntos de conexión seguros en PNRP y pueden representar cualquier recurso que participe en una red punto a punto, incluidos servicios y grupos punto a punto seguros.

## <a name="secure-peer-to-peer-groups"></a>Proteger grupos punto a punto

La API de agrupación punto a punto combina las [API](grouping-api.md) de grafos punto a punto, Identity Manager y PNRP para formar una solución cohesiva y cómoda para el desarrollo de aplicaciones de red punto a punto. La API de agrupación punto a punto usa la API de Peer-to-Peer Identity Manager y un esquema de certificado autofirmado para garantizar la seguridad dentro de la infraestructura de grafos. Cada grupo se puede resolver y registrar a través de PNRP, lo que permite la resolución de nombres de pares aleatorios dentro de un grupo punto a punto registrado. Un grupo puede ser un punto de conexión en PNRP, al igual que un elemento del mismo nivel.

Para obtener información general sobre la infraestructura punto a punto, consulte el artículo "Introducción a las Windows xp punto a[punto".](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)

Para obtener información general de las API de la infraestructura punto a punto, vea el tema ¿Qué es [la infraestructura del mismo nivel?](what-is-the-peer-infrastructure-.md).

 

 



