---
title: Implementación de IAccessibleEx para proveedores
description: En esta sección se explica cómo agregar capacidades del proveedor de automatización de la interfaz de usuario de Microsoft a un servidor de Microsoft Active Accessibility mediante la implementación de la interfaz IAccessibleEx.
ms.assetid: c03dc552-7919-4a35-8ff2-4cdd822bc0b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9460ccbd243aef390b7ade0deb41626173c927a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714390"
---
# <a name="implementing-iaccessibleex-for-providers"></a>Implementación de IAccessibleEx para proveedores

En esta sección se explica cómo agregar capacidades del proveedor de automatización de la interfaz de usuario de Microsoft a un servidor de Microsoft Active Accessibility mediante la implementación de la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Antes de implementar [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), tenga en cuenta los siguientes requisitos:

-   La base de referencia de Microsoft Active Accessibility la jerarquía de objetos accesibles debe estar limpia. [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) no puede corregir problemas con jerarquías de objetos accesibles existentes. Cualquier problema con la estructura del modelo de objetos debe corregirse en la implementación de Microsoft Active Accessibility antes de implementar **IAccessibleEx**.
-   La implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) debe cumplir la especificación de Microsoft Active Accessibility y la especificación de automatización de la interfaz de usuario. Hay herramientas disponibles para validar el cumplimiento en ambas especificaciones. Para obtener más información, vea [herramientas de prueba](testing-tools.md) y comprobación de [UI Automation (UIA Verify) marco de automatización de pruebas](https://www.codeplex.com/UIAutomationVerify/).

La implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) requiere estos pasos principales:

-   Implemente **IServiceProvider** en el objeto accesible para que la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) se pueda encontrar en este u otro objeto.
-   Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en el objeto accesible.
-   Cree objetos accesibles para cualquier elemento secundario de Microsoft Active Accessibility, que en Microsoft Active Accessibility se representan mediante la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el objeto primario (por ejemplo, elementos de lista). Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en estos objetos.
-   Implemente [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) en todos los objetos accesibles.
-   Implemente las interfaces de patrón de control adecuadas en los objetos accesibles.

### <a name="implementing-the-iserviceprovider-interface"></a>Implementar la interfaz IServiceProvider

Dado que la implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para un control puede residir en un objeto independiente, las aplicaciones cliente no pueden basarse en [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener esta interfaz. En su lugar, se espera que los clientes llamen a **IServiceProvider:: QueryService**. En la siguiente implementación de ejemplo de este método, se supone que **IAccessibleEx** no se implementa en un objeto independiente; por lo tanto, el método simplemente llama a a **QueryInterface**.


```C++
           
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_NOINTERFACE;
    }
};      
```



### <a name="implementing-the-iaccessibleex-interface"></a>Implementar la interfaz IAccessibleEx

En Microsoft Active Accessibility, un elemento de la interfaz de usuario siempre se identifica mediante una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y un identificador secundario. Una sola instancia de **IAccessible** puede representar varios elementos de la interfaz de usuario.

Dado que cada instancia de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) representa solo un único elemento de la interfaz de usuario, cada [**par de identificador**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de elemento de interfaz de usuario y de identificador secundario debe estar asignado a una única instancia de **IAccessibleEx** . **IAccessibleEx** incluye dos métodos para controlar esta asignación:

-   [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild): recupera la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para el elemento secundario especificado. Este método devuelve **null** si la implementación de **IAccessibleEx** no reconoce el identificador secundario especificado, no tiene un **IAccessibleEx** para el elemento secundario especificado o representa un elemento secundario.
-   [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair): recupera la interfaz [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y el identificador secundario para el elemento [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . En el caso de las implementaciones de **IAccessible** que no usan un identificador secundario, este método recupera el objeto **IACCESSIBLE** correspondiente y CHILDID \_ Self.

En el ejemplo siguiente se muestra la implementación de los métodos [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) y [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) para un elemento en una vista de lista personalizada. Los métodos habilitan la automatización de la interfaz de usuario para asignar el elemento [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y el par ID. secundario a una instancia de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondiente.


```C++
           
HRESULT CListboxAccessibleObject::GetObjectForChild(
    long idChild, IAccessibleEx **ppRetVal)
{ 
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;
    HRESULT hr = ValidateChildId(vChild);
    if (FAILED(hr))
    {
        return E_INVALIDARG;
    }
    // List item accessible objects are stored as an array of
    // pointers; for the purpose of this example it is assumed that 
    // the list contents will not change. Accessible objects are
    // created only when needed.
    if (itemProviders[idChild - 1] == NULL)
    {
        // Create an object that supports UI Automation and
        // IAccessibleEx for the item.
        itemProviders[idChild - 1] = 
          new CListItemAccessibleObject(idChild, 
          g_pListboxControl);
        if (itemProviders[idChild - 1] == NULL)
        {
            return E_OUTOFMEMORY;
        }
    }
    IAccessibleEx* pAccEx = static_cast<IAccessibleEx*>
      (itemProviders[idChild - 1]);
    if (pAccEx != NULL)
    {
      pAccEx->AddRef();
    }
    *ppRetVal = pAccEx;
    return S_OK; 
}

HRESULT CListItemAccessibleObject::GetIAccessiblePair(
    IAccessible **ppAcc, long *pidChild)
{ 
    if (ppAcc == NULL || pidChild == NULL)
    {
        return E_INVALIDARG;   
    }

                CListboxAccessibleObject* pParent = 
        m_control->GetAccessibleObject();

    HRESULT hr = pParent->QueryInterface( 
        __uuidof(IAccessible), (void**)ppAcc);
    if (FAILED(hr))
    {
        *pidChild = 0;
        return E_NOINTERFACE;
    }
    *pidChild = m_childID; 
    return S_OK; 
}
}
```



Si una implementación de objeto accesible no utiliza un identificador secundario, los métodos se pueden implementar tal y como se muestra en el siguiente fragmento de código.


```C++
           

    // This sample implements IAccessibleEx on the same object; it could use a tear-off
    // or inner object instead.
    class MyAccessibleImpl: public IAccessible,
                        public IAccessibleEx,
                        public IRawElementProviderSimple
    {
    public:
    ...
   HRESULT STDMETHODCALLTYPE GetObjectForChild( long idChild, IAccessibleEx **ppRetVal )
    {
        // This implementation does not support child IDs.
        *ppRetVal = NULL;
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE GetIAccessiblePair( IAccessible ** ppAcc, long * pidChild )
    {
        // This implementation assumes that IAccessibleEx is implemented on same object as
        // IAccessible.
        *ppAcc = static_cast<IAccessible *>(this);
        (*ppAcc)->AddRef();
        *pidChild = CHILDID_SELF;
        return S_OK;
    }
```



### <a name="implement-the-irawelementprovidersimple-interface"></a>Implementar la interfaz IRawElementProviderSimple

Los servidores usan [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para exponer información sobre los patrones de control y las propiedades de automatización de la interfaz de usuario. **IRawElementProviderSimple** incluye los siguientes métodos:

-   [**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider): este método se usa para exponer las interfaces de patrón de control. Devuelve un objeto que admite el patrón de control especificado, o **null** si no se admite el patrón de control.
-   [**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue): este método se usa para exponer los valores de propiedad de automatización de la interfaz de usuario.
-   [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider): este método no se usa con implementaciones de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .
-   [**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions): este método no se usa con implementaciones de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Un servidor [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) expone patrones de control mediante la implementación de [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider). Este método toma un parámetro de entero que especifica el patrón de control. El servidor devuelve **null** si no se admite el patrón. Si se admite la interfaz de patrón de control, los servidores devuelven [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) y el cliente llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener el patrón de control adecuado.

Un servidor [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) puede admitir las propiedades de automatización de la interfaz de usuario (como LabeledBy y IsRequiredForForm) implementando [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) y proporcionando un entero PROPERTYID que identifica la propiedad como un parámetro. Esta técnica solo se aplica a las propiedades de automatización de la interfaz de usuario que no están incluidas en una interfaz de patrón de control. Las propiedades asociadas a una interfaz de patrón de control se exponen mediante el método de interfaz de patrón de control. Por ejemplo, la propiedad IsSelected del patrón de control [SelectionItem](uiauto-implementingselectionitem.md) se expondría con [**ISelectionItemProvider:: get \_ IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).

 

 