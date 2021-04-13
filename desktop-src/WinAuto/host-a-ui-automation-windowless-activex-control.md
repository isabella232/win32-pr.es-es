---
title: Hospedar un control ActiveX sin ventanas de automatización de la interfaz de usuario
description: Aprenda a crear un contenedor de controles que puede hospedar controles ActiveX de Microsoft sin ventanas que implementan la automatización de la interfaz de usuario de Microsoft.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- Automatización de la interfaz de usuario, control ActiveX sin ventanas
- Control ActiveX sin ventanas, automatización de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359025"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a><span data-ttu-id="c673d-105">Hospedar un control ActiveX sin ventanas de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="c673d-105">Host a UI Automation Windowless ActiveX Control</span></span>

<span data-ttu-id="c673d-106">Aprenda a crear un contenedor de controles que puede hospedar controles ActiveX de Microsoft sin ventanas que implementan la automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c673d-106">Learn how to create a control container that can host windowless Microsoft ActiveX controls that implement Microsoft UI Automation.</span></span> <span data-ttu-id="c673d-107">Con los pasos que se describen aquí, puede asegurarse de que todos los controles sin ventanas de automatización de la interfaz de usuario que se hospedan en el contenedor de control son accesibles a las aplicaciones cliente de tecnología de asistencia (AT).</span><span class="sxs-lookup"><span data-stu-id="c673d-107">By using the steps described here, you can ensure that any UI Automation windowless controls that are hosted in your control container are accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c673d-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="c673d-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c673d-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="c673d-109">Technologies</span></span>

-   [<span data-ttu-id="c673d-110">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="c673d-110">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="c673d-111">Automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="c673d-111">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="c673d-112">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c673d-112">Prerequisites</span></span>

-   <span data-ttu-id="c673d-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="c673d-113">C/C++</span></span>
-   <span data-ttu-id="c673d-114">Programación de Microsoft Win32 y del modelo de objetos componentes (COM)</span><span class="sxs-lookup"><span data-stu-id="c673d-114">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="c673d-115">Controles ActiveX sin ventanas</span><span class="sxs-lookup"><span data-stu-id="c673d-115">Windowless ActiveX controls</span></span>
-   <span data-ttu-id="c673d-116">Proveedores de UI Automation</span><span class="sxs-lookup"><span data-stu-id="c673d-116">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="c673d-117">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="c673d-117">Instructions</span></span>

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a><span data-ttu-id="c673d-118">Paso 1: proporcionar la interfaz IRawElementProviderSimple en nombre del control sin ventana.</span><span class="sxs-lookup"><span data-stu-id="c673d-118">Step 1: Provide the IRawElementProviderSimple interface on behalf of the windowless control.</span></span>

<span data-ttu-id="c673d-119">Siempre que el sistema necesita el puntero [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para la raíz de un control sin ventana, el sistema consulta el contenedor del control.</span><span class="sxs-lookup"><span data-stu-id="c673d-119">Whenever the system needs the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer for the root of a windowless control, the system queries the control container.</span></span> <span data-ttu-id="c673d-120">Para recuperar el puntero, el contenedor llama a la implementación del control sin ventana del método [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c673d-120">To retrieve the pointer, the container calls the windowless control's implementation of the [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>

<span data-ttu-id="c673d-121">Si el contenedor de control tiene una implementación de automatización de la interfaz de usuario, puede devolver el puntero [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) del control sin ventana al sistema.</span><span class="sxs-lookup"><span data-stu-id="c673d-121">If the control container has a UI Automation implementation, it can return the windowless control's [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer to the system.</span></span>

<span data-ttu-id="c673d-122">Si el contenedor de control tiene una implementación de Microsoft Active Accessibility, llame a la función [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) para obtener un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que represente el control y, a continuación, devuelva el puntero de la interfaz **IAccessible** al sistema.</span><span class="sxs-lookup"><span data-stu-id="c673d-122">If the control container has a Microsoft Active Accessibility implementation, call the [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) function to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer that represents the control, and then return the **IAccessible** interface pointer to the system.</span></span>

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a><span data-ttu-id="c673d-123">Paso 2: implementar la interfaz IRawElementProviderWindowlessSite.</span><span class="sxs-lookup"><span data-stu-id="c673d-123">Step 2: Implement the IRawElementProviderWindowlessSite interface.</span></span>

<span data-ttu-id="c673d-124">Un contenedor de controles implementa la interfaz [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) . habilite un control sin ventanas basado en la automatización de la interfaz de usuario para comunicar su información de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="c673d-124">A control container implements the [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) interface enable a windowless control that is based on UI Automation to communicate its accessibility information.</span></span>

1.  <span data-ttu-id="c673d-125">Implemente [**IRawElementProviderWindowlessSite:: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span><span class="sxs-lookup"><span data-stu-id="c673d-125">Implement [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span></span>

    <span data-ttu-id="c673d-126">Un fragmento de control sin ventana debe crear un identificador de tiempo de ejecución único para sí mismo.</span><span class="sxs-lookup"><span data-stu-id="c673d-126">A windowless control fragment must create a unique runtime ID for itself.</span></span> <span data-ttu-id="c673d-127">Para crear su identificador en tiempo de ejecución, un fragmento de control sin ventanas recupera un valor de prefijo llamando al método [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) del sitio de control y, a continuación, anexa al prefijo un valor entero que es único en relación con todos los demás fragmentos del control sin ventana.</span><span class="sxs-lookup"><span data-stu-id="c673d-127">To create its runtime ID, a windowless control fragment retrieves a prefix value by calling the control site's [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method, and then appends to the prefix an integer value that is unique relative to all other fragments in the windowless control.</span></span>

    <span data-ttu-id="c673d-128">El sitio de control de un control sin ventanas debe implementar el método [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) formando un **SAFEARRAY** que contenga la constante **UiaAppendRuntimeId**, seguido de un valor entero que sea único para el sitio.</span><span class="sxs-lookup"><span data-stu-id="c673d-128">The control site for a windowless control should implement the [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method by forming a **SAFEARRAY** that contains the constant **UiaAppendRuntimeId**, followed by an integer value that is unique to the site.</span></span>

    <span data-ttu-id="c673d-129">En este ejemplo se muestra cómo devolver un prefijo de identificador en tiempo de ejecución para un control sin ventana.</span><span class="sxs-lookup"><span data-stu-id="c673d-129">This example shows how to return a runtime ID prefix for a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  <span data-ttu-id="c673d-130">Implemente el método [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) .</span><span class="sxs-lookup"><span data-stu-id="c673d-130">Implement the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method.</span></span>

    <span data-ttu-id="c673d-131">Un control que implementa la automatización de la interfaz de usuario debe devolver un puntero al proveedor de fragmentos primarios del control.</span><span class="sxs-lookup"><span data-stu-id="c673d-131">A control that implements UI Automation must return a pointer to the control's parent fragment provider.</span></span>

    <span data-ttu-id="c673d-132">Para devolver el elemento primario del fragmento, un objeto que implementa la interfaz [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) debe poder implementar el método [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .</span><span class="sxs-lookup"><span data-stu-id="c673d-132">To return the parent of the fragment, an object that implements the [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) interface must be able to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span> <span data-ttu-id="c673d-133">La implementación de **Navigate** es difícil para un control sin ventana porque es posible que el control no pueda determinar su ubicación en el árbol accesible del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="c673d-133">Implementing **Navigate** is difficult for a windowless control because the control might be unable to determine its location in the accessible tree of the parent object.</span></span> <span data-ttu-id="c673d-134">El método [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) permite al control sin ventana consultar su sitio para el fragmento adyacente y, a continuación, devolver ese fragmento al cliente que llamó a **Navigate**.</span><span class="sxs-lookup"><span data-stu-id="c673d-134">The [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method enables the windowless control to query its site for the adjacent fragment, and then return that fragment to the client that called **Navigate**.</span></span>

    <span data-ttu-id="c673d-135">En este ejemplo se muestra cómo un contenedor de controles recupera el fragmento primario de un control sin ventana.</span><span class="sxs-lookup"><span data-stu-id="c673d-135">This example shows how a control container retrieves the parent fragment of a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a><span data-ttu-id="c673d-136">Paso 3: opcional: implemente la interfaz IRawElementProviderHostingAccessibles.</span><span class="sxs-lookup"><span data-stu-id="c673d-136">Step 3: Optional: Implement the IRawElementProviderHostingAccessibles interface.</span></span>

<span data-ttu-id="c673d-137">Implemente la interfaz [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) si el contenedor de control tiene una implementación del proveedor de automatización de la interfaz de usuario que es la raíz de un árbol de accesibilidad que incluye controles ActiveX sin ventanas que admiten Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="c673d-137">Implement the [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) interface if your control container has a UI Automation provider implementation that is the root of an accessibility tree that includes windowless ActiveX controls that support Microsoft Active Accessibility.</span></span> <span data-ttu-id="c673d-138">La interfaz **IRawElementProviderHostingAccessibles** tiene un único método, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), que recupera los punteros de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de todos los controles ActiveX sin ventanas basados en Microsoft Active Accessibility que se hospedan en el contenedor de controles.</span><span class="sxs-lookup"><span data-stu-id="c673d-138">The **IRawElementProviderHostingAccessibles** interface has a single method, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), which retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers of all Microsoft Active Accessibility-based windowless ActiveX controls that are hosted by your control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c673d-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c673d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c673d-140">Cómo hospedar un control ActiveX sin ventanas de MSAA</span><span class="sxs-lookup"><span data-stu-id="c673d-140">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[<span data-ttu-id="c673d-141">Accesibilidad de controles ActiveX sin ventanas</span><span class="sxs-lookup"><span data-stu-id="c673d-141">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 