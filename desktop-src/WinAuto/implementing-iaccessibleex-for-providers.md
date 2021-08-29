---
title: Implementación de IAccessibleEx para proveedores
description: En esta sección se explica cómo agregar funcionalidades Automatización de la interfaz de usuario proveedor de Microsoft a un servidor Microsoft Active Accessibility mediante la implementación de la interfaz IAccessibleEx.
ms.assetid: c03dc552-7919-4a35-8ff2-4cdd822bc0b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af83192ed445494a87ecccb1fd579aa49ac099468482ff9feefacf2357293660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098495"
---
# <a name="implementing-iaccessibleex-for-providers"></a>Implementación de IAccessibleEx para proveedores

En esta sección se explica cómo agregar funcionalidades Automatización de la interfaz de usuario proveedor de Microsoft a un servidor Microsoft Active Accessibility mediante la implementación de la [**interfaz IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)

Antes de implementar [**IAccessibleEx,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)tenga en cuenta los siguientes requisitos:

-   La línea Microsoft Active Accessibility jerarquía de objetos accesibles debe estar limpia. [**IAccessibleEx no**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) puede corregir problemas con jerarquías de objetos accesibles existentes. Cualquier problema con la estructura del modelo de objetos debe corregirse en la implementación Microsoft Active Accessibility antes de implementar **IAccessibleEx**.
-   La [**implementación de IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) debe cumplir con la especificación Microsoft Active Accessibility y la Automatización de la interfaz de usuario estándar. Las herramientas están disponibles para validar el cumplimiento según ambas especificaciones. Para obtener más información, vea [Herramientas de pruebas](testing-tools.md) y Automatización de la interfaz de usuario Marco de automatización de pruebas de comprobación [de UIA (UIA Verify).](https://www.codeplex.com/UIAutomationVerify/)

La implementación [**de IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) requiere estos pasos principales:

-   Implemente **IServiceProvider en** el objeto accesible para que la [**interfaz IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) se pueda encontrar en este objeto o en otro.
-   Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en el objeto accesible.
-   Cree objetos accesibles para Microsoft Active Accessibility elementos secundarios, que en Microsoft Active Accessibility se representan mediante la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el objeto primario (por ejemplo, elementos de lista). Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en estos objetos.
-   Implemente [**IRawElementProviderSimple en**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) todos los objetos accesibles.
-   Implemente las interfaces de patrón de control adecuadas en los objetos accesibles.

### <a name="implementing-the-iserviceprovider-interface"></a>Implementación de la interfaz IServiceProvider

Dado que la implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para un control puede residir en un objeto independiente, las aplicaciones cliente no pueden confiar en [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener esta interfaz. En su lugar, se espera que los clientes **llamen a IServiceProvider::QueryService**. En la siguiente implementación de ejemplo de este método, se supone que **IAccessibleEx** no se implementa en un objeto independiente; por lo tanto, el método simplemente llama a **a QueryInterface**.


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



### <a name="implementing-the-iaccessibleex-interface"></a>Implementación de la interfaz IAccessibleEx

En Microsoft Active Accessibility, un elemento de interfaz de usuario siempre se identifica mediante una [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y un identificador secundario. Una única instancia de **IAccessible** puede representar varios elementos de la interfaz de usuario.

Dado que [**cada instancia de IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) representa solo un elemento de interfaz de usuario, cada par de identificadores [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y secundarios debe asignarse a una única **instancia de IAccessibleEx.** **IAccessibleEx incluye** dos métodos para controlar esta asignación:

-   [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild): recupera la [**interfaz IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para el elemento secundario especificado. Este método devuelve **NULL si** la implementación de **IAccessibleEx** no reconoce el identificador secundario especificado, no tiene un **valor IAccessibleEx** para el elemento secundario especificado o representa un elemento secundario.
-   [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair): recupera la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y el identificador secundario del [**elemento IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) En el caso de las implementaciones de **IAccessible** que no usan un identificador secundario, este método recupera el objeto **IAccessible** correspondiente y CHILDID \_ SELF.

En el ejemplo siguiente se muestra la implementación de [**los métodos GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) y [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) para un elemento en una vista de lista personalizada. Los métodos permiten Automatización de la interfaz de usuario asignar el par [**de identificadores IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y secundario a una [**instancia de IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondiente.


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



Si una implementación de objeto accesible no usa un identificador secundario, los métodos todavía se pueden implementar como se muestra en el siguiente fragmento de código.


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



### <a name="implement-the-irawelementprovidersimple-interface"></a>Implementación de la interfaz IRawElementProviderSimple

Los servidores [**usan IRawElementProviderSimple para**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) exponer información sobre Automatización de la interfaz de usuario propiedades y patrones de control. **IRawElementProviderSimple incluye** los métodos siguientes:

-   [**GetPatternProvider :**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)este método se usa para exponer interfaces de patrón de control. Devuelve un objeto que admite el patrón de control especificado o **NULL** si no se admite el patrón de control.
-   [**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue): este método se usa para exponer Automatización de la interfaz de usuario valores de propiedad.
-   [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider): este método no se usa con implementaciones [**de IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)
-   [**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions): este método no se usa con [**implementaciones de IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)

Un [**servidor IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) expone patrones de control mediante la implementación [**de IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider). Este método toma un parámetro entero que especifica el patrón de control. El servidor devuelve **NULL** si no se admite el patrón. Si se admite la interfaz del patrón de control, los servidores [**devuelven un IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) y el cliente llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener el patrón de control adecuado.

Un [**servidor IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) puede admitir propiedades de Automatización de la interfaz de usuario (como LabeledBy e IsRequiredForForm) implementando [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) y suministrando un valor ENTERO PROPERTYID que identifica la propiedad como un parámetro. Esta técnica solo se aplica a Automatización de la interfaz de usuario propiedades que no están incluidas en una interfaz de patrón de control. Las propiedades asociadas a una interfaz de patrón de control se exponen a través del método de interfaz de patrón de control. Por ejemplo, la propiedad IsSelected del patrón de control [SelectionItem](uiauto-implementingselectionitem.md) se exponería con [**ISelectionItemProvider::get \_ IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).

 

 