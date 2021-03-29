---
description: A partir de Windows 7, las incoherencias permanecen en el control y el análisis de direcciones URL. En este tema se proporciona una guía limitada para desplazarse por las incoherencias en los formatos de URL de archivo.
ms.assetid: E9792368-517B-4FD7-A244-6C4B7F78B66E
title: Requisitos de formato de dirección URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08d7945578118f4d3103f44e6da60b96022e472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540611"
---
# <a name="url-formatting-requirements"></a>Requisitos de formato de dirección URL

A partir de Windows 7, las incoherencias permanecen en el control y el análisis de direcciones URL. En este tema se proporciona una guía limitada para desplazarse por las incoherencias en los formatos de URL de archivo.

Este tema se organiza de la siguiente manera:

-   [Formatos de dirección URL en uso](#url-formats-in-use)
-   [Dirección de barra diagonal, estrella final y la barra diagonal final](#slash-direction-trailing-star-and-trailing-slash-sensitivity)
-   [Formatos de dirección URL por API y consulta](#url-formats-by-api-and-query)
-   [Temas relacionados](#related-topics)

## <a name="url-formats-in-use"></a>Formatos de dirección URL en uso

Los protocolos de terceros son responsables de definir el formato de la dirección URL y de definir consultas de manera que se ajuste a su estándar. Por ejemplo, Microsoft Outlook admite nombres de carpeta con caracteres arbitrarios, incluidos los que no son válidos en direcciones URL como el `"?"` carácter. El controlador de protocolo MAPI realiza su propia codificación de dirección URL de sus direcciones URL. Por lo tanto, el índice almacena `"%3F"` en lugar de `"?"` y Outlook debe tener esto en cuenta al crear consultas.

En la tabla siguiente se enumeran los distintos formatos y se les asigna un identificador de letra para hacer referencia a ellos más adelante en este tema.



| id  | Dirección URL del archivo local o remota | Ejemplo                     |
|-----|--------------------------|-----------------------------|
| A   | Local                    | file:///c: \\ ejemplo de prueba \\\\ |
| B   | Local                    | archivo: c:/test/example/       |
| C   | Local                    | c: \\ ejemplo de prueba \\\\         |
| D   | Remote                   | \\ \\ \\ recurso compartido de File:///Server\\ |
| E   | Remote                   | file://server/share/        |
| F   | Remote                   | \\\\\\recurso compartido de servidor\\         |



 

## <a name="slash-direction-trailing-star-and-trailing-slash-sensitivity"></a>Dirección de barra diagonal, estrella final y la barra diagonal final

En Windows Search, no hay mucha sensibilidad a la dirección de la barra diagonal. Si `c:\test\example` se acepta el formato, se acepta también c:/test/example. Sin embargo, aunque el [ámbito](-search-sql-folderdepth.md) no suele ser sensible a la dirección de la barra diagonal, es sensible a la dirección de la barra diagonal en el caso del formato de dirección URL remota F. por lo tanto, no `Scope = '//server/share'` funciona.

La única API que es sensible a las estrellas finales y distingue entre `c:\test\ ` y `c:\test\*` es [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager). Si hay una regla de exclusión para `c:\test\*` , el propio directorio de la dirección URL `c:\test` se seguirá indizando. Pero si la dirección URL de exclusión es `c:\test\` , el directorio de la dirección URL `c:\test` no se indexará.

Hay dos lugares donde Windows Search es sensible a las barras diagonales finales: ItemUrl y path queries. Si hay un directorio `c:\test` , Windows Search trata `c:\test\` de forma diferente de los `c:\test` predicados como `path = 'c:\test'` y `System.ItemUrl = 'c:\test'` . Por ejemplo, el predicado `path='file:c:/test'` coincidiría con el directorio `c:\test` , pero `path='file:c:/test/'` no, debido a la barra diagonal final.

## <a name="url-formats-by-api-and-query"></a>Formatos de dirección URL por API y consulta

En la tabla siguiente se enumeran los formatos de dirección URL de archivo local que aceptan las API y consultas seleccionadas. Los formatos están asociados a una letra (de la a a la F), cuyo significado se ha indicado en la sección "[formatos de dirección URL en uso](#url-formats-in-use)", anteriormente en este tema.



| API o consulta                                                                                                    | Dar formato A un | Formato B | Formato C |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | Y        | N        | Y        |
| [**IGatherNotifyInline:: OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | Y        | Y        | Y        |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | Y        | Y        | Y        |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | Y        | N        | N        |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | Y        | Y        | Y        |
| Ámbito =                                                                                                          | N        | Y        | Y        |
| Directorio =                                                                                                      | N        | Y        | Y        |
| ItemUrl =                                                                                                        | N        | Y        | Y        |
| Ruta de acceso =                                                                                                           | N        | Y        | Y        |



 

En la tabla siguiente se enumeran los formatos de dirección URL de archivo remoto que aceptan las consultas seleccionadas.



| Consultar                                                                                                           | Formato D | Formato E | Formato F |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | N/D      | N/D      | N/D      |
| [**IGatherNotifyInline:: OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | N/D      | N/D      | N/D      |
| Ámbito =                                                                                                          | Y        | Y        | Y        |
| Directorio =                                                                                                      | Y        | Y        | Y        |
| ItemUrl =                                                                                                        | Y        | Y        | Y        |
| Ruta de acceso =                                                                                                           | Y        | Y        | Y        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Qué se incluye en el índice](-search-indexing-process-overview.md)
</dt> <dt>

[Proceso de indexación en Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Consulta del proceso en Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Proceso de notificaciones en Windows Search](-search-3x-wds-support.md)
</dt> </dl>

 

 
