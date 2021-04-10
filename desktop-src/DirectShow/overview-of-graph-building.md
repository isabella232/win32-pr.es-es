---
description: Información general sobre la creación de gráficos
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Información general sobre la creación de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152284"
---
# <a name="overview-of-graph-building"></a>Información general sobre la creación de gráficos

Para crear un gráfico de filtro, empiece por crear una instancia de Filter Graph Manager:


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



Filter Graph Manager admite los siguientes métodos de creación de gráficos:

-   [**IFilterGraph:: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) intenta establecer una conexión directa entre dos clavijas. Si los PIN no se pueden conectar, se produce un error en el método.
-   [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) conecta dos clavijas. Si es posible, realiza una conexión directa. De lo contrario, utiliza filtros intermedios para completar la conexión.
-   [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) comienza en un terminal de salida y compila el resto del gráfico. Estos métodos agregan filtros según sea necesario, trabajando de forma descendente hasta que alcanzan un filtro de representador.
-   [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) crea un gráfico de reproducción de archivos completo.
-   [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) agrega un filtro al gráfico. No conecta el filtro. Debe crear el filtro antes de llamar a este método, ya sea mediante una llamada a **CoCreateInstance** o mediante el enumerador de filtros o de dispositivos del sistema.

Estos métodos proporcionan tres enfoques básicos para crear el gráfico:

1.  El administrador de gráficos de filtro compila todo el gráfico.
2.  El administrador de gráficos de filtro compila parte del gráfico.
3.  La aplicación crea el gráfico completo.

**El administrador de gráficos de filtro compila todo el gráfico**

Si simplemente desea reproducir un archivo que se creó en un formato reconocido, como AVI, MPEG, WAV o MP3, use el método **RenderFile** . En el artículo [Cómo reproducir un archivo](how-to-play-a-file.md) se muestra cómo hacerlo.

El método **RenderFile** se inicia buscando en el registro un filtro de origen que puede analizar el archivo. Usa el protocolo (como " `https://` " en la dirección URL), la extensión de archivo o los patrones de bytes predefinidos en el archivo para determinar el filtro de origen. Para obtener más información, consulte [registrar un tipo de archivo personalizado](registering-a-custom-file-type.md).

Para compilar el resto del gráfico, el administrador de gráficos de filtro utiliza un proceso iterativo en el que toma los tipos de medios que admite un filtro en sus clavijas de salida y busca en el registro filtros que acepten ese tipo de medio como entrada. Usa varios criterios para restringir los filtros de búsqueda y priorización:

-   La *categoría de filtro* identifica la funcionalidad general del filtro.
-   El tipo de medio describe el tipo de datos que el filtro puede aceptar como entrada o entrega como salida.
-   El *mérito* determina el orden en el que se intentan los filtros. Si dos filtros de la misma categoría de filtro admiten los mismos tipos de entrada, el administrador de gráficos de filtro selecciona el que tiene el valor de mérito más alto. A algunos filtros se les asigna intencionadamente un valor de mérito bajo porque están diseñados para fines especializados y la aplicación solo debe agregarlos al gráfico.

Filter Graph Manager usa el objeto de [asignador de filtros](filter-mapper.md) para buscar en el registro.

A medida que se agrega cada filtro, el administrador de gráficos de filtros intenta conectarlo al código PIN de salida del filtro anterior. Los filtros negocian para determinar si se pueden conectar y, si es así, el tipo de medio que se utilizará para la conexión. Si el nuevo filtro no se puede conectar, el administrador de gráficos de filtros lo descarta e intenta otro filtro. Este proceso continúa hasta que se representan todos los flujos.

**El administrador de gráficos de filtro compila parte del gráfico**

Para hacer algo más allá de simplemente reproducir un archivo, la aplicación debe realizar al menos algunos de los trabajos de creación de gráficos. Por ejemplo, una aplicación de captura de vídeo debe seleccionar un filtro de origen de captura y agregarlo al gráfico. Si va a escribir datos en un archivo AVI, debe agregar los filtros AVI MUX y escritor de archivos al gráfico. Sin embargo, a menudo es posible permitir que el administrador de gráficos de filtro complete el gráfico. Por ejemplo, puede representar un PIN para la vista previa llamando al método **Render** .

**La aplicación crea el gráfico completo**

En algunos escenarios, es posible que la aplicación necesite crear el gráfico agregando y conectando cada filtro. En este caso, probablemente sepa específicamente qué filtros se deben agregar al gráfico. Con este enfoque, la aplicación agrega cada filtro llamando a **addFilter**, enumera los pin de los filtros y los conecta llamando a **Connect** o **ConnectDirect**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Generar gráficos con el generador de gráficos de captura](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[Enumerar dispositivos y filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Enumerar objetos en un gráfico de filtros](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Técnicas generales de Graph-Building](general-graph-building-techniques.md)
</dt> <dt>

[Compilar el gráfico de filtro](building-the-filter-graph.md)
</dt> </dl>

 

 



