---
description: A partir Windows 7, las incoherencias permanecen en el control y el análisis de direcciones URL. En este tema se proporciona una guía limitada para navegar por incoherencias en formatos de dirección URL de archivo.
ms.assetid: E9792368-517B-4FD7-A244-6C4B7F78B66E
title: Requisitos de formato de dirección URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1bb413501548922eaf1b60801b6d35495d7f8a37dc743675052d4e0e5bae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462237"
---
# <a name="url-formatting-requirements"></a>Requisitos de formato de dirección URL

A partir Windows 7, las incoherencias permanecen en el control y el análisis de direcciones URL. En este tema se proporciona una guía limitada para navegar por incoherencias en formatos de dirección URL de archivo.

Este tema se organiza de la siguiente manera:

-   [Formatos de dirección URL en uso](#url-formats-in-use)
-   [Dirección de barra diagonal, estrella final y sensibilidad de barra diagonal final](#slash-direction-trailing-star-and-trailing-slash-sensitivity)
-   [Formatos de dirección URL por API y consulta](#url-formats-by-api-and-query)
-   [Temas relacionados](#related-topics)

## <a name="url-formats-in-use"></a>Formatos de dirección URL en uso

Los protocolos de terceros son responsables de definir su formato de dirección URL y definir consultas de una manera que se ajuste a su estándar. Por ejemplo, Microsoft Outlook admite nombres de carpeta con caracteres arbitrarios, incluidos los que no son válidos en direcciones URL como el `"?"` carácter. El controlador de protocolos DE LAN realiza su propia codificación de direcciones URL de sus direcciones URL. Por lo tanto, los almacenes de índices en lugar Outlook deben tener esto en cuenta `"%3F"` `"?"` al crear consultas.

Los distintos formatos se enumeran en la tabla siguiente y cada uno tiene asignado un identificador de letra para hacer referencia a ellos más adelante en este tema.



| ID  | Dirección URL de archivo local o remota | Ejemplo                     |
|-----|--------------------------|-----------------------------|
| A   | Local                    | file:///c: ejemplo \\ de \\ prueba\\ |
| B   | Local                    | file:c:/test/example/       |
| C   | Local                    | c: \\ ejemplo de \\ prueba\\         |
| D   | Remoto                   | file:/// recurso \\ \\ compartido de \\ servidor\\ |
| E   | Remoto                   | file://server/share/        |
| F   | Remoto                   | \\\\recurso \\ compartido de servidor\\         |



 

## <a name="slash-direction-trailing-star-and-trailing-slash-sensitivity"></a>Dirección de barra diagonal, estrella final y sensibilidad de barra diagonal final

En Windows búsqueda no hay en gran medida ninguna sensibilidad a la dirección de la barra diagonal. Si se acepta el formato, también se acepta `c:\test\example` c:/test/example. Sin embargo, aunque [SCOPE](-search-sql-folderdepth.md) no suele tener en cuenta la dirección de la barra diagonal, es sensible a la dirección de la barra diagonal en el caso del formato de dirección URL remota F. Por lo tanto, no `Scope = '//server/share'` funciona.

La única API que es sensible a las estrellas finales y distingue entre `c:\test\ ` `c:\test\*` y es [**ISearchCrawlScopeManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) Si hay una regla de exclusión para , se indexará el propio directorio de dirección `c:\test\*` `c:\test` URL. Pero si la dirección URL de exclusión es , no se indexará el `c:\test\` propio directorio de dirección `c:\test` URL.

Hay dos lugares en los que Windows Search es sensible a las barras diagonales finales: ItemUrl y Path. Si hay un directorio , Windows Search trata de `c:\test` forma diferente a para `c:\test\` `c:\test` predicados como y `path = 'c:\test'` `System.ItemUrl = 'c:\test'` . Por ejemplo, el predicado coincidiría con el directorio , pero `path='file:c:/test'` `c:\test` no lo `path='file:c:/test/'` haría, debido a la barra diagonal final.

## <a name="url-formats-by-api-and-query"></a>Formatos de dirección URL por API y consulta

Los formatos de dirección URL de archivo local aceptados por las API y consultas seleccionadas se enumeran en la tabla siguiente. Los formatos están asociados a una letra (de A a F), cuyo significado se denotó en la sección["Formatos](#url-formats-in-use)de dirección URL en uso" anteriormente en este tema.



| API o consulta                                                                                                    | Formato A | Formato B | Formato C |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | Y        | N        | Y        |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | Y        | Y        | Y        |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | Y        | Y        | Y        |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | Y        | N        | N        |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | Y        | Y        | Y        |
| Ámbito=                                                                                                          | N        | Y        | Y        |
| Directory=                                                                                                      | N        | Y        | Y        |
| ItemUrl=                                                                                                        | N        | Y        | Y        |
| Ruta de acceso=                                                                                                           | N        | Y        | Y        |



 

Los formatos de dirección URL de archivo remotos aceptados por las consultas seleccionadas se enumeran en la tabla siguiente.



| Consulta                                                                                                           | Formato D | Formato E | Formato F |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | N/D      | N/D      | N/D      |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | N/D      | N/D      | N/D      |
| Ámbito=                                                                                                          | Y        | Y        | Y        |
| Directorio=                                                                                                      | Y        | Y        | Y        |
| ItemUrl=                                                                                                        | Y        | Y        | Y        |
| Ruta de acceso=                                                                                                           | Y        | Y        | Y        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Qué se incluye en el índice](-search-indexing-process-overview.md)
</dt> <dt>

[Proceso de indexación en Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Proceso de consulta en Windows Búsqueda](querying-process--windows-search-.md)
</dt> <dt>

[Proceso de notificaciones en Windows Search](-search-3x-wds-support.md)
</dt> </dl>

 

 
