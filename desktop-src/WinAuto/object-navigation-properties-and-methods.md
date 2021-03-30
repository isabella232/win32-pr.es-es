---
title: Métodos y propiedades de navegación de objetos
description: Los clientes navegan de un objeto a otro usando métodos como IAccessible accNavigate y IAccessible accHitTest.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994125"
---
# <a name="object-navigation-properties-and-methods"></a><span data-ttu-id="ee049-103">Métodos y propiedades de navegación de objetos</span><span class="sxs-lookup"><span data-stu-id="ee049-103">Object Navigation Properties and Methods</span></span>

<span data-ttu-id="ee049-104">Los clientes *navegan* de un objeto a otro usando métodos como [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) y [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span><span class="sxs-lookup"><span data-stu-id="ee049-104">Clients *navigate* from one object to another using methods such as [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span></span> <span data-ttu-id="ee049-105">Estos métodos permiten a los clientes recuperar un identificador secundario o la dirección de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de otro objeto.</span><span class="sxs-lookup"><span data-stu-id="ee049-105">These methods allow clients to retrieve either a child ID or the address of another object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="ee049-106">La navegación permite a los clientes explorar cómo se relacionan entre sí los objetos.</span><span class="sxs-lookup"><span data-stu-id="ee049-106">Navigation allows clients to explore how objects are related to each other.</span></span> <span data-ttu-id="ee049-107">Tenga en cuenta que al navegar a otro objeto no se cambia la selección o el foco.</span><span class="sxs-lookup"><span data-stu-id="ee049-107">Note that navigating to another object does not change the selection or focus.</span></span>

<span data-ttu-id="ee049-108">La interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proporciona propiedades y métodos que admiten los siguientes tipos de navegación:</span><span class="sxs-lookup"><span data-stu-id="ee049-108">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface provides properties and methods that support the following kinds of navigation:</span></span>

-   [<span data-ttu-id="ee049-109">Navegación jerárquica</span><span class="sxs-lookup"><span data-stu-id="ee049-109">Hierarchical Navigation</span></span>](hierarchical-navigation.md)
-   [<span data-ttu-id="ee049-110">Navegación espacial y lógica</span><span class="sxs-lookup"><span data-stu-id="ee049-110">Spatial and Logical Navigation</span></span>](spatial-and-logical-navigation.md)
-   [<span data-ttu-id="ee049-111">Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla</span><span class="sxs-lookup"><span data-stu-id="ee049-111">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)

 

 




