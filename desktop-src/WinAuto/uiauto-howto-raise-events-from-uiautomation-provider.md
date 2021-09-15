---
title: Cómo generar eventos desde un proveedor Automatización de la interfaz de usuario datos
description: Este tema contiene código de ejemplo que muestra cómo un proveedor Automatización de la interfaz de usuario Microsoft genera un evento.
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417c86771c24cc1a67fd907aaf0628037edce44d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567281"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a>Cómo generar eventos desde un proveedor Automatización de la interfaz de usuario datos

Este tema contiene código de ejemplo que muestra cómo un proveedor Automatización de la interfaz de usuario Microsoft genera un evento.

En el código de ejemplo siguiente se muestra un método de una aplicación que implementa un botón personalizado. La aplicación llama al método cada vez que se invoca el botón personalizado. El método comprueba si algún cliente está escuchando eventos y, si es así, genera el evento [**\_ Invoke \_ InvokedEventId de UIA**](uiauto-event-ids.md) para notificar a los clientes que se invocó el botón.


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

**Conceptual**
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Temas de ayuda para proveedores Automatización de la interfaz de usuario de aplicaciones](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




