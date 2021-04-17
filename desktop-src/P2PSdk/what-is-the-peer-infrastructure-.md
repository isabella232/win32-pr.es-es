---
description: La infraestructura del mismo nivel es un conjunto de varias API que son eficaces y flexibles.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: ¿Qué es la infraestructura del mismo nivel?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667368"
---
# <a name="what-is-the-peer-infrastructure"></a>¿Qué es la infraestructura del mismo nivel?

La infraestructura del mismo nivel es un conjunto de varias API que son eficaces y flexibles. Entre los componentes principales se incluyen los siguientes:

-   [API de gráficos del mismo nivel](#peer-graphing-api)
-   [API de agrupación del mismo nivel](#peer-grouping-api)
-   [API del administrador de identidades del mismo nivel](#peer-identity-manager-api)
-   [API del proveedor de espacio de nombres PNRP](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a>API de gráficos del mismo nivel

La infraestructura del mismo nivel proporciona una tecnología de gráficos que puede pasar información de forma eficaz y confiable entre los elementos del mismo nivel en un grafo del mismo nivel. La [API de gráficos del mismo nivel](graphing-api.md) garantiza que cada nodo tiene una vista coherente de los datos de un gráfico.

Puede usar la [API de gráficos del mismo nivel](graphing-api.md) para hacer lo siguiente:

-   Crear y administrar gráficos del mismo nivel
-   Enumerar e interactuar con otros elementos del mismo nivel en un grafo del mismo nivel
-   Enviar datos en forma de un [registro](records.md) a cada nodo de un grafo del mismo nivel

## <a name="peer-grouping-api"></a>API de agrupación del mismo nivel

La [API de agrupación del mismo nivel](grouping-api.md) combina y mejora las API [PNRP](#pnrp-namespace-provider-api) y de [gráficos](#peer-graphing-api) del mismo nivel, y agrega los dos componentes siguientes:

-   Una capa de multiplexación que permite que varias aplicaciones que se ejecutan en una entidad del mismo nivel se conecten a un grupo
-   Un modelo de seguridad específico que garantiza que solo los elementos del mismo nivel invitados a un grupo pueden conectarse al grupo a través de la duración del grupo.

Puede usar la API de agrupación del mismo nivel para hacer lo siguiente:

-   Crear y administrar grupos de pares seguros
-   Enumerar e interactuar con otros elementos del mismo nivel en un grupo
-   Enviar datos en forma de un [registro](records.md) a cada nodo de un grupo del mismo nivel

## <a name="peer-identity-manager-api"></a>API del administrador de identidades del mismo nivel

Mediante el uso de la [API del administrador de identidad del mismo nivel](identity-manager-api.md) , puede crear [nombres de mismo nivel](peer-names.md) seguros que PNRP pueda usar para asegurarse de que una persona que publica un nombre posee oficialmente el nombre. Los nombres de mismo nivel también se denominan identidades y se utilizan en la API de agrupación del mismo nivel para identificar a los usuarios de un grupo.

Puede usar la [API del administrador de identidades del mismo nivel](identity-manager-api.md) para hacer lo siguiente:

-   Crear, enumerar y administrar identidades del mismo nivel.

## <a name="pnrp-namespace-provider-api"></a>API del proveedor de espacio de nombres PNRP

La infraestructura del mismo nivel proporciona una tecnología de resolución de nombres sin servidor denominada [API del proveedor de espacio de nombres PNRP](pnrp-namespace-provider-api.md). Mediante el uso de la API del proveedor de espacio de nombres PNRP de Winsock 2, un punto de conexión del mismo nivel, servicio, dispositivo informático y punto de conexión de grupo del mismo nivel puede administrar, registrar, anular el registro y resolver otro punto de conexión en una [nube](clouds.md)PNRP.

> [!Note]  
> PNRP es un acrónimo del **Protocolo de resolución de nombres de mismo nivel**.

 

 

 



