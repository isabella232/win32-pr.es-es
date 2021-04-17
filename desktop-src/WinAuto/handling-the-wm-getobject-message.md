---
title: Controlar el mensaje de WM_GETOBJECT
description: Tanto Microsoft Active Accessibility como la automatización de la interfaz de usuario de Microsoft envían el mensaje de WM \_ GETOBJECT a una aplicación de servidor o de proveedor para recuperar información sobre un objeto accesible compatible con el servidor o el proveedor.
ms.assetid: 4b8e551f-aba7-4a89-8874-ba690175f525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695fad8f050606f0a95a1780551d35499e39d166
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714425"
---
# <a name="handling-the-wm_getobject-message"></a>Controlar el mensaje de WM \_ GETOBJECT

Tanto Microsoft Active Accessibility como la automatización de la interfaz de usuario de Microsoft envían el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) a una aplicación de servidor o de proveedor para recuperar información sobre un objeto accesible compatible con el servidor o el proveedor. Los clientes nunca envían directamente **WM \_ GETOBJECT** . En su lugar, Microsoft Active Accessibility envía este mensaje cuando un cliente llama a las funciones [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)y [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) . La automatización de la interfaz de usuario envía **WM \_ GETOBJECT** cuando un cliente llama a [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)y [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), y al controlar los eventos para los que el cliente se ha registrado.

Microsoft Active Accessibility o la automatización de la interfaz de usuario especifica el tipo de objeto para el que necesita información pasando un valor denominado *identificador de objeto* con el mensaje de [**\_ GETOBJECT de WM**](wm-getobject.md) . Cuando recibe el mensaje, el servidor o el proveedor examina el identificador de objeto para determinar cómo responder al mensaje. La respuesta depende de si la aplicación receptora implementa Microsoft Active Accessibility (un servidor), automatización de la interfaz de usuario (un proveedor) o ninguna de ellas para el objeto especificado.

-   Si la aplicación receptora es un servidor de Microsoft Active Accessibility y el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) incluye un identificador de objeto de [**\_ cliente de OBJID**](object-identifiers.md), el servidor debe devolver el valor obtenido pasando la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto a la función [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Si la aplicación receptora es un proveedor de automatización de aUI y el identificador de objeto es **UiaRootObjectId**, el proveedor debe devolver la interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) del objeto. El proveedor obtiene la interfaz mediante una llamada a la función [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Si la aplicación receptora no implementa Microsoft Active Accessibility ni la automatización de la interfaz de usuario, debe pasar el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Al pasar el mensaje, se habilita el marco de accesibilidad para determinar si un proxy está disponible para el objeto especificado.
-   Si el identificador de objeto no es [**un \_ cliente de OBJID**](object-identifiers.md) ni UiaRootObjectId, la aplicación receptora debe pasar el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Al pasar el mensaje, el marco de accesibilidad podrá usar los proveedores predeterminados para los elementos de la interfaz de usuario estándar.

Microsoft Active Accessibility y la automatización de la interfaz de usuario pueden pasar los identificadores de objetos personalizados en un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) para recuperar los objetos o los valores definidos por la aplicación de un servidor o proveedor. El identificador de objeto [**objid \_ NATIVEOM**](object-identifiers.md) o [**objid \_ QUERYCLASSNAMEIDX**](object-identifiers.md) se puede usar para recuperar una interfaz del modelo de objetos nativo o para solicitar un objeto proxy específico compatible con Oleacc.dll.

Mediante el control de los identificadores de objeto **UiaRootObjectId** y el [**\_ cliente de OBJID**](object-identifiers.md) , una implementación de Microsoft Active Accessibility Server puede coexistir junto con una implementación del proveedor de automatización de la interfaz de usuario. Dado que la mayoría de los controles estándar de Windows y los controles comunes que implementa la biblioteca de controles comunes (ComCtl32.dll) no implementan Microsoft Active Accessibility o la automatización de la interfaz de usuario, estos controles normalmente no controlan el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) . En su lugar, Microsoft Active Accessibility o el marco de automatización de la interfaz de usuario comprueba si un objeto proxy está disponible para un elemento de la interfaz de usuario determinado. De lo contrario, proporciona el objeto proxy predeterminado para el objeto de ventana host.

 

 