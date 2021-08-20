---
description: Puede usar la interfaz ISearchQueryHelper para consultar el índice. Esta interfaz se implementa como una clase auxiliar para ISearchCatalogManager (e ISearchCatalogManager2) y se obtiene mediante una llamada a ISearchCatalogManager::GetQueryHelper.
ms.assetid: 6e567c09-8763-4866-bf02-ad6651b454db
title: Consulta del índice con ISearchQueryHelper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db9bf2fe8d593d95a1a8f58e25faebb4b76a65ac28fe4c1bc6d6dc2f25ab87d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118052107"
---
# <a name="querying-the-index-with-isearchqueryhelper"></a>Consulta del índice con ISearchQueryHelper

Puede usar la [**interfaz ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para consultar el índice. Esta interfaz se implementa como una clase auxiliar para [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) y se obtiene llamando a [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Esta interfaz le permite:

-   Obtenga una cadena OLE DB de conexión para conectarse a la base de datos Windows Search.
-   Convertir consultas de usuario de advanced query syntax (AQS) en Windows Search Lenguaje de consulta estructurado (SQL).
-   Especifique restricciones de consulta que se pueden expresar en SQL, pero no en AQS.

Este tema se organiza de la siguiente manera:

-   [Tareas iniciales con ISearchQueryHelper](#getting-started-with-isearchqueryhelper)
-   [Usar el método GenerateSqlFromUserQuery](#using-the-generatesqlfromuserquery-method)
-   [Trabajar con identificadores de configuración regional](#working-with-locale-identifiers)
-   [Trabajar con propiedades y columnas](#working-with-properties-and-columns)
-   [Trabajar con la expansión de términos de consulta](#working-with-query-term-expansion)
-   [Trabajar con otros métodos ISearchQueryHelper](#working-with-other-isearchqueryhelper-methods)
-   [Temas relacionados](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a>Tareas iniciales con ISearchQueryHelper

Hay algunas interfaces y métodos clave que debe tener en cuenta antes de empezar a consultar mediante programación Windows Search mediante la [**interfaz ISearchQueryHelper.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) En un nivel alto, debe seguir estos pasos:

1.  Cree una instancia de [**ISearchManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  Obtenga una instancia de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) mediante [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog). El nombre del catálogo del sistema para Windows Search es `SYSTEMINDEX` .
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  Obtenga una instancia de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) mediante [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  Después de tener una instancia de [**ISearchQueryHelper,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)puede obtener la cadena de conexión que se usa para conectarse al índice de Windows Search OLE DB conector.
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a>Usar el método GenerateSqlFromUserQuery

El [**método ISearchQueryHelper::GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) transforma la entrada del usuario en una cadena de consulta de SQL, que luego se puede enviar al proveedor de OLE DB para Windows Search. Este método convierte la consulta Advanced [Query Syntax](-search-3x-advancedquerysyntax.md) (AQS) o Natural Query Syntax (NQS) especificada por el usuario en SQL y le permite agregar otros fragmentos de SQL según sea necesario.

La SQL de consulta se devuelve en el formato siguiente:


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



A continuación se muestra un ejemplo del SQL cadena devuelta por la llamada `GenerateSQLFromUserQuery("comput")` a :


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> El método genera los predicados FREETEXT y CONTAINS porque CONTAINS por sí solo no genera una clasificación significativa.

 

## <a name="working-with-locale-identifiers"></a>Trabajar con identificadores de configuración regional



| Método                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper::get \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/<br/> [**ISearchQueryHelper::put \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | Obtiene o coloca el identificador de código de idioma (LCID) de la consulta. Esto ayuda a obtener el cortador de palabras y el lematizador correctos para comparar los términos de consulta con el catálogo o índice invertido. El valor predeterminado es la configuración regional de entrada actual. |
| [**ISearchQueryHelper::get \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/<br/> [**ISearchQueryHelper::put \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | Obtiene o coloca el LCID del lenguaje que se va a usar al analizar palabras clave de sintaxis de consulta avanzada (AQS). El valor predeterminado es la configuración regional del usuario predeterminada.                                                                              |



 

La configuración **regional** de contenido y la configuración regional de palabras clave son identificadores de configuración regional (LCID) que ayudan al motor de búsqueda a usar los separadores de palabras correctos mediante la identificación del idioma de los términos de consulta y el idioma de las palabras clave de AQS.  No siempre son los mismos LCID porque Windows Search se ofrece en varias versiones internacionales y también incluye paquetes de Interfaz de usuario multilingüe (MUI) para más idiomas. La configuración regional de contenido identifica el LCID para el idioma en el que los usuarios introducen su consulta de búsqueda, mientras que la configuración regional de la palabra clave identifica el LCID que usa el motor de búsqueda al analizar palabras clave de sintaxis de consulta avanzada (AQS).

Por ejemplo, si tiene la versión en inglés-EE. UU. sin paquetes DE NIIA, la configuración regional del contenido y la configuración regional de la palabra clave son 1033. Si tiene la versión en alemán sin paquetes DE MONEDA, la configuración regional del contenido y la configuración regional de la palabra clave son 1031 (gr-gr). Sin embargo, si tiene la versión en inglés con el paquete DE E/S de 2072 (ro), la configuración regional del contenido es 1033 (en-us).

## <a name="working-with-properties-and-columns"></a>Trabajar con propiedades y columnas



| Métodos                                                                                                                                                                                                                                                  | Descripción                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper::get \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/<br/> [**ISearchQueryHelper::put \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | Obtiene o establece las propiedades de contenido de la búsqueda (columna de propiedades enumerada en las cláusulas CONTAINS o FREETEXT).                                   |
| [**ISearchQueryHelper::get \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/<br/> [**ISearchQueryHelper::put \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | Obtiene o establece las columnas (o propiedades) solicitadas en la instrucción SELECT. El valor predeterminado es System.ItemUrl y las propiedades usadas en la cláusula WHERE. |



 

Los elementos se representan en el almacén de propiedades como una fila. Cada fila contiene un número de columnas que representan las propiedades de ese elemento. No todos los elementos tendrán un valor para una propiedad determinada. Por ejemplo, un archivo de audio normalmente no contendrá un valor para la propiedad System.Property.FromName, pero puede contener información relacionada con el sistema. Música. Artista.

Con estos métodos, se accede a la propiedad o se modifica con una cadena Unicode delimitada por comas, terminada en NULL que especifica uno o varios nombres de columna del almacén de propiedades: "System.Document. Autor, System.Document. Title".

## <a name="working-with-query-term-expansion"></a>Trabajar con la expansión de términos de consulta



| Métodos                                                                                                                                                                                                                                 | Descripción                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [**ISearchQueryHelper::get \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [**ISearchQueryHelper::put \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | Obtiene o establece la marca de expansión del término de búsqueda. |



 

Este método permite la expansión de algunos términos de consulta con caracteres comodín, de forma similar a la expansión de expresiones regulares. La expansión de prefijos busca palabras con el mismo prefijo (embudo o embudo). Si no se establece, el valor predeterminado es SEARCH \_ TERM \_ PREFIX \_ ALL. Los valores admitidos de la [**enumeración SEARCH \_ TERM \_ EXPANSION**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) son los siguientes:

-   SEARCH TERM PREFIX ALL : se expanden todos los \_ \_ \_ términos de búsqueda
-   TÉRMINO \_ DE BÚSQUEDA NO \_ \_ EXPANSIÓN: no se expanden términos de búsqueda

## <a name="working-with-other-isearchqueryhelper-methods"></a>Trabajar con otros métodos ISearchQueryHelper

Muchos de los métodos de la [**interfaz ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) se usan para establecer argumentos de consulta o definir las propiedades devueltas.



| Métodos                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper::get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | Devuelve la OLE DB de conexión. Este es el método preferido para obtener una cadena de conexión correcta y con formato correcto.                                  |
| [**ISearchQueryHelper::get \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [**ISearchQueryHelper::put \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | Obtiene o establece el número máximo de resultados que va a devolver una consulta (es decir, SELECT TOP n). El valor predeterminado es -1, lo que significa que no se genera ninguna cláusula de resultados máximo. |
| [**ISearchQueryHelper::get \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [**ISearchQueryHelper::put \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | Obtiene o establece el criterio de ordenación para el conjunto de resultados de la consulta (ORDER BY). Si no existe ninguna cláusula ORDER BY, los resultados se devuelven en orden no determinista.                   |
| [**ISearchQueryHelper::get \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [**ISearchQueryHelper::put \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | Obtiene o establece la sintaxis de la consulta: Sintaxis de consulta avanzada o Sintaxis de consulta natural.                                                                                  |
| [**ISearchQueryHelper::get \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [**ISearchQueryHelper::put \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | Obtiene o establece las restricciones anexadas a través de cláusulas WHERE.                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consulta del índice mediante programación](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Usar SQL y enfoques de AQS para consultar el índice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Consulta del índice con el protocolo search-ms](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Consulta del índice con la sintaxis Windows búsqueda SQL búsqueda](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Usar la sintaxis de consulta avanzada mediante programación](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




