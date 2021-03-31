---
description: Quitar todos los filtros del gráfico
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Quitar todos los filtros del gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d414ef7e532eaf5df9143a6b601a57e4a8bd45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805876"
---
# <a name="remove-all-the-filters-in-the-graph"></a>Quitar todos los filtros del gráfico

La forma más fácil de quitar todos los filtros de un gráfico de filtros es simplemente liberar el administrador de gráficos de filtro y crear uno nuevo. Asegúrese de liberar todos los punteros que la aplicación tenga a cualquier interfaz de los administradores de gráficos de filtro, así como punteros a objetos del gráfico, incluidos filtros, PIN, el reloj de referencia, etc.

Como alternativa, puede quitar los filtros de uno en uno, mediante el método [**IFilterGraph:: removeFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) :


```C++
// Stop the graph.
pControl->Stop();

// Enumerate the filters in the graph.
IEnumFilters *pEnum = NULL;
HRESULT hr = pGraph->EnumFilters(&pEnum);
if (SUCCEEDED(hr))
{
    IBaseFilter *pFilter = NULL;
    while (S_OK == pEnum->Next(1, &pFilter, NULL))
     {
         // Remove the filter.
         pGraph->RemoveFilter(pFilter);
         // Reset the enumerator.
         pEnum->Reset();
         pFilter->Release();
    }
    pEnum->Release();
}
```



En este ejemplo se usa el método [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) para enumerar los filtros del gráfico. Al quitar un filtro, el objeto de enumerador deja de estar sincronizado con el gráfico. Use el método [**IEnumFilters:: RESET**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) para restablecer el enumerador. De lo contrario, se producirá un error en cualquier llamada subsiguiente a [**IEnumFilters:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) .

 

 



