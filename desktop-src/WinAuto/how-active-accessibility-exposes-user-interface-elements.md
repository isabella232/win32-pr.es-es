---
title: Cómo expone Active Accessibility elementos de la interfaz de usuario
description: Microsoft Active Accessibility crea un objeto proxy para cada elemento de la interfaz de usuario que expone.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b450ebe79aa467100fe9b6fb3bc4cdfb5540b60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268762"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a><span data-ttu-id="ce420-103">Cómo expone Active Accessibility elementos de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="ce420-103">How Active Accessibility Exposes User Interface Elements</span></span>

<span data-ttu-id="ce420-104">Microsoft Active Accessibility crea un objeto *proxy* para cada elemento de la interfaz de usuario que expone.</span><span class="sxs-lookup"><span data-stu-id="ce420-104">Microsoft Active Accessibility creates a *proxy* object for each user interface element that it exposes.</span></span> <span data-ttu-id="ce420-105">Un objeto proxy actúa como intermediario entre la utilidad de cliente y el elemento de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ce420-105">A proxy object acts as an intermediary between the client utility and the UI element.</span></span> <span data-ttu-id="ce420-106">El propósito del objeto proxy es supervisar el intervalo de vida del elemento de la interfaz de usuario e implementar las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en nombre del elemento de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ce420-106">The purpose of the proxy object is to monitor the life span of the UI element and to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods on behalf of the UI element.</span></span> <span data-ttu-id="ce420-107">Los desarrolladores de servidor que crean controles personalizados u otros elementos de interfaz de usuario personalizados también deben crear objetos proxy.</span><span class="sxs-lookup"><span data-stu-id="ce420-107">Server developers who create custom controls or other custom UI elements should also create proxy objects.</span></span> <span data-ttu-id="ce420-108">Para obtener más información, consulte [crear objetos proxy](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ce420-108">For more information, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

<span data-ttu-id="ce420-109">Cuando Microsoft Active Accessibility crea un objeto para exponer un control predefinido o común, realmente crea al menos dos objetos: uno para el control y otro para la ventana que rodea el control.</span><span class="sxs-lookup"><span data-stu-id="ce420-109">When Microsoft Active Accessibility creates an object to expose a predefined or common control, it actually creates at least two objects: one for the control and one for the window that surrounds the control.</span></span> <span data-ttu-id="ce420-110">En la mayoría de los casos, estas ventanas principales tienen la [propiedad role](role-property.md) de la [**\_ \_ ventana del sistema de roles**](object-roles.md) y tienen la misma [propiedad nombre](name-property.md) y el nombre de clase de ventana que el control.</span><span class="sxs-lookup"><span data-stu-id="ce420-110">In most cases, these parent windows have the [Role property](role-property.md) of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and have the same [Name property](name-property.md) and window class name as the control.</span></span> <span data-ttu-id="ce420-111">La información sobre el control que los clientes transmiten a los usuarios finales está contenida en el objeto que Microsoft Active Accessibility crea para exponer el control, no en el objeto primario que expone la ventana que rodea el control.</span><span class="sxs-lookup"><span data-stu-id="ce420-111">The information about the control that clients convey to end users is contained in the object that Microsoft Active Accessibility creates to expose the control, not the parent object that exposes the window that surrounds the control.</span></span>

<span data-ttu-id="ce420-112">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="ce420-112">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="ce420-113">Detección de objetos innecesarios</span><span class="sxs-lookup"><span data-stu-id="ce420-113">Screening Out Unnecessary Objects</span></span>](screening-out-unnecessary-objects.md)
-   [<span data-ttu-id="ce420-114">Proporcionar la propiedad Name</span><span class="sxs-lookup"><span data-stu-id="ce420-114">Providing the Name Property</span></span>](providing-the-name-property.md)
-   [<span data-ttu-id="ce420-115">Asegurarse de que los elementos de la interfaz de usuario se denominan correctamente</span><span class="sxs-lookup"><span data-stu-id="ce420-115">Ensuring that UI Elements are Correctly Named</span></span>](ensure-that-ui-elements-are-named-correctly.md)
-   [<span data-ttu-id="ce420-116">Elementos de la interfaz de usuario no admitidos</span><span class="sxs-lookup"><span data-stu-id="ce420-116">Unsupported User Interface Elements</span></span>](unsupported-user-interface-elements.md)

 

 




