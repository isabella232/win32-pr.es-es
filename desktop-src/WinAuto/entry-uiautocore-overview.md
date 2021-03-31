---
title: Fundamentos de UI Automation
description: En esta sección se explican los conceptos fundamentales en los que se basa la automatización de la interfaz de usuario.
ms.assetid: 109f113f-9ed0-4a57-b3af-90e831e53c42
keywords:
- Automatización de la interfaz de usuario, API de Microsoft Win32
- Automatización de la interfaz de usuario, API Win32
- Automatización de la interfaz de usuario, proveedores
- Automatización de la interfaz de usuario, aplicaciones cliente
- clientes, Microsoft UI Automation para Microsoft Win32 API
- clientes, UI Automation para Microsoft Win32 API
- API Win32
- Microsoft Win32 API
- Automatización de la interfaz de usuario para Microsoft Win32 API
- Automatización de la interfaz de usuario de Microsoft para Microsoft Win32 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba8147a8dd7f8d03340fad43465c225a174e606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418918"
---
# <a name="ui-automation-fundamentals"></a><span data-ttu-id="4b316-113">Fundamentos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4b316-113">UI Automation Fundamentals</span></span>

<span data-ttu-id="4b316-114">Microsoft UI Automation permite que las aplicaciones de tecnología de asistencia y las herramientas de pruebas automatizadas interactúen con los controles de interfaz de usuario de otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4b316-114">Microsoft UI Automation enables assistive technology applications and automated testing tools to interact with the UI controls of other applications.</span></span> <span data-ttu-id="4b316-115">En esta sección se explican los conceptos fundamentales en los que se basa la automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4b316-115">This section explains the fundamental concepts that UI Automation is based on.</span></span>

<span data-ttu-id="4b316-116">La API de automatización de la interfaz de usuario se encuentra en dos partes.</span><span class="sxs-lookup"><span data-stu-id="4b316-116">The UI Automation API is in two parts.</span></span> <span data-ttu-id="4b316-117">Una parte la usan las aplicaciones del proveedor de automatización de la *interfaz de usuario* y la otra la usan las aplicaciones cliente de automatización de la interfaz de *usuario* .</span><span class="sxs-lookup"><span data-stu-id="4b316-117">One part is used by *UI Automation provider* applications, and the other is used by *UI Automation client* applications.</span></span> <span data-ttu-id="4b316-118">La API de proveedor de permite a los desarrolladores de controles personalizados de Microsoft Win32 y otros marcos de control exponer esos controles a la automatización de la interfaz de usuario y hacerlos visibles en las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="4b316-118">The provider API enables developers of Microsoft Win32 custom control and other control frameworks to expose those controls to UI Automation and make them visible to client applications.</span></span> <span data-ttu-id="4b316-119">La API de cliente permite a las aplicaciones interactuar con los controles de otras aplicaciones y recuperar información sobre ellos.</span><span class="sxs-lookup"><span data-stu-id="4b316-119">The client API enables applications to interact with controls in other applications and retrieve information about them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4b316-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4b316-120">In this section</span></span>

-   [<span data-ttu-id="4b316-121">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="4b316-121">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
-   [<span data-ttu-id="4b316-122">Automatización y Active Accessibility de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="4b316-122">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
-   [<span data-ttu-id="4b316-123">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="4b316-123">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
-   [<span data-ttu-id="4b316-124">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4b316-124">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
-   [<span data-ttu-id="4b316-125">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4b316-125">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
-   [<span data-ttu-id="4b316-126">Información general acerca de las propiedades de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4b316-126">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
-   [<span data-ttu-id="4b316-127">Información general sobre eventos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4b316-127">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
-   [<span data-ttu-id="4b316-128">Propiedades, eventos y patrones de control personalizados</span><span class="sxs-lookup"><span data-stu-id="4b316-128">Custom Properties, Events, and Control Patterns</span></span>](uiauto-custompropertieseventscontrolpatterns.md)
-   [<span data-ttu-id="4b316-129">Compatibilidad de UI Automation para el contenido textual</span><span class="sxs-lookup"><span data-stu-id="4b316-129">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
-   [<span data-ttu-id="4b316-130">Compatibilidad de UI Automation para arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="4b316-130">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
-   [<span data-ttu-id="4b316-131">Consideraciones de seguridad para las tecnologías de asistencia</span><span class="sxs-lookup"><span data-stu-id="4b316-131">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
-   [<span data-ttu-id="4b316-132">Prácticas recomendadas para usar matrices seguras</span><span class="sxs-lookup"><span data-stu-id="4b316-132">Best Practices for Using Safe Arrays</span></span>](uiauto-workingwithsafearrays.md)
-   [<span data-ttu-id="4b316-133">Especificación de Automatización de la interfaz de usuario y Promesa de la comunidad</span><span class="sxs-lookup"><span data-stu-id="4b316-133">UI Automation Specification and Community Promise</span></span>](uiauto-specandcommunitypromise.md)

## <a name="related-topics"></a><span data-ttu-id="4b316-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4b316-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b316-135">Automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="4b316-135">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




