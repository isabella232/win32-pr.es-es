---
description: Selección de un descodificador en DirectShow Editing Services
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Selección de un descodificador en DirectShow Editing Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcff63d44918a189f49e11527fe6fef35d108b7f20c1dadefa0a045e2c895b0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341275"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a>Selección de un descodificador en DirectShow Editing Services

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Cuando [DirectShow Editing Services](directshow-editing-services.md) (DES) representa un proyecto de edición de vídeo, el motor de representación selecciona automáticamente los descodificadores necesarios. Esto puede ocurrir dentro del [**método IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) o de forma dinámica durante la representación.

Un usuario podría instalar varios descodificadores que sean capaces de descodificar un archivo determinado. Cuando hay varios descodificadores disponibles, DES usa el algoritmo [de Conectar](intelligent-connect.md) inteligente para seleccionar el descodificador.

No hay ninguna manera de que la aplicación especifique directamente qué descodificador usar. Sin embargo, puede elegir el descodificador indirectamente a través de la interfaz de devolución de llamada [**IAMGraphBuilderCallback.**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) Al implementar esta interfaz en la aplicación, puede recibir notificaciones durante el proceso de creación de grafos y rechazar determinados filtros del gráfico.

Empiece por implementar una clase que expone la [**interfaz IAMGraphBuilderCallback:**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback)


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



A continuación, cree el motor de representación y llame al método [**IRenderEngine::SetFilterGraph**](irenderengine-setfiltergraph.md) con un puntero a Filter Graph Manager. Esto garantiza que el motor de representación no crea su propio Administrador de filtros Graph, sino que usa la instancia que ha configurado para las devoluciones de llamada.


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



Cuando se representa el proyecto, se llama al método [**IAMGraphBuilderCallback::SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) de la aplicación inmediatamente antes de que filter Graph Manager cree un nuevo filtro. El **método SelectedFilter** recibe un puntero a una **interfaz IMoniker** que representa un moniker para el filtro. Examine el moniker y, si decide rechazar el filtro, devuelva un código de error del **método SelectedFilter.**

La parte difícil es identificar qué monikers representan descodificadores y, en particular, qué monikers representan descodificadores que desea rechazar. Una solución es la siguiente:

-   Antes de representar el proyecto, use el método [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) para crear una lista de filtros registrados como que aceptan el tipo de entrada deseado. Para los tipos de compresión de audio o vídeo, esta lista debe asignarse a un conjunto de descodificadores.
-   El **método EnumMatchingFilters** devuelve una colección de monikers. Para cada moniker de la colección, obtenga la propiedad **DisplayName,** como se describe en [Uso del asignador de filtros.](using-the-filter-mapper.md)
-   Almacene una lista de los nombres para mostrar, pero omita el nombre para mostrar que coincida con el filtro que desea usar para lacoding. Los nombres para mostrar de los filtros de software tienen el formato siguiente:

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

    

    es el CLSID del filtro. En el caso de las DDO, el formato es el mismo, pero cambie `sw` a `dmo` .

    La lista ahora contiene nombres para mostrar para cada filtro que genera el tipo de medio deseado, pero no es el filtro preferido.

-   En el **método SelectedFilter,** obtenga la **propiedad DisplayName** en el moniker propuesto y compróquela en la lista almacenada. Si el nombre para mostrar coincide con una entrada de la lista, rechace ese filtro. De lo contrario, acepte la devolución de S \_ OK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de un Project](rendering-a-project.md)
</dt> </dl>

 

 



