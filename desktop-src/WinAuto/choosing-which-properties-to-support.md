---
title: Elección de las propiedades que se van a admitir
description: Las propiedades IAccessible proporcionan una manera para que los desarrolladores de servidores describan una amplia variedad de elementos de la interfaz de usuario.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357333"
---
# <a name="choosing-which-properties-to-support"></a><span data-ttu-id="dac6c-103">Elección de las propiedades que se van a admitir</span><span class="sxs-lookup"><span data-stu-id="dac6c-103">Choosing Which Properties to Support</span></span>

<span data-ttu-id="dac6c-104">Las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proporcionan una manera para que los desarrolladores de servidores describan una amplia variedad de elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dac6c-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties provide a way for server developers to describe a wide variety of user interface elements.</span></span> <span data-ttu-id="dac6c-105">Pero no todas las propiedades se aplican a cada tipo de elemento de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dac6c-105">But not all of the properties are applicable for every kind of user interface element.</span></span> <span data-ttu-id="dac6c-106">Además, algunas propiedades proporcionan información descriptiva que es útil, pero no esencial.</span><span class="sxs-lookup"><span data-stu-id="dac6c-106">Additionally, some properties provide descriptive information that is useful but not essential.</span></span>

<span data-ttu-id="dac6c-107">Los servidores deben admitir los siguientes métodos y propiedades para todos los objetos:</span><span class="sxs-lookup"><span data-stu-id="dac6c-107">Servers must support the following properties and methods for every object:</span></span>

-   [<span data-ttu-id="dac6c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="dac6c-108">**Name**</span></span>](name-property.md)
-   [<span data-ttu-id="dac6c-109">**Role**</span><span class="sxs-lookup"><span data-stu-id="dac6c-109">**Role**</span></span>](role-property.md)
-   [<span data-ttu-id="dac6c-110">**State**</span><span class="sxs-lookup"><span data-stu-id="dac6c-110">**State**</span></span>](state-property.md)
-   <span data-ttu-id="dac6c-111">[**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) y [ **IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span><span class="sxs-lookup"><span data-stu-id="dac6c-111">[**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span></span>
-   <span data-ttu-id="dac6c-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) y [ **IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span><span class="sxs-lookup"><span data-stu-id="dac6c-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span></span>

<span data-ttu-id="dac6c-113">Se deben admitir las siguientes propiedades y métodos si son aplicables al objeto:</span><span class="sxs-lookup"><span data-stu-id="dac6c-113">The following properties and method must be supported if they are applicable to the object:</span></span>

-   [<span data-ttu-id="dac6c-114">**KeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="dac6c-114">**KeyboardShortcut**</span></span>](keyboardshortcut-property.md)
-   [<span data-ttu-id="dac6c-115">**Value**</span><span class="sxs-lookup"><span data-stu-id="dac6c-115">**Value**</span></span>](value-property.md)

<span data-ttu-id="dac6c-116">Se deben admitir las siguientes propiedades y métodos si el objeto tiene elementos secundarios:</span><span class="sxs-lookup"><span data-stu-id="dac6c-116">The following properties and method must be supported if the object has children:</span></span>

-   <span data-ttu-id="dac6c-117">[**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) y [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span><span class="sxs-lookup"><span data-stu-id="dac6c-117">[**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) and [**ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span></span>
-   <span data-ttu-id="dac6c-118">[**Focus, Selection**](selection-and-focus-properties-and-methods.md)y [ **IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span><span class="sxs-lookup"><span data-stu-id="dac6c-118">[**Focus, Selection**](selection-and-focus-properties-and-methods.md), and [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span></span>

<span data-ttu-id="dac6c-119">Las siguientes propiedades son opcionales, pero proporcionan información descriptiva útil sobre el objeto.</span><span class="sxs-lookup"><span data-stu-id="dac6c-119">The following properties are optional, but provide useful descriptive information about the object.</span></span> <span data-ttu-id="dac6c-120">La propiedad [**Description**](description-property.md) se implementa para describir mapas de bits y otras imágenes.</span><span class="sxs-lookup"><span data-stu-id="dac6c-120">The [**Description**](description-property.md) property is implemented to describe bitmaps and other images.</span></span>

-   [<span data-ttu-id="dac6c-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dac6c-121">**Description**</span></span>](description-property.md)
-   <span data-ttu-id="dac6c-122">[**DEFAULTACTION**](defaultaction-property.md) y [ **IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span><span class="sxs-lookup"><span data-stu-id="dac6c-122">[**DefaultAction**](defaultaction-property.md) and [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span></span>
-   [<span data-ttu-id="dac6c-123">**Ayuda**</span><span class="sxs-lookup"><span data-stu-id="dac6c-123">**Help**</span></span>](help-property.md)
-   [<span data-ttu-id="dac6c-124">**HelpTopic**</span><span class="sxs-lookup"><span data-stu-id="dac6c-124">**HelpTopic**</span></span>](helptopic-property.md)

 

 




