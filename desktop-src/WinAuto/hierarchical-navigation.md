---
title: Navegación jerárquica
description: A menudo, los clientes deben moverse entre objetos en función de sus relaciones de elementos primarios y secundarios. Por ejemplo, es posible que un cliente ya tenga información sobre un control de la barra de herramientas, pero que no tenga información sobre los botones contenidos en él.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268754"
---
# <a name="hierarchical-navigation"></a><span data-ttu-id="df9b9-104">Navegación jerárquica</span><span class="sxs-lookup"><span data-stu-id="df9b9-104">Hierarchical Navigation</span></span>

<span data-ttu-id="df9b9-105">A menudo, los clientes deben moverse entre objetos en función de sus relaciones de elementos primarios y secundarios.</span><span class="sxs-lookup"><span data-stu-id="df9b9-105">Often clients must move between objects based on their parent-child relationships.</span></span> <span data-ttu-id="df9b9-106">Por ejemplo, es posible que un cliente ya tenga información sobre un control de la barra de herramientas, pero que no tenga información sobre los botones contenidos en él.</span><span class="sxs-lookup"><span data-stu-id="df9b9-106">For example, a client might already have information about a toolbar control, but not have information about the buttons contained within it.</span></span>

<span data-ttu-id="df9b9-107">La interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) expone las relaciones jerárquicas entre los objetos.</span><span class="sxs-lookup"><span data-stu-id="df9b9-107">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface exposes the hierarchical relationships between objects.</span></span> <span data-ttu-id="df9b9-108">Los clientes pueden desplazarse de un objeto primario a sus elementos secundarios o de un objeto secundario a su elemento primario llamando a [**IAccessible:: get \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) o [**IAccessible:: get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).</span><span class="sxs-lookup"><span data-stu-id="df9b9-108">Clients can navigate from a parent object to its children or from a child object to its parent by calling [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) or [**IAccessible::get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).</span></span>

 

 




