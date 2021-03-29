---
title: Asignación del peso del filtro
description: Cada filtro de la plataforma de filtrado de Windows (WFP) tiene un peso asociado, que se utiliza durante el arbitraje del filtro.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/26/2020
ms.locfileid: "104420463"
---
# <a name="filter-weight-assignment"></a>Asignación del peso del filtro

Cada filtro de la plataforma de filtrado de Windows (WFP) tiene un peso asociado, que se utiliza durante el [arbitraje del filtro](filter-arbitration.md).

El peso de filtro usado por el motor de filtrado de base (BFE) es de tipo [**FWP \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). Los llamadores tienen tres opciones al agregar filtros.

-   Establezca el peso en un valor de [**FWP \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). BFE usa el peso proporcionado tal cual.
-   Establezca el peso en el valor de [**FWP \_ vacío**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). BFE genera automáticamente un peso en el intervalo comprendido entre \[ 0 y 2 ⁶ ⁰).
-   Establezca el peso en un valor de [**FWP \_ UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) en el intervalo de \[ 0 a 15 \] . BFE usa el peso proporcionado como identificador de intervalo de peso.

    BFE genera automáticamente los bits 60 de orden inferior (exactamente como si el peso se hubiera establecido en [**FWP \_ vacío**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)) y, a continuación, usa el valor proporcionado para establecer los 4 bits de orden superior. Esto permite a los autores de llamadas dividir manualmente el espacio de peso en 16 intervalos, a la vez que se sigue usando la ponderación automática dentro de un intervalo.

> [!Note]  
> Cuando dos o más llamadas se registran en la misma subcapa, pueden producirse problemas cuando se asigna el mismo peso a los filtros. Este problema se puede evitar al hacer que las llamadas creen su propia subcapa mediante [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Identificadores de peso de filtro**](filter-weight-identifiers.md)
</dt> </dl>

 

 




