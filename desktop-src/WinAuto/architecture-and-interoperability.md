---
title: Arquitectura e interoperabilidad
description: En este tema se describe brevemente la arquitectura de Microsoft Active Accessibility y la automatización de la interfaz de usuario de Microsoft, así como los componentes que permiten la interoperabilidad entre aplicaciones basadas en las dos tecnologías diferentes.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "104149045"
---
# <a name="architecture-and-interoperability"></a><span data-ttu-id="9824f-103">Arquitectura e interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="9824f-103">Architecture and Interoperability</span></span>

<span data-ttu-id="9824f-104">En este tema se describe brevemente la arquitectura de Microsoft Active Accessibility y la automatización de la interfaz de usuario de Microsoft, así como los componentes que permiten la interoperabilidad entre aplicaciones basadas en las dos tecnologías diferentes.</span><span class="sxs-lookup"><span data-stu-id="9824f-104">This topic briefly describes the architecture of Microsoft Active Accessibility and Microsoft UI Automation, and the components that allow interoperability between applications based on the two different technologies.</span></span>

<span data-ttu-id="9824f-105">Para obtener más información sobre la interoperabilidad de Microsoft Active Accessibility y UI Automation, vea [Common Infrastructure](common-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="9824f-105">For more information about Microsoft Active Accessibility and UI Automation interoperability, see [Common Infrastructure](common-infrastructure.md).</span></span>

<span data-ttu-id="9824f-106">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="9824f-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9824f-107">Arquitectura de Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="9824f-107">Microsoft Active Accessibility Architecture</span></span>](#microsoft-active-accessibility-architecture)
-   [<span data-ttu-id="9824f-108">Arquitectura de UI Automation</span><span class="sxs-lookup"><span data-stu-id="9824f-108">UI Automation Architecture</span></span>](#ui-automation-architecture)
-   [<span data-ttu-id="9824f-109">Interoperabilidad de Microsoft Active Accessibility y UI Automation</span><span class="sxs-lookup"><span data-stu-id="9824f-109">Microsoft Active Accessibility and UI Automation Interoperability</span></span>](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [<span data-ttu-id="9824f-110">La interfaz IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="9824f-110">The IAccessibleEx Interface</span></span>](#the-iaccessibleex-interface)
-   [<span data-ttu-id="9824f-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9824f-111">Related topics</span></span>](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a><span data-ttu-id="9824f-112">Arquitectura de Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="9824f-112">Microsoft Active Accessibility Architecture</span></span>

<span data-ttu-id="9824f-113">Microsoft Active Accessibility expone información básica sobre controles como el nombre del control, la ubicación en la pantalla y el tipo de control, así como información de estado como la visibilidad y el estado habilitado/deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="9824f-113">Microsoft Active Accessibility exposes basic information about controls such as control name, location on screen, and type of control, as well as state information such as visibility and enabled/disabled status.</span></span> <span data-ttu-id="9824f-114">La interfaz de usuario se representa como una jerarquía de objetos accesibles; los cambios y las acciones se representan como WinEvents.</span><span class="sxs-lookup"><span data-stu-id="9824f-114">The UI is represented as a hierarchy of accessible objects; changes and actions are represented as WinEvents.</span></span>

<span data-ttu-id="9824f-115">Microsoft Active Accessibility consta de los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="9824f-115">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="9824f-116">Objeto accesible: elemento lógico de la interfaz de usuario (por ejemplo, un botón) representado por una interfaz del modelo de objetos componentes (COM) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y un identificador secundario entero (ChildID).</span><span class="sxs-lookup"><span data-stu-id="9824f-116">Accessible object—A logical UI element (such as a button) that is represented by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Component Object Model (COM) interface and an integer child identifier (ChildID).</span></span>
-   <span data-ttu-id="9824f-117">WinEvents: sistema de eventos que permite a los servidores notificar a los clientes cuando cambia un objeto accesible.</span><span class="sxs-lookup"><span data-stu-id="9824f-117">WinEvents—An event system that enables servers to notify clients when an accessible object changes.</span></span> <span data-ttu-id="9824f-118">Para obtener más información, vea [WinEvents](winevents-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="9824f-118">For more information, see [WinEvents](winevents-infrastructure.md).</span></span>
-   <span data-ttu-id="9824f-119">OLEACC.dll: la biblioteca de vínculos dinámicos en tiempo de ejecución que proporciona la API de Microsoft Active Accessibility y el marco de trabajo del sistema de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="9824f-119">OLEACC.dll—The run-time, dynamic-link library that provides the Microsoft Active Accessibility API and the accessibility system framework.</span></span> <span data-ttu-id="9824f-120">OLEACC implementa objetos proxy que proporcionan información de accesibilidad predeterminada para los elementos de la interfaz de usuario estándar, incluidos los controles de usuario, los menús de usuario y los controles comunes.</span><span class="sxs-lookup"><span data-stu-id="9824f-120">OLEACC implements proxy objects that provide default accessibility information for standard UI elements, including USER controls, USER menus, and common controls.</span></span>

<span data-ttu-id="9824f-121">En el caso de Microsoft Active Accessibility, el componente sistema del marco de accesibilidad (OLEACC) ayuda a la comunicación entre las tecnologías de asistencia (herramientas de accesibilidad) y las aplicaciones, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="9824f-121">For Microsoft Active Accessibility, the system component of the accessibility framework (OLEACC) helps the communication between assistive technologies (accessibility tools) and applications, as the following illustration shows.</span></span>

![Ilustración que muestra cómo las herramientas de accesibilidad interactúan con las aplicaciones](images/msaaarch.gif)

<span data-ttu-id="9824f-123">Las aplicaciones (servidores de Microsoft Active Accessibility) proporcionan información de accesibilidad de la interfaz de usuario a las herramientas (clientes de Microsoft Active Accessibility), que interactúan con la interfaz de usuario en nombre de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="9824f-123">The applications (Microsoft Active Accessibility servers) provide UI accessibility information to tools (Microsoft Active Accessibility clients), which interact with the UI on behalf of users.</span></span> <span data-ttu-id="9824f-124">El límite del código es mediante programación y un límite de proceso.</span><span class="sxs-lookup"><span data-stu-id="9824f-124">The code boundary is both a programmatic and a process boundary.</span></span>

## <a name="ui-automation-architecture"></a><span data-ttu-id="9824f-125">Arquitectura de UI Automation</span><span class="sxs-lookup"><span data-stu-id="9824f-125">UI Automation Architecture</span></span>

<span data-ttu-id="9824f-126">Con la automatización de la interfaz de usuario, el componente principal de automatización de la interfaz de usuario (UIAutomationCore.dll) se carga en los procesos de las herramientas de accesibilidad y de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9824f-126">With UI Automation, the UI Automation core component (UIAutomationCore.dll) is loaded into both the accessibility tools' and applications' processes.</span></span> <span data-ttu-id="9824f-127">El componente principal administra la comunicación entre procesos, proporciona servicios de nivel superior, como la búsqueda de elementos por valores de propiedad, y habilita la captura masiva o el almacenamiento en caché de propiedades, lo que proporciona un mejor rendimiento que la implementación de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="9824f-127">The core component manages cross-process communication, provides higher level services such as searching for elements by property values, and enables bulk fetching or caching of properties, which provides better performance than the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="9824f-128">UI Automation incluye objetos proxy que proporcionan información de la interfaz de usuario sobre elementos de la interfaz de usuario estándar, como controles de usuario, menús de usuario y controles comunes.</span><span class="sxs-lookup"><span data-stu-id="9824f-128">UI Automation includes proxy objects that provide UI information about standard UI elements such as USER controls, USER menus, and common controls.</span></span> <span data-ttu-id="9824f-129">También incluye servidores proxy que permiten a los clientes de automatización de la interfaz de usuario obtener información de la interfaz de usuario de servidores de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="9824f-129">It also includes proxies that enable UI Automation clients to get UI information from Microsoft Active Accessibility servers.</span></span>

<span data-ttu-id="9824f-130">En la ilustración siguiente se muestran las relaciones entre los diversos compontents de automatización de la interfaz de usuario usados en herramientas de accesibilidad (clientes) y en aplicaciones (proveedores).</span><span class="sxs-lookup"><span data-stu-id="9824f-130">The following illustration shows the relationships among the various UI Automation compontents used in accessibility tools (clients) and in applications (providers).</span></span>

![Ilustración en la que se muestra cómo interactúan los componentes de herramientas de accesibilidad con los de las aplicaciones](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a><span data-ttu-id="9824f-132">Interoperabilidad de Microsoft Active Accessibility y UI Automation</span><span class="sxs-lookup"><span data-stu-id="9824f-132">Microsoft Active Accessibility and UI Automation Interoperability</span></span>

<span data-ttu-id="9824f-133">La automatización de la interfaz de usuario a Microsoft Active Accessibility Bridge permite a los clientes de Microsoft Active Accessibility acceder a los proveedores de UI Automation convirtiendo el modelo de objetos de automatización de la interfaz de usuario en un modelo de objetos de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="9824f-133">The UI Automation to Microsoft Active Accessibility Bridge enables Microsoft Active Accessibility clients to access UI Automation providers by converting the UI Automation object model to a Microsoft Active Accessibility object model.</span></span> <span data-ttu-id="9824f-134">En la ilustración siguiente se muestra el rol del puente de automatización de la interfaz de usuario a Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="9824f-134">The following illustration shows the role of the UI Automation-to-Microsoft Active Accessibility Bridge.</span></span>

![Ilustración en la que se muestra cómo funciona automatización de la interfaz de usuario con aplicaciones y herramientas de accesibilidad](images/uiatomsaabridge.gif)

<span data-ttu-id="9824f-136">Del mismo modo, el proxy de automatización de Microsoft Active Accessibility a la interfaz de usuario convierte modelos de objetos de servidor basados en Active Accessibility de Microsoft para clientes de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9824f-136">Similarly, the Microsoft Active Accessibility-to-UI Automation Proxy translates Microsoft Active Accessibility-based server object models for UI Automation clients.</span></span> <span data-ttu-id="9824f-137">En la ilustración siguiente se muestra el rol del proxy de automatización de Microsoft Active Accessibility a la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9824f-137">The following illustration shows the role of the Microsoft Active Accessibility-to-UI Automation Proxy.</span></span>

![Ilustración que muestra cómo funciona el proxy de automatización de la interfaz de usuario con aplicaciones y herramientas de accesibilidad](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a><span data-ttu-id="9824f-139">La interfaz IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="9824f-139">The IAccessibleEx Interface</span></span>

<span data-ttu-id="9824f-140">La interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) permite a las aplicaciones o bibliotecas de interfaz de usuario existentes ampliar su modelo de objetos de Microsoft Active Accessibility para admitir la automatización de la interfaz de usuario sin tener que volver a escribir la implementación desde el principio.</span><span class="sxs-lookup"><span data-stu-id="9824f-140">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface enables existing applications or UI libraries to extend their Microsoft Active Accessibility object model to support UI Automation without rewriting the implementation from scratch.</span></span> <span data-ttu-id="9824f-141">Con **IAccessibleEx**, solo puede implementar las propiedades de automatización de la interfaz de usuario y los patrones de control adicionales necesarios para describir completamente la interfaz de usuario y su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="9824f-141">With **IAccessibleEx**, you can implement only the additional UI Automation properties and control patterns needed to fully describe the UI and its functionality.</span></span>

<span data-ttu-id="9824f-142">Dado que el proxy de automatización de Microsoft Active Accessibility a la interfaz de usuario convierte los modelos de objetos de los servidores de Microsoft Active Accessibility habilitados para [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)como modelos de objetos de automatización de la interfaz de usuario, los clientes de automatización de la interfaz de usuario no necesitan realizar ningún trabajo adicional.</span><span class="sxs-lookup"><span data-stu-id="9824f-142">Because the Microsoft Active Accessibility-to-UI Automation Proxy translates the object models of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)-enabled Microsoft Active Accessibility servers as UI Automation object models, UI Automation clients do not need to do any extra work.</span></span> <span data-ttu-id="9824f-143">La interfaz **IAccessibleEx** también puede permitir que los clientes de Microsoft Active Accessibility en proceso interactúen directamente con los proveedores de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9824f-143">The **IAccessibleEx** interface can also enable in-process Microsoft Active Accessibility clients to interact directly with UI Automation providers.</span></span>

<span data-ttu-id="9824f-144">Para obtener más información, consulte [la interfaz IAccessibleEx](iaccessibleex.md).</span><span class="sxs-lookup"><span data-stu-id="9824f-144">For more information, see [The IAccessibleEx Interface](iaccessibleex.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9824f-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9824f-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9824f-146">Introducción a la API de automatización de Windows</span><span class="sxs-lookup"><span data-stu-id="9824f-146">Windows Automation API Overview</span></span>](windows-automation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="9824f-147">La interfaz IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="9824f-147">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> <dt>

[<span data-ttu-id="9824f-148">Consideraciones de seguridad para las tecnologías de asistencia</span><span class="sxs-lookup"><span data-stu-id="9824f-148">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
</dt> </dl>

 

 




