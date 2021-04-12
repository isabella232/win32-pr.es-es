---
title: Propiedad Value
description: La propiedad Value proporciona una representación textual de la información visual contenida en un objeto. No todos los objetos admiten la propiedad Value.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6cd3ad86b9ce3a4fcc917fc4f49792adf432bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357159"
---
# <a name="value-property"></a><span data-ttu-id="e921a-104">Propiedad Value</span><span class="sxs-lookup"><span data-stu-id="e921a-104">Value Property</span></span>

<span data-ttu-id="e921a-105">La propiedad **Value** proporciona una representación textual de la información visual contenida en un objeto.</span><span class="sxs-lookup"><span data-stu-id="e921a-105">The **Value** property provides a textual representation of the visual information contained in an object.</span></span> <span data-ttu-id="e921a-106">No todos los objetos admiten la propiedad **Value** .</span><span class="sxs-lookup"><span data-stu-id="e921a-106">Not all objects support the **Value** property.</span></span>

<span data-ttu-id="e921a-107">La propiedad **Value** se recupera llamando a [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span><span class="sxs-lookup"><span data-stu-id="e921a-107">The **Value** property is retrieved by calling [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="e921a-108">La propiedad **Value** indica al cliente la información visual contenida en un objeto.</span><span class="sxs-lookup"><span data-stu-id="e921a-108">The **Value** property tells the client about the visual information contained in an object.</span></span> <span data-ttu-id="e921a-109">Por ejemplo, el valor de un control de edición es el texto que contiene, mientras que un elemento de menú no tiene ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e921a-109">For example, an edit control's value is the text it contains, whereas a menu item has no value.</span></span>

## <a name="providing-hierarchical-information"></a><span data-ttu-id="e921a-110">Proporcionar información jerárquica</span><span class="sxs-lookup"><span data-stu-id="e921a-110">Providing Hierarchical Information</span></span>

<span data-ttu-id="e921a-111">La propiedad **Value** proporciona información jerárquica en casos como un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="e921a-111">The **Value** property provides hierarchical information in cases such as a tree view control.</span></span> <span data-ttu-id="e921a-112">Aunque el objeto primario en el control de vista de árbol no proporciona información en la propiedad **Value** , cada elemento del control tiene un valor basado en cero que representa su nivel dentro de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="e921a-112">Although the parent object in the tree view control does not provide information in the **Value** property, each item within the control has a zero-based value that represents its level within the hierarchy.</span></span> <span data-ttu-id="e921a-113">Los elementos de nivel superior tienen un valor de cero, los elementos de segundo nivel tienen un valor de uno, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="e921a-113">Top-level items have a value of zero, second-level items have a value of one, and so on.</span></span>

 

 




