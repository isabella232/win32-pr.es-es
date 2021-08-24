---
title: Tunnel Modo
description: El Tunnel de directiva IPsec en modo de configuración se usa para aplicar la protección del modo de túnel IPsec para todo el tráfico que coincida entre dos puntos de conexión de túnel.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbac16de0dc01bc37e0e4f4b997d00d19339de021ffce66a0d3cf6957addbe90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639075"
---
# <a name="tunnel-mode"></a>Tunnel Modo

El Tunnel de directiva IPsec en modo de configuración se usa para aplicar la protección del modo de túnel IPsec para todo el tráfico que coincida entre dos puntos de conexión de túnel.

Este escenario de directiva se usa normalmente para proteger el tráfico entre varias subredes de sucursales, cuando se reenvía entre las puertas de enlace correspondientes en Internet. También se puede usar para proteger la comunicación de un extremo a otro entre dos máquinas host, también denominada túneles de punto a punto.

Para implementar una directiva de modo Tunnel mediante la plataforma de filtrado de Windows (WFP), llame a la función [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) que crea instancias de los filtros de modo de túnel adecuados en las capas adecuadas en nombre del autor de la llamada. El autor de la llamada debe especificar el modo principal, los contextos del proveedor del modo rápido y las condiciones de filtro que describen el tráfico que debe protegerse dentro del túnel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo: Uso del modo Tunnel datos](using-tunnel-mode.md)
</dt> <dt>

[**Filtrado de identificadores de capa**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




