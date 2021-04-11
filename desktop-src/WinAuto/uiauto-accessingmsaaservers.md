---
title: Acceso a servidores de Microsoft Active Accessibility
description: Microsoft Active Accessibility al proxy de automatización de la interfaz de usuario es un componente de software que permite a los clientes de automatización de la interfaz de usuario de Microsoft interactuar con servidores de Microsoft Active Accessibility que implementan la interfaz IAccessible de forma nativa.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Automatización de la interfaz de usuario, obtener acceso a Active Accessibility
- Automatización de la interfaz de usuario, Active Accessibility
- Proxy de automatización de la interfaz de usuario
- Automatización de la interfaz de usuario, proxy de UI Automation
- Patrón de control LegacyIAccessible
- Automatización de la interfaz de usuario, patrón de control LegacyIAccessible
- Microsoft Active Accessibility
- Active Accessibility
- clientes, acceso a servidores de Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97319028203351cd9f45b39d133fa38727d6861e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075421"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a><span data-ttu-id="004e6-112">Acceso a servidores de Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="004e6-112">Accessing Microsoft Active Accessibility Servers</span></span>

<span data-ttu-id="004e6-113">Microsoft Active Accessibility al proxy de automatización de la interfaz de usuario es un componente de software que permite a los clientes de automatización de la interfaz de usuario de Microsoft interactuar con servidores de Microsoft Active Accessibility que implementan la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="004e6-113">The Microsoft Active Accessibility to UI Automation Proxy is a software component that enables Microsoft UI Automation clients to interact with Microsoft Active Accessibility servers that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface natively.</span></span> <span data-ttu-id="004e6-114">El proxy admite el patrón de control [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) y proporciona una instancia de la interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) para cada servidor de Microsoft Active Accessibility detectado.</span><span class="sxs-lookup"><span data-stu-id="004e6-114">The proxy supports the [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) control pattern, and supplies an instance of the [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface for each Microsoft Active Accessibility server detected.</span></span> <span data-ttu-id="004e6-115">Los clientes de automatización de la interfaz de usuario usan los métodos expuestos por **IUIAutomationLegacyIAccessiblePattern** para tener acceso a las propiedades y los objetos de Microsoft Active Accessibility compatibles con el servidor.</span><span class="sxs-lookup"><span data-stu-id="004e6-115">UI Automation clients use the methods exposed by **IUIAutomationLegacyIAccessiblePattern** to access the Microsoft Active Accessibility properties and objects supported by the server.</span></span>

<span data-ttu-id="004e6-116">Si un elemento de automatización de la interfaz de usuario tiene una implementación subyacente de Microsoft Active Accessibility, un cliente puede obtener un puntero de interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) para el elemento pasando el identificador de patrón de control [**UIA \_ LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) a uno de los siguientes métodos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) :</span><span class="sxs-lookup"><span data-stu-id="004e6-116">If a UI Automation element has an underlying Microsoft Active Accessibility implementation, a client can obtain an [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface pointer for the element by passing the [**UIA\_LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) control pattern ID to one of the following [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) methods:</span></span>

-   [<span data-ttu-id="004e6-117">**GetCachedPattern**</span><span class="sxs-lookup"><span data-stu-id="004e6-117">**GetCachedPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [<span data-ttu-id="004e6-118">**GetCachedPatternAs**</span><span class="sxs-lookup"><span data-stu-id="004e6-118">**GetCachedPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [<span data-ttu-id="004e6-119">**GetCurrentPattern**</span><span class="sxs-lookup"><span data-stu-id="004e6-119">**GetCurrentPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [<span data-ttu-id="004e6-120">**GetCurrentPatternAs**</span><span class="sxs-lookup"><span data-stu-id="004e6-120">**GetCurrentPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

<span data-ttu-id="004e6-121">La interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) no está disponible para los controles basados en la automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="004e6-121">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface is not available for controls based on UI Automation.</span></span>

<span data-ttu-id="004e6-122">La interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) permite a los clientes de automatización de la interfaz de usuario tener acceso a la implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) subyacente de un elemento de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="004e6-122">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface enables UI Automation clients to access the underlying [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation of an Microsoft Active Accessibility element.</span></span> <span data-ttu-id="004e6-123">Sin embargo, la interfaz no admite métodos que son obsoletos o redundantes con las características de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="004e6-123">However, the interface does not support methods that are obsolete or redundant with UI Automation features.</span></span> <span data-ttu-id="004e6-124">Por ejemplo, **IUIAutomationLegacyIAccessiblePattern** no tiene un método que sea equivalente a [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) porque la ubicación actual de un elemento de la interfaz de usuario está disponible desde la propiedad BoundingRectangle de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="004e6-124">For example, **IUIAutomationLegacyIAccessiblePattern** does not have a method that is equivalent to [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because the current location of a UI element is available from the UI Automation BoundingRectangle property.</span></span>

<span data-ttu-id="004e6-125">El método [**IUIAutomationLegacyIAccessiblePattern:: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) permite a un cliente recuperar un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de un elemento de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="004e6-125">The [**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) method enables a client to retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer from an UI Automation element.</span></span> <span data-ttu-id="004e6-126">También es posible usar los métodos [**IUIAutomation:: ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) y [**IUIAutomation:: ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) .</span><span class="sxs-lookup"><span data-stu-id="004e6-126">The reverse is also possible by using the [**IUIAutomation::ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) and [**IUIAutomation::ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) methods.</span></span>

<span data-ttu-id="004e6-127">[**IUIAutomationLegacyIAccessiblePattern:: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) devuelve **null** si un objeto proxy proporciona la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento desde OLEACC.dll o desde la automatización de la interfaz de usuario a Microsoft Active Accessibility Bridge.</span><span class="sxs-lookup"><span data-stu-id="004e6-127">[**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) returns **NULL** if the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element is provided by a proxy object from OLEACC.dll or from the UI Automation to Microsoft Active Accessibility Bridge.</span></span>

## <a name="related-topics"></a><span data-ttu-id="004e6-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="004e6-128">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="004e6-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="004e6-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="004e6-130">Automatización y Active Accessibility de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="004e6-130">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
</dt> <dt>

[<span data-ttu-id="004e6-131">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="004e6-131">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




