---
description: Seleccionar un descodificador en servicios de edición de DirectShow
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Seleccionar un descodificador en servicios de edición de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956ad0284722eb394590b1b0065f167c55b3cf51
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494885"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a>Seleccionar un descodificador en servicios de edición de DirectShow

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Cuando los [servicios de edición de DirectShow](directshow-editing-services.md) (des) representan un proyecto de edición de vídeo, el motor de representación selecciona automáticamente los descodificadores necesarios. Esto puede ocurrir dentro del método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) , o bien de forma dinámica durante la representación.

Un usuario puede instalar varios descodificadores que pueden descodificar un archivo determinado. Cuando hay varios descodificadores disponibles, DES usa el algoritmo de [conexión inteligente](intelligent-connect.md) para seleccionar el descodificador.

No hay ninguna manera de que la aplicación especifique directamente el descodificador que se va a usar. Sin embargo, puede elegir el descodificador indirectamente a través de la interfaz de devolución de llamada [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) . Al implementar esta interfaz en la aplicación, puede recibir notificaciones durante el proceso de creación de gráficos y rechazar ciertos filtros del gráfico.

Comience implementando una clase que exponga la interfaz [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) :


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



A continuación, cree una instancia de Filter Graph Manager y registre la clase para recibir notificaciones de devolución de llamada:


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



A continuación, cree el motor de representación y llame al método [**IRenderEngine:: SetFilterGraph**](irenderengine-setfiltergraph.md) con un puntero al administrador de gráficos de filtro. Esto garantiza que el motor de representación no crea su propio administrador de gráficos de filtro, sino que utiliza la instancia que ha configurado para las devoluciones de llamada.


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



Cuando se representa el proyecto, se llama al método [**IAMGraphBuilderCallback:: SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) de la aplicación inmediatamente antes de que el administrador de gráficos de filtros cree un nuevo filtro. El método **SelectedFilter** recibe un puntero a una interfaz **IMoniker** que representa un moniker para el filtro. Examine el moniker y, si decide rechazar el filtro, devuelva un código de error del método **SelectedFilter** .

La parte difícil es identificar qué monikers representan descodificadores y, en concreto, qué monikers representan descodificadores que desea rechazar. Una solución es la siguiente:

-   Antes de representar el proyecto, use el método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) para crear una lista de filtros que se registran para aceptar el tipo de entrada deseado. En el caso de los tipos de compresión de audio o vídeo, esta lista debe asignarse a un conjunto de descodificadores.
-   El método **EnumMatchingFilters** devuelve una colección de monikers. Para cada moniker de la colección, obtenga la propiedad **displayName** , como se describe en [usar el asignador de filtros](using-the-filter-mapper.md).
-   Almacene una lista de los nombres para mostrar, pero omita el nombre para mostrar que coincida con el filtro que desea utilizar para la descodificación. Los nombres para mostrar de los filtros de software tienen el formato siguiente:

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    where

    ```C++
    CategoryGUID
    ```

    

    es el GUID de la categoría de filtro y

    ```C++
    FilterCLSID
    ```

    

    es el CLSID del filtro. En el caso de DMOs, el formato es el mismo, pero cambie `sw` a `dmo` .

    La lista contiene ahora los nombres para mostrar de todos los filtros que generan el tipo de medio deseado, pero no el filtro preferido.

-   En el método **SelectedFilter** , obtenga la propiedad **displayName** en el moniker propuesto y compruébelo en la lista almacenada. Si el nombre para mostrar coincide con una entrada de la lista, rechace ese filtro. De lo contrario, se debe aceptar si se devuelven los elementos \_ correctos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar un proyecto](rendering-a-project.md)
</dt> </dl>

 

 



