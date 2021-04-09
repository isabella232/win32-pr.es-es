---
title: Cómo usar la automatización de la interfaz de usuario para hacer que un control ActiveX sin ventanas sea accesible
description: Describe cómo usar la automatización de la interfaz de usuario de Microsoft \ 32; API para asegurarse de que el control Microsoft ActiveX sin ventanas está accesible para las aplicaciones cliente de tecnología de asistencia (AT).
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- Control ActiveX sin ventanas, accesibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ada1d26463b0654c1808f6e4fd43f571687d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792465"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="3ae03-104">Cómo usar la automatización de la interfaz de usuario para hacer que un control ActiveX sin ventanas sea accesible</span><span class="sxs-lookup"><span data-stu-id="3ae03-104">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>

<span data-ttu-id="3ae03-105">Describe cómo usar la API de automatización de la interfaz de usuario de Microsoft para asegurarse de que el control ActiveX sin ventanas de Microsoft es accesible para las aplicaciones cliente de tecnología de asistencia (AT).</span><span class="sxs-lookup"><span data-stu-id="3ae03-105">Describes how to use the Microsoft UI Automation API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3ae03-106">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="3ae03-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3ae03-107">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="3ae03-107">Technologies</span></span>

-   [<span data-ttu-id="3ae03-108">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="3ae03-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="3ae03-109">Automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="3ae03-109">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="3ae03-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3ae03-110">Prerequisites</span></span>

-   <span data-ttu-id="3ae03-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="3ae03-111">C/C++</span></span>
-   <span data-ttu-id="3ae03-112">Programación de Microsoft Win32 y del modelo de objetos componentes (COM)</span><span class="sxs-lookup"><span data-stu-id="3ae03-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="3ae03-113">Controles ActiveX sin ventanas</span><span class="sxs-lookup"><span data-stu-id="3ae03-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="3ae03-114">Proveedores de UI Automation</span><span class="sxs-lookup"><span data-stu-id="3ae03-114">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="3ae03-115">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="3ae03-115">Instructions</span></span>

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a><span data-ttu-id="3ae03-116">Paso 1: implementar las interfaces del proveedor de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3ae03-116">Step 1: Implement the UI Automation provider interfaces.</span></span>

<span data-ttu-id="3ae03-117">Para que la aplicación sea accesible, debe implementar las interfaces del proveedor de automatización de la interfaz de usuario para el control ActiveX sin ventanas, como [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)y [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span><span class="sxs-lookup"><span data-stu-id="3ae03-117">To make your application accessible, you must implement the UI Automation provider interfaces for your windowless ActiveX control, including [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), and [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span></span> <span data-ttu-id="3ae03-118">Debe implementar estas interfaces del mismo modo que lo haría para un control basado en ventanas, excepto como se describe en los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="3ae03-118">You should implement these interfaces just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="3ae03-119">Para obtener más información sobre la implementación de interfaces de proveedor de UIA, vea [la guía del programador del proveedor de automatización](uiauto-providerportal.md)de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3ae03-119">For more information about implementing UIA provider interfaces, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="3ae03-120">Paso 2: implementar la interfaz IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="3ae03-120">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="3ae03-121">Cuando un cliente necesita información de accesibilidad sobre el control sin ventana, el contenedor de control llama al método **IServiceProvider:: QueryService** del control para recuperar el puntero de la interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para el control.</span><span class="sxs-lookup"><span data-stu-id="3ae03-121">When a client needs accessibility information about your windowless control, the control container calls your control's **IServiceProvider::QueryService** method to retrieve the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface pointer for your control.</span></span>

<span data-ttu-id="3ae03-122">En el ejemplo siguiente se muestra cómo implementar el método **QueryService** .</span><span class="sxs-lookup"><span data-stu-id="3ae03-122">The following example shows how to implement the **QueryService** method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a><span data-ttu-id="3ae03-123">Paso 3: implemente el método IRawElementProviderFragment:: Navigate.</span><span class="sxs-lookup"><span data-stu-id="3ae03-123">Step 3: Implement the IRawElementProviderFragment::Navigate method.</span></span>

<span data-ttu-id="3ae03-124">Cuando se llama al método [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) del control sin ventana para navegar hasta el elemento primario o un elemento relacionado del proveedor raíz del control sin ventana, el método **Navigate** debe delegar al método [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) del contenedor de controles.</span><span class="sxs-lookup"><span data-stu-id="3ae03-124">When your windowless control’s [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method is called to navigate to the parent or a sibling of the windowless control's root provider, your **Navigate** method should delegate to the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method of the control container.</span></span>

<span data-ttu-id="3ae03-125">En el ejemplo siguiente se muestra cómo implementar el método [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .</span><span class="sxs-lookup"><span data-stu-id="3ae03-125">The following example shows how to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a><span data-ttu-id="3ae03-126">Paso 4: implemente el método IRawElementProviderFragment:: GetRuntimeId.</span><span class="sxs-lookup"><span data-stu-id="3ae03-126">Step 4: Implement the IRawElementProviderFragment::GetRuntimeId method.</span></span>

<span data-ttu-id="3ae03-127">Cuando el control sin ventana recibe una llamada a su método [**IRawElementProviderFragment:: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) , el control debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3ae03-127">When your windowless control receives a call to its [**IRawElementProviderFragment::GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) method, the control must do the following:</span></span>

1.  <span data-ttu-id="3ae03-128">Recupere un prefijo de identificador en tiempo de ejecución llamando al método [**IRawElementProviderWindowlessSite:: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) del sitio del control.</span><span class="sxs-lookup"><span data-stu-id="3ae03-128">Retrieve a runtime ID prefix by calling the control site's [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>
2.  <span data-ttu-id="3ae03-129">Cree un identificador de tiempo de ejecución único para el control anexando un entero al prefijo de identificador en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3ae03-129">Create a unique runtime ID for the control by appending an integer to the runtime ID prefix.</span></span>
3.  <span data-ttu-id="3ae03-130">Devuelve el identificador en tiempo de ejecución al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3ae03-130">Return the runtime ID to the caller.</span></span>

<span data-ttu-id="3ae03-131">En el ejemplo siguiente se muestra cómo implementar el método [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) .</span><span class="sxs-lookup"><span data-stu-id="3ae03-131">The following example shows how to implement the [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a><span data-ttu-id="3ae03-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3ae03-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ae03-133">Usar MSAA para hacer que un control ActiveX sin ventanas sea accesible</span><span class="sxs-lookup"><span data-stu-id="3ae03-133">Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="3ae03-134">Accesibilidad de controles ActiveX sin ventanas</span><span class="sxs-lookup"><span data-stu-id="3ae03-134">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 