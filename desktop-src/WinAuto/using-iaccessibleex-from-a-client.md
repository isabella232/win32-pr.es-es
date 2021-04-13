---
title: Usar IAccessibleEx desde un cliente
description: En este tema se explica cómo los clientes acceden a la implementación de IAccessibleEx de un servidor y cómo usarlos para obtener propiedades de UI Automation y patrones de control para los elementos de la interfaz de usuario.
ms.assetid: e057bbe8-5dd7-41fc-a5d5-bcf4c1c6433d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b14b935bd7ed432ea4d378034763635309213f
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104421607"
---
# <a name="using-iaccessibleex-from-a-client"></a><span data-ttu-id="5a34e-103">Usar IAccessibleEx desde un cliente</span><span class="sxs-lookup"><span data-stu-id="5a34e-103">Using IAccessibleEx from a Client</span></span>

<span data-ttu-id="5a34e-104">En este tema se explica cómo los clientes acceden a la implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) de un servidor y cómo usarlos para obtener propiedades de UI Automation y patrones de control para los elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5a34e-104">This topic explains how clients access the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementation of a server and use it to get UI Automation properties and control patterns for UI elements.</span></span>

<span data-ttu-id="5a34e-105">En los procedimientos y ejemplos de esta sección se supone que hay un cliente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que ya está en curso y un servidor de Microsoft Active Accessibility existente.</span><span class="sxs-lookup"><span data-stu-id="5a34e-105">The procedures and examples in this section assume an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) client that is already in-process, and an existing Microsoft Active Accessibility server.</span></span> <span data-ttu-id="5a34e-106">También suponen que el cliente ya ha obtenido un objeto **IAccessible** mediante una de las funciones del marco de accesibilidad como [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="5a34e-106">They also assume that the client has already obtained an **IAccessible** object by using one of the accessibility framework functions such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a><span data-ttu-id="5a34e-107">Obtener una interfaz IAccessibleEx desde la interfaz IAccessible</span><span class="sxs-lookup"><span data-stu-id="5a34e-107">Obtaining an IAccessibleEx Interface from the IAccessible Interface</span></span>

<span data-ttu-id="5a34e-108">Un cliente que tenga una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para un objeto accesible puede utilizarlo para obtener la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondiente siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="5a34e-108">A client that has an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for an accessible object can use it to obtain the corresponding [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface by following these steps:</span></span>

-   <span data-ttu-id="5a34e-109">Llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original con un IID de \_ \_ uuidof (IServiceProvider).</span><span class="sxs-lookup"><span data-stu-id="5a34e-109">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with an IID of \_\_uuidof(IServiceProvider).</span></span>
-   <span data-ttu-id="5a34e-110">Llame a **IServiceProvider:: QueryService** para obtener [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).</span><span class="sxs-lookup"><span data-stu-id="5a34e-110">Call **IServiceProvider::QueryService** to get the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).</span></span>

### <a name="handling-the-child-id"></a><span data-ttu-id="5a34e-111">Controlar el identificador secundario</span><span class="sxs-lookup"><span data-stu-id="5a34e-111">Handling the Child ID</span></span>

<span data-ttu-id="5a34e-112">Los clientes deben estar preparados para servidores con un identificador secundario distinto de CHILDID \_ Self.</span><span class="sxs-lookup"><span data-stu-id="5a34e-112">Clients must be prepared for servers with a child ID other than CHILDID\_SELF.</span></span> <span data-ttu-id="5a34e-113">Después de obtener una interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) de un [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), los clientes deben llamar a [**IAccessibleEx:: GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) si el identificador secundario no es CHILDID \_ Self (lo que indica un objeto primario).</span><span class="sxs-lookup"><span data-stu-id="5a34e-113">After obtaining an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface from an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), clients must call [**IAccessibleEx::GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) if the child ID is not CHILDID\_SELF (indicating a parent object).</span></span>

<span data-ttu-id="5a34e-114">En el ejemplo siguiente se muestra cómo obtener un [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) determinado y un identificador secundario.</span><span class="sxs-lookup"><span data-stu-id="5a34e-114">The following example shows how to get an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a particular [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span>


```C++
   
HRESULT GetIAccessibleExFromIAccessible(IAccessible * pAcc, long idChild, 
                                           IAccessibleEx ** ppaex)
{
    *ppaex = NULL;

    // First, get IServiceProvider from the IAccessible.
    IServiceProvider * pSp = NULL;
    HRESULT hr = pAcc->QueryInterface(IID_IServiceProvider, (void **) & pSp);
    if(FAILED(hr))
        return hr;
    if(pSp == NULL)
        return E_NOINTERFACE;

    // Next, get the IAccessibleEx for the parent object.
    IAccessibleEx * paex = NULL;
    hr = pSp->QueryService(__uuidof(IAccessibleEx), __uuidof(IAccessibleEx),
                                                                 (void **)&paex);
    pSp->Release();
    if(FAILED(hr))
        return hr;
    if(paex == NULL)
        return E_NOINTERFACE;

    // If this is for CHILDID_SELF, we're done. Otherwise, we have a child ID and 
    // can request the object for child.
    if(idChild == CHILDID_SELF)
    {
        *ppaex = paex;
        return S_OK;
    }
    else
    {
        // Get the IAccessibleEx for the specified child.
        IAccessibleEx * paexChild = NULL;
        hr = paex->GetObjectForChild(idChild, &paexChild);
        paex->Release();
        if(FAILED(hr))
            return hr;
        if(paexChild == NULL)
            return E_NOINTERFACE;
        *ppaex = paexChild;
        return S_OK;
    }
}
```



### <a name="obtaining-the-irawelementprovidersimple-interface"></a><span data-ttu-id="5a34e-115">Obtención de la interfaz IRawElementProviderSimple</span><span class="sxs-lookup"><span data-stu-id="5a34e-115">Obtaining the IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="5a34e-116">Si un cliente tiene una interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , puede utilizar QueryInterface para llegar a la interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) , como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="5a34e-116">If a client has an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, it can use QueryInterface to get to the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface, as the following example shows.</span></span>


```C++
HRESULT GetIRawElementProviderFromIAccessible(IAccessible * pAcc, long idChild,
                                                 IRawElementProviderSimple ** ppEl)
{
    * ppEl = NULL;

    // First, get the IAccessibleEx for the IAccessible and child ID pair.
    IAccessibleEx * paex;
    HRESULT hr = GetIAccessibleExFromIAccessible( pAcc, idChild, &paex );
    if(FAILED(hr))
        return hr;

    // Next, use QueryInterface.
    hr = paex->QueryInterface(__uuidof(IRawElementProviderSimple), (void **)ppEl);
    paex->Release();
    return hr;
}
```



### <a name="retrieving-control-patterns"></a><span data-ttu-id="5a34e-117">Recuperación de patrones de control</span><span class="sxs-lookup"><span data-stu-id="5a34e-117">Retrieving Control Patterns</span></span>

<span data-ttu-id="5a34e-118">Si un cliente tiene acceso a la interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) , puede recuperar interfaces de patrón de control implementadas por los proveedores y, a continuación, llamar a métodos en esas interfaces.</span><span class="sxs-lookup"><span data-stu-id="5a34e-118">If a client has access to the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface, it can retrieve control pattern interfaces that have been implemented by providers, and can then call methods on those interfaces.</span></span> <span data-ttu-id="5a34e-119">El ejemplo siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="5a34e-119">The following example shows how to do this.</span></span>


```C++
// Helper function to get a pattern interface from an IAccessible and child ID 
// pair. Gets the IAccessibleEx, then calls GetPatternObject and QueryInterface.
HRESULT GetPatternFromIAccessible(IAccessible * pAcc, long idChild,
                                     PATTERNID patternId, REFIID iid, void ** ppv)
{
    // First, get the IAccesibleEx for this IAccessible and child ID pair.
    IRawElementProviderSimple * pel;
    HRESULT hr = GetIRawElementProviderSimpleFromIAccessible(pAcc, idChild, &pel);
    if(FAILED(hr))
        return hr;
    if(pel == NULL)
        return E_NOINTERFACE;

    // Now get the pattern object.
    IUnknown * pPatternObject = NULL;
    hr = pel->GetPatternProvider(patternId, &pPatternObject);
    pel->Release();
    if(FAILED(hr))
        return hr;
    if(pPatternObject == NULL)
        return E_NOINTERFACE;

    // Finally, use QueryInterface to get the correct interface type.
    hr = pPatternObject->QueryInterface(iid, ppv);
    pPatternObject->Release();
    if(*ppv == NULL)
        return E_NOINTERFACE;
    return hr;
}

HRESULT CallInvokePatternMethod(IAccessible * pAcc, long idChild)
{
    IInvokeProvider * pPattern;
    HRESULT hr = GetPatternFromIAccessible(pAcc, varChild,
                                  UIA_InvokePatternId, __uuidof(IInvokeProvider),
                                  (void **)&pPattern);
    if(FAILED(hr))
        return hr;

    hr = pPattern->Invoke();
    pPattern->Release();
    return hr;
}
```



### <a name="retrieving-property-values"></a><span data-ttu-id="5a34e-120">Recuperar valores de propiedad</span><span class="sxs-lookup"><span data-stu-id="5a34e-120">Retrieving Property Values</span></span>

<span data-ttu-id="5a34e-121">Si un cliente tiene acceso a [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), puede recuperar los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5a34e-121">If a client has access to [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), it can retrieve property values.</span></span> <span data-ttu-id="5a34e-122">En el ejemplo siguiente se muestra cómo obtener los valores de las propiedades de automatización de la interfaz de usuario de Microsoft AutomationId y LabeledBy.</span><span class="sxs-lookup"><span data-stu-id="5a34e-122">The following example shows how to get values for the AutomationId and LabeledBy Microsoft UI Automation properties.</span></span>


```C++
#include <initguid.h>
#include <uiautomationcoreapi.h> // Includes the UI Automation property GUID definitions.
#include <uiautomationcoreids.h> // Includes definitions of pattern/property IDs.

// Assume we already have a IRawElementProviderSimple * pEl.

VARIANT varValue;

// Get AutomationId property:
varValue.vt = VT_EMPTY;
HRESULT hr = pEl->GetPropertyValue(UIA_AutomationIdPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_BSTR)
    {
        // AutomationId is varValue.bstrVal.
    }
    VariantClear(&varValue);
}


// Get LabeledBy property:
varValue.vt = VT_EMPTY;
hr = pEl->GetPropertyValue(UIA_LabeledByPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_UNKNOWN || varValue.punkVal != NULL)
    {
        // Use QueryInterface to get IRawElementProviderSimple.
        IRawElementProviderSimple * pElLabel = NULL;
        hr = varValue.punkVal->QueryInterface(__uuidof(IRawElementProviderSimple),
                                              (void**)& pElLabel);
        if (SUCCEEDED(hr))
        {
            if(pElLabel != NULL)
            {
            // Use the pElLabel pointer here.
            pElLabel ->Release();
            }
        }
    }
    VariantClear(&varValue);
}
```



<span data-ttu-id="5a34e-123">El ejemplo anterior se aplica a las propiedades que no están asociadas a un patrón de control.</span><span class="sxs-lookup"><span data-stu-id="5a34e-123">The preceding example applies to properties that are not associated with a control pattern.</span></span> <span data-ttu-id="5a34e-124">Para obtener acceso a las propiedades de patrón de control, un cliente debe obtener y usar una interfaz de patrón de control.</span><span class="sxs-lookup"><span data-stu-id="5a34e-124">To access control pattern properties, a client must obtain and use a control pattern interface.</span></span>

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a><span data-ttu-id="5a34e-125">Recuperar una interfaz IAccessible desde una interfaz IRawElementProviderSimple</span><span class="sxs-lookup"><span data-stu-id="5a34e-125">Retrieving an IAccessible Interface from an IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="5a34e-126">Si un cliente obtiene la interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para un elemento de la interfaz de usuario, el cliente puede utilizar esa interfaz para obtener una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) correspondiente para el elemento.</span><span class="sxs-lookup"><span data-stu-id="5a34e-126">If a client obtains the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface for a UI element, the client can use that interface to obtain a corresponding [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="5a34e-127">Esto resulta útil si el cliente necesita tener acceso a las propiedades de Microsoft Active Accessibility para el elemento.</span><span class="sxs-lookup"><span data-stu-id="5a34e-127">This is useful if the client needs to access the Microsoft Active Accessibility properties for the element.</span></span>

<span data-ttu-id="5a34e-128">Un cliente puede obtener la interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) como un valor de propiedad (por ejemplo, llamando a [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) con UIA \_ LabeledByPropertyId) o como un elemento recuperado por un método (por ejemplo, llamando a [**ISelectionProvider:: getSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) para recuperar una matriz de interfaces **IRawElementProviderSimple** de los elementos seleccionados).</span><span class="sxs-lookup"><span data-stu-id="5a34e-128">A client can obtain the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface as a property value (for example, by calling [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) with UIA\_LabeledByPropertyId), or as an item retrieved by a method (for example, by calling [**ISelectionProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) to retrieve an array of **IRawElementProviderSimple** interfaces of selected elements).</span></span> <span data-ttu-id="5a34e-129">Después de obtener la interfaz **IRawElementProviderSimple** , un cliente puede utilizarla para obtener un [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) correspondiente siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="5a34e-129">After obtaining the **IRawElementProviderSimple** interface, a client can use it to obtain a corresponding [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) by following these steps:</span></span>

-   <span data-ttu-id="5a34e-130">Intente usar QueryInterface para obtener la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="5a34e-130">Attempt to use QueryInterface to get the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span>
-   <span data-ttu-id="5a34e-131">Si se produce un error en QueryInterface, llame a [**IAccessibleEx:: ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) en la instancia de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) desde la que se obtuvo originalmente la propiedad.</span><span class="sxs-lookup"><span data-stu-id="5a34e-131">If QueryInterface fails, call [**IAccessibleEx::ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) on the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance from which the property was originally obtained.</span></span>
-   <span data-ttu-id="5a34e-132">Llame al método [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) en la nueva instancia de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para obtener un identificador de elemento de la interfae de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y un identificador secundario.</span><span class="sxs-lookup"><span data-stu-id="5a34e-132">Call the [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) method on the new [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interfae and child ID.</span></span>

<span data-ttu-id="5a34e-133">En el fragmento de código siguiente se muestra cómo obtener la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de una interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) obtenida previamente.</span><span class="sxs-lookup"><span data-stu-id="5a34e-133">The following code snippet demonstrates how to obtain the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface from a previously-obtained [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface.</span></span>


```C++
// IRawElementProviderSimple * pVal - an element returned by a property or method
// from another IRawElementProviderSimple.

IAccessible * pAcc = NULL;
long idChild;

// First, try to use QueryInterface to get the IAccessibleEx interface.
IAccessibleEx * pAccEx;
HRESULT hr = pVal->QueryInterface(__uuidof(IAccessibleEx), (void**)&pAccEx);
if (SUCCEEDED(hr)
{
    if (!pAccEx)
    {
        // If QueryInterface fails, and the IRawElementProviderSimple was 
              // obtained as a property or return value from another 
              // IRawElementProviderSimple, pass it to the 
              // IAccessibleEx::ConvertReturnedValue method of the
        // originating element.

        pAccExOrig->ConvertReturnedElement(pVal, &pAccEx);
    }

    if (pAccEx)
    {
        // Call GetIAccessiblePair to get an IAccessible interface and 
              // child ID.
        pAccEx->GetIAccessiblePair(&pAcc, &idChild);
    }

    // Finally, use the IAccessible interface and child ID.
    if (pAcc)
    {
        // Use IAccessible methods to get further information about this UI
              // element, or pass it to existing code that works in terms of 
              // IAccessible.
        ...
    }
}    
```



 

 