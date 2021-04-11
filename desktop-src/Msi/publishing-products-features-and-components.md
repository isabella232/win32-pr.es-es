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
# <a name="publishing-products-features-and-components"></a><span data-ttu-id="4987d-103">Publicar productos, características y componentes</span><span class="sxs-lookup"><span data-stu-id="4987d-103">Publishing Products, Features, and Components</span></span>

<span data-ttu-id="4987d-104">Para [publicar](components-and-features.md) un producto, un componente o una característica, use una de las acciones de publicación.</span><span class="sxs-lookup"><span data-stu-id="4987d-104">To [publish](components-and-features.md) a product, component, or feature, use one of the publishing actions.</span></span> <span data-ttu-id="4987d-105">La [acción PublishProduct](publishproduct-action.md) registra la información del producto con el sistema.</span><span class="sxs-lookup"><span data-stu-id="4987d-105">The [PublishProduct action](publishproduct-action.md) registers the product information with the system.</span></span> <span data-ttu-id="4987d-106">Después de ejecutar la acción PublishProduct, publique los componentes con la [acción PublishComponents](publishcomponents-action.md), que a su vez usa la [tabla PublishComponent](publishcomponent-table.md) para determinar los componentes que se establecen como anunciados.</span><span class="sxs-lookup"><span data-stu-id="4987d-106">After executing the PublishProduct action, publish the components with the [PublishComponents action](publishcomponents-action.md), which in turn uses the [PublishComponent table](publishcomponent-table.md) to determine the components that are set as advertised.</span></span> <span data-ttu-id="4987d-107">Para publicar en función de cada característica, invoque la [acción PublishFeatures](publishfeatures-action.md).</span><span class="sxs-lookup"><span data-stu-id="4987d-107">To publish on a per-feature basis, invoke the [PublishFeatures action](publishfeatures-action.md).</span></span> <span data-ttu-id="4987d-108">Esta acción utiliza la [tabla FeatureComponents](featurecomponents-table.md) como datos para resolver qué características se anuncian.</span><span class="sxs-lookup"><span data-stu-id="4987d-108">This action uses the [FeatureComponents table](featurecomponents-table.md) as data to resolve which features are advertised.</span></span>

<span data-ttu-id="4987d-109">También hay dos acciones correspondientes que anulan la publicación de una característica o un componente: la [acción UnpublishComponents](unpublishcomponents-action.md) y la [acción UnpublishFeatures](unpublishfeatures-action.md).</span><span class="sxs-lookup"><span data-stu-id="4987d-109">There are also two corresponding actions that unpublish a feature or a component: the [UnpublishComponents action](unpublishcomponents-action.md) and the [UnpublishFeatures action](unpublishfeatures-action.md).</span></span>

 

 



