---
description: 'Puede usar la interfaz ISearchQueryHelper para consultar el índice. Esta interfaz se implementa como una clase auxiliar para ISearchCatalogManager (y ISearchCatalogManager2) y se obtiene llamando a ISearchCatalogManager:: GetQueryHelper.'
ms.assetid: 6e567c09-8763-4866-bf02-ad6651b454db
title: Consultar el índice con ISearchQueryHelper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b9d970a1e3f416081d3b7fd3e9d6c2af0a2bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275269"
---
# <a name="querying-the-index-with-isearchqueryhelper"></a>Consultar el índice con ISearchQueryHelper

Puede usar la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para consultar el índice. Esta interfaz se implementa como una clase auxiliar para [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (y [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) y se obtiene llamando a [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Esta interfaz le permite:

-   Obtenga una cadena de conexión OLE DB para conectarse a la base de datos de Windows Search.
-   Convertir las consultas de usuario de la sintaxis de consulta avanzada (AQS) en Lenguaje de consulta estructurado de Windows Search (SQL).
-   Especifique restricciones de consulta que se pueden expresar en SQL, pero no en AQS.

Este tema se organiza de la siguiente manera:

-   [Introducción con ISearchQueryHelper](#getting-started-with-isearchqueryhelper)
-   [Usar el método GenerateSqlFromUserQuery](#using-the-generatesqlfromuserquery-method)
-   [Trabajar con identificadores de configuración regional](#working-with-locale-identifiers)
-   [Trabajar con propiedades y columnas](#working-with-properties-and-columns)
-   [Trabajar con la expansión de términos de consulta](#working-with-query-term-expansion)
-   [Trabajar con otros métodos de ISearchQueryHelper](#working-with-other-isearchqueryhelper-methods)
-   [Temas relacionados](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a>Introducción con ISearchQueryHelper

Hay algunas interfaces y métodos clave que debe tener en cuenta antes de empezar a realizar consultas mediante programación en la búsqueda de Windows mediante la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) . En un nivel alto, debe seguir estos pasos:

1.  Cree una instancia de [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  Obtenga una instancia de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) mediante [**ISearchManager:: GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog). El nombre del catálogo del sistema para Windows Search es `SYSTEMINDEX` .
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  Obtenga una instancia de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) mediante [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  Después de tener una instancia de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), puede obtener la cadena de conexión utilizada para conectarse al conector de Windows Search OLE DB Connector.
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a>Usar el método GenerateSqlFromUserQuery

El método [**ISearchQueryHelper:: GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) transforma la entrada del usuario en una cadena de consulta SQL, que se puede enviar a continuación al proveedor de OLE DB para la búsqueda de Windows. Este método convierte la consulta de sintaxis de consulta [avanzada](-search-3x-advancedquerysyntax.md) (AQS) o la sintaxis de consulta natural (NQS) especificada por el usuario en SQL y permite agregar otros fragmentos de SQL según sea necesario.

La cadena de consulta SQL se devuelve de la forma siguiente:


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



El siguiente es un ejemplo de la cadena de SQL devuelta desde la llamada `GenerateSQLFromUserQuery("comput")` :


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> El método genera los predicados FREETEXT y Contains porque Contains by by no genera una clasificación significativa.

 

## <a name="working-with-locale-identifiers"></a>Trabajar con identificadores de configuración regional



| Método                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper:: get \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/<br/> [**ISearchQueryHelper::p UT \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | Obtiene o coloca el identificador de código de idioma (LCID) de la consulta. Esto ayuda a obtener el separador de palabrasización y el analizador correctos para comparar los términos de consulta con el índice inverso o el catálogo. El valor predeterminado es la configuración regional de entrada actual. |
| [**ISearchQueryHelper:: get \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/<br/> [**ISearchQueryHelper::p UT \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | Obtiene o coloca el LCID del idioma que se va a utilizar al analizar palabras clave de la sintaxis de consulta avanzada (AQS). El valor predeterminado es la configuración regional predeterminada del usuario.                                                                              |



 

La configuración regional de **contenido** y de **palabras clave** son los identificadores de configuración regional (LCID) que ayudan al motor de búsqueda a usar los separadores de palabras correctos mediante la identificación del idioma de los términos de la consulta y el idioma de las palabras clave de AQS. Estos no son siempre los mismos LCID porque Windows Search se ofrece en varias versiones internacionales y también incluye paquetes de interfaz de usuario multilingüe (MUI) para más idiomas. La configuración regional de contenido identifica el LCID para el idioma en el que los usuarios escriben su consulta de búsqueda en, mientras que la palabra clave regional identifica el LCID que el motor de búsqueda utiliza al analizar palabras clave de sintaxis de consulta avanzada (AQS).

Por ejemplo, si tiene la versión en Inglés de Estados Unidos sin paquetes MUI, tanto la configuración regional de contenido como la configuración regional de palabra clave son 1033. Si tiene la versión alemana sin paquetes MUI, tanto la configuración regional de contenido como la configuración regional de palabra clave son 1031 (gr-gr). Sin embargo, si tiene la versión en inglés con el paquete de MUI de rumano, la configuración regional de contenido es 2072 (RO) y la configuración regional de la palabra clave es 1033 (en-US).

## <a name="working-with-properties-and-columns"></a>Trabajar con propiedades y columnas



| Métodos                                                                                                                                                                                                                                                  | Descripción                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper:: get \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/<br/> [**ISearchQueryHelper::p UT \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | Obtiene o establece las propiedades de contenido para la búsqueda (columna de propiedad enumerada en las cláusulas Contains o FREETEXT).                                   |
| [**ISearchQueryHelper:: get \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/<br/> [**ISearchQueryHelper::p UT \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | Obtiene o establece las columnas (o propiedades) solicitadas en la instrucción SELECT. El valor predeterminado es System. ItemUrl y las propiedades que se usan en la cláusula WHERE. |



 

Los elementos se representan en el almacén de propiedades como una fila. Cada fila contiene un número de columnas que representan las propiedades de ese elemento. No todos los elementos tendrán un valor para una propiedad determinada. Por ejemplo, un archivo de audio normalmente no contendría un valor para la propiedad System. Property. FromName, pero puede contener información relacionada con System. Music. artista.

Con estos métodos, se tiene acceso o modificación de la propiedad con una cadena Unicode delimitada por comas, terminada en null que especifica uno o más nombres de columna del almacén de propiedades: "System.Document. Autor, System.Document. Título ".

## <a name="working-with-query-term-expansion"></a>Trabajar con la expansión de términos de consulta



| Métodos                                                                                                                                                                                                                                 | Descripción                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [**ISearchQueryHelper:: get \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [**ISearchQueryHelper::p UT \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | Obtiene o establece la marca de expansión del término de búsqueda. |



 

Este método permite la expansión de algunos términos de consulta con caracteres comodín, similar a la expansión de la expresión regular. La expansión de prefijo busca palabras con el mismo prefijo (diversión/embudo). Si no se establece, el valor predeterminado es el \_ Prefijo de término de búsqueda \_ \_ ALL. Los valores admitidos de la enumeración de [**\_ \_ expansión del término de búsqueda**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) son los siguientes:

-   \_Prefijo \_ \_ de términos de búsqueda todos: todos los términos de búsqueda están expandidos
-   \_Término \_ de búsqueda sin \_ expansión: no se expanden términos de búsqueda

## <a name="working-with-other-isearchqueryhelper-methods"></a>Trabajar con otros métodos de ISearchQueryHelper

Muchos de los métodos de la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) se usan para establecer argumentos de consulta o definir las propiedades devueltas.



| Métodos                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper:: get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | Devuelve la cadena de conexión de OLE DB. Este es el método preferido para obtener una cadena de conexión correctamente formateada y correcta.                                  |
| [**ISearchQueryHelper:: get \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [**ISearchQueryHelper::p UT \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | Obtiene o establece el número máximo de resultados que debe devolver una consulta (es decir, SELECT TOP n). El valor predeterminado es-1, lo que significa que no se genera ninguna cláusula de resultados máxima. |
| [**ISearchQueryHelper:: get \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [**ISearchQueryHelper::p UT \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | Obtiene o establece el criterio de ordenación para el conjunto de resultados de la consulta (ORDER BY). Si no existe ninguna cláusula ORDER BY, los resultados se devuelven en orden no determinista.                   |
| [**ISearchQueryHelper:: get \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [**ISearchQueryHelper::p UT \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | Obtiene o establece la sintaxis de la consulta: sintaxis de consulta avanzada o sintaxis de consulta natural.                                                                                  |
| [**ISearchQueryHelper:: get \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [**ISearchQueryHelper::p UT \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | Obtiene o establece las restricciones que se anexan a través de las cláusulas WHERE.                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consulta del índice mediante programación](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Uso de enfoques de SQL y AQS para consultar el índice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Consultar el índice con el protocolo Search-MS](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Consultar el índice con la sintaxis SQL de Windows Search](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Usar la sintaxis de consulta avanzada mediante programación](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




