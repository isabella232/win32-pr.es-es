---
title: La interfaz IAccessibleEx
description: Los controles que no tienen un proveedor de automatización de la interfaz de usuario de Microsoft, pero que implementan IAccessible, se pueden actualizar fácilmente para proporcionar alguna funcionalidad de automatización de la interfaz de usuario mediante la implementación de la interfaz IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148837"
---
# <a name="the-iaccessibleex-interface"></a><span data-ttu-id="b6055-103">La interfaz IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="b6055-103">The IAccessibleEx Interface</span></span>

<span data-ttu-id="b6055-104">Los controles que no tienen un proveedor de automatización de la interfaz de usuario de Microsoft, pero que implementan [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), se pueden actualizar fácilmente para proporcionar alguna funcionalidad de automatización de la interfaz de usuario mediante la implementación de la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="b6055-104">Controls that do not have a Microsoft UI Automation provider, but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), can easily be upgraded to provide some UI Automation functionality by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="b6055-105">Esta interfaz permite que el control exponga las propiedades y los patrones de control de la automatización de la interfaz de usuario, sin necesidad de una implementación completa de las interfaces del proveedor de automatización de la interfaz de usuario, como [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span><span class="sxs-lookup"><span data-stu-id="b6055-105">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="b6055-106">Para usar **IAccessibleEx**, **IRawElementProviderFragment** y todas las demás interfaces de automatización de la interfaz de usuario, incluya el archivo de encabezado UIAutomation. h en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="b6055-106">To use **IAccessibleEx**, **IRawElementProviderFragment**, and all other UI Automation interfaces, include the UIAutomation.h header file in your source code.</span></span>

<span data-ttu-id="b6055-107">Por ejemplo, considere un control personalizado que tiene un valor de intervalo.</span><span class="sxs-lookup"><span data-stu-id="b6055-107">For example, consider a custom control that has a range value.</span></span> <span data-ttu-id="b6055-108">El servidor de Microsoft Active Accessibility para el control define el rol del control y puede devolver su valor actual.</span><span class="sxs-lookup"><span data-stu-id="b6055-108">The Microsoft Active Accessibility server for the control defines the control's role and is able to return its current value.</span></span> <span data-ttu-id="b6055-109">Sin embargo, dado que Microsoft Active Accessibility no define las propiedades mínima y máxima, el servidor carece de los medios para devolver los valores mínimo y máximo del control.</span><span class="sxs-lookup"><span data-stu-id="b6055-109">However, because Microsoft Active Accessibility does not define minimum and maximum properties, the server lacks the means to return the minimum and maximum values of the control.</span></span> <span data-ttu-id="b6055-110">Un cliente de automatización de la interfaz de usuario puede recuperar el rol del control, el valor actual y otras propiedades de Microsoft Active Accessibility, porque el núcleo de automatización de la interfaz de usuario puede obtenerlos a través de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="b6055-110">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="b6055-111">Sin embargo, sin acceso a una interfaz [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) en el objeto, la automatización de la interfaz de usuario tampoco puede recuperar los valores máximo y mínimo.</span><span class="sxs-lookup"><span data-stu-id="b6055-111">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="b6055-112">El desarrollador del control podría proporcionar un proveedor de automatización de la interfaz de usuario completo para el control, pero esto supondría duplicar gran parte de la funcionalidad existente de la implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : por ejemplo, navegación y propiedades comunes.</span><span class="sxs-lookup"><span data-stu-id="b6055-112">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="b6055-113">En su lugar, el desarrollador puede seguir confiando en **IAccessible** para proporcionar esta funcionalidad, al tiempo que agrega compatibilidad para las propiedades específicas del control a través de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span><span class="sxs-lookup"><span data-stu-id="b6055-113">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b6055-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b6055-114">In this section</span></span>

-   [<span data-ttu-id="b6055-115">Instrucciones de implementación de IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="b6055-115">IAccessibleEx Implementation Guidelines</span></span>](iaccessibleex-implementation-guidelines.md)
-   [<span data-ttu-id="b6055-116">Implementación de IAccessibleEx para proveedores</span><span class="sxs-lookup"><span data-stu-id="b6055-116">Implementing IAccessibleEx for Providers</span></span>](implementing-iaccessibleex-for-providers.md)
-   [<span data-ttu-id="b6055-117">Usar IAccessibleEx desde un cliente</span><span class="sxs-lookup"><span data-stu-id="b6055-117">Using IAccessibleEx from a Client</span></span>](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a><span data-ttu-id="b6055-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6055-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6055-119">Infraestructura común</span><span class="sxs-lookup"><span data-stu-id="b6055-119">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




