---
title: Cómo buscar elementos de la interfaz de usuario
description: Este tema contiene código de ejemplo que muestra cómo buscar elementos de interfaz de usuario en el Automatización de la interfaz de usuario de datos.
ms.assetid: b613eb18-e14d-468e-833d-072bad29ba06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887ef914d7abcf5ed6dfc546f0930334f53215d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070510"
---
# <a name="how-to-find-ui-elements"></a>Cómo buscar elementos de la interfaz de usuario

Este tema contiene código de ejemplo que muestra cómo buscar elementos de interfaz de usuario en el Automatización de la interfaz de usuario de datos.

-   [Buscar un elemento por nombre](#finding-an-element-by-name)
-   [Buscar elementos relacionados](#finding-related-elements)
-   [Temas relacionados](#related-topics)

## <a name="finding-an-element-by-name"></a>Buscar un elemento por nombre

En el ejemplo siguiente se busca el Automatización de la interfaz de usuario de Microsoft que tiene el nombre especificado y es un elemento secundario de la ventana de escritorio.


```C++
IUIAutomationElement* GetTopLevelWindowByName(LPWSTR windowName)
{
    if (windowName == NULL)
    {
        return NULL;
    }

    VARIANT varProp;
    varProp.vt = VT_BSTR;
    varProp.bstrVal = SysAllocString(windowName);
    if (varProp.bstrVal == NULL)
    {
        return NULL;
    }

    IUIAutomationElement* pRoot = NULL;
    IUIAutomationElement* pFound = NULL;

    // Get the desktop element. 
    HRESULT hr = g_pAutomation->GetRootElement(&pRoot);
    if (FAILED(hr) || pRoot == NULL)
        goto cleanup;

    // Get a top-level element by name, such as "Program Manager"
    IUIAutomationCondition* pCondition;
    hr = g_pAutomation->CreatePropertyCondition(UIA_NamePropertyId, varProp, &pCondition);
    if (FAILED(hr))
        goto cleanup;

    pRoot->FindFirst(TreeScope_Children, pCondition, &pFound);

cleanup:
    if (pRoot != NULL)
        pRoot->Release();

    if (pCondition != NULL)
        pCondition->Release();

    VariantClear(&varProp);
    return pFound;
}
```



## <a name="finding-related-elements"></a>Buscar elementos relacionados

La siguiente función de ejemplo devuelve una colección de todos los botones habilitados que son elementos secundarios del elemento especificado.


```C++
IUIAutomationElementArray* GetEnabledButtons(IUIAutomationElement* pParent)
{
    if (pParent == NULL)
    {
        return NULL;
    }
    IUIAutomationCondition* pButtonCondition = NULL;
    IUIAutomationCondition* pEnabledCondition = NULL;
    IUIAutomationCondition* pCombinedCondition = NULL;
    IUIAutomationElementArray* pFound = NULL;

    // Create a property condition for the button control type.
    VARIANT varProp;
    varProp.vt = VT_I4;
    varProp.lVal = UIA_ButtonControlTypeId;
    g_pAutomation->CreatePropertyCondition(UIA_ControlTypePropertyId, varProp, &pButtonCondition);
    if (pButtonCondition == NULL)
        goto cleanup;

    // Create a property condition for the enabled property.
    varProp.vt = VT_BOOL;
    varProp.boolVal = VARIANT_TRUE;
    g_pAutomation->CreatePropertyCondition(UIA_IsEnabledPropertyId, varProp, &pEnabledCondition);
    if (pEnabledCondition == NULL)
        goto cleanup;

    // Combine the conditions.
    g_pAutomation->CreateAndCondition(pButtonCondition, pEnabledCondition, &pCombinedCondition);
    if (pCombinedCondition == NULL)
        goto cleanup;

    // Find the matching elements. Note that if the scope is changed to TreeScope_Descendants, 
    // system buttons on the caption bar will be found as well.
    pParent->FindAll(TreeScope_Children, pCombinedCondition, &pFound);

cleanup:
    if (pButtonCondition != NULL)
        pButtonCondition->Release();

    if (pEnabledCondition != NULL) 
        pEnabledCondition->Release();
    
    if (pCombinedCondition != NULL)
        pCombinedCondition->Release();

    return pFound;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Obtener elementos de UI Automation](uiauto-obtainingelements.md)
</dt> <dt>

[Temas de ayuda para Automatización de la interfaz de usuario clientes](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




