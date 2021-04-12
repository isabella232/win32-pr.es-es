---
title: Patrones de control compatibles en un proveedor de UI Automation
description: En este tema se muestra cómo un proveedor de automatización de la interfaz de usuario de Microsoft implementa patrones de control para un control. Los patrones de control permiten a las aplicaciones cliente manipular el control y obtener información sobre él.
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54e75fa12dba891bc4eded5fd9763f7825eb7f88
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104358453"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a><span data-ttu-id="ef1c6-104">Patrones de control compatibles en un proveedor de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ef1c6-104">Support Control Patterns in a UI Automation Provider</span></span>

<span data-ttu-id="ef1c6-105">En este tema se muestra cómo un proveedor de automatización de la interfaz de usuario de Microsoft implementa patrones de control para un control.</span><span class="sxs-lookup"><span data-stu-id="ef1c6-105">This topic shows how a Microsoft UI Automation provider implements control patterns for a control.</span></span> <span data-ttu-id="ef1c6-106">Los patrones de control permiten a las aplicaciones cliente manipular el control y obtener información sobre él.</span><span class="sxs-lookup"><span data-stu-id="ef1c6-106">Control patterns enable client applications to manipulate the control and get information about it.</span></span>

<span data-ttu-id="ef1c6-107">Un proveedor implementa un patrón de control siguiendo estos pasos principales:</span><span class="sxs-lookup"><span data-stu-id="ef1c6-107">A provider implements a control pattern by following these main steps:</span></span>

1.  <span data-ttu-id="ef1c6-108">Implemente la interfaz de proveedor que admite el patrón de control.</span><span class="sxs-lookup"><span data-stu-id="ef1c6-108">Implement the provider interface that supports the control pattern.</span></span> <span data-ttu-id="ef1c6-109">Por ejemplo, para admitir el patrón de control [Selection](uiauto-implementingselection.md) , un proveedor para un control de lista personalizado implementaría la interfaz [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .</span><span class="sxs-lookup"><span data-stu-id="ef1c6-109">For example, to support the [Selection](uiauto-implementingselection.md) control pattern, a provider for a custom list control would implement the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>
2.  <span data-ttu-id="ef1c6-110">Devuelve un objeto que contiene la interfaz del proveedor del patrón de control cuando la automatización de la interfaz de usuario llama al método [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ef1c6-110">Return an object that contains the control pattern provider interface when UI Automation calls the provider's [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) method.</span></span>

<span data-ttu-id="ef1c6-111">En el ejemplo siguiente se muestra la implementación de la interfaz [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) para un control de lista de selección única personalizado.</span><span class="sxs-lookup"><span data-stu-id="ef1c6-111">The following example shows the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface implementation for a custom, single-selection list control.</span></span> <span data-ttu-id="ef1c6-112">La implementación incluye métodos de recuperación de propiedades para las propiedades IsSelectionRequired y CanSelectMultiple, y un método para recuperar el proveedor para el elemento de lista seleccionado.</span><span class="sxs-lookup"><span data-stu-id="ef1c6-112">The implementation includes property-retrieval methods for the IsSelectionRequired and CanSelectMultiple properties, and a method for retrieving the provider for the selected list item.</span></span>


```C++
// Specifies whether the list control supports the selection of
// multiple items at the same time.
IFACEMETHODIMP ListProvider::get_CanSelectMultiple(BOOL *pRetVal)
{
    *pRetVal = FALSE;
    return S_OK;
} 

// Specifies whether the list must have an item selected at all times.
IFACEMETHODIMP ListProvider::get_IsSelectionRequired(BOOL *pRetVal)
{
   *pRetVal = TRUE;
   return S_OK;
}

// Retrieves the provider of the selected item in a custom list control. 
//
// m_pControl - pointer to an application-defined object for managing
//   the custom list control. 
//
// ListItemProvider - application-defined class that inherits the 
//   IRawElementProviderSimple interface.
//
// GetItemProviderByIndex - application-defined method that retrieves the 
//   IRawElementProviderSimple interface of the selected item.
IFACEMETHODIMP ListProvider::GetSelection(SAFEARRAY** pRetVal)
{
    // Create a safe array to store the IRawElementProviderSimple pointer.
    SAFEARRAY *psa = SafeArrayCreateVector(VT_UNKNOWN, 0, 1);

    // Retrieve the index of the selected list item. 
    int index = m_pControl->GetSelectedIndex(); 

    // Retrieve the IRawElementProviderSimple pointer of the selected list
    // item. ListItemProvider is an application-defined class that 
    // inherits the IRawElementProviderSimple interface. 
    ListItemProvider* pItem = GetItemProviderByIndex(index); 
    if (pItem != NULL)
    {
        LONG i = 0;
        SafeArrayPutElement(psa, &i, pItem);
    }
    *pRetVal = psa;
    return S_OK;
}
```



<span data-ttu-id="ef1c6-113">En el ejemplo siguiente se muestra una implementación de [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) que devuelve un objeto que implementa [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="ef1c6-113">The following example shows an implementation of [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) that returns an object that implements [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span> <span data-ttu-id="ef1c6-114">La mayoría de los controles de lista también admitirían otros patrones, pero en este ejemplo se devuelve una referencia null para todos los demás identificadores de patrón de control.</span><span class="sxs-lookup"><span data-stu-id="ef1c6-114">Most list controls would support other patterns as well, but this example returns a null reference for all other control pattern identifiers.</span></span>


```C++
// Retrieves an object that supports the control pattern provider interface 
// for the specified control pattern. 
IFACEMETHODIMP ListProvider::GetPatternProvider(PATTERNID patternId, IUnknown** pRetVal)
{
    *pRetVal = NULL;
    if (patternId == UIA_SelectionPatternId) 
    {
        // Return the object that implements ISelectionProvider. In this example, 
        // ISelectionProvider is implemented in the current object (this).
        *pRetVal = static_cast<IRawElementProviderSimple*>(this);
        AddRef();  
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="ef1c6-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef1c6-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ef1c6-116">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ef1c6-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ef1c6-117">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ef1c6-117">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="ef1c6-118">Temas de procedimientos para los proveedores de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="ef1c6-118">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




