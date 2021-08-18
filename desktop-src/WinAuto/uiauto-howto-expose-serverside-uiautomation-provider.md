---
title: Cómo exponer un proveedor Server-Side Automatización de la interfaz de usuario datos
description: Este tema contiene código de ejemplo que muestra cómo exponer un proveedor de microsoft Automatización de la interfaz de usuario servidor para un control personalizado.
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771e81a058af16320673e46a7981cf49ee22105fa841807bc07e3a528ff223cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133318"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a>Cómo exponer un proveedor Server-Side Automatización de la interfaz de usuario datos

Este tema contiene código de ejemplo que muestra cómo exponer un proveedor de microsoft Automatización de la interfaz de usuario servidor para un control personalizado.

Microsoft Automatización de la interfaz de usuario el mensaje [**\_ WM GETOBJECT**](wm-getobject.md) a una aplicación de proveedor para recuperar información sobre un objeto accesible admitido por el proveedor. Automatización de la interfaz de usuario **envía WM \_ GETOBJECT** cuando un cliente llama a [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)y [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), y al controlar eventos para los que el cliente se ha registrado.

Cuando un proveedor recibe un [**mensaje \_ GETOBJECT**](wm-getobject.md) de WM, debe comprobar si el parámetro *lParam* es igual a **UiaRootObjectId.** Si es así, el proveedor debe devolver la [**interfaz IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) del objeto . El proveedor devuelve la interfaz llamando a [**la función UiaReturnRawElementProvider.**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)

En el ejemplo siguiente se muestra cómo responder a [**WM \_ GETOBJECT**](wm-getobject.md).


```C++
    // Expose the custom button's server-side provider to UI Automation.
    case WM_GETOBJECT:
        {
            // If lParam matches UiaRootObjectId, return IRawElementProviderSimple.
            if (static_cast<long>(lParam) == static_cast<long>(UiaRootObjectId))
            {
                // Retrieve the pointer to the custom button object from the
                // window data.
                CustomButton* pControl = reinterpret_cast<CustomButton*>(
                    GetWindowLongPtr(hwnd, GWLP_USERDATA));

                // Call an application-defined method to get the
                // IRawElementProviderSimple pointer.
                IRawElementProviderSimple* pRootProvider = 
                    pControl->GetUIAutomationProvider(hwnd);

                // Return the IRawElementProviderSimple pointer to UI Automation.
                return UiaReturnRawElementProvider(hwnd, wParam, lParam, 
                    pRootProvider);
            }
            return 0;
        }
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Implementación de un proveedor Server-Side Automatización de la interfaz de usuario aplicación](uiauto-serversideprovider.md)
</dt> <dt>

[Mensaje \_ GETOBJECT de WM](the-wm-getobject-message.md)
</dt> <dt>

[Temas de ayuda para proveedores de Automatización de la interfaz de usuario](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




