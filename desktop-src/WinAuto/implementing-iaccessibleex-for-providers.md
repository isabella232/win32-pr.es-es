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
# <a name="implementing-iaccessibleex-for-providers"></a><span data-ttu-id="d447a-103">Implementación de IAccessibleEx para proveedores</span><span class="sxs-lookup"><span data-stu-id="d447a-103">Implementing IAccessibleEx for Providers</span></span>

<span data-ttu-id="d447a-104">En esta sección se explica cómo agregar capacidades del proveedor de automatización de la interfaz de usuario de Microsoft a un servidor de Microsoft Active Accessibility mediante la implementación de la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="d447a-104">This section explains how to add Microsoft UI Automation provider capabilities to a Microsoft Active Accessibility server by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span>

<span data-ttu-id="d447a-105">Antes de implementar [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), tenga en cuenta los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="d447a-105">Before implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), consider the following requirements:</span></span>

-   <span data-ttu-id="d447a-106">La base de referencia de Microsoft Active Accessibility la jerarquía de objetos accesibles debe estar limpia.</span><span class="sxs-lookup"><span data-stu-id="d447a-106">The baseline Microsoft Active Accessibility accessible object hierarchy must be clean.</span></span> <span data-ttu-id="d447a-107">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) no puede corregir problemas con jerarquías de objetos accesibles existentes.</span><span class="sxs-lookup"><span data-stu-id="d447a-107">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) cannot correct problems with existing accessible object hierarchies.</span></span> <span data-ttu-id="d447a-108">Cualquier problema con la estructura del modelo de objetos debe corregirse en la implementación de Microsoft Active Accessibility antes de implementar **IAccessibleEx**.</span><span class="sxs-lookup"><span data-stu-id="d447a-108">Any problems with the object model structure must be corrected in the Microsoft Active Accessibility implementation before implementing **IAccessibleEx**.</span></span>
-   <span data-ttu-id="d447a-109">La implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) debe cumplir la especificación de Microsoft Active Accessibility y la especificación de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d447a-109">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementation must comply with both the Microsoft Active Accessibility specification and the UI Automation specification.</span></span> <span data-ttu-id="d447a-110">Hay herramientas disponibles para validar el cumplimiento en ambas especificaciones.</span><span class="sxs-lookup"><span data-stu-id="d447a-110">Tools are available to validate compliance under both specifications.</span></span> <span data-ttu-id="d447a-111">Para obtener más información, vea [herramientas de prueba](testing-tools.md) y comprobación de [UI Automation (UIA Verify) marco de automatización de pruebas](https://www.codeplex.com/UIAutomationVerify/).</span><span class="sxs-lookup"><span data-stu-id="d447a-111">For more information, see [Testing Tools](testing-tools.md) and [UI Automation Verify (UIA Verify) Test Automation Framework](https://www.codeplex.com/UIAutomationVerify/).</span></span>

<span data-ttu-id="d447a-112">La implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) requiere estos pasos principales:</span><span class="sxs-lookup"><span data-stu-id="d447a-112">Implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) requires these main steps:</span></span>

-   <span data-ttu-id="d447a-113">Implemente **IServiceProvider** en el objeto accesible para que la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) se pueda encontrar en este u otro objeto.</span><span class="sxs-lookup"><span data-stu-id="d447a-113">Implement **IServiceProvider** on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="d447a-114">Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en el objeto accesible.</span><span class="sxs-lookup"><span data-stu-id="d447a-114">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="d447a-115">Cree objetos accesibles para cualquier elemento secundario de Microsoft Active Accessibility, que en Microsoft Active Accessibility se representan mediante la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el objeto primario (por ejemplo, elementos de lista).</span><span class="sxs-lookup"><span data-stu-id="d447a-115">Create accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility are represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="d447a-116">Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en estos objetos.</span><span class="sxs-lookup"><span data-stu-id="d447a-116">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="d447a-117">Implemente [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) en todos los objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="d447a-117">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="d447a-118">Implemente las interfaces de patrón de control adecuadas en los objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="d447a-118">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

### <a name="implementing-the-iserviceprovider-interface"></a><span data-ttu-id="d447a-119">Implementar la interfaz IServiceProvider</span><span class="sxs-lookup"><span data-stu-id="d447a-119">Implementing the IServiceProvider Interface</span></span>

<span data-ttu-id="d447a-120">Dado que la implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para un control puede residir en un objeto independiente, las aplicaciones cliente no pueden basarse en [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="d447a-120">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="d447a-121">En su lugar, se espera que los clientes llamen a **IServiceProvider:: QueryService**.</span><span class="sxs-lookup"><span data-stu-id="d447a-121">Instead, clients are expected to call **IServiceProvider::QueryService**.</span></span> <span data-ttu-id="d447a-122">En la siguiente implementación de ejemplo de este método, se supone que **IAccessibleEx** no se implementa en un objeto independiente; por lo tanto, el método simplemente llama a a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="d447a-122">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


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



### <a name="implementing-the-iaccessibleex-interface"></a><span data-ttu-id="d447a-123">Implementar la interfaz IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="d447a-123">Implementing the IAccessibleEx Interface</span></span>

<span data-ttu-id="d447a-124">En Microsoft Active Accessibility, un elemento de la interfaz de usuario siempre se identifica mediante una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y un identificador secundario.</span><span class="sxs-lookup"><span data-stu-id="d447a-124">In Microsoft Active Accessibility, a UI element is always identified by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and a child ID.</span></span> <span data-ttu-id="d447a-125">Una sola instancia de **IAccessible** puede representar varios elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d447a-125">A single instance of **IAccessible** can represent multiple UI elements.</span></span>

<span data-ttu-id="d447a-126">Dado que cada instancia de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) representa solo un único elemento de la interfaz de usuario, cada [**par de identificador**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de elemento de interfaz de usuario y de identificador secundario debe estar asignado a una única instancia de **IAccessibleEx** .</span><span class="sxs-lookup"><span data-stu-id="d447a-126">Because each [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance represents only a single UI element, each [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair must be mapped to a single **IAccessibleEx** instance.</span></span> <span data-ttu-id="d447a-127">**IAccessibleEx** incluye dos métodos para controlar esta asignación:</span><span class="sxs-lookup"><span data-stu-id="d447a-127">**IAccessibleEx** includes two methods to handle this mapping:</span></span>

-   <span data-ttu-id="d447a-128">[**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild): recupera la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para el elemento secundario especificado.</span><span class="sxs-lookup"><span data-stu-id="d447a-128">[**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)—Retrieves the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface for the specified child.</span></span> <span data-ttu-id="d447a-129">Este método devuelve **null** si la implementación de **IAccessibleEx** no reconoce el identificador secundario especificado, no tiene un **IAccessibleEx** para el elemento secundario especificado o representa un elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="d447a-129">This method returns **NULL** if the **IAccessibleEx** implementation does not recognize the specified child ID, does not have an **IAccessibleEx** for the specified child, or represents a child element.</span></span>
-   <span data-ttu-id="d447a-130">[**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair): recupera la interfaz [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y el identificador secundario para el elemento [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="d447a-130">[**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)—Retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and child ID for the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) element.</span></span> <span data-ttu-id="d447a-131">En el caso de las implementaciones de **IAccessible** que no usan un identificador secundario, este método recupera el objeto **IACCESSIBLE** correspondiente y CHILDID \_ Self.</span><span class="sxs-lookup"><span data-stu-id="d447a-131">For **IAccessible** implementations that do not use a child ID, this method retrieves the corresponding **IAccessible** object and CHILDID\_SELF.</span></span>

<span data-ttu-id="d447a-132">En el ejemplo siguiente se muestra la implementación de los métodos [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) y [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) para un elemento en una vista de lista personalizada.</span><span class="sxs-lookup"><span data-stu-id="d447a-132">The following example shows the implementation of the [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) and [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) methods for an item in a custom list view.</span></span> <span data-ttu-id="d447a-133">Los métodos habilitan la automatización de la interfaz de usuario para asignar el elemento [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y el par ID. secundario a una instancia de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d447a-133">The methods enable UI Automation to map the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair to a corresponding [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance.</span></span>


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



<span data-ttu-id="d447a-134">Si una implementación de objeto accesible no utiliza un identificador secundario, los métodos se pueden implementar tal y como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="d447a-134">If an accessible object implementation does not use a child ID, the methods can still be implemented as shown in the following code snippet.</span></span>


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



### <a name="implement-the-irawelementprovidersimple-interface"></a><span data-ttu-id="d447a-135">Implementar la interfaz IRawElementProviderSimple</span><span class="sxs-lookup"><span data-stu-id="d447a-135">Implement the IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="d447a-136">Los servidores usan [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para exponer información sobre los patrones de control y las propiedades de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d447a-136">Servers use [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) to expose information about UI Automation properties and control patterns.</span></span> <span data-ttu-id="d447a-137">**IRawElementProviderSimple** incluye los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="d447a-137">**IRawElementProviderSimple** includes the following methods:</span></span>

-   <span data-ttu-id="d447a-138">[**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider): este método se usa para exponer las interfaces de patrón de control.</span><span class="sxs-lookup"><span data-stu-id="d447a-138">[**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)—This method is used to expose control pattern interfaces.</span></span> <span data-ttu-id="d447a-139">Devuelve un objeto que admite el patrón de control especificado, o **null** si no se admite el patrón de control.</span><span class="sxs-lookup"><span data-stu-id="d447a-139">It returns an object that supports the specified control pattern, or **NULL** if the control pattern is not supported.</span></span>
-   <span data-ttu-id="d447a-140">[**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue): este método se usa para exponer los valores de propiedad de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d447a-140">[**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)—This method is used to expose UI Automation property values.</span></span>
-   <span data-ttu-id="d447a-141">[**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider): este método no se usa con implementaciones de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="d447a-141">[**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>
-   <span data-ttu-id="d447a-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions): este método no se usa con implementaciones de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="d447a-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>

<span data-ttu-id="d447a-143">Un servidor [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) expone patrones de control mediante la implementación de [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider).</span><span class="sxs-lookup"><span data-stu-id="d447a-143">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server exposes control patterns by implementing [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider).</span></span> <span data-ttu-id="d447a-144">Este método toma un parámetro de entero que especifica el patrón de control.</span><span class="sxs-lookup"><span data-stu-id="d447a-144">This method takes an integer parameter that specifies the control pattern.</span></span> <span data-ttu-id="d447a-145">El servidor devuelve **null** si no se admite el patrón.</span><span class="sxs-lookup"><span data-stu-id="d447a-145">The server returns **NULL** if the pattern is not supported.</span></span> <span data-ttu-id="d447a-146">Si se admite la interfaz de patrón de control, los servidores devuelven [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) y el cliente llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener el patrón de control adecuado.</span><span class="sxs-lookup"><span data-stu-id="d447a-146">If the control pattern interface is supported, servers return an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) and the client then calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the appropriate control pattern.</span></span>

<span data-ttu-id="d447a-147">Un servidor [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) puede admitir las propiedades de automatización de la interfaz de usuario (como LabeledBy y IsRequiredForForm) implementando [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) y proporcionando un entero PROPERTYID que identifica la propiedad como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="d447a-147">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server can support UI Automation properties (such as LabeledBy, and IsRequiredForForm) by implementing [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) and supplying an integer PROPERTYID identifying the property as a parameter.</span></span> <span data-ttu-id="d447a-148">Esta técnica solo se aplica a las propiedades de automatización de la interfaz de usuario que no están incluidas en una interfaz de patrón de control.</span><span class="sxs-lookup"><span data-stu-id="d447a-148">This technique applies only to UI Automation properties that are not included in a control pattern interface.</span></span> <span data-ttu-id="d447a-149">Las propiedades asociadas a una interfaz de patrón de control se exponen mediante el método de interfaz de patrón de control.</span><span class="sxs-lookup"><span data-stu-id="d447a-149">Properties associated with a control pattern interface are exposed through the control pattern interface method.</span></span> <span data-ttu-id="d447a-150">Por ejemplo, la propiedad IsSelected del patrón de control [SelectionItem](uiauto-implementingselectionitem.md) se expondría con [**ISelectionItemProvider:: get \_ IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).</span><span class="sxs-lookup"><span data-stu-id="d447a-150">For example, the IsSelected property from the [SelectionItem](uiauto-implementingselectionitem.md) control pattern would be exposed with [**ISelectionItemProvider::get\_IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).</span></span>

 

 