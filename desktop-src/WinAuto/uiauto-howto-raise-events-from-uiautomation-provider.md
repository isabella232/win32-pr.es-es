---
title: Cómo generar eventos desde un proveedor de automatización de la interfaz de usuario
description: Este tema contiene código de ejemplo que muestra cómo un proveedor de automatización de la interfaz de usuario de Microsoft genera un evento.
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417c86771c24cc1a67fd907aaf0628037edce44d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714225"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a><span data-ttu-id="507be-103">Cómo generar eventos desde un proveedor de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="507be-103">How to Raise Events from a UI Automation Provider</span></span>

<span data-ttu-id="507be-104">Este tema contiene código de ejemplo que muestra cómo un proveedor de automatización de la interfaz de usuario de Microsoft genera un evento.</span><span class="sxs-lookup"><span data-stu-id="507be-104">This topic contains example code that shows how a Microsoft UI Automation provider raises an event.</span></span>

<span data-ttu-id="507be-105">En el ejemplo de código siguiente se muestra un método de una aplicación que implementa un botón personalizado.</span><span class="sxs-lookup"><span data-stu-id="507be-105">The following example code shows a method from an application that implements a custom button.</span></span> <span data-ttu-id="507be-106">La aplicación llama al método cada vez que se invoca el botón personalizado.</span><span class="sxs-lookup"><span data-stu-id="507be-106">The application calls the method whenever the custom button is invoked.</span></span> <span data-ttu-id="507be-107">El método comprueba si algún cliente está escuchando eventos y, en caso afirmativo, genera el evento [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md) para notificar a los clientes que se invocó el botón.</span><span class="sxs-lookup"><span data-stu-id="507be-107">The method checks whether any clients are listening for events and, if so, raises the [**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md) event to notify the clients that the button was invoked.</span></span>


```C++
// Responds to a button click. The source of the click could 
// be the mouse, the keyboard, or a client's call to 
// IUIAutomationInvokePattern::Invoke.
void CustomButton::InvokeButton(HWND hwnd)
{
    // TODO: Perform program actions invoked by the control.

    // Check whether any clients are listening for UI Automation 
    // events.
    if (UiaClientsAreListening())
    {
        // Raise an Invoked event. GetUIAutomationProvider is an
        // application-defined method that returns a pointer to
        // the application's IRawElementProviderSimple interface.
        UiaRaiseAutomationEvent(
            GetUIAutomationProvider(hwnd), UIA_Invoke_InvokedEventId); 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="507be-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="507be-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="507be-109">**Vista**</span><span class="sxs-lookup"><span data-stu-id="507be-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="507be-110">Información general sobre eventos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="507be-110">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="507be-111">Temas de procedimientos para los proveedores de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="507be-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




