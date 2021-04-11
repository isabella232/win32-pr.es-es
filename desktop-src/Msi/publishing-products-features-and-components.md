---
description: Para publicar un producto, un componente o una característica, use una de las acciones de publicación.
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: Publicar productos, características y componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdd8c8445491646399c7d118a69ae497d27faff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276711"
---
# <a name="publishing-products-features-and-components"></a>Publicar productos, características y componentes

Para [publicar](components-and-features.md) un producto, un componente o una característica, use una de las acciones de publicación. La [acción PublishProduct](publishproduct-action.md) registra la información del producto con el sistema. Después de ejecutar la acción PublishProduct, publique los componentes con la [acción PublishComponents](publishcomponents-action.md), que a su vez usa la [tabla PublishComponent](publishcomponent-table.md) para determinar los componentes que se establecen como anunciados. Para publicar en función de cada característica, invoque la [acción PublishFeatures](publishfeatures-action.md). Esta acción utiliza la [tabla FeatureComponents](featurecomponents-table.md) como datos para resolver qué características se anuncian.

También hay dos acciones correspondientes que anulan la publicación de una característica o un componente: la [acción UnpublishComponents](unpublishcomponents-action.md) y la [acción UnpublishFeatures](unpublishfeatures-action.md).

 

 



