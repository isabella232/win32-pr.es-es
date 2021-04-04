---
title: Desarrollo frente a implementación en la red
description: La mayoría de los desarrolladores escriben y prueban el software en una LAN de confianza rápida.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075598"
---
# <a name="development-vs-deployment-in-the-network"></a>Desarrollo frente a implementación en la red

La mayoría de los desarrolladores escriben y prueban el software en una LAN de confianza rápida. El cliente y el servidor suelen estar en el mismo segmento de red. En tales circunstancias, la red rara vez no responde y la conectividad rara vez se pierde. Sin embargo, cuando se implementa en un entorno de cliente, el cliente y el servidor suelen estar en distintos segmentos de red, posiblemente de forma geográfica remota, y el servidor está muy cargado con otros clientes. En otras palabras: no se puede asumir la capacidad de respuesta de red.

En este artículo se explica cómo construir sólidas arquitecturas de cliente/servidor en caso de incertidumbre introducida por una red intrínsecamente confiable y servidores potencialmente no disponibles.

 

 




