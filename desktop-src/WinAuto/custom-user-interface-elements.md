---
title: Elementos de la interfaz de usuario personalizada
description: Los desarrolladores de servidores diseñan objetos accesibles basándose en la interfaz de usuario de una aplicación.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903226"
---
# <a name="custom-user-interface-elements"></a><span data-ttu-id="8e988-103">Elementos de la interfaz de usuario personalizada</span><span class="sxs-lookup"><span data-stu-id="8e988-103">Custom User Interface Elements</span></span>

<span data-ttu-id="8e988-104">Los desarrolladores de servidores diseñan objetos accesibles basándose en la interfaz de usuario de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8e988-104">Server developers design accessible objects based on an application's UI.</span></span> <span data-ttu-id="8e988-105">Dado que [Active Accessibility implementa la interfaz IAccessible en nombre de los elementos de la interfaz de usuario proporcionados por el sistema](appendix-a--supported-user-interface-elements-reference.md) , como cuadros de lista, menús y controles TrackBar, debe implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) solo para los siguientes tipos de elementos de la interfaz de usuario personalizados:</span><span class="sxs-lookup"><span data-stu-id="8e988-105">Because [Active Accessibility implements the IAccessible interface on behalf of system-provided user interface elements](appendix-a--supported-user-interface-elements-reference.md) such as list boxes, menus, and trackbar controls, you need to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface only for the following kinds of custom UI elements:</span></span>

-   <span data-ttu-id="8e988-106">Controles personalizados creados mediante el registro de una clase de ventana definida por la aplicación</span><span class="sxs-lookup"><span data-stu-id="8e988-106">Custom controls created by registering an application-defined window class</span></span>
-   <span data-ttu-id="8e988-107">Controles personalizados dibujados directamente en la pantalla que no tienen un **hWnd** asociado</span><span class="sxs-lookup"><span data-stu-id="8e988-107">Custom controls drawn directly on the screen that do not have an associated **HWND**</span></span>
-   <span data-ttu-id="8e988-108">Controles personalizados como Microsoft ActiveX y controles Java</span><span class="sxs-lookup"><span data-stu-id="8e988-108">Custom controls such as Microsoft ActiveX and Java controls</span></span>
-   <span data-ttu-id="8e988-109">Controles u objetos de la ventana de cliente de la aplicación que aún no están expuestos</span><span class="sxs-lookup"><span data-stu-id="8e988-109">Controls or objects in the application's client window that aren't already exposed</span></span>

<span data-ttu-id="8e988-110">Los menús y controles dibujados por el propietario son accesibles siempre que se sigan las directrices descritas en [accesos directos para exponer elementos de la interfaz de usuario personalizados](shortcuts-for-exposing-custom-user-interface-elements.md).</span><span class="sxs-lookup"><span data-stu-id="8e988-110">Owner-drawn controls and menus are accessible as long as you follow the guidelines discussed in [Shortcuts for Exposing Custom User Interface Elements](shortcuts-for-exposing-custom-user-interface-elements.md).</span></span> <span data-ttu-id="8e988-111">Si sigue estas instrucciones, no es necesario implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para los menús y controles dibujados por el propietario.</span><span class="sxs-lookup"><span data-stu-id="8e988-111">If you follow these guidelines, then you do not need to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for owner-drawn controls and menus.</span></span>

<span data-ttu-id="8e988-112">En la mayoría de los casos, se puede tener acceso a los controles con subclases y subclases porque el sistema controla la funcionalidad básica del control.</span><span class="sxs-lookup"><span data-stu-id="8e988-112">In most cases, superclassed and subclassed controls are accessible because the system handles the basic functionality of the control.</span></span> <span data-ttu-id="8e988-113">Sin embargo, si un control superclase o subclase modifica significativamente el comportamiento del control proporcionado por el sistema en el que se basa, debe implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="8e988-113">However, if a superclassed or subclassed control significantly modifies the behavior of the system-provided control on which it is based, then you must implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="8e988-114">Para obtener más información, vea [exponer controles basados en controles del sistema](exposing-controls-based-on-system-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8e988-114">For more information, see [Exposing Controls Based on System Controls](exposing-controls-based-on-system-controls.md).</span></span>

<span data-ttu-id="8e988-115">Si una aplicación solo usa elementos de la interfaz de usuario proporcionados por el sistema, no es necesario implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), excepto para su ventana de cliente.</span><span class="sxs-lookup"><span data-stu-id="8e988-115">If an application uses only system-provided user interface elements, then it does not need to implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), except for its client window.</span></span> <span data-ttu-id="8e988-116">Por ejemplo, una aplicación que incluye un editor de texto, no implementado mediante un control de edición, expone líneas de texto como objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="8e988-116">For example, an application that includes a text editor, not implemented using an edit control, exposes lines of text as accessible objects.</span></span> <span data-ttu-id="8e988-117">Tenga en cuenta que Microsoft Active Accessibility expone automáticamente el texto en los controles de edición y edición enriquecida como una sola cadena de texto en la propiedad [**Value**](value-property.md) del control.</span><span class="sxs-lookup"><span data-stu-id="8e988-117">Note that Microsoft Active Accessibility automatically exposes the text in edit and rich edit controls as a single string of text in the [**Value**](value-property.md) property of the control.</span></span>

 

 




