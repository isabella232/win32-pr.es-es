---
title: Interfaces de control de eventos para clientes
description: En esta sección se describen las interfaces de control de eventos para las aplicaciones cliente de automatización de la interfaz de usuario no administradas.
ms.assetid: ce9c4044-f46b-42b7-af44-05aee728a0e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458be6fcf5ce47f285d46c0e61f80e0897f15613
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714227"
---
# <a name="event-handling-interfaces-for-clients"></a><span data-ttu-id="c5a86-103">Interfaces de control de eventos para clientes</span><span class="sxs-lookup"><span data-stu-id="c5a86-103">Event Handling Interfaces for Clients</span></span>

<span data-ttu-id="c5a86-104">En esta sección se describen las interfaces de control de eventos para las aplicaciones cliente de automatización de la interfaz de usuario no administradas.</span><span class="sxs-lookup"><span data-stu-id="c5a86-104">This section describes the event handling interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5a86-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c5a86-105">In this section</span></span>



| <span data-ttu-id="c5a86-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="c5a86-106">Interface</span></span>                                                                                                              | <span data-ttu-id="c5a86-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5a86-107">Description</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5a86-108">**IUIAutomationChangesEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c5a86-108">**IUIAutomationChangesEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationchangeseventhandler)<br/>                         | <span data-ttu-id="c5a86-109">Expone un método para controlar los eventos de automatización de la interfaz de usuario de Microsoft que se producen cuando se cambia una propiedad.</span><span class="sxs-lookup"><span data-stu-id="c5a86-109">Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.</span></span><br/>                      |
| [<span data-ttu-id="c5a86-110">**IUIAutomationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c5a86-110">**IUIAutomationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)<br/>                                       | <span data-ttu-id="c5a86-111">Expone un método para controlar eventos de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c5a86-111">Exposes a method to handle UI Automation events.</span></span><br/>                                                                      |
| [<span data-ttu-id="c5a86-112">**IUIAutomationFocusChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c5a86-112">**IUIAutomationFocusChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)<br/>               | <span data-ttu-id="c5a86-113">Expone un método para controlar los eventos que se producen cuando el foco de teclado se mueve a otro elemento de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c5a86-113">Exposes a method to handle events that are raised when the keyboard focus moves to another UI Automation element.</span></span><br/>     |
| [<span data-ttu-id="c5a86-114">**IUIAutomationNotificationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c5a86-114">**IUIAutomationNotificationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)<br/>               | <span data-ttu-id="c5a86-115">Expone un método para controlar los eventos de notificación de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c5a86-115">Exposes a method to handle UI Automation notification events.</span></span><br/>                                                         |
| [<span data-ttu-id="c5a86-116">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c5a86-116">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)<br/>         | <span data-ttu-id="c5a86-117">Expone un método para controlar eventos de automatización de la interfaz de usuario que se producen cuando se cambia una propiedad.</span><span class="sxs-lookup"><span data-stu-id="c5a86-117">Exposes a method to handle UI Automation events that occur when a property is changed.</span></span><br/>                                |
| [<span data-ttu-id="c5a86-118">**IUIAutomationStructureChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c5a86-118">**IUIAutomationStructureChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler)<br/>       | <span data-ttu-id="c5a86-119">Expone un método para controlar los eventos que se producen cuando se cambia la estructura de árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c5a86-119">Exposes a method to handle events that occur when the UI Automation tree structure is changed.</span></span><br/>                        |
| [<span data-ttu-id="c5a86-120">**IUIAutomationTextEditTextChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c5a86-120">**IUIAutomationTextEditTextChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextedittextchangedeventhandler)<br/> | <span data-ttu-id="c5a86-121">Expone un método para controlar los eventos que se producen cuando la automatización de la interfaz de usuario informa de un evento de cambio de texto de los controles de edición de texto.</span><span class="sxs-lookup"><span data-stu-id="c5a86-121">Exposes a method to handle events that occur when UI Automation reports a text-changed event from text edit controls.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c5a86-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5a86-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5a86-123">Clientes de UI Automation</span><span class="sxs-lookup"><span data-stu-id="c5a86-123">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





