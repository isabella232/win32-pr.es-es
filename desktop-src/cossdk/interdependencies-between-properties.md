---
description: Interdependencias entre propiedades
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Interdependencias entre propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000634"
---
# <a name="interdependencies-between-properties"></a><span data-ttu-id="82673-103">Interdependencias entre propiedades</span><span class="sxs-lookup"><span data-stu-id="82673-103">Interdependencies Between Properties</span></span>

<span data-ttu-id="82673-104">Al establecer las propiedades, el catálogo de COM+ impone cierta lógica de coherencia para asegurarse de que se configuran los elementos de forma razonable.</span><span class="sxs-lookup"><span data-stu-id="82673-104">When you set properties, the COM+ catalog enforces some coherency logic to ensure that you configure elements in a reasonable way.</span></span> <span data-ttu-id="82673-105">Esta lógica se puede implementar de dos maneras, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="82673-105">This logic can be implemented in two ways, as follows:</span></span>

-   <span data-ttu-id="82673-106">**Dependencias.**</span><span class="sxs-lookup"><span data-stu-id="82673-106">**Dependencies.**</span></span> <span data-ttu-id="82673-107">Es posible que no pueda realizar algunos cambios porque otra propiedad depende de un valor determinado para una propiedad que se intenta establecer.</span><span class="sxs-lookup"><span data-stu-id="82673-107">You might be blocked from making some changes because another property depends on a particular setting for a property you attempt to set.</span></span> <span data-ttu-id="82673-108">Por ejemplo, si un componente se establece con las transacciones de atributo necesarias y, a continuación, intenta cambiar la configuración de sincronización a ninguno, se genera un error al intentar llamar a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) porque las transacciones dependen de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="82673-108">For example, if a component is set with the attribute Transactions Required and if you then attempt to change the Synchronization setting to None, an error is generated when you attempt to call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) because transactions depend on synchronization.</span></span>
-   <span data-ttu-id="82673-109">**Efectos secundarios.**</span><span class="sxs-lookup"><span data-stu-id="82673-109">**Side effects.**</span></span> <span data-ttu-id="82673-110">Es posible que algunas propiedades se cambien automáticamente sin que las establezca explícitamente.</span><span class="sxs-lookup"><span data-stu-id="82673-110">Some properties might be changed for you without your explicitly setting them.</span></span> <span data-ttu-id="82673-111">Por ejemplo, si establece un componente con las transacciones de atributo necesarias, la sincronización se establecerá también en requerido.</span><span class="sxs-lookup"><span data-stu-id="82673-111">For example, if you set a component with the attribute Transactions Required, Synchronization will be set to Required as well.</span></span> <span data-ttu-id="82673-112">En realidad, es el lado de volteo de las dependencias: una propiedad tiene prioridad sobre otra, y su dependencia se expresa mediante el establecimiento de la propiedad secundaria y el bloqueo de los cambios en ella.</span><span class="sxs-lookup"><span data-stu-id="82673-112">This is really the flip side of dependencies—one property takes precedence over another, and its dependency is expressed through first setting the secondary property and then blocking changes to it.</span></span>

<span data-ttu-id="82673-113">En la lista de propiedades expuestas por los elementos de una colección, todas enumeradas en [colecciones de administración de com+](com--administration-collections.md), se indican las dependencias y los efectos secundarios para cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="82673-113">In the list of properties exposed by items in a collection, all listed in [COM+ Administration Collections](com--administration-collections.md), the dependencies and side effects are stated for each property.</span></span> <span data-ttu-id="82673-114">Al configurar aplicaciones y componentes COM+, debe tener en cuenta las restricciones que se imponen en las configuraciones.</span><span class="sxs-lookup"><span data-stu-id="82673-114">When you configure COM+ applications and components, you should be aware of what constraints are imposed on configurations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82673-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82673-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82673-116">Obtener y establecer propiedades</span><span class="sxs-lookup"><span data-stu-id="82673-116">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="82673-117">Consultar las propiedades disponibles</span><span class="sxs-lookup"><span data-stu-id="82673-117">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="82673-118">Guardar o descartar cambios</span><span class="sxs-lookup"><span data-stu-id="82673-118">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



