---
description: Para publicar un producto, componente o característica, use una de las acciones de publicación.
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: Publicar productos, características y componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dd62e080cf58188405e20d1fd69507f849dd37ceddd01eaf1f4bbe7c59ea76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041995"
---
# <a name="publishing-products-features-and-components"></a>Publicar productos, características y componentes

Para [publicar](components-and-features.md) un producto, componente o característica, use una de las acciones de publicación. La [acción PublishProduct](publishproduct-action.md) registra la información del producto con el sistema. Después de ejecutar la acción PublishProduct, publique los componentes con la acción [PublishComponents](publishcomponents-action.md), que a su vez usa la tabla [PublishComponent](publishcomponent-table.md) para determinar los componentes que se establecen como anunciados. Para publicar por característica, invoque la [acción PublishFeatures](publishfeatures-action.md). Esta acción usa la [tabla FeatureComponents como](featurecomponents-table.md) datos para resolver qué características se anuncian.

También hay dos acciones correspondientes que despublican una característica o un componente: la acción [UnpublishComponents](unpublishcomponents-action.md) y la [acción UnpublishFeatures](unpublishfeatures-action.md).

 

 



