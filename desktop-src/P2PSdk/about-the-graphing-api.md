---
description: La API de gráficos del mismo nivel permite a las aplicaciones pasar datos entre pares de manera eficaz y confiable. Los conceptos básicos de la tecnología de gráficos del mismo nivel son los nodos de un grafo del mismo nivel y los avisos de eventos.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Acerca de la API de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b08e320f1c8d176d0bd34cc7a9a9422c6cfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667463"
---
# <a name="about-the-graphing-api"></a>Acerca de la API de gráficos

La API de gráficos del mismo nivel permite a las aplicaciones pasar datos entre pares de manera eficaz y confiable. Los conceptos básicos de la tecnología de gráficos del mismo nivel son los **nodos** de un grafo del mismo nivel y los avisos de eventos.

## <a name="nodes"></a>Nodos

Un nodo representa una instancia específica de un elemento del mismo nivel en una red. La infraestructura de la API de gráficos del mismo nivel garantiza que cada nodo tiene una vista coherente de los datos de un gráfico. Un nodo tiene las siguientes características:

-   Puede conectarse a un nodo diferente y formar una red interrelacionada denominada grafo del mismo nivel.
-   Puede compartir datos con otros nodos de un gráfico en forma de [registro](records.md).
-   Puede crear conexiones directas independientes de los gráficos del mismo nivel establecidos mediante la [API de agrupación](about-the-grouping-api.md)del mismo nivel.
    > [!Note]  
    > Las conexiones directas permiten a los nodos enviar datos privados entre sí.

     

## <a name="event-notices"></a>Avisos de eventos

La API de gráficos del mismo nivel tiene una infraestructura de eventos que permite a una aplicación registrar y recibir un aviso de un evento del mismo nivel dentro de la infraestructura de la API de gráficos del mismo nivel. Cuando algo cambia dentro de un gráfico del mismo nivel, una aplicación envía un aviso de eventos para identificar que se ha producido un cambio.

 

 



