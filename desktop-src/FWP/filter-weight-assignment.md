---
title: Asignación del peso del filtro
description: Cada filtro de la plataforma Windows filtrado de filtros (WFP) tiene un peso asociado, que se usa durante el arbitraje del filtro.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9042b15da0df5f81c71a32deb923369a54243854e86aeaed1ba30c7fc8484193
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746875"
---
# <a name="filter-weight-assignment"></a>Asignación del peso del filtro

Cada filtro de la plataforma Windows filtrado de filtros (WFP) tiene un peso asociado, que se usa durante el [arbitraje del filtro.](filter-arbitration.md)

El grosor del filtro utilizado por el motor de filtrado base (BFE) es del tipo [**FWP \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). Los llamadores tienen tres opciones al agregar filtros.

-   Establezca el peso en [**un fwp \_ UINT64.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) BFE usa el peso proporcionado tal y como está.
-   Establezca el peso en [**FWP \_ EMPTY.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) BFE genera automáticamente un peso en el intervalo \[ de 0, 2⁶ 3).
-   Establezca el peso en [**un FWP \_ UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) en el intervalo \[ 0, 15 \] . BFE usa el peso proporcionado como identificador de intervalo de peso.

    BFE genera automáticamente los 60 bits de orden bajo (exactamente como si el peso se hubiera establecido en [**FWP \_ EMPTY)**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)y, a continuación, usa el valor proporcionado para establecer los 4 bits de orden alto. Esto permite a los autores de llamadas dividir manualmente el espacio de peso en 16 intervalos, mientras siguen usando el peso automático dentro de un intervalo.

> [!Note]  
> Cuando se registran dos o más llamadas en la misma subcapa, pueden producirse problemas cuando se asigna el mismo peso a los filtros. Este problema se puede evitar haciendo que las llamadas creen su propia subcapa mediante [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Filtrar identificadores de peso**](filter-weight-identifiers.md)
</dt> </dl>

 

 




