---
title: Definir categorías de componentes
description: Definir categorías de componentes
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269454"
---
# <a name="defining-component-categories"></a><span data-ttu-id="fc7a4-103">Definir categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="fc7a4-103">Defining Component Categories</span></span>

<span data-ttu-id="fc7a4-104">El autor de una definición de categoría de componente crea un GUID único (CATId) que se publica junto con la definición.</span><span class="sxs-lookup"><span data-stu-id="fc7a4-104">The author of a component category definition creates a unique GUID (the CATID) that is published along with the definition.</span></span> <span data-ttu-id="fc7a4-105">Otras partes conocen la definición de este tipo y pueden hacer uso de las clases admitidas en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="fc7a4-105">Other parties know the definition of this type and can make use of its supported classes accordingly.</span></span> <span data-ttu-id="fc7a4-106">Al igual que la firma de método de una interfaz, la semántica de una categoría no debe modificarse después de instalarse.</span><span class="sxs-lookup"><span data-stu-id="fc7a4-106">Like the method signature of an interface, a category's semantics should not be modified after being installed.</span></span> <span data-ttu-id="fc7a4-107">Es mejor mantener la compatibilidad con versiones anteriores de la categoría mediante la introducción de un nuevo identificador de categoría con semántica revisada.</span><span class="sxs-lookup"><span data-stu-id="fc7a4-107">It is better to maintain backward compatibility of the category by introducing a new category identifier with revised semantics.</span></span>

<span data-ttu-id="fc7a4-108">Dado que los identificadores de interfaz (IID) y los identificadores de categoría de componente (CATId) existen en diferentes espacios de nombres, parece que si fuera posible usar el mismo GUID para un IID y un CATId.</span><span class="sxs-lookup"><span data-stu-id="fc7a4-108">Because interface identifiers (IID) and component category identifiers (CATID) exist in different namespaces, it seems as if it would be possible to use the same GUID for both an IID and a CATID.</span></span> <span data-ttu-id="fc7a4-109">Sin embargo, como los IID se suelen usar para el CLSID del servidor proxy/stub de la interfaz, existe la posibilidad de que se produzcan conflictos.</span><span class="sxs-lookup"><span data-stu-id="fc7a4-109">However, since IIDs are often used for the CLSID of the interface's proxy/stub server, there is the potential for conflict.</span></span> <span data-ttu-id="fc7a4-110">Por lo tanto, no use el mismo GUID para un IID y CATId.</span><span class="sxs-lookup"><span data-stu-id="fc7a4-110">Therefore, do not use the same GUID for an IID and CATID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc7a4-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc7a4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc7a4-112">Asociar iconos a una categoría</span><span class="sxs-lookup"><span data-stu-id="fc7a4-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="fc7a4-113">Categorización por funcionalidad de componentes</span><span class="sxs-lookup"><span data-stu-id="fc7a4-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="fc7a4-114">Clasificar por capacidades de contenedor</span><span class="sxs-lookup"><span data-stu-id="fc7a4-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="fc7a4-115">Clases y asociaciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="fc7a4-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="fc7a4-116">Administrador de categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="fc7a4-116">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




