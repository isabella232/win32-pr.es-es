---
description: La red punto a punto es una tecnología de red sin servidor que permite que varios dispositivos de red compartan recursos y se comuniquen entre sí directamente.
ms.assetid: d2a43d3b-2782-4777-8c65-05e2c52930d0
title: ¿Qué es la red del mismo nivel?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c456fac9b7695a2846765ee0ccd38c1e5df646e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001990"
---
# <a name="what-is-peer-networking"></a>¿Qué es la red del mismo nivel?

La red punto a punto es una tecnología de red sin servidor que permite que varios dispositivos de red compartan recursos y se comuniquen entre sí directamente. Esta tecnología está disponible para Windows XP con Service Pack 1 (SP1) y clientes posteriores que ejecutan Advanced Networking Pack para la infraestructura punto a punto.

La infraestructura punto a punto es un conjunto de API de red que le ayudarán a desarrollar aplicaciones de red descentralizadas que usan la eficacia colectiva de los equipos de una red. Por ejemplo, las aplicaciones punto a punto pueden ser comunicaciones de colaboración, tecnologías de distribución de contenido, etc.

La infraestructura punto a punto proporciona una infraestructura de red sólida para que pueda concentrarse en el desarrollo de aplicaciones, ya que la infraestructura se desarrolla para usted.

La infraestructura punto a punto incluye los componentes principales siguientes:

-   [Resolución de nombres de mismo nivel segura y escalable](#scalable-and-secure-peer-name-resolution)
-   [Comunicación Multipoint eficaz](#efficient-multipoint-communication)
-   [Administración de datos distribuidos](#distributed-data-management)
-   [Identidades seguras del mismo nivel](#secure-peer-identities)
-   [Proteger grupos punto a punto](#secure-peer-to-peer-groups)

## <a name="scalable-and-secure-peer-name-resolution"></a>Resolución de nombres de mismo nivel segura y escalable

La [API del proveedor de espacios de nombres del Protocolo de resolución de nombres de mismo nivel (PNRP)](pnrp-namespace-provider-api.md) es un protocolo de resolución de nombres a direcciones IP. El ámbito o contexto IPv6 que incluye todos los elementos del mismo nivel participantes se denomina [nube](clouds.md). PNRP permite que los pares interactúen entre sí dentro de una nube.

## <a name="efficient-multipoint-communication"></a>Comunicación Multipoint eficaz

La infraestructura punto a punto incluye la API de [gráficos](graphing-api.md) que proporciona comunicación Multipoint eficaz. Como PNRP, la representación gráfica punto a punto permite que un conjunto de nodos interactúe y pase datos entre sí en forma de un [registro](records.md). Cada registro que un elemento del mismo nivel genera o actualiza se envía a todos los nodos de un gráfico.

## <a name="distributed-data-management"></a>Administración de datos distribuido

La administración de datos distribuidos almacena automáticamente todos los registros enviados a un grafo punto a punto hasta la hora de expiración especificada para cada registro. La red punto a punto garantiza que cada nodo de un grafo punto a punto tiene una vista similar de la base de datos de registros. Si un grafo punto a punto tiene un modelo de seguridad asociado, el gráfico contiene la siguiente información:

-   Quién puede y no puede conectarse a un grafo
-   Quién puede proteger y validar registros en función de criterios definidos externamente

## <a name="secure-peer-identities"></a>Identidades seguras del mismo nivel

La infraestructura punto a punto proporciona una [API de administrador de identidades](identity-manager-api.md) punto a punto que permite crear, administrar y manipular las identidades del mismo nivel. Las identidades del mismo nivel se usan para definir los nombres de los puntos de conexión seguros en PNRP y pueden representar cualquier recurso que participa en una red punto a punto, incluidos los servicios y grupos de punto a punto seguros.

## <a name="secure-peer-to-peer-groups"></a>Proteger grupos punto a punto

La [API de agrupación](grouping-api.md) punto a punto combina los gráficos de punto a punto, el administrador de identidades y las API de PNRP para formar una solución coherente y cómoda para el desarrollo de aplicaciones de red punto a punto. La API de agrupación punto a punto usa la API del administrador de identidades punto a punto y un esquema de certificado autofirmado para garantizar la seguridad dentro de la infraestructura de gráficos. Cada grupo se puede resolver y registrar a través de PNRP, lo que permite la resolución de nombres de pares aleatorios dentro de un grupo de punto a punto registrado. Un grupo puede ser un punto de conexión en PNRP, al igual que un elemento del mismo nivel.

Para obtener información general sobre la infraestructura punto a punto, consulte el artículo "[Introducción a las redes de punto a punto de Windows XP](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)".

Para obtener información general sobre las API de la infraestructura punto a punto, vea el tema [¿Qué es la infraestructura del mismo nivel?](what-is-the-peer-infrastructure-.md)

 

 



