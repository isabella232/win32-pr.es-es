---
description: Varios entornos de red afectan al comportamiento en red de una aplicación.
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: Diferentes entornos de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13acdd27930a9b60af3004440b2cb4cf3a049cf2cce5f72f387cb51699e23782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858444"
---
# <a name="different-network-environments"></a>Diferentes entornos de red

Varios entornos de red afectan al comportamiento en red de una aplicación. Las propiedades que diferencian los entornos de red incluyen un ancho de banda bajo frente a alto, y un RTT bajo frente a alto. Los entornos de red afectan a las aplicaciones transaccionales y de streaming de maneras diferentes. Las aplicaciones transaccionales son más sensibles a RTT; las aplicaciones de streaming son más sensibles a los productos con retraso de ancho de banda.

![Diagrama que muestra cómo afectan los distintos entornos de red al comportamiento en red de una aplicación.](images/hperf-1.png)

Las redes de acceso telefónico y algunas redes inalámbricas tienen una rtt variable. Las redes satélite suelen tener un ancho de banda asimétrico entre la cadena ascendente y la bajada. La LAN inalámbrica y xDSL son buenos ejemplos de redes con productos de retraso de ancho de banda similares a los de Fast Ethernet.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de sockets Windows alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensiones de rendimiento](performance-dimensions-2.md)
</dt> </dl>

 

 



