---
title: Objetos accesibles
description: Con Microsoft Active Accessibility, los elementos de la interfaz de usuario se exponen a los clientes como objetos del modelo de objetos componentes (COM).
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba496e011d42fac9a3c4b047a7d8c3b9e0ecf84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419118"
---
# <a name="accessible-objects"></a><span data-ttu-id="f7055-103">Objetos accesibles</span><span class="sxs-lookup"><span data-stu-id="f7055-103">Accessible Objects</span></span>

<span data-ttu-id="f7055-104">Con Microsoft Active Accessibility, los elementos de la interfaz de usuario se exponen a los clientes como objetos del modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="f7055-104">With Microsoft Active Accessibility, UI elements are exposed to clients as Component Object Model (COM) objects.</span></span> <span data-ttu-id="f7055-105">Estos *objetos accesibles* mantienen fragmentos de información, denominados *propiedades*, que describen el nombre del objeto, la ubicación de la pantalla y otra información necesaria para las ayudas de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="f7055-105">These *accessible objects* maintain pieces of information, called *properties*, which describe the object's name, screen location, and other information needed by accessibility aids.</span></span> <span data-ttu-id="f7055-106">Los objetos accesibles también proporcionan *métodos* a los que llaman los clientes para hacer que el objeto realice alguna acción.</span><span class="sxs-lookup"><span data-stu-id="f7055-106">Accessible objects also provide *methods* that clients call to cause the object to perform some action.</span></span> <span data-ttu-id="f7055-107">Los objetos accesibles que tienen elementos simples asociados a ellos también se denominan elementos *primarios* o *contenedores*.</span><span class="sxs-lookup"><span data-stu-id="f7055-107">Accessible objects that have simple elements associated with them are also called *parents*, or *containers*.</span></span>

<span data-ttu-id="f7055-108">Los objetos accesibles se implementan mediante la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) basada en com de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="f7055-108">Accessible objects are implemented using Microsoft Active Accessibility's COM-based [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="f7055-109">Los métodos y propiedades de **IAccessible** permiten a las aplicaciones cliente obtener información sobre los elementos de interfaz de usuario que necesitan los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f7055-109">The **IAccessible** methods and properties enable client applications to get information about UI elements needed by users.</span></span> <span data-ttu-id="f7055-110">Por ejemplo, [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) devuelve un puntero de interfaz a un elemento primario de un objeto accesible, y [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) proporciona un medio para que los clientes obtengan información sobre otros objetos dentro de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="f7055-110">For example, [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) returns an interface pointer to an accessible object's parent, and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) provides a means for clients to get information about other objects within a container.</span></span>

<span data-ttu-id="f7055-111">Para obtener más información sobre cómo se relacionan los objetos accesibles y los elementos simples, vea [elementos simples](simple-elements.md).</span><span class="sxs-lookup"><span data-stu-id="f7055-111">For more information about how accessible objects and simple elements are related, see [Simple Elements](simple-elements.md).</span></span>

 

 




