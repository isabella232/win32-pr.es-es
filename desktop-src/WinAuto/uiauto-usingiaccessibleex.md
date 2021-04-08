---
title: Agregar la funcionalidad de automatización de la interfaz de usuario a los servidores de Active Accessibility
description: Los controles que no tienen un proveedor de automatización de la interfaz de usuario de Microsoft, pero que implementan IAccessible se pueden actualizar fácilmente para proporcionar alguna funcionalidad de automatización de la interfaz de usuario mediante la implementación de la interfaz IAccessibleEx.
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- Automatización de la interfaz de usuario, servidores de Active Accessibility
- Automatización de la interfaz de usuario, servidores de Microsoft Active Accessibility
- Automatización de la interfaz de usuario, IAccessible
- Automatización de la interfaz de usuario, IAccessibleEx
- Automatización de la interfaz de usuario, exponer IAccessibleEx
- Automatización de la interfaz de usuario, implementar IAccessibleEx
- IAccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- exponer IAccessibleEx
- implementación de IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995311"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a><span data-ttu-id="90cdb-115">Agregar la funcionalidad de automatización de la interfaz de usuario a los servidores de Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="90cdb-115">Adding UI Automation Functionality to Active Accessibility Servers</span></span>

<span data-ttu-id="90cdb-116">Los controles que no tienen un proveedor de automatización de la interfaz de usuario de Microsoft, pero que implementan [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) se pueden actualizar fácilmente para proporcionar alguna funcionalidad de automatización de la interfaz de usuario mediante la implementación de la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="90cdb-116">Controls that do not have a Microsoft UI Automation provider but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) can easily be upgraded to provide some UI Automation functionality, by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="90cdb-117">Esta interfaz permite que el control exponga las propiedades y los patrones de control de la automatización de la interfaz de usuario, sin necesidad de una implementación completa de las interfaces del proveedor de automatización de la interfaz de usuario, como [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span><span class="sxs-lookup"><span data-stu-id="90cdb-117">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="90cdb-118">Para implementar **IAccessibleEx**, la jerarquía de objetos de Microsoft Active Accessibility de línea de base no debe contener errores ni incoherencias (como un objeto secundario cuyo objeto primario no lo muestre como elemento secundario) y no debe entrar en conflicto con las especificaciones de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="90cdb-118">To implement **IAccessibleEx**, the baseline Microsoft Active Accessibility object hierarchy must contain no errors or inconsistencies (such as a child object whose parent object does not list it as a child), and must not conflict with UI Automation specifications.</span></span> <span data-ttu-id="90cdb-119">Si la jerarquía de objetos de Microsoft Active Accessibility cumple estos requisitos, es un buen candidato para agregar funcionalidad mediante **IAccessibleEx**; de lo contrario, debe implementar la automatización de la interfaz de usuario solo o junto con la implementación de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="90cdb-119">If the Microsoft Active Accessibility object hierarchy meets these requirements, it is a good candidate for adding functionality by using **IAccessibleEx**; otherwise, you must implement UI Automation alone or alongside the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="90cdb-120">Tome las mayúsculas y minúsculas de un control personalizado que tenga un valor de intervalo.</span><span class="sxs-lookup"><span data-stu-id="90cdb-120">Take the case of a custom control that has a range value.</span></span> <span data-ttu-id="90cdb-121">El servidor de Microsoft Active Accessibility para el control define su función y puede devolver su valor actual, pero carece de los medios para devolver los valores mínimo y máximo del control, ya que estas propiedades no están definidas en Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="90cdb-121">The Microsoft Active Accessibility server for the control defines its role, and is able to return its current value, but lacks the means to return the minimum and maximum values of the control, because these properties are not defined in Microsoft Active Accessibility.</span></span> <span data-ttu-id="90cdb-122">Un cliente de automatización de la interfaz de usuario puede recuperar el rol del control, el valor actual y otras propiedades de Microsoft Active Accessibility, porque el núcleo de automatización de la interfaz de usuario puede obtenerlos a través de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="90cdb-122">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="90cdb-123">Sin embargo, sin acceso a una interfaz [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) en el objeto, la automatización de la interfaz de usuario tampoco puede recuperar los valores máximo y mínimo.</span><span class="sxs-lookup"><span data-stu-id="90cdb-123">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="90cdb-124">El desarrollador del control podría proporcionar un proveedor de automatización de la interfaz de usuario completo para el control, pero esto supondría duplicar gran parte de la funcionalidad existente de la implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : por ejemplo, navegación y propiedades comunes.</span><span class="sxs-lookup"><span data-stu-id="90cdb-124">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="90cdb-125">En su lugar, el desarrollador puede seguir confiando en **IAccessible** para proporcionar esta funcionalidad, al tiempo que agrega compatibilidad para las propiedades específicas del control a través de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span><span class="sxs-lookup"><span data-stu-id="90cdb-125">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

<span data-ttu-id="90cdb-126">La actualización del control personalizado requiere estos pasos principales:</span><span class="sxs-lookup"><span data-stu-id="90cdb-126">Updating the custom control requires these main steps:</span></span>

-   <span data-ttu-id="90cdb-127">Implemente [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) en el objeto accesible para que la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) se pueda encontrar en este u otro objeto.</span><span class="sxs-lookup"><span data-stu-id="90cdb-127">Implement [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="90cdb-128">Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en el objeto accesible.</span><span class="sxs-lookup"><span data-stu-id="90cdb-128">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="90cdb-129">Cree objetos accesibles distintos para cualquier elemento secundario de Microsoft Active Accessibility, que en Microsoft Active Accessibility podría haber sido representado por la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el objeto primario (por ejemplo, elementos de lista).</span><span class="sxs-lookup"><span data-stu-id="90cdb-129">Create distinct accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility might have been represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="90cdb-130">Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en estos objetos.</span><span class="sxs-lookup"><span data-stu-id="90cdb-130">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="90cdb-131">Implemente [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) en todos los objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="90cdb-131">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="90cdb-132">Implemente las interfaces de patrón de control adecuadas en los objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="90cdb-132">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

<span data-ttu-id="90cdb-133">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="90cdb-133">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="90cdb-134">Exponer IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="90cdb-134">Exposing IAccessibleEx</span></span>](#exposing-iaccessibleex)
-   [<span data-ttu-id="90cdb-135">Implementación de IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="90cdb-135">Implementing IAccessibleEx</span></span>](#implementing-iaccessibleex)
-   [<span data-ttu-id="90cdb-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90cdb-136">Related topics</span></span>](#related-topics)

## <a name="exposing-iaccessibleex"></a><span data-ttu-id="90cdb-137">Exponer IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="90cdb-137">Exposing IAccessibleEx</span></span>

<span data-ttu-id="90cdb-138">Dado que la implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para un control puede residir en un objeto independiente, las aplicaciones cliente no pueden basarse en [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="90cdb-138">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="90cdb-139">En su lugar, se espera que los clientes llamen a [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="90cdb-139">Instead, clients are expected to call [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span></span> <span data-ttu-id="90cdb-140">En la siguiente implementación de ejemplo de este método, se supone que **IAccessibleEx** no se implementa en un objeto independiente; por lo tanto, el método simplemente llama a a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="90cdb-140">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
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
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a><span data-ttu-id="90cdb-141">Implementación de IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="90cdb-141">Implementing IAccessibleEx</span></span>

<span data-ttu-id="90cdb-142">El método de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) que es más interesante es [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span><span class="sxs-lookup"><span data-stu-id="90cdb-142">The method of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) that is of most interest is [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span></span> <span data-ttu-id="90cdb-143">Este método proporciona a Microsoft Active Accessibility Server la oportunidad de crear un objeto accesible (uno que exponga, como mínimo, **IAccessibleEx**) para un elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="90cdb-143">This method gives the Microsoft Active Accessibility server an opportunity to create an accessible object (one that exposes, at a minimum, **IAccessibleEx**) for a child item.</span></span> <span data-ttu-id="90cdb-144">En Microsoft Active Accessibility, los elementos secundarios normalmente no se representan como objetos accesibles, sino como elementos secundarios de un objeto accesible.</span><span class="sxs-lookup"><span data-stu-id="90cdb-144">In Microsoft Active Accessibility, child items typically are not represented as accessible objects but as children of an accessible object.</span></span> <span data-ttu-id="90cdb-145">Sin embargo, dado que la automatización de la interfaz de usuario requiere que cada elemento se represente mediante un objeto accesible independiente, **GetObjectForChild** debe crear un objeto independiente para cada secundario a petición.</span><span class="sxs-lookup"><span data-stu-id="90cdb-145">However, because UI Automation requires that each element be represented by a separate accessible object, **GetObjectForChild** must create a separate object for each child on demand.</span></span>

<span data-ttu-id="90cdb-146">En la implementación de ejemplo siguiente se devuelve un objeto accesible para un elemento de una vista de lista personalizada.</span><span class="sxs-lookup"><span data-stu-id="90cdb-146">The following example implementation returns an accessible object for an item in a custom list view.</span></span>


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



<span data-ttu-id="90cdb-147">Para obtener una implementación de ejemplo completa, vea [crear controles personalizados accesibles, parte 5: usar IAccessibleEx para agregar compatibilidad de UI Automation a un control personalizado](/previous-versions/msdn10/cc307850(v=msdn.10)) en MSDN.</span><span class="sxs-lookup"><span data-stu-id="90cdb-147">For a complete sample implementation, see [Making Custom Controls Accessible, Part 5: Using IAccessibleEx to Add UI Automation Support to a Custom Control](/previous-versions/msdn10/cc307850(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90cdb-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90cdb-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90cdb-149">Guía del programador del proveedor de UI Automation</span><span class="sxs-lookup"><span data-stu-id="90cdb-149">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 