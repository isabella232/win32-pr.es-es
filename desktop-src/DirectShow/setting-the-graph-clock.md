---
description: Establecimiento del Graph reloj
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Establecimiento del Graph reloj
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab93fcefe4ba88aa7724bf59b775c493313783b2f4ad3801925e16b9a1818c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904145"
---
# <a name="setting-the-graph-clock"></a>Establecimiento del Graph reloj

Al compilar un gráfico de filtros, el Administrador de filtros Graph automáticamente elige un reloj de referencia para el gráfico. Todos los filtros del gráfico se sincronizan con el reloj de referencia. En concreto, los filtros de representador usan el reloj de referencia para determinar el tiempo de presentación de cada muestra.

Normalmente no hay ninguna razón para que una aplicación invalide el reloj de referencia de filter Graph Manager. Sin embargo, puede hacerlo llamando al método [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) en filter Graph Manager. Este método toma un puntero a la interfaz **IReferenceClock del** reloj. Llame al método mientras se detiene el gráfico.

Si un filtro proporciona un reloj, puede obtener el puntero **IReferenceClock** llamando a **QueryInterface** en el filtro. Como alternativa, puede implementar un reloj de referencia externo que no proporciona un filtro, siempre que el reloj externo implemente **IReferenceClock**. En el ejemplo siguiente se muestra cómo especificar un reloj:


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



En este ejemplo se supone que CreateMyPrivateClock es una función definida por la aplicación que crea un reloj y devuelve un **puntero IReferenceClock.**

También puede establecer el gráfico de filtro para que se ejecute sin reloj; para ello, llame a **SetSyncSource** con el valor **NULL**. Si no hay ningún reloj, el gráfico se ejecuta lo más rápido posible. Sin reloj, los filtros del representador no esperan el tiempo de presentación de una muestra. En su lugar, representan cada muestra en cuanto llega. Establecer el gráfico para que se ejecute sin un reloj es útil si desea procesar los datos rápidamente, en lugar de obtener una vista previa de ellos en tiempo real.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas DirectShow básicas](basic-directshow-tasks.md)
</dt> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



