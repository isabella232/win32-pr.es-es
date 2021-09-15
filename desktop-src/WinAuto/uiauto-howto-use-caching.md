---
title: Uso del Almacenamiento en caché
description: Este tema contiene código de ejemplo que muestra cómo usar las funcionalidades de almacenamiento en caché (o captura masiva) de Microsoft Automatización de la interfaz de usuario árbol.
ms.assetid: d72fa637-35ca-4c28-922d-263f469cb1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758621a8499202b820a6ffc3459fade57c2a485
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567260"
---
# <a name="how-to-use-caching"></a>Uso del Almacenamiento en caché

Este tema contiene código de ejemplo que muestra cómo usar las funcionalidades de almacenamiento en caché (o captura masiva) de Microsoft Automatización de la interfaz de usuario árbol. Describe los temas siguientes:

-   [Capturar propiedades y patrones de control en la memoria caché](#fetching-properties-and-control-patterns-into-the-cache)
-   [Recuperar propiedades y patrones de control de la memoria caché](#retrieving-properties-and-control-patterns-from-the-cache)
-   [Temas relacionados](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a>Capturar propiedades y patrones de control en la memoria caché

En el ejemplo de código siguiente se muestra una función que recupera elementos de un control de lista y almacena en caché el patrón de control SelectionItem y la propiedad Name de cada elemento. De forma predeterminada, los elementos de lista se devuelven con una referencia completa, por lo que todas las propiedades actuales siguen estando disponibles.


```C++
// Given a list element, caches a control pattern and a property for
// all the list items.
IUIAutomationElementArray* FindAndCacheListItems(IUIAutomationElement* pList)
{
    if (pList == NULL)
        return NULL;
    
    IUIAutomationCondition* pCondition = NULL;
    IUIAutomationCacheRequest* pCacheRequest = NULL;
    IUIAutomationElementArray* pFound = NULL;

    HRESULT hr = g_pAutomation->CreateTrueCondition(&pCondition);
    if (FAILED(hr))
        goto cleanup;

    hr = g_pAutomation->CreateCacheRequest(&pCacheRequest);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddPattern(UIA_SelectionItemPatternId);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddProperty(UIA_NamePropertyId);
    if (FAILED(hr))
        goto cleanup;

    pList->FindAllBuildCache(TreeScope_Children, pCondition, pCacheRequest, &pFound);
    
cleanup:
    if (pCondition != NULL)
        pCondition->Release();

    if (pCacheRequest != NULL)
        pCacheRequest->Release();

    return pFound;
}
```



## <a name="retrieving-properties-and-control-patterns-from-the-cache"></a>Recuperar propiedades y patrones de control de la memoria caché

El código siguiente muestra cómo recuperar propiedades y patrones de control de la memoria caché. Recupera el patrón de control SelectionItem y la propiedad Name de un elemento de lista.


```C++
// Demonstrates retrieval of cached properties from a list item
// obtained in FindAndCacheListItems.
HRESULT GetCachedListItem(IUIAutomationElement* pItem)
{           
    if (pItem == NULL)
    {
        return E_INVALIDARG;
    }

    IUIAutomationSelectionItemPattern* pSelectionItemPattern;
    HRESULT hr = pItem->GetCachedPatternAs(UIA_SelectionItemPatternId, 
        IID_IUIAutomationSelectionItemPattern, (void**)&pSelectionItemPattern);
    if (pSelectionItemPattern != NULL)
    {
        // ... To do: Do something with the pattern.

        pSelectionItemPattern->Release();
    }

    // Retrieve a cached property.
    BSTR bstrName;
    hr = pItem->get_CachedName(&bstrName);
    if (SUCCEEDED(hr))
    {
        // ... To do: Do something with the property.

        // Clean up when done with name.
        SysFreeString(bstrName);
        bstrName = NULL;
    }

    BOOL isControl;

    // The following returns E_INVALIDARG because the property was not cached.
    // hr = pItem->get_CachedIsControlElement(&isControl);

    // The following is valid because we have a full reference to the object, therefore
    // we can get current properties. If the cache request had been made with 
    // AutomationElementMode_None, no current properties would be available from
    // this IUIAutomationElement.
    hr = pItem->get_CurrentIsControlElement(&isControl);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Almacenar en Automatización de la interfaz de usuario propiedades y patrones de control](uiauto-cachingforclients.md)
</dt> <dt>

[Temas de ayuda para Automatización de la interfaz de usuario clientes](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




