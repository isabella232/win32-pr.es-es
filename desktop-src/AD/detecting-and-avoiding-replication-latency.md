---
title: Detección y prevención de la latencia de replicación
description: La latencia de replicación es un hecho de vida en un sistema distribuido de acoplamiento flexible.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773255"
---
# <a name="detecting-and-avoiding-replication-latency"></a>Detección y prevención de la latencia de replicación

La latencia de replicación es un hecho de vida en un sistema distribuido de acoplamiento flexible. Las aplicaciones deben adaptarse a este. La mejor manera de adaptarse a la latencia de replicación es diseñar aplicaciones para minimizar los efectos. La aplicación ideal habilitada para el directorio:

-   No distingue el sesgo de la versión.
-   No depende de las relaciones entre varios objetos.
-   No tiene ningún requisito de coherencia entre objetos.

No es necesario que las aplicaciones y los servicios que se ajustan a este perfil afecten a la latencia de replicación. Otras aplicaciones deben diseñarse teniendo en cuenta la latencia de replicación. La clave para el éxito en el diseño de una aplicación de este tipo es el conocimiento del proceso de replicación. Pasos que se llevan a cabo en el tiempo de diseño para reducir las dependencias entre objetos y minimizar las ventanas de actualización parciales pagará grandes dividendos en tiempo de ejecución. Los enfoques para tratar con la latencia de replicación se dividen en dos clases: evitar estrategias que reducen el impacto de la latencia y las estrategias de detección que permiten a una aplicación detectar Estados inducidos por latencia.

 

 




