---
title: Uso de IAccessibleEx desde un cliente
description: En este tema se explica cómo los clientes acceden a la implementación de IAccessibleEx de un servidor y la usan para obtener Automatización de la interfaz de usuario propiedades y patrones de control para los elementos de la interfaz de usuario.
ms.assetid: e057bbe8-5dd7-41fc-a5d5-bcf4c1c6433d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b14b935bd7ed432ea4d378034763635309213f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466621"
---
# <a name="using-iaccessibleex-from-a-client"></a>Uso de IAccessibleEx desde un cliente

En este tema se explica cómo los clientes acceden a la implementación [**de IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) de un servidor y la usan para obtener Automatización de la interfaz de usuario propiedades y patrones de control para los elementos de la interfaz de usuario.

En los procedimientos y ejemplos de esta sección se supone que hay un cliente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que ya está en proceso y un servidor Microsoft Active Accessibility existente. También suponen que el cliente ya ha obtenido un objeto **IAccessible** mediante una de las funciones del marco de accesibilidad, como [**AccessibleObjectFromEvent,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a>Obtención de una interfaz IAccessibleEx desde la interfaz IAccessible

Un cliente que tenga una [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para un objeto accesible puede usarla para obtener la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondiente siguiendo estos pasos:

-   Llame [**a QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el [**objeto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original con un IID de \_ \_ uuidof(IServiceProvider).
-   Llame **a IServiceProvider::QueryService** para obtener [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).

### <a name="handling-the-child-id"></a>Control del identificador secundario

Los clientes deben estar preparados para servidores con un identificador secundario distinto de CHILDID \_ SELF. Después de obtener una [**interfaz IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) de [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)los clientes deben llamar a [**IAccessibleEx::GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) si el identificador secundario no es CHILDID SELF (lo que indica un \_ objeto primario).

En el ejemplo siguiente se muestra cómo obtener [**una IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) determinado y un identificador secundario.


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



### <a name="obtaining-the-irawelementprovidersimple-interface"></a>Obtención de la interfaz IRawElementProviderSimple

Si un cliente tiene una [**interfaz IAccessibleEx,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) puede usar QueryInterface para llegar a la [**interfaz IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) como se muestra en el ejemplo siguiente.


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



### <a name="retrieving-control-patterns"></a>Recuperar patrones de control

Si un cliente tiene acceso a la interfaz [**IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) puede recuperar interfaces de patrón de control implementadas por proveedores y, a continuación, llamar a métodos en esas interfaces. El ejemplo siguiente muestra cómo hacerlo.


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



### <a name="retrieving-property-values"></a>Recuperar valores de propiedad

Si un cliente tiene acceso a [**IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)puede recuperar valores de propiedad. En el ejemplo siguiente se muestra cómo obtener valores para las propiedades AutomationId y LabeledBy Automatización de la interfaz de usuario Microsoft.


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



El ejemplo anterior se aplica a las propiedades que no están asociadas a un patrón de control. Para acceder a las propiedades del patrón de control, un cliente debe obtener y usar una interfaz de patrón de control.

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a>Recuperar una interfaz IAccessible desde una interfaz IRawElementProviderSimple

Si un cliente obtiene la interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para un elemento de interfaz de usuario, el cliente puede usar esa interfaz para obtener una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) correspondiente para el elemento. Esto resulta útil si el cliente necesita tener acceso al Microsoft Active Accessibility propiedades del elemento.

Un cliente puede obtener la interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) como un valor de propiedad (por ejemplo, llamando a [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) con UIA LabeledByPropertyId) o como un elemento recuperado por un método \_ (por ejemplo, llamando a [**ISelectionProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) para recuperar una matriz de interfaces **IRawElementProviderSimple** de elementos seleccionados). Después de obtener la **interfaz IRawElementProviderSimple,** un cliente puede usarla para obtener un [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) correspondiente siguiendo estos pasos:

-   Intente usar QueryInterface para obtener la [**interfaz IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)
-   Si se produce un error en QueryInterface, llame a [**IAccessibleEx::ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) en la [**instancia de IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) de la que se obtuvo originalmente la propiedad.
-   Llame al [**método GetIAccessiblePair en**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) la nueva instancia [**de IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para obtener un identificador secundario e interfae [**de IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

El siguiente fragmento de código muestra cómo obtener la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de una interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) obtenida previamente.


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



 

 