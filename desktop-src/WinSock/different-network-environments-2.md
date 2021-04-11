---
description: Varios entornos de red afectan al comportamiento en red de una aplicación.
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: Entornos de red diferentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dca7eacd48973a9106e6a1e3a4eb5959afcfef
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104279757"
---
# <a name="different-network-environments"></a>Entornos de red diferentes

Varios entornos de red afectan al comportamiento en red de una aplicación. Las propiedades que diferencian los entornos de red incluyen el ancho de banda bajo y alto, y el RTT bajo y alto. Los entornos de red afectan a las aplicaciones transaccionales y de streaming de maneras diferentes. Las aplicaciones transaccionales son más sensibles a RTT; las aplicaciones de streaming son más sensibles a los productos de retraso de ancho de banda.

![Diagrama que muestra cómo los distintos entornos de red afectan al comportamiento de red de una aplicación.](images/hperf-1.png)

Las redes de acceso telefónico y algunas redes inalámbricas tienen un RTT variable. Por lo general, las redes satélite tienen un ancho de banda asimétrico entre el nivel ascendente y el inferior. LAN inalámbrica y xDSL son buenos ejemplos de redes con productos de retraso de ancho de banda similares al de Fast Ethernet.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de Windows Sockets de alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensiones de rendimiento](performance-dimensions-2.md)
</dt> </dl>

 

 



