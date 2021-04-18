---
title: Modo de túnel
description: El escenario de directiva IPsec de modo de túnel se usa para aplicar la protección del modo de túnel IPsec para todo el tráfico coincidente entre dos extremos de túnel.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75fdecb7f959a2f95aae2649a6e3f8f94def9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357429"
---
# <a name="tunnel-mode"></a>Modo de túnel

El escenario de directiva IPsec de modo de túnel se usa para aplicar la protección del modo de túnel IPsec para todo el tráfico coincidente entre dos extremos de túnel.

Este escenario de Directiva se usa normalmente para proteger el tráfico entre varias subredes de sucursal, cuando se reenvía entre las puertas de enlace correspondientes en Internet. También se puede usar para proteger la comunicación de un extremo a otro entre dos equipos host, también denominados túneles punto a punto.

Para implementar la Directiva de modo de túnel mediante la plataforma de filtrado de Windows (WFP), llame a la función [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) que crea instancias de los filtros de modo de túnel adecuados en las capas adecuadas en nombre del autor de la llamada. El autor de la llamada debe especificar el modo principal, los contextos de proveedor de modo rápido y las condiciones de filtro que describen el tráfico que debe protegerse dentro del túnel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo: uso del modo de túnel](using-tunnel-mode.md)
</dt> <dt>

[**Filtrado de identificadores de capas**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




