---
title: Usar MSAA para hacer que un control ActiveX sin ventanas sea accesible
description: Describe cómo usar Microsoft Active Accessibility \ 32; API para asegurarse de que el control Microsoft ActiveX sin ventanas está accesible para las aplicaciones cliente de tecnología de asistencia (AT).
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- Control ActiveX, accesibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704997"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="7bc13-104">Usar MSAA para hacer que un control ActiveX sin ventanas sea accesible</span><span class="sxs-lookup"><span data-stu-id="7bc13-104">Use MSAA to make a windowless ActiveX control accessible</span></span>

<span data-ttu-id="7bc13-105">Describe cómo usar la API de Microsoft Active Accessibility para asegurarse de que el control ActiveX sin ventanas de Microsoft es accesible para las aplicaciones cliente de tecnología de asistencia (AT).</span><span class="sxs-lookup"><span data-stu-id="7bc13-105">Describes how to use the Microsoft Active Accessibility API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7bc13-106">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="7bc13-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7bc13-107">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="7bc13-107">Technologies</span></span>

-   [<span data-ttu-id="7bc13-108">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="7bc13-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="7bc13-109">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="7bc13-109">Microsoft Active Accessibility</span></span>](microsoft-active-accessibility.md)

### <a name="prerequisites"></a><span data-ttu-id="7bc13-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7bc13-110">Prerequisites</span></span>

-   <span data-ttu-id="7bc13-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="7bc13-111">C/C++</span></span>
-   <span data-ttu-id="7bc13-112">Programación de Microsoft Win32 y del modelo de objetos componentes (COM)</span><span class="sxs-lookup"><span data-stu-id="7bc13-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="7bc13-113">Controles ActiveX sin ventanas</span><span class="sxs-lookup"><span data-stu-id="7bc13-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="7bc13-114">Servidores de Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="7bc13-114">Microsoft Active Accessibility servers</span></span>

## <a name="instructions"></a><span data-ttu-id="7bc13-115">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="7bc13-115">Instructions</span></span>

### <a name="step-1-implement-the-iaccessible-interface"></a><span data-ttu-id="7bc13-116">Paso 1: implementar la interfaz IAccessible.</span><span class="sxs-lookup"><span data-stu-id="7bc13-116">Step 1: Implement the IAccessible interface.</span></span>

<span data-ttu-id="7bc13-117">Para que el control ActiveX sin ventanas sea accesible, debe implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de Microsoft Active Accessibility, del mismo modo que lo haría para un control basado en ventanas, excepto como se describe en los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="7bc13-117">To make your windowless ActiveX control accessible, you must implement the Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface, just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="7bc13-118">Para obtener más información sobre cómo implementar **IAccessible**, consulte [la guía del desarrollador para Active Accessibility servidores](developer-s-guide-for-active-accessibility-servers.md).</span><span class="sxs-lookup"><span data-stu-id="7bc13-118">For more information about implementing **IAccessible**, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="7bc13-119">Paso 2: implementar la interfaz IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="7bc13-119">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="7bc13-120">Cuando un cliente solicita información de accesibilidad sobre el control sin ventana, el contenedor llama al método [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) del control para recuperar el puntero de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="7bc13-120">When a client requests accessibility information about your windowless control, the container calls your control's [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method to retrieve the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="7bc13-121">En este ejemplo se muestra cómo implementar el método [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7bc13-121">This example shows how to implement the [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a><span data-ttu-id="7bc13-122">Paso 3: delegue las llamadas al método IAccessible:: get \_ accParent en el método IAccessibleWindowlessSite:: GetParentAccessible del sitio de control.</span><span class="sxs-lookup"><span data-stu-id="7bc13-122">Step 3: Delegate IAccessible::get\_accParent method calls to the control site's IAccessibleWindowlessSite::GetParentAccessible method.</span></span>

<span data-ttu-id="7bc13-123">Cuando un cliente solicita el objeto primario del control sin ventana, el contenedor llama al método [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) del control.</span><span class="sxs-lookup"><span data-stu-id="7bc13-123">When a client requests the parent object of your windowless control, the container calls your control's [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span> <span data-ttu-id="7bc13-124">La implementación **Get \_ accParent** debe delegar al método [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) del contenedor.</span><span class="sxs-lookup"><span data-stu-id="7bc13-124">Your **get\_accParent** implementation should delegate to the [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) method of the container.</span></span>

<span data-ttu-id="7bc13-125">Este ejemplo muestra cómo implementar el método [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) .</span><span class="sxs-lookup"><span data-stu-id="7bc13-125">This example shows how to implement the [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span>


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a><span data-ttu-id="7bc13-126">Paso 4: adquirir un intervalo de identificadores de objeto para asignar a los orígenes de eventos en el control sin ventana.</span><span class="sxs-lookup"><span data-stu-id="7bc13-126">Step 4: Acquire a range of object IDs to assign to the event sources in your windowless control.</span></span>

<span data-ttu-id="7bc13-127">Al igual que los controles basados en ventanas, un control ActiveX sin ventanas llama a la función [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para notificar a los clientes de eventos importantes.</span><span class="sxs-lookup"><span data-stu-id="7bc13-127">Like window-based controls, a windowless ActiveX control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function to notify clients of important events.</span></span> <span data-ttu-id="7bc13-128">Los parámetros de función incluyen el ID. de objeto del elemento que está generando el evento.</span><span class="sxs-lookup"><span data-stu-id="7bc13-128">The function parameters include the object ID of the item that is raising the event.</span></span> <span data-ttu-id="7bc13-129">El control sin ventana debe asignar identificadores de objeto mediante un valor de un intervalo adquirido llamando al método [**IAccessibleWindowlessSite:: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) del sitio de control.</span><span class="sxs-lookup"><span data-stu-id="7bc13-129">Your windowless control must assign object IDs by using a value from a range acquired by calling the control site’s [**IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) method.</span></span>

<span data-ttu-id="7bc13-130">En este ejemplo se muestra cómo adquirir un intervalo de valores de ID. de objeto del contenedor de control.</span><span class="sxs-lookup"><span data-stu-id="7bc13-130">This example shows how to acquire a range of object ID values from the control container.</span></span>


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a><span data-ttu-id="7bc13-131">Paso 5: implementar la interfaz IAccessibleHandler.</span><span class="sxs-lookup"><span data-stu-id="7bc13-131">Step 5: Implement the IAccessibleHandler interface.</span></span>

<span data-ttu-id="7bc13-132">Cuando un control sin ventana llama a la función [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , el control especifica el identificador de objeto del elemento de la interfaz de usuario que está generando el evento y especifica el contenedor de control como la ventana que responderá a los mensajes de [**WM \_ GETOBJECT**](wm-getobject.md) en nombre del control.</span><span class="sxs-lookup"><span data-stu-id="7bc13-132">When a windowless control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function, the control specifies the object ID of the UI item that is raising the event, and specifies the control container as the window that will respond to [**WM\_GETOBJECT**](wm-getobject.md) messages on behalf of the control.</span></span>

<span data-ttu-id="7bc13-133">Si una aplicación cliente responde al evento, el contenedor de control recibe un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) que incluye el identificador de objeto del elemento de la interfaz de usuario que ha generado el evento.</span><span class="sxs-lookup"><span data-stu-id="7bc13-133">If a client application responds to the event, the control container receives a [**WM\_GETOBJECT**](wm-getobject.md) message that includes the object ID of the UI item that raised the event.</span></span> <span data-ttu-id="7bc13-134">El contenedor de control responde buscando el control sin ventanas que "posee" el identificador de objeto y, a continuación, llamando al método [**IAccessibleHandler:: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) de ese control.</span><span class="sxs-lookup"><span data-stu-id="7bc13-134">The control container responds by looking up the windowless control that "owns" the object ID, and then calling that control's [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) method.</span></span> <span data-ttu-id="7bc13-135">El método **AccessibleObjectFromID** devuelve el puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento de interfaz de usuario y el contenedor de control reenvía el puntero a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="7bc13-135">The **AccessibleObjectFromID** method returns the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the UI item, and the control container forwards the pointer to the client application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bc13-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bc13-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bc13-137">Usar la automatización de la interfaz de usuario para hacer que un control ActiveX sin ventanas sea accesible</span><span class="sxs-lookup"><span data-stu-id="7bc13-137">Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="7bc13-138">Accesibilidad de controles ActiveX sin ventanas</span><span class="sxs-lookup"><span data-stu-id="7bc13-138">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 