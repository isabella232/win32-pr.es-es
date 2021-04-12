---
title: Cómo exponer un proveedor de automatización de la interfaz de usuario de Server-Side
description: Este tema contiene código de ejemplo que muestra cómo exponer un proveedor de automatización de la interfaz de usuario de Microsoft de servidor para un control personalizado.
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5af3fa9e663bc737df95015db94cdedc1073ab9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268985"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a><span data-ttu-id="e5a32-103">Cómo exponer un proveedor de automatización de la interfaz de usuario de Server-Side</span><span class="sxs-lookup"><span data-stu-id="e5a32-103">How to Expose a Server-Side UI Automation Provider</span></span>

<span data-ttu-id="e5a32-104">Este tema contiene código de ejemplo que muestra cómo exponer un proveedor de automatización de la interfaz de usuario de Microsoft de servidor para un control personalizado.</span><span class="sxs-lookup"><span data-stu-id="e5a32-104">This topic contains example code that shows how to expose a server-side Microsoft UI Automation provider for a custom control.</span></span>

<span data-ttu-id="e5a32-105">La automatización de la interfaz de usuario de Microsoft envía el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) a una aplicación de proveedor para recuperar información sobre un objeto accesible compatible con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="e5a32-105">Microsoft UI Automation sends the [**WM\_GETOBJECT**](wm-getobject.md) message to a provider application to retrieve information about an accessible object supported by the provider.</span></span> <span data-ttu-id="e5a32-106">La automatización de la interfaz de usuario envía **WM \_ GETOBJECT** cuando un cliente llama a [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)y [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), y al controlar los eventos para los que el cliente se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="e5a32-106">UI Automation sends **WM\_GETOBJECT** when a client calls [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which the client has registered.</span></span>

<span data-ttu-id="e5a32-107">Cuando un proveedor recibe un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) , debe comprobar si el parámetro *lParam* es igual a **UiaRootObjectId**.</span><span class="sxs-lookup"><span data-stu-id="e5a32-107">When a provider receives a [**WM\_GETOBJECT**](wm-getobject.md) message, it should check whether the *lParam* parameter is equal to **UiaRootObjectId**.</span></span> <span data-ttu-id="e5a32-108">Si es así, el proveedor debe devolver la interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) del objeto.</span><span class="sxs-lookup"><span data-stu-id="e5a32-108">If it is, the provider should return the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface of the object.</span></span> <span data-ttu-id="e5a32-109">El proveedor devuelve la interfaz mediante una llamada a la función [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="e5a32-109">The provider returns the interface by calling the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>

<span data-ttu-id="e5a32-110">En el ejemplo siguiente se muestra cómo responder a [**WM \_ GETOBJECT**](wm-getobject.md).</span><span class="sxs-lookup"><span data-stu-id="e5a32-110">The following example demonstrates shows how to respond to [**WM\_GETOBJECT**](wm-getobject.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e5a32-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5a32-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e5a32-112">**Vista**</span><span class="sxs-lookup"><span data-stu-id="e5a32-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e5a32-113">Implementar un proveedor de automatización de la interfaz de usuario de Server-Side</span><span class="sxs-lookup"><span data-stu-id="e5a32-113">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="e5a32-114">\_Mensaje GETOBJECT de WM</span><span class="sxs-lookup"><span data-stu-id="e5a32-114">The WM\_GETOBJECT Message</span></span>](the-wm-getobject-message.md)
</dt> <dt>

[<span data-ttu-id="e5a32-115">Temas de procedimientos para los proveedores de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="e5a32-115">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




