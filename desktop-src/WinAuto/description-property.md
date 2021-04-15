---
title: Propiedad Description (características de accesibilidad de Windows)
description: La propiedad Description de un objeto proporciona una descripción textual de la apariencia visual de un objeto.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488872"
---
# <a name="description-property-windows-accessibility-features"></a><span data-ttu-id="72108-103">Propiedad Description (características de accesibilidad de Windows)</span><span class="sxs-lookup"><span data-stu-id="72108-103">Description Property (Windows Accessibility features)</span></span>

> [!Note]  
> <span data-ttu-id="72108-104">La propiedad **Description** se suele usar incorrectamente y no es compatible con la automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="72108-104">The **Description** property is often used incorrectly and is not supported by Microsoft UI Automation.</span></span> <span data-ttu-id="72108-105">Los desarrolladores de Microsoft Active Accessibility Server no deben usar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="72108-105">Microsoft Active Accessibility server developers should not use this property.</span></span> <span data-ttu-id="72108-106">Si se necesita más información para escenarios de accesibilidad y automatización, use las propiedades admitidas por los elementos de UI Automation y los patrones de control.</span><span class="sxs-lookup"><span data-stu-id="72108-106">If more information is needed for accessibility and automation scenarios, use the properties supported by UI Automation elements and control patterns.</span></span>

 

<span data-ttu-id="72108-107">La propiedad **Description** de un objeto proporciona una descripción textual de la apariencia visual de un objeto.</span><span class="sxs-lookup"><span data-stu-id="72108-107">An object's **Description** property provides a textual description about an object's visual appearance.</span></span> <span data-ttu-id="72108-108">La descripción se usa principalmente para proporcionar más contexto a los usuarios ciegos o de baja visión, pero también se usa para la búsqueda de contexto o para otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="72108-108">The description is primarily used to provide greater context for low-vision or blind users, but is also used for context searching or other applications.</span></span> <span data-ttu-id="72108-109">Esta propiedad puede ayudar a los usuarios a entender un icono o la apariencia visual general.</span><span class="sxs-lookup"><span data-stu-id="72108-109">This property can help users understand an icon or the overall visual appearance.</span></span>

<span data-ttu-id="72108-110">La propiedad **Description** se recupera llamando a [**IAccessible:: get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span><span class="sxs-lookup"><span data-stu-id="72108-110">The **Description** property is retrieved by calling [**IAccessible::get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span></span>

## <a name="when-to-support-the-description-property"></a><span data-ttu-id="72108-111">Cuándo se debe admitir la propiedad Description</span><span class="sxs-lookup"><span data-stu-id="72108-111">When to Support the Description Property</span></span>

<span data-ttu-id="72108-112">Los servidores admiten la propiedad **Description** si la descripción no es obvia, o cuando no es redundante en función del [**nombre**](name-property.md)del objeto, el [**rol**](role-property.md), el [**Estado**](state-property.md)y las propiedades de [**valor**](value-property.md) .</span><span class="sxs-lookup"><span data-stu-id="72108-112">Servers support the **Description** property if the description is not obvious, or when it is not redundant based on the object's [**Name**](name-property.md), [**Role**](role-property.md), [**State**](state-property.md), and [**Value**](value-property.md) properties.</span></span> <span data-ttu-id="72108-113">Por ejemplo, un botón con la etiqueta "OK" no necesitaría información adicional, mientras que un botón que muestra una imagen de un cactus.</span><span class="sxs-lookup"><span data-stu-id="72108-113">For example, a button labeled "OK" would not need additional information, whereas a button that shows a picture of a cactus would.</span></span> <span data-ttu-id="72108-114">Las propiedades **nombre**, **rol** y [**ayuda**](help-property.md) de este botón describen su finalidad, pero la propiedad **Descripción** transmite información que es menos tangible; por ejemplo, "este botón muestra una imagen de un cactus".</span><span class="sxs-lookup"><span data-stu-id="72108-114">The **Name**, **Role**, and [**Help**](help-property.md) properties for such a button describe its purpose, but the **Description** property conveys information that is less tangible; for example, "This button shows a picture of a cactus."</span></span>

<span data-ttu-id="72108-115">Un servidor de Microsoft Active Accessibility puede Agregar compatibilidad para la automatización de la interfaz de usuario mediante el uso de la [anotación directa](direct-annotation.md), el uso de la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) o la implementación de Microsoft Active Accessibility y la automatización de la interfaz de usuario en paralelo con las dos implementaciones que controlan el mensaje de la función [**\_ GETOBJECT de WM**](wm-getobject.md) .</span><span class="sxs-lookup"><span data-stu-id="72108-115">A Microsoft Active Accessibility server can add support for UI Automation by using [Direct Annotation](direct-annotation.md), using the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, or by implementing Microsoft Active Accessibility and UI Automation side-by-side with both implementations handling the [**WM\_GETOBJECT**](wm-getobject.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72108-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="72108-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72108-117">Usar la anotación directa</span><span class="sxs-lookup"><span data-stu-id="72108-117">Using Direct Annotation</span></span>](using-direct-annotation.md)
</dt> <dt>

[<span data-ttu-id="72108-118">La interfaz IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="72108-118">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> </dl>

 

 




