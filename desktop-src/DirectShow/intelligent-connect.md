---
description: Conexión inteligente
ms.assetid: 938ba1b0-822e-4871-8786-b7eeee243867
title: Conexión inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12aead305867ccec1f1f1f0cbd76c652ba3ec412
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495479"
---
# <a name="intelligent-connect"></a>Conexión inteligente

Conexión inteligente es el mecanismo que utiliza el administrador de gráficos de filtro para generar gráficos de filtro. Consta de varios algoritmos relacionados que seleccionan filtros y los agregan al gráfico de filtros.

Lea este tema si tiene problemas para crear un gráfico de filtros determinado y desea solucionar el problema, o si está escribiendo su propio filtro y desea que esté disponible para la creación automática de gráficos.

La conexión inteligente implica los siguientes métodos [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) :

-   [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)
-   [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)
-   [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)
-   [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)

### <a name="igraphbuilderaddsourcefilter"></a>IGraphBuilder::AddSourceFilter

El método [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) agrega un filtro de origen que puede representar un archivo especificado. Primero busca en el registro y coincide con el protocolo (como `https://` ), la extensión de nombre de archivo o un conjunto de *bytes de comprobación* predeterminados, que son bytes en determinados desplazamientos en el archivo que coinciden con determinados patrones. Para obtener más información, consulte [registrar un tipo de archivo personalizado](registering-a-custom-file-type.md). Suponiendo que el método busca un filtro de origen adecuado, crea una instancia de ese filtro, lo agrega al gráfico y llama al método [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) del filtro con el nombre de archivo.

### <a name="igraphbuilderrender"></a>IGraphBuilder:: Render

El método [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) crea una subsección de un gráfico. Se inicia a partir de un PIN de salida no conectado y funciona de forma descendente, agregando nuevos filtros según sea necesario. El filtro inicial debe estar ya en el gráfico. En cada paso, el método **Render** busca un filtro que pueda conectarse al filtro anterior. La secuencia se puede bifurcar si un filtro de conexión tiene varios terminales de salida. La búsqueda se detiene cuando cada flujo tiene un representador. Si el método **Render** se bloquea, podría hacer una copia de seguridad e intentarlo de nuevo, con un conjunto diferente de filtros.

Para conectar cada pin de salida, el método [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) hace lo siguiente:

1.  Si el PIN es compatible con la interfaz [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) , el administrador de gráficos de filtro delega el proceso completo en el método [**IStreamBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-istreambuilder-render) del PIN. Al exponer esta interfaz, el PIN asume la responsabilidad de crear el resto del gráfico, hasta el representador. Sin embargo, muy pocos PIN admiten esta interfaz.
2.  El administrador de gráficos de filtro intenta utilizar los filtros que se almacenan en la memoria caché, si los hay. A lo largo del proceso de conexión inteligente, el administrador de gráficos de filtro puede almacenar en caché filtros de pasos anteriores en el proceso. (Consulte también [creación de gráficos dinámicos](dynamic-graph-building.md)).
3.  Si el gráfico de filtros contiene algún filtro con clavijas de entrada sin conexión, el administrador de gráficos de filtro los probará. Puede forzar que el método [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) intente un filtro determinado agregando ese filtro al gráfico antes de llamar a **Render**.
4.  A partir de Windows 7, DirectShow tiene una lista de filtros preferidos para determinados subtipos de medios. Si hay un filtro preferido para el tipo de medio que se está representando, el administrador de gráficos de filtro intentará el filtro siguiente. Una aplicación puede modificar la lista de filtros preferidos mediante la interfaz [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) . Los cambios en la lista afectan al proceso actual de la aplicación y se descartan una vez finalizado el proceso.
5.  Por último, si no se encuentra ningún filtro adecuado, el administrador de gráficos de filtros busca en el registro mediante el método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) . Intenta hacer coincidir los tipos de medios preferidos del terminal de salida con los tipos de medios que se enumeran en el registro.

    Cada filtro se registra con un *mérito*, un valor numérico que indica la preferencia del filtro, con respecto a otros filtros. El método [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) devuelve los filtros en orden de mérito, con una cantidad mínima de **méritos que \_ \_ no \_ usa** + 1. Omite los filtros con un mérito de **mérito \_ \_ no \_ usar** o menos. Los filtros también se agrupan en categorías, definidas por GUID. Las propias categorías tienen méritos, y el método **EnumMatchingFilters** omite cualquier categoría con un mérito **de \_ mérito \_ no \_ utiliza** o menos, incluso si los filtros de esa categoría tienen valores de méritos más altos.

    A partir de Windows 7, DirectShow tiene una lista de filtros bloqueados para determinados subtipos de medios. El administrador de gráficos de filtro omite los filtros de esta lista. Una aplicación puede modificar la lista de filtros bloqueados mediante la interfaz [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) . Los cambios en esta lista afectan al proceso actual de la aplicación y se descartan una vez finalizado el proceso.

En Resumen, el método [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) intenta filtrar en el orden siguiente:

1.  Use [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder).
2.  Pruebe los filtros en caché.
3.  Pruebe los filtros del gráfico.
4.  Windows 7 o posterior: Pruebe el filtro preferido para el tipo de medio, si existe.
5.  Buscar filtros en el registro.

### <a name="igraphbuilderrenderfile"></a>IGraphBuilder:: RenderFile

El método [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) crea un gráfico de reproducción predeterminado a partir de un nombre de archivo. Internamente, este método usa [**AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para buscar el filtro de origen correcto y [**representar**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para compilar el resto del gráfico.

### <a name="igraphbuilderconnect"></a>IGraphBuilder:: Connect

El método [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) conecta un PIN de salida a un PIN de entrada. Este método agrega filtros intermedios si es necesario, utilizando una variación del algoritmo descrito para el método [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) :

1.  Pruebe una conexión directa entre los filtros, sin filtros intermedios.
2.  Pruebe los filtros en caché.
3.  Pruebe los filtros del gráfico.
4.  Windows 7 o posterior: Pruebe el filtro preferido para el tipo de medio, si existe.
5.  Buscar filtros en el registro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías de filtro](filter-categories.md)
</dt> <dt>

[Fundament](merit.md)
</dt> <dt>

[Simular la compilación de gráficos con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[Compilar el gráfico de filtro](building-the-filter-graph.md)
</dt> </dl>

 

 



