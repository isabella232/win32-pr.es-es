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
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a>Agregar la funcionalidad de automatización de la interfaz de usuario a los servidores de Active Accessibility

Los controles que no tienen un proveedor de automatización de la interfaz de usuario de Microsoft, pero que implementan [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) se pueden actualizar fácilmente para proporcionar alguna funcionalidad de automatización de la interfaz de usuario mediante la implementación de la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Esta interfaz permite que el control exponga las propiedades y los patrones de control de la automatización de la interfaz de usuario, sin necesidad de una implementación completa de las interfaces del proveedor de automatización de la interfaz de usuario, como [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Para implementar **IAccessibleEx**, la jerarquía de objetos de Microsoft Active Accessibility de línea de base no debe contener errores ni incoherencias (como un objeto secundario cuyo objeto primario no lo muestre como elemento secundario) y no debe entrar en conflicto con las especificaciones de automatización de la interfaz de usuario. Si la jerarquía de objetos de Microsoft Active Accessibility cumple estos requisitos, es un buen candidato para agregar funcionalidad mediante **IAccessibleEx**; de lo contrario, debe implementar la automatización de la interfaz de usuario solo o junto con la implementación de Microsoft Active Accessibility.

Tome las mayúsculas y minúsculas de un control personalizado que tenga un valor de intervalo. El servidor de Microsoft Active Accessibility para el control define su función y puede devolver su valor actual, pero carece de los medios para devolver los valores mínimo y máximo del control, ya que estas propiedades no están definidas en Microsoft Active Accessibility. Un cliente de automatización de la interfaz de usuario puede recuperar el rol del control, el valor actual y otras propiedades de Microsoft Active Accessibility, porque el núcleo de automatización de la interfaz de usuario puede obtenerlos a través de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Sin embargo, sin acceso a una interfaz [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) en el objeto, la automatización de la interfaz de usuario tampoco puede recuperar los valores máximo y mínimo.

El desarrollador del control podría proporcionar un proveedor de automatización de la interfaz de usuario completo para el control, pero esto supondría duplicar gran parte de la funcionalidad existente de la implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : por ejemplo, navegación y propiedades comunes. En su lugar, el desarrollador puede seguir confiando en **IAccessible** para proporcionar esta funcionalidad, al tiempo que agrega compatibilidad para las propiedades específicas del control a través de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

La actualización del control personalizado requiere estos pasos principales:

-   Implemente [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) en el objeto accesible para que la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) se pueda encontrar en este u otro objeto.
-   Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en el objeto accesible.
-   Cree objetos accesibles distintos para cualquier elemento secundario de Microsoft Active Accessibility, que en Microsoft Active Accessibility podría haber sido representado por la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el objeto primario (por ejemplo, elementos de lista). Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en estos objetos.
-   Implemente [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) en todos los objetos accesibles.
-   Implemente las interfaces de patrón de control adecuadas en los objetos accesibles.

En este tema se incluyen las siguientes secciones.

-   [Exponer IAccessibleEx](#exposing-iaccessibleex)
-   [Implementación de IAccessibleEx](#implementing-iaccessibleex)
-   [Temas relacionados](#related-topics)

## <a name="exposing-iaccessibleex"></a>Exponer IAccessibleEx

Dado que la implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para un control puede residir en un objeto independiente, las aplicaciones cliente no pueden basarse en [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener esta interfaz. En su lugar, se espera que los clientes llamen a [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)). En la siguiente implementación de ejemplo de este método, se supone que **IAccessibleEx** no se implementa en un objeto independiente; por lo tanto, el método simplemente llama a a **QueryInterface**.


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



## <a name="implementing-iaccessibleex"></a>Implementación de IAccessibleEx

El método de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) que es más interesante es [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild). Este método proporciona a Microsoft Active Accessibility Server la oportunidad de crear un objeto accesible (uno que exponga, como mínimo, **IAccessibleEx**) para un elemento secundario. En Microsoft Active Accessibility, los elementos secundarios normalmente no se representan como objetos accesibles, sino como elementos secundarios de un objeto accesible. Sin embargo, dado que la automatización de la interfaz de usuario requiere que cada elemento se represente mediante un objeto accesible independiente, **GetObjectForChild** debe crear un objeto independiente para cada secundario a petición.

En la implementación de ejemplo siguiente se devuelve un objeto accesible para un elemento de una vista de lista personalizada.


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



Para obtener una implementación de ejemplo completa, vea [crear controles personalizados accesibles, parte 5: usar IAccessibleEx para agregar compatibilidad de UI Automation a un control personalizado](/previous-versions/msdn10/cc307850(v=msdn.10)) en MSDN.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía del programador del proveedor de UI Automation](uiauto-providerportal.md)
</dt> </dl>

 

 