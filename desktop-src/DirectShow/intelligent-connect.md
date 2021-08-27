---
description: Inteligencia Conectar
ms.assetid: 938ba1b0-822e-4871-8786-b7eeee243867
title: Inteligencia Conectar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2248dc936076dfcad1b2ad934da4ef6a8b1e28a260ff75ebca3a63ec6356bf6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107705"
---
# <a name="intelligent-connect"></a>Inteligencia Conectar

Intelligent Conectar es el mecanismo que usa el Administrador de filtros Graph para crear gráficos de filtro. Consta de varios algoritmos relacionados que seleccionan filtros y los agregan al gráfico de filtros.

Lea este tema si tiene problemas para crear un gráfico de filtros determinado y desea solucionar el problema, o si está escribiendo su propio filtro y desea que esté disponible para la creación automática de grafos.

Intelligent Conectar implica los siguientes [**métodos de IGraphBuilder:**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)

-   [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)
-   [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)
-   [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)
-   [**IGraphBuilder::Conectar**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)

### <a name="igraphbuilderaddsourcefilter"></a>IGraphBuilder::AddSourceFilter

El [**método IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) agrega un filtro de origen que puede representar un archivo especificado. En primer lugar, busca en el Registro y coincide con el protocolo (por ejemplo, ), la extensión de nombre de archivo o un conjunto de bytes de comprobación predeterminados, que son bytes en desplazamientos concretos del archivo que coinciden con `https://` determinados patrones.  Para obtener más información, [vea Registrar un tipo de archivo personalizado.](registering-a-custom-file-type.md) Suponiendo que el método busca un filtro de origen adecuado, crea una instancia de ese filtro, lo agrega al gráfico y llama al método [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) del filtro con el nombre de archivo.

### <a name="igraphbuilderrender"></a>IGraphBuilder::Render

El [**método IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) compila una subsección de un gráfico. Se inicia desde un pin de salida no conectada y funciona de bajada, agregando nuevos filtros según sea necesario. El filtro inicial ya debe estar en el gráfico. En cada paso, el **método Render** busca un filtro que pueda conectarse al filtro anterior. La secuencia puede bifurcar si un filtro de conexión tiene varios pines de salida. La búsqueda se detiene cuando cada secuencia tiene un representador. Si el **método Render** se queda bloqueado, podría hacer una copia de seguridad e intentarlo de nuevo con un conjunto diferente de filtros.

Para conectar cada pin de salida, el [**método Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) hace lo siguiente:

1.  Si el pin admite la [**interfaz IStreamBuilder,**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) filter Graph Manager delega todo el proceso al método [**IStreamBuilder::Render del**](/windows/desktop/api/Strmif/nf-strmif-istreambuilder-render) pin. Al exponer esta interfaz, el pin asume la responsabilidad de compilar el resto del gráfico, hasta el representador. Sin embargo, muy pocos pines admiten esta interfaz.
2.  El Administrador Graph filtros intenta usar filtros almacenados en caché en memoria, si los hay. A lo largo del proceso de Conectar, el Administrador de Graph filtros puede almacenar en caché los filtros de los pasos anteriores del proceso. (Consulte también Dynamic [Graph Building [Creación dinámica]).](dynamic-graph-building.md)
3.  Si el gráfico de filtros contiene algún filtro con pasadores de entrada no conectados, el Administrador Graph filtros los prueba a continuación. Puede forzar al método [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) a probar un filtro determinado agregando ese filtro al gráfico antes de llamar a **Render**.
4.  A partir Windows 7, DirectShow tiene una lista de filtros preferidos para determinados subtipos multimedia. Si hay un filtro preferido para el tipo de medio que se representa, el Administrador de Graph intenta ese filtro a continuación. Una aplicación puede modificar la lista de filtros preferidos mediante la [**interfaz IAMPluginControl.**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) Los cambios en la lista afectan al proceso actual de la aplicación y se descartan una vez que finaliza el proceso.
5.  Por último, si no se encuentra ningún filtro adecuado, el Administrador de filtros Graph busca en el Registro mediante el método [**IFilterMapper2::EnumMatchingFilters.**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) Intenta hacer coincidir los tipos de medios preferidos del pin de salida con los tipos de medios enumerados en el Registro.

    Cada filtro se registra con un *atributo ,* un valor numérico que indica lo preferible que es el filtro, en relación con otros filtros. El [**método EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) devuelve filtros en orden de mes, con un mínimo de **VALOR DE NO \_ \_ \_ USAR** + 1. Omite los filtros con una gran **cantidad de VALOR DE NO USAR \_ \_ \_ O** menos. Los filtros también se agrupan en categorías, definidas por GUID. Las propias categorías son merecedores, y el método **EnumMatchingFilters** omite cualquier categoría con el grado DE NO USAR **O \_ \_ \_** menos, incluso si los filtros de esa categoría tienen valores de valor más altos.

    A partir Windows 7, DirectShow una lista de filtros bloqueados para determinados subtipos multimedia. Filter Graph Manager omite los filtros de esta lista. Una aplicación puede modificar la lista de filtros bloqueados mediante la [**interfaz IAMPluginControl.**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) Los cambios en esta lista afectan al proceso actual de la aplicación y se descartan una vez que finaliza el proceso.

En resumen, el [**método Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) intenta los filtros en el orden siguiente:

1.  Use [**IStreamBuilder.**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder)
2.  Pruebe los filtros almacenados en caché.
3.  Pruebe los filtros del gráfico.
4.  Windows 7 o posterior: pruebe el filtro preferido para el tipo de medio, si lo hubiera.
5.  Busque filtros en el Registro.

### <a name="igraphbuilderrenderfile"></a>IGraphBuilder::RenderFile

El [**método IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) compila un gráfico de reproducción predeterminado a partir de un nombre de archivo. Internamente, este método usa [**AddSourceFilter para**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) buscar el filtro de origen correcto y [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para compilar el resto del gráfico.

### <a name="igraphbuilderconnect"></a>IGraphBuilder::Conectar

El [**método IGraphBuilder::Conectar**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) conecta un pin de salida a un pin de entrada. Este método agrega filtros intermedios si es necesario, utilizando una variación del algoritmo descrito para el [**método Render:**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)

1.  Pruebe una conexión directa entre los filtros, sin filtros intermedios.
2.  Pruebe los filtros almacenados en caché.
3.  Pruebe los filtros del gráfico.
4.  Windows 7 o posterior: pruebe el filtro preferido para el tipo de medio, si lo hubiera.
5.  Busque filtros en el Registro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías de filtro](filter-categories.md)
</dt> <dt>

[Mérito](merit.md)
</dt> <dt>

[Simulación de Graph building con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[Compilar el filtro Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



