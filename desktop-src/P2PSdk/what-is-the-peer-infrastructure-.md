---
description: La infraestructura del mismo nivel es un conjunto de varias API que son eficaces y flexibles.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: ¿Qué es la infraestructura del mismo nivel?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069195"
---
# <a name="what-is-the-peer-infrastructure"></a>¿Qué es la infraestructura del mismo nivel?

La infraestructura del mismo nivel es un conjunto de varias API que son eficaces y flexibles. Los componentes principales incluyen lo siguiente:

-   [Peer Graphing API](#peer-graphing-api)
-   [API de agrupación del mismo nivel](#peer-grouping-api)
-   [Peer Identity Manager API](#peer-identity-manager-api)
-   [PNRP Namespace Provider API](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a>Peer Graphing API

La infraestructura del mismo nivel proporciona una tecnología de grafos que puede pasar información de forma eficaz y confiable entre los pares de un grafo del mismo nivel. Peer [Graphing API garantiza](graphing-api.md) que cada nodo tiene una vista coherente de los datos de un gráfico.

Puede usar Peer [Graphing API para](graphing-api.md) hacer lo siguiente:

-   Creación y administración de gráficos del mismo nivel
-   Enumerar e interactuar con otros elementos del mismo nivel en un gráfico del mismo nivel
-   Envío de datos en forma de [registro](records.md) a cada nodo de un gráfico del mismo nivel

## <a name="peer-grouping-api"></a>API de agrupación del mismo nivel

Peer [Grouping API](grouping-api.md) combina y mejora las API de [grafos](#peer-graphing-api) y [PNRP](#pnrp-namespace-provider-api) del mismo nivel, y agrega los dos componentes siguientes:

-   Capa de multiplexación que permite que varias aplicaciones que se ejecutan en una entidad del mismo nivel se conecten a un grupo
-   Un modelo de seguridad específico que garantiza que solo los compañeros invitados a un grupo puedan conectarse al grupo durante la vigencia del grupo.

Puede usar la API de agrupación del mismo nivel para hacer lo siguiente:

-   Creación y administración de grupos del mismo nivel seguros
-   Enumerar e interactuar con otros elementos del mismo nivel de un grupo
-   Envío de datos en forma de [registro](records.md) a cada nodo de un grupo del mismo nivel

## <a name="peer-identity-manager-api"></a>Peer Identity Manager API

Mediante el uso de la API [](peer-names.md) de Peer [Identity Manager,](identity-manager-api.md) puede crear nombres seguros del mismo nivel que PNRP puede usar para asegurarse de que una persona que publica un nombre posee oficialmente el nombre. Los nombres del mismo nivel también se denominan identidades y se usan en la API de agrupación del mismo nivel para identificar a las personas de un grupo.

Puede usar la [API de Peer Identity Manager](identity-manager-api.md) para hacer lo siguiente:

-   Crear, enumerar y administrar identidades del mismo nivel.

## <a name="pnrp-namespace-provider-api"></a>PNRP Namespace Provider API

La infraestructura del mismo nivel proporciona una tecnología de resolución de nombres sin servidor denominada API del proveedor de [espacios de nombres PNRP](pnrp-namespace-provider-api.md). Mediante el uso de la API del proveedor de espacios de nombres DE WINSOCK 2 PNRP, un punto de [](clouds.md)conexión del mismo nivel, servicio, dispositivo informático y grupo del mismo nivel puede administrar, registrar, anular el registro y resolver otro punto de conexión en una nube PNRP.

> [!Note]  
> PNRP es un acrónimo del protocolo **de resolución de nombres del mismo nivel.**

 

 

 



