---
title: Control del mensaje WM_GETOBJECT mensaje
description: Tanto Microsoft Active Accessibility como Microsoft Automatización de la interfaz de usuario el mensaje GETOBJECT de WM a una aplicación de servidor o proveedor para recuperar información sobre un objeto accesible compatible con el servidor \_ o el proveedor.
ms.assetid: 4b8e551f-aba7-4a89-8874-ba690175f525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695fad8f050606f0a95a1780551d35499e39d166
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465709"
---
# <a name="handling-the-wm_getobject-message"></a>Control del mensaje \_ GETOBJECT de WM

Tanto Microsoft Active Accessibility como Microsoft Automatización de la interfaz de usuario el mensaje [**\_ GETOBJECT**](wm-getobject.md) de WM a una aplicación de servidor o proveedor para recuperar información sobre un objeto accesible compatible con el servidor o el proveedor. Los clientes nunca **envían WM \_ GETOBJECT** directamente. En su lugar, Microsoft Active Accessibility este mensaje cuando un cliente llama a las funciones [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)y [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) Automatización de la interfaz de usuario envía **WM \_ GETOBJECT** cuando un cliente llama a [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)y [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), y al controlar eventos para los que el cliente se ha registrado.

Microsoft Active Accessibility o Automatización de la interfaz de usuario especifica el tipo de objeto para el que necesita información pasando un valor denominado identificador de objeto *con* el [**mensaje \_ GETOBJECT de WM.**](wm-getobject.md) Cuando recibe el mensaje, el servidor o el proveedor examina el identificador de objeto para determinar cómo responder al mensaje. La respuesta depende de si la aplicación receptora implementa Microsoft Active Accessibility (un servidor), Automatización de la interfaz de usuario (un proveedor) o ninguno para el objeto especificado.

-   Si la aplicación receptora es un servidor Microsoft Active Accessibility y el mensaje [**\_ GETOBJECT**](wm-getobject.md) de WM incluye un identificador de objeto de [**OBJID \_ CLIENT**](object-identifiers.md), el servidor debe devolver el valor obtenido pasando la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto a la función [**LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
-   Si la aplicación receptora es un proveedor de Automatización de la interfaz de usuario y el identificador de objeto es **UiaRootObjectId**, el proveedor debe devolver la [**interfaz IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) del objeto. El proveedor obtiene la interfaz llamando a la [**función UiaReturnRawElementProvider.**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)
-   Si la aplicación receptora no implementa Microsoft Active Accessibility ni Automatización de la interfaz de usuario, debe pasar el [**mensaje \_ GETOBJECT**](wm-getobject.md) de WM a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Pasar el mensaje permite que el marco de accesibilidad determine si hay un proxy disponible para el objeto especificado.
-   Si el identificador de objeto no es [**ni OBJID \_ CLIENT**](object-identifiers.md) ni UiaRootObjectId, la aplicación receptora debe pasar el [**mensaje \_ GETOBJECT**](wm-getobject.md) de WM a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Pasar el mensaje permite que el marco de accesibilidad use los proveedores predeterminados para los elementos de interfaz de usuario estándar.

Microsoft Active Accessibility y Automatización de la interfaz de usuario pueden pasar identificadores de objeto personalizados en un mensaje [**\_ GETOBJECT**](wm-getobject.md) de WM para recuperar objetos u valores definidos por la aplicación de un servidor o proveedor. El identificador de objeto [**OBJID \_ NATIVEOM**](object-identifiers.md) o [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) se puede usar para recuperar una interfaz nativa del modelo de objetos o para solicitar un objeto proxy específico compatible con Oleacc.dll.

Al controlar los identificadores de objeto [**OBJID \_ CLIENT**](object-identifiers.md) y **UiaRootObjectId,** una implementación de servidor Microsoft Active Accessibility puede coexistir junto con una implementación de Automatización de la interfaz de usuario proveedor. Dado que la mayoría de los controles Windows estándar y los controles comunes implementados por la biblioteca de controles comunes (ComCtl32.dll) no implementan Microsoft Active Accessibility o Automatización de la interfaz de usuario, estos controles normalmente no controlan el [**mensaje \_ GETOBJECT de WM.**](wm-getobject.md) En su lugar, Microsoft Active Accessibility o marco de trabajo de automatización de la interfaz de usuario comprueba si un objeto proxy está disponible para un elemento de interfaz de usuario determinado. De lo contrario, proporciona el objeto proxy predeterminado para el objeto de ventana host.

 

 