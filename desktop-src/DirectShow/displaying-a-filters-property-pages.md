---
description: Mostrar las páginas de propiedades de un filtro
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Mostrar las páginas de propiedades de un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0845a12b73363dc6ed93654439fd31826bf9cfc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061675"
---
# <a name="displaying-a-filters-property-pages"></a>Mostrar las páginas de propiedades de un filtro

Una página de propiedades es una manera de que un filtro admita las propiedades que el usuario puede establecer. En este artículo se describe cómo mostrar las páginas de propiedades de un filtro en una aplicación. Para más información sobre las páginas de propiedades, consulte la documentación de Platform SDK.

> [!Note]  
> Aunque muchos de los filtros proporcionados con DirectShow admiten páginas de propiedades, están diseñados para fines de depuración y no se recomiendan para el uso de la aplicación. En la mayoría de los casos, la funcionalidad equivalente se proporciona a través de una interfaz personalizada en el filtro. Una aplicación debe controlar estos filtros mediante programación, en lugar de exponer sus páginas de propiedades a los usuarios.

 

Los filtros con páginas de propiedades exponen **la interfaz ISpecifyPropertyPages.** Para determinar si un filtro define una página de propiedades, consulte el filtro para esta interfaz mediante **QueryInterface**.

Si creó directamente una instancia de un filtro (mediante una llamada a **CoCreateInstance),** ya tiene un puntero al filtro. Si no es así, puede enumerar los filtros del gráfico mediante el [**método IFilterGraph::EnumFilters.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) Para obtener más información, [vea Enumerar objetos en un filtro Graph](enumerating-objects-in-a-filter-graph.md).

Una vez que tenga el puntero de interfaz **ISpecifyPropertyPages,** recupere las páginas de propiedades del filtro llamando al **método ISpecifyPropertyPages::GetPages.** Este método rellena una matriz con recuento de identificadores únicos globales (GUID) con el identificador de clase (CLSID) de cada página de propiedades. Una matriz con recuento se define mediante una **estructura CAUUID,** que debe asignar pero no tiene que inicializar. El **método GetPages** asigna la matriz , que se encuentra en el **miembro pElems** de la **estructura CAUUID.** Cuando haya terminado, libera la matriz mediante una llamada a la **función CoTaskMemFree.**

La **función OleCreatePropertyFrame** proporciona una manera sencilla de mostrar las páginas de propiedades dentro de un cuadro de diálogo modal.


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas DirectShow básicas](basic-directshow-tasks.md)
</dt> </dl>

 

 



