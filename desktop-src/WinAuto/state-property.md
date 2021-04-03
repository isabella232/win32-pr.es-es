---
title: Propiedad State
description: La propiedad State describe el estado de un objeto en un momento dado. Todos los objetos admiten la propiedad State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903832"
---
# <a name="state-property"></a><span data-ttu-id="35907-104">Propiedad State</span><span class="sxs-lookup"><span data-stu-id="35907-104">State Property</span></span>

<span data-ttu-id="35907-105">La propiedad **State** describe el estado de un objeto en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="35907-105">The **State** property describes an object's status at a moment in time.</span></span> <span data-ttu-id="35907-106">Todos los objetos admiten la propiedad **State** .</span><span class="sxs-lookup"><span data-stu-id="35907-106">All objects support the **State** property.</span></span>

<span data-ttu-id="35907-107">La propiedad **State** se recupera llamando a [**IAccessible:: get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).</span><span class="sxs-lookup"><span data-stu-id="35907-107">The **State** property is retrieved by calling [**IAccessible::get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).</span></span>

<span data-ttu-id="35907-108">Microsoft Active Accessibility proporciona [constantes de estado de objeto](object-state-constants.md), definidas en oleacc. h, que se combinan para identificar el estado de un objeto.</span><span class="sxs-lookup"><span data-stu-id="35907-108">Microsoft Active Accessibility provides [object state constants](object-state-constants.md), defined in oleacc.h, that are combined to identify an object's state.</span></span> <span data-ttu-id="35907-109">Se recomienda que los desarrolladores de servidor utilicen estos valores de estado predefinidos.</span><span class="sxs-lookup"><span data-stu-id="35907-109">It is recommended that server developers use these predefined state values.</span></span> <span data-ttu-id="35907-110">Si se devuelven valores de estado predefinidos, los clientes utilizan [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar una cadena localizada que describe el estado.</span><span class="sxs-lookup"><span data-stu-id="35907-110">If predefined state values are returned, clients use [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) to retrieve a localized string that describes the state.</span></span>

<span data-ttu-id="35907-111">Los gráficos que se animan ocasionalmente deberían tener la propiedad **State** establecida en [**estado \_ \_ animado del sistema**](object-state-constants.md) y la propiedad [**rol**](role-property.md) establecida en [**gráfico de \_ sistema \_ de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="35907-111">Graphics that are occasionally animated should have the **State** property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md) and the [**Role**](role-property.md) property set to [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

 

 




