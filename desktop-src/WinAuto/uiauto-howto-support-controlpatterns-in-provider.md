---
title: Patrones de control compatibles en un proveedor de UI Automation
description: En este tema se muestra cómo un proveedor Automatización de la interfaz de usuario microsoft implementa patrones de control para un control. Los patrones de control permiten a las aplicaciones cliente manipular el control y obtener información sobre él.
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54e75fa12dba891bc4eded5fd9763f7825eb7f88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567276"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a>Patrones de control compatibles en un proveedor de UI Automation

En este tema se muestra cómo un proveedor Automatización de la interfaz de usuario microsoft implementa patrones de control para un control. Los patrones de control permiten a las aplicaciones cliente manipular el control y obtener información sobre él.

Un proveedor implementa un patrón de control siguiendo estos pasos principales:

1.  Implemente la interfaz del proveedor que admite el patrón de control. Por ejemplo, para admitir el patrón de control [Selection,](uiauto-implementingselection.md) un proveedor para un control de lista personalizado implementaría la [**interfaz ISelectionProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)
2.  Devuelve un objeto que contiene la interfaz del proveedor de patrones de control cuando Automatización de la interfaz de usuario llama al método [**IRawElementProviderSimple::GetPatternProvider del**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) proveedor.

En el ejemplo siguiente se muestra la implementación de la interfaz [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) para un control personalizado de lista de selección única. La implementación incluye métodos de recuperación de propiedades para las propiedades IsSelectionRequired y CanSelectMultiple, y un método para recuperar el proveedor para el elemento de lista seleccionado.


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



En el ejemplo siguiente se muestra una implementación de [**IRawElementProviderSimple::GetPatternProvider que**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) devuelve un objeto que implementa [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider). La mayoría de los controles de lista también admitirían otros patrones, pero este ejemplo devuelve una referencia nula para todos los demás identificadores de patrón de control.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Temas de ayuda para proveedores de Automatización de la interfaz de usuario](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




