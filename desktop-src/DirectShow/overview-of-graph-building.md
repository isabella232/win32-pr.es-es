---
description: Información general de Graph Building
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Información general de Graph Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362358"
---
# <a name="overview-of-graph-building"></a>Información general de Graph Building

Para crear un gráfico de filtros, comience por crear una instancia de Filter Graph Manager:


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



Filter Graph Manager admite los siguientes métodos de creación de grafos:

-   [**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) intenta establecer una conexión directa entre dos pines. Si los pines no se pueden conectar, se produce un error en el método .
-   [**IGraphBuilder::Conectar**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) conecta dos pines. Si es posible, realiza una conexión directa. De lo contrario, usa filtros intermedios para completar la conexión.
-   [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) comienza desde un pin de salida y compila el resto del gráfico. Estos métodos agregan filtros según sea necesario, trabajando de bajada, hasta que llega a un filtro de representador.
-   [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) crea un gráfico de reproducción de archivos completo.
-   [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) agrega un filtro al gráfico. No conecta el filtro. Debe crear el filtro antes de llamar a este método, ya sea mediante una llamada a **CoCreateInstance** o mediante el asignador de filtros o el enumerador de dispositivos del sistema.

Estos métodos proporcionan tres enfoques básicos para crear el gráfico:

1.  El administrador Graph filtro compila todo el gráfico.
2.  Filter Graph Manager compila parte del gráfico.
3.  La aplicación compila todo el gráfico.

**El Administrador Graph filtros compila toda la Graph**

Si simplemente quiere reproducir un archivo que se ha escrito en un formato reconocido, como AVI, MPEG, WAV o MP3, use el **método RenderFile.** En el [artículo Cómo reproducir un archivo](how-to-play-a-file.md) se muestra cómo hacerlo.

El **método RenderFile** comienza buscando en el Registro un filtro de origen que pueda analizar el archivo. Usa el protocolo (como " " en la dirección URL), la extensión de archivo o patrones de bytes predefinidos en el archivo para determinar `https://` el filtro de origen. Para obtener más información, [vea Registrar un tipo de archivo personalizado.](registering-a-custom-file-type.md)

Para compilar el resto del gráfico, el Administrador de filtros Graph usa un proceso iterativo en el que toma los tipos de medios que admite un filtro en sus pines de salida y busca en el Registro filtros que acepten ese tipo de medio como entrada. Usa varios criterios para restringir la búsqueda y priorizar los filtros:

-   La *categoría de* filtro identifica la funcionalidad general del filtro.
-   El tipo de medio describe qué tipo de datos puede aceptar el filtro como entrada o entregar como salida.
-   El *resultado* determina el orden en el que se van a probar los filtros. Si dos filtros de la misma categoría de filtro admiten los mismos tipos de entrada, filter Graph Manager selecciona el que tiene el valor más alto. A algunos filtros se les da a propósito un valor bajo porque están diseñados para fines especializados y la aplicación solo debe agregar al gráfico.

El Administrador Graph filtro usa el [objeto Asignador de](filter-mapper.md) filtros para buscar en el Registro.

A medida que se agrega cada filtro, el administrador de Graph intenta conectarlo al pin de salida del filtro anterior. Los filtros negocian para determinar si se pueden conectar y, si es así, qué tipo de medio usar para la conexión. Si el nuevo filtro no se puede conectar, Graph Administrador de filtros lo descarta e intenta otro filtro. Este proceso continúa hasta que se representa cada secuencia.

**La parte de Graph Administrador de filtros del administrador de Graph**

Para hacer algo más allá de simplemente reproducir un archivo, la aplicación debe realizar al menos parte del trabajo de creación de grafos. Por ejemplo, una aplicación de captura de vídeo debe seleccionar un filtro de origen de captura y agregarlo al gráfico. Si escribe datos en un archivo AVI, debe agregar los filtros Mux y File Writer de AVI al gráfico. Sin embargo, a menudo es posible permitir que filter Graph Manager complete el gráfico. Por ejemplo, puede representar un pin para la vista previa mediante una llamada al **método Render.**

**La aplicación compila toda la Graph**

En algunos escenarios, es posible que la aplicación tenga que compilar el gráfico agregando y conectando cada filtro. En este caso, probablemente sepa específicamente qué filtros se deben agregar al gráfico. Con este enfoque, la aplicación agrega cada filtro mediante una llamada a **AddFilter,** enumera los pines de los filtros y los conecta mediante una llamada **a Conectar** o **ConnectDirect**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de gráficos con capture Graph Builder](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[Enumeración de dispositivos y filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Enumerar objetos en un filtro Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Técnicas de Graph-Building generales](general-graph-building-techniques.md)
</dt> <dt>

[Creación del filtro Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



