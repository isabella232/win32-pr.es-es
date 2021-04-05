---
title: Interfaces de condición de propiedad para clientes
description: En esta sección se describen las interfaces de condiciones de propiedad para los clientes de automatización de la interfaz de usuario para aplicaciones Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077841"
---
# <a name="property-condition-interfaces-for-clients"></a><span data-ttu-id="d06dc-103">Interfaces de condición de propiedad para clientes</span><span class="sxs-lookup"><span data-stu-id="d06dc-103">Property Condition Interfaces for Clients</span></span>

<span data-ttu-id="d06dc-104">En esta sección se describen las interfaces de condiciones de propiedad para los clientes de automatización de la interfaz de usuario para aplicaciones Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="d06dc-104">This section describes property condition interfaces for UI Automation clients for Microsoft Win32 applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d06dc-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d06dc-105">In this section</span></span>



| <span data-ttu-id="d06dc-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="d06dc-106">Interface</span></span>                                                                                  | <span data-ttu-id="d06dc-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d06dc-107">Description</span></span>                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d06dc-108">**IUIAutomationAndCondition**</span><span class="sxs-lookup"><span data-stu-id="d06dc-108">**IUIAutomationAndCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | <span data-ttu-id="d06dc-109">Expone propiedades y métodos que las aplicaciones cliente de automatización de la interfaz de usuario de Microsoft pueden usar para recuperar información sobre una condición de propiedad basada en y.</span><span class="sxs-lookup"><span data-stu-id="d06dc-109">Exposes properties and methods that Microsoft UI Automation client applications can use to retrieve information about an AND-based property condition.</span></span> <br/> |
| [<span data-ttu-id="d06dc-110">**IUIAutomationBoolCondition**</span><span class="sxs-lookup"><span data-stu-id="d06dc-110">**IUIAutomationBoolCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | <span data-ttu-id="d06dc-111">Representa una condición que puede ser **true** (selecciona todos los elementos) o **false** (no selecciona ningún elemento).</span><span class="sxs-lookup"><span data-stu-id="d06dc-111">Represents a condition that can be either **TRUE** (selects all elements) or **FALSE** (selects no elements).</span></span><br/>                                           |
| [<span data-ttu-id="d06dc-112">**IUIAutomationCondition**</span><span class="sxs-lookup"><span data-stu-id="d06dc-112">**IUIAutomationCondition**</span></span>](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | <span data-ttu-id="d06dc-113">Esta es la interfaz principal para las condiciones usadas en el filtrado cuando se buscan elementos en el árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d06dc-113">This is the primary interface for conditions used in filtering when searching for elements in the UI Automation tree.</span></span><br/>                                   |
| [<span data-ttu-id="d06dc-114">**IUIAutomationNotCondition**</span><span class="sxs-lookup"><span data-stu-id="d06dc-114">**IUIAutomationNotCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | <span data-ttu-id="d06dc-115">Representa una condición que es el valor negativo de otra condición.</span><span class="sxs-lookup"><span data-stu-id="d06dc-115">Represents a condition that is the negative of another condition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d06dc-116">**IUIAutomationOrCondition**</span><span class="sxs-lookup"><span data-stu-id="d06dc-116">**IUIAutomationOrCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | <span data-ttu-id="d06dc-117">Representa una condición que se compone de varias condiciones, al menos una de las cuales debe ser true.</span><span class="sxs-lookup"><span data-stu-id="d06dc-117">Represents a condition made up of multiple conditions, at least one of which must be true.</span></span><br/>                                                              |
| [<span data-ttu-id="d06dc-118">**IUIAutomationPropertyCondition**</span><span class="sxs-lookup"><span data-stu-id="d06dc-118">**IUIAutomationPropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | <span data-ttu-id="d06dc-119">Representa una condición basada en un valor de propiedad que se usa para buscar elementos de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d06dc-119">Represents a condition based on a property value that is used to find UI Automation elements.</span></span><br/>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="d06dc-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d06dc-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d06dc-121">Clientes de UI Automation</span><span class="sxs-lookup"><span data-stu-id="d06dc-121">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

