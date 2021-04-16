---
description: Establecer el reloj del gráfico
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Establecer el reloj del gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686267"
---
# <a name="setting-the-graph-clock"></a>Establecer el reloj del gráfico

Al compilar un gráfico de filtros, el administrador de gráficos de filtros elige automáticamente un reloj de referencia para el gráfico. Todos los filtros del gráfico se sincronizan con el reloj de referencia. En concreto, los filtros de representador usan el reloj de referencia para determinar el tiempo de presentación de cada ejemplo.

Por lo general, no hay ninguna razón para que una aplicación invalide el reloj de referencia del administrador de gráficos de filtro. Sin embargo, puede hacerlo llamando al método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) en el administrador de gráficos de filtro. Este método toma un puntero a la interfaz **IReferenceClock** del reloj. Llame al método mientras se detiene el gráfico.

Si un filtro proporciona un reloj, puede obtener el puntero **IReferenceClock** llamando a **QueryInterface** en el filtro. Como alternativa, puede implementar un reloj de referencia externo que no sea proporcionado por un filtro, siempre que el reloj externo implemente **IReferenceClock**. En el ejemplo siguiente se muestra cómo especificar un reloj:


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



En este ejemplo se da por supuesto que CreateMyPrivateClock es una función definida por la aplicación que crea un reloj y devuelve un puntero **IReferenceClock** .

También puede establecer que el gráfico de filtro se ejecute sin ningún reloj, llamando a **SetSyncSource** con el valor **null**. Si no hay ningún reloj, el gráfico se ejecuta lo más rápido posible. Sin ningún reloj, los filtros de representador no esperan el tiempo de presentación de un ejemplo. En su lugar, representan cada ejemplo en cuanto llega. Configurar el gráfico para que se ejecute sin un reloj es útil si desea procesar los datos rápidamente, en lugar de obtener una vista previa en tiempo real.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas básicas de DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



