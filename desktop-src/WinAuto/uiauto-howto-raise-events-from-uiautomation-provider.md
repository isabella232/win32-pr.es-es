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
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a>Cómo generar eventos desde un proveedor de automatización de la interfaz de usuario

Este tema contiene código de ejemplo que muestra cómo un proveedor de automatización de la interfaz de usuario de Microsoft genera un evento.

En el ejemplo de código siguiente se muestra un método de una aplicación que implementa un botón personalizado. La aplicación llama al método cada vez que se invoca el botón personalizado. El método comprueba si algún cliente está escuchando eventos y, en caso afirmativo, genera el evento [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md) para notificar a los clientes que se invocó el botón.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Temas de procedimientos para los proveedores de automatización de la interfaz de usuario](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




