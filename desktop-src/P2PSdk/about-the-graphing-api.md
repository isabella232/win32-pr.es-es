---
description: Peer Graphing API permite a las aplicaciones pasar datos entre pares de forma eficaz y confiable. Los conceptos básicos de la tecnología de grafos del mismo nivel son los nodos de un grafo del mismo nivel y los avisos de eventos.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Acerca de Graphing API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735bf7993744aa8d1e76b8c5d98e8d6856bb4e1757224cd0c98f2e7b1b6f710b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011793"
---
# <a name="about-the-graphing-api"></a>Acerca de Graphing API

Peer Graphing API permite a las aplicaciones pasar datos entre pares de forma eficaz y confiable. Los conceptos básicos de la tecnología de grafos del mismo nivel son **los nodos** de un grafo del mismo nivel y los avisos de eventos.

## <a name="nodes"></a>Nodos

Un nodo representa una instancia específica de un elemento del mismo nivel en una red. La infraestructura de Peer Graphing API garantiza que cada nodo tenga una vista coherente de los datos de un gráfico. Un nodo tiene las siguientes características:

-   Puede conectarse a otro nodo y formar una red interrelacionado denominada grafo del mismo nivel.
-   Puede compartir datos con otros nodos de un gráfico en forma de [un registro](records.md).
-   Puede crear conexiones directas independientes de los gráficos del mismo nivel establecidos mediante la [API de agrupación del mismo nivel](about-the-grouping-api.md).
    > [!Note]  
    > Las conexiones directas permiten a los nodos enviar datos privados entre sí.

     

## <a name="event-notices"></a>Avisos de eventos

Peer Graphing API tiene una infraestructura de eventos que permite que una aplicación se registre y reciba un aviso de un evento del mismo nivel dentro de la infraestructura de Peer Graphing API. Cuando algo cambia dentro de un gráfico del mismo nivel, una aplicación envía un aviso de evento para identificar que se ha producido un cambio.

 

 



