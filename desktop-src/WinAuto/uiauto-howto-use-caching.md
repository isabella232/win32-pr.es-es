---
title: Uso del Almacenamiento en caché
description: Este tema contiene código de ejemplo que muestra cómo usar las capacidades de almacenamiento en caché (o captura masiva) del árbol de automatización de la interfaz de usuario de Microsoft.
ms.assetid: d72fa637-35ca-4c28-922d-263f469cb1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758621a8499202b820a6ffc3459fade57c2a485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714161"
---
# <a name="how-to-use-caching"></a>Uso del Almacenamiento en caché

Este tema contiene código de ejemplo que muestra cómo usar las capacidades de almacenamiento en caché (o captura masiva) del árbol de automatización de la interfaz de usuario de Microsoft. Se tratan los temas siguientes:

-   [Capturar propiedades y patrones de control en la memoria caché](#fetching-properties-and-control-patterns-into-the-cache)
-   [Recuperar propiedades y patrones de control de la memoria caché](#retrieving-properties-and-control-patterns-from-the-cache)
-   [Temas relacionados](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a>Capturar propiedades y patrones de control en la memoria caché

En el ejemplo de código siguiente se muestra una función que recupera elementos de un control de lista y almacena en caché el patrón de control SelectionItem y la propiedad Name de cada elemento. De forma predeterminada, los elementos de la lista se devuelven con una referencia completa, de modo que todas las propiedades actuales siguen estando disponibles.


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

En el código siguiente se muestra cómo recuperar las propiedades y los patrones de control de la memoria caché. Recupera el patrón de control SelectionItem y la propiedad Name para un elemento de lista.


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

**Vista**
</dt> <dt>

[Propiedades y patrones de control de la automatización de la interfaz de usuario](uiauto-cachingforclients.md)
</dt> <dt>

[Temas de procedimientos para clientes de automatización de la interfaz de usuario](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




