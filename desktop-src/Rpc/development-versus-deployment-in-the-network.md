---
title: Desarrollo frente a implementación en la red
description: La mayoría de los desarrolladores escriben y prueban su software en una LAN confiable rápida.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ff9da31ecd80b9e0a699d9ec0eb450e885a423b9380b85e2015e9ef7c1af7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930625"
---
# <a name="development-vs-deployment-in-the-network"></a>Desarrollo frente a implementación en la red

La mayoría de los desarrolladores escriben y prueban su software en una LAN confiable rápida. Su cliente y servidor suelen estar en el mismo segmento de red. En tales circunstancias, la red rara vez no responde y la conectividad rara vez se pierde. Sin embargo, cuando se implementa en un entorno de cliente, el cliente y el servidor suelen estar en segmentos de red diferentes, posiblemente geográficamente remotos, y el servidor se carga en gran medida con otros clientes. En otras palabras: no se puede asumir la capacidad de respuesta de la red.

En este artículo se explica cómo construir arquitecturas sólidas de cliente y servidor frente a la incertidumbre introducida por una red intrínsecamente poco confiable y servidores potencialmente no disponibles.

 

 




