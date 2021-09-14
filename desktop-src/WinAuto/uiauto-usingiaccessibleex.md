---
title: Agregar Automatización de la interfaz de usuario funcionalidad a Active Accessibility Server
description: Los controles que no tienen un proveedor de Microsoft Automatización de la interfaz de usuario pero que implementan IAccessible se pueden actualizar fácilmente para proporcionar alguna funcionalidad Automatización de la interfaz de usuario, mediante la implementación de la interfaz IAccessibleEx.
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- Automatización de la interfaz de usuario,Active Accessibility servidores
- Automatización de la interfaz de usuario,Microsoft Active Accessibility servidores
- Automatización de la interfaz de usuario,IAccessible
- Automatización de la interfaz de usuario,IAccessibleEx
- Automatización de la interfaz de usuario, exponer IAccessibleEx
- Automatización de la interfaz de usuario, implementar IAccessibleEx
- IAccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- exponer IAccessibleEx
- implementar IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359225"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a>Agregar Automatización de la interfaz de usuario funcionalidad a Active Accessibility Server

Los controles que no tienen un proveedor de Microsoft Automatización de la interfaz de usuario pero que implementan [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) se pueden actualizar fácilmente para proporcionar alguna funcionalidad Automatización de la interfaz de usuario, mediante la implementación de la [**interfaz IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) Esta interfaz permite al control exponer Automatización de la interfaz de usuario propiedades y patrones de control, sin necesidad de una implementación completa de interfaces de proveedor de Automatización de la interfaz de usuario como [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Para implementar **IAccessibleEx**, la jerarquía de objetos Microsoft Active Accessibility de línea de base no debe contener errores ni incoherencias (por ejemplo, un objeto secundario cuyo objeto primario no lo muestra como secundario) y no debe estar en conflicto con las especificaciones Automatización de la interfaz de usuario. Si la Microsoft Active Accessibility de objetos cumple estos requisitos, es un buen candidato para agregar funcionalidad mediante **IAccessibleEx**; De lo contrario, debe implementar Automatización de la interfaz de usuario solo o junto con la Microsoft Active Accessibility implementación.

Tome el caso de un control personalizado que tenga un valor de intervalo. El servidor Microsoft Active Accessibility para el control define su rol y es capaz de devolver su valor actual, pero carece de los medios para devolver los valores mínimo y máximo del control, ya que estas propiedades no están definidas en Microsoft Active Accessibility. Un Automatización de la interfaz de usuario cliente puede recuperar el rol del control, el valor actual y otras propiedades Microsoft Active Accessibility, ya que el núcleo Automatización de la interfaz de usuario puede obtenerlos a través de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Sin embargo, sin acceso a una [**interfaz IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) en el objeto , Automatización de la interfaz de usuario tampoco puede recuperar los valores máximo y mínimo.

El desarrollador del control podría proporcionar un proveedor de Automatización de la interfaz de usuario completo para el control, pero esto significaría duplicar gran parte de la funcionalidad existente de la implementación [**de IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) por ejemplo, la navegación y las propiedades comunes. En su lugar, el desarrollador puede seguir dependiendo de **IAccessible** para proporcionar esta funcionalidad, al tiempo que agrega compatibilidad con propiedades específicas del control a través [**de IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

La actualización del control personalizado requiere estos pasos principales:

-   Implemente [IServiceProvider en](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) el objeto accesible para que la [**interfaz IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) se pueda encontrar en este objeto o en otro.
-   Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en el objeto accesible.
-   Cree distintos objetos accesibles para cualquier elemento secundario de Microsoft Active Accessibility, que en Microsoft Active Accessibility podría haber sido representado por la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el objeto primario (por ejemplo, elementos de lista). Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) en estos objetos.
-   Implemente [**IRawElementProviderSimple en**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) todos los objetos accesibles.
-   Implemente las interfaces de patrón de control adecuadas en los objetos accesibles.

En este tema se incluyen las siguientes secciones.

-   [Exposición de IAccessibleEx](#exposing-iaccessibleex)
-   [Implementación de IAccessibleEx](#implementing-iaccessibleex)
-   [Temas relacionados](#related-topics)

## <a name="exposing-iaccessibleex"></a>Exposición de IAccessibleEx

Dado que la implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para un control puede residir en un objeto independiente, las aplicaciones cliente no pueden confiar en [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener esta interfaz. En su lugar, se espera que los clientes [**llamen a IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)). En la siguiente implementación de ejemplo de este método, se supone que **IAccessibleEx** no se implementa en un objeto independiente; por lo tanto, el método simplemente llama a **a QueryInterface**.


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

El método de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) que es de mayor interés [**es GetObjectForChild.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) Este método ofrece al servidor Microsoft Active Accessibility una oportunidad de crear un objeto accesible (uno que expone, como mínimo, **IAccessibleEx**) para un elemento secundario. En Microsoft Active Accessibility, los elementos secundarios normalmente no se representan como objetos accesibles, sino como elementos secundarios de un objeto accesible. Sin embargo, dado Automatización de la interfaz de usuario que cada elemento se represente mediante un objeto accesible independiente, **GetObjectForChild** debe crear un objeto independiente para cada elemento secundario a petición.

La siguiente implementación de ejemplo devuelve un objeto accesible para un elemento en una vista de lista personalizada.


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



Para obtener una implementación de ejemplo completa, vea [Making Custom Controls Accessible, Part 5: Using IAccessibleEx to Add Automatización de la interfaz de usuario Support to a Custom Control](/previous-versions/msdn10/cc307850(v=msdn.10)) on MSDN (Hacer accesibles los controles personalizados, Parte 5: Usar IAccessibleEx para agregar compatibilidad con Automatización de la interfaz de usuario a un control personalizado en MSDN).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatización de la interfaz de usuario del programador del proveedor de aplicaciones](uiauto-providerportal.md)
</dt> </dl>

 

 