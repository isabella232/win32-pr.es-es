---
title: Mensaje de WM_GETOBJECT (Winuser. h)
description: Lo envían Microsoft Active Accessibility y la automatización de la interfaz de usuario de Microsoft para obtener información sobre un objeto accesible incluido en una aplicación de servidor.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- WM_GETOBJECT mensaje accesibilidad a Windows
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcac5c7f6dd8203c32b9f6f3c4eb59144cc3f8ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151214"
---
# <a name="wm_getobject-message"></a><span data-ttu-id="ad455-104">\_Mensaje GETOBJECT de WM</span><span class="sxs-lookup"><span data-stu-id="ad455-104">WM\_GETOBJECT message</span></span>

<span data-ttu-id="ad455-105">Lo envían Microsoft Active Accessibility y la automatización de la interfaz de usuario de Microsoft para obtener información sobre un objeto accesible incluido en una aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="ad455-105">Sent by both Microsoft Active Accessibility and Microsoft UI Automation to obtain information about an accessible object contained in a server application.</span></span>

<span data-ttu-id="ad455-106">Las aplicaciones nunca envían este mensaje directamente.</span><span class="sxs-lookup"><span data-stu-id="ad455-106">Applications never send this message directly.</span></span> <span data-ttu-id="ad455-107">Microsoft Active Accessibility envía este mensaje en respuesta a las llamadas a [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)o [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="ad455-107">Microsoft Active Accessibility sends this message in response to calls to [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span> <span data-ttu-id="ad455-108">Sin embargo, las aplicaciones de servidor controlan este mensaje.</span><span class="sxs-lookup"><span data-stu-id="ad455-108">However, server applications handle this message.</span></span> <span data-ttu-id="ad455-109">La automatización de la interfaz de usuario envía este mensaje en respuesta a las llamadas a [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)y [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), y al controlar los eventos para los que se ha registrado un cliente.</span><span class="sxs-lookup"><span data-stu-id="ad455-109">UI Automation sends this message in response to calls to [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which a client has registered.</span></span>


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ad455-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad455-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad455-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ad455-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="ad455-112">Proporciona información adicional sobre el mensaje y solo lo utiliza el sistema.</span><span class="sxs-lookup"><span data-stu-id="ad455-112">Provides additional information about the message and is used only by the system.</span></span> <span data-ttu-id="ad455-113">Los servidores pasan *dwFlags* como el parámetro *wParam* en la llamada a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) al administrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ad455-113">Servers pass *dwFlags* as the *wParam* parameter in the call to [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) when handling the message.</span></span>

</dd> <dt>

<span data-ttu-id="ad455-114">*dwObjId*</span><span class="sxs-lookup"><span data-stu-id="ad455-114">*dwObjId*</span></span> 
</dt> <dd>

<span data-ttu-id="ad455-115">Identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="ad455-115">Object identifier.</span></span> <span data-ttu-id="ad455-116">Este valor es una de las constantes de [identificador de objeto](object-identifiers.md) o un identificador de objeto personalizado.</span><span class="sxs-lookup"><span data-stu-id="ad455-116">This value is one of the [object identifier](object-identifiers.md) constants or a custom object identifier.</span></span> <span data-ttu-id="ad455-117">Una aplicación de servidor debe comprobar este valor para identificar el tipo de información que se solicita.</span><span class="sxs-lookup"><span data-stu-id="ad455-117">A server application must check this value to identify the type of information being requested.</span></span> <span data-ttu-id="ad455-118">Antes de comparar este valor con los valores de OBJID \_ , el servidor debe convertirlo en **DWORD**; de lo contrario, en Windows de 64 bits, la extensión de signo de *lParam* puede interferir con la comparación.</span><span class="sxs-lookup"><span data-stu-id="ad455-118">Before comparing this value against the OBJID\_ values, the server must cast it to **DWORD**; otherwise, on 64-bit Windows, the sign extension of the *lParam* can interfere with the comparison.</span></span>

-   <span data-ttu-id="ad455-119">Si *dwObjId* es uno de los valores de objid \_ como [**el \_ cliente de objid**](object-identifiers.md), la solicitud es para un objeto de Active Accessibility de Microsoft que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="ad455-119">If *dwObjId* is one of the OBJID\_ values such as [**OBJID\_CLIENT**](object-identifiers.md), the request is for a Microsoft Active Accessibility object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>
-   <span data-ttu-id="ad455-120">Si *dwObjId* es igual a **UiaRootObjectId**, la solicitud es para un proveedor de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ad455-120">If *dwObjId* is equal to **UiaRootObjectId**, the request is for a UI Automation provider.</span></span> <span data-ttu-id="ad455-121">Si el servidor está implementando la automatización de la interfaz de usuario, debe devolver un proveedor mediante la función [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="ad455-121">If the server is implementing UI Automation, it should return a provider using the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="ad455-122">Si *dwObjId* es [**OBJID \_ NATIVEOM**](object-identifiers.md), la solicitud es para el modelo de objetos subyacente del control.</span><span class="sxs-lookup"><span data-stu-id="ad455-122">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md), the request is for the control's underlying object model.</span></span> <span data-ttu-id="ad455-123">Si el control admite esta solicitud, debe devolver una interfaz COM adecuada llamando a la función [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="ad455-123">If the control supports this request, it should return an appropriate COM interface by calling the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="ad455-124">Si *dwObjId* es [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md), la solicitud es para que el control se identifique como un control estándar de Windows o un control común implementado por la biblioteca de controles comunes (ComCtrl.dll).</span><span class="sxs-lookup"><span data-stu-id="ad455-124">If *dwObjId* is [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md), the request is for the control to identify itself as a standard Windows control or a common control implemented by the common control library (ComCtrl.dll).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad455-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad455-125">Return value</span></span>

<span data-ttu-id="ad455-126">Si la ventana o el control no necesitan responder a este mensaje, debe pasar el mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . de lo contrario, la ventana o el control deben devolver un valor que corresponda a la solicitud especificada por *dwObjId*:</span><span class="sxs-lookup"><span data-stu-id="ad455-126">If the window or control does not need to respond to this message, it should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function; otherwise, the window or control should return a value that corresponds to the request specified by *dwObjId*:</span></span>

-   <span data-ttu-id="ad455-127">Si la ventana o el control implementan la automatización de la interfaz de usuario, la ventana o el control deben devolver el valor obtenido mediante una llamada a la función [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="ad455-127">If the window or control implements UI Automation, the window or control should return the value obtained by a call to the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="ad455-128">Si *dwObjId* es [**OBJID \_ NATIVEOM**](object-identifiers.md) y la ventana expone un modelo de objetos nativo, las ventanas deben devolver el valor obtenido mediante una llamada a la función [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="ad455-128">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md) and the window exposes a native Object Model, the windows should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="ad455-129">Si *dwObjId* es [**el \_ cliente de OBJID**](object-identifiers.md) y la ventana implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), la ventana debe devolver el valor obtenido mediante una llamada a la función [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="ad455-129">If *dwObjId* is [**OBJID\_CLIENT**](object-identifiers.md) and the window implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), the window should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad455-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad455-130">Remarks</span></span>

<span data-ttu-id="ad455-131">Cuando un cliente llama a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) o a cualquiera de las otras funciones de **AccessibleObjectFrom**_X_ que recuperan una interfaz en un objeto, Microsoft Active Accessibility envía el mensaje de **WM \_ GETOBJECT** al procedimiento de ventana adecuado en la aplicación de servidor adecuada.</span><span class="sxs-lookup"><span data-stu-id="ad455-131">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other **AccessibleObjectFrom**_X_ functions that retrieve an interface to an object, Microsoft Active Accessibility sends the **WM\_GETOBJECT** message to the appropriate window procedure within the appropriate server application.</span></span> <span data-ttu-id="ad455-132">Al procesar **WM \_ GETOBJECT**, las aplicaciones de servidor llaman a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) y usan el valor devuelto de esta función como valor devuelto para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ad455-132">While processing **WM\_GETOBJECT**, server applications call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) and use the return value of this function as the return value for the message.</span></span> <span data-ttu-id="ad455-133">Microsoft Active Accessibility, junto con la biblioteca COM, realiza el cálculo de referencias adecuado y pasa el puntero de interfaz del servidor de vuelta al cliente.</span><span class="sxs-lookup"><span data-stu-id="ad455-133">Microsoft Active Accessibility, in conjunction with the COM library, performs the appropriate marshaling and passes the interface pointer from the server back to the client.</span></span>

<span data-ttu-id="ad455-134">Los servidores no responden a **WM \_ GETOBJECT** antes de que el objeto se inicialice por completo o después de que empiece a cerrarse.</span><span class="sxs-lookup"><span data-stu-id="ad455-134">Servers do not respond to **WM\_GETOBJECT** before the object is fully initialized or after it begins to close down.</span></span> <span data-ttu-id="ad455-135">Cuando una aplicación crea una ventana nueva, el sistema envía [**el \_ objeto \_ de evento Create**](event-constants.md) para notificar a los clientes antes de enviar el mensaje de [ \_ creación de WM](../winmsg/wm-create.md) al procedimiento de ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ad455-135">When an application creates a new window, the system sends [**EVENT\_OBJECT\_CREATE**](event-constants.md) to notify clients before it sends the [WM\_CREATE](../winmsg/wm-create.md) message to the application's window procedure.</span></span> <span data-ttu-id="ad455-136">Dado que muchas aplicaciones usan WM \_ Create para iniciar su proceso de inicialización, los servidores no responden al mensaje de la **\_ GETOBJECT de WM** hasta que finaliza el procesamiento del mensaje de **\_ creación de WM** .</span><span class="sxs-lookup"><span data-stu-id="ad455-136">Because many applications use WM\_CREATE to start their initialization process, servers do not respond to the **WM\_GETOBJECT** message until finished processing the **WM\_CREATE** message.</span></span>

<span data-ttu-id="ad455-137">Un servidor utiliza **WM \_ GETOBJECT** para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="ad455-137">A server uses **WM\_GETOBJECT** to perform the following tasks:</span></span>

-   [<span data-ttu-id="ad455-138">Crear nuevos objetos accesibles</span><span class="sxs-lookup"><span data-stu-id="ad455-138">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="ad455-139">Reutilizar punteros existentes a objetos</span><span class="sxs-lookup"><span data-stu-id="ad455-139">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="ad455-140">Crear nuevas interfaces para el mismo objeto</span><span class="sxs-lookup"><span data-stu-id="ad455-140">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

<span data-ttu-id="ad455-141">En el caso de los clientes, esto significa que podrían recibir punteros de interfaz distintos para el mismo elemento de la interfaz de usuario, dependiendo de la acción del servidor.</span><span class="sxs-lookup"><span data-stu-id="ad455-141">For clients, this means that they might receive distinct interface pointers for the same user interface element, depending on the server's action.</span></span> <span data-ttu-id="ad455-142">Para determinar si dos punteros de interfaz apuntan al mismo elemento de la interfaz de usuario, los clientes comparan las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto.</span><span class="sxs-lookup"><span data-stu-id="ad455-142">To determine if two interface pointers point to the same user interface element, clients compare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties of the object.</span></span> <span data-ttu-id="ad455-143">La comparación de punteros no funciona.</span><span class="sxs-lookup"><span data-stu-id="ad455-143">Comparing pointers does not work.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad455-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad455-144">Requirements</span></span>



| <span data-ttu-id="ad455-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad455-145">Requirement</span></span> | <span data-ttu-id="ad455-146">Value</span><span class="sxs-lookup"><span data-stu-id="ad455-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad455-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad455-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ad455-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ad455-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ad455-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad455-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ad455-150">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad455-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad455-151">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ad455-151">Redistributable</span></span><br/>          | <span data-ttu-id="ad455-152">Active Accessibility 1,3 RDK en Windows NT 4,0 con SP6 y versiones posteriores y Windows 95</span><span class="sxs-lookup"><span data-stu-id="ad455-152">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>              |
| <span data-ttu-id="ad455-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad455-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad455-154"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad455-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad455-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad455-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad455-156">Cómo administrar WM \_ GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="ad455-156">How to Handle WM\_GETOBJECT</span></span>](how-to-handle-wm-getobject.md)
</dt> <dt>

[<span data-ttu-id="ad455-157">Cómo \_ funciona WM GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="ad455-157">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
</dt> <dt>

[<span data-ttu-id="ad455-158">**LresultFromObject**</span><span class="sxs-lookup"><span data-stu-id="ad455-158">**LresultFromObject**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

