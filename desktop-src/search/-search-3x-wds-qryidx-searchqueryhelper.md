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
# <a name="querying-the-index-with-isearchqueryhelper"></a><span data-ttu-id="9c0a0-104">Consultar el índice con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="9c0a0-104">Querying the Index with ISearchQueryHelper</span></span>

<span data-ttu-id="9c0a0-105">Puede usar la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para consultar el índice.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-105">You can use the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface to query the index.</span></span> <span data-ttu-id="9c0a0-106">Esta interfaz se implementa como una clase auxiliar para [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (y [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) y se obtiene llamando a [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-106">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (and [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)), and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span> <span data-ttu-id="9c0a0-107">Esta interfaz le permite:</span><span class="sxs-lookup"><span data-stu-id="9c0a0-107">This interface permits you to:</span></span>

-   <span data-ttu-id="9c0a0-108">Obtenga una cadena de conexión OLE DB para conectarse a la base de datos de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-108">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
-   <span data-ttu-id="9c0a0-109">Convertir las consultas de usuario de la sintaxis de consulta avanzada (AQS) en Lenguaje de consulta estructurado de Windows Search (SQL).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-109">Convert Advanced Query Syntax (AQS) user queries to Windows Search Structured Query Language (SQL).</span></span>
-   <span data-ttu-id="9c0a0-110">Especifique restricciones de consulta que se pueden expresar en SQL, pero no en AQS.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-110">Specify query restrictions that can be expressed in SQL, but not in AQS.</span></span>

<span data-ttu-id="9c0a0-111">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9c0a0-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="9c0a0-112">Introducción con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="9c0a0-112">Getting Started with ISearchQueryHelper</span></span>](#getting-started-with-isearchqueryhelper)
-   [<span data-ttu-id="9c0a0-113">Usar el método GenerateSqlFromUserQuery</span><span class="sxs-lookup"><span data-stu-id="9c0a0-113">Using the GenerateSqlFromUserQuery Method</span></span>](#using-the-generatesqlfromuserquery-method)
-   [<span data-ttu-id="9c0a0-114">Trabajar con identificadores de configuración regional</span><span class="sxs-lookup"><span data-stu-id="9c0a0-114">Working with Locale Identifiers</span></span>](#working-with-locale-identifiers)
-   [<span data-ttu-id="9c0a0-115">Trabajar con propiedades y columnas</span><span class="sxs-lookup"><span data-stu-id="9c0a0-115">Working with Properties and Columns</span></span>](#working-with-properties-and-columns)
-   [<span data-ttu-id="9c0a0-116">Trabajar con la expansión de términos de consulta</span><span class="sxs-lookup"><span data-stu-id="9c0a0-116">Working with Query Term Expansion</span></span>](#working-with-query-term-expansion)
-   [<span data-ttu-id="9c0a0-117">Trabajar con otros métodos de ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="9c0a0-117">Working with Other ISearchQueryHelper Methods</span></span>](#working-with-other-isearchqueryhelper-methods)
-   [<span data-ttu-id="9c0a0-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9c0a0-118">Related topics</span></span>](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a><span data-ttu-id="9c0a0-119">Introducción con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="9c0a0-119">Getting Started with ISearchQueryHelper</span></span>

<span data-ttu-id="9c0a0-120">Hay algunas interfaces y métodos clave que debe tener en cuenta antes de empezar a realizar consultas mediante programación en la búsqueda de Windows mediante la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="9c0a0-120">There are a few key interfaces and methods you should be aware of before you can start programmatically querying Windows Search using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface.</span></span> <span data-ttu-id="9c0a0-121">En un nivel alto, debe seguir estos pasos:</span><span class="sxs-lookup"><span data-stu-id="9c0a0-121">At a high level, you need to follow these steps:</span></span>

1.  <span data-ttu-id="9c0a0-122">Cree una instancia de [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .</span><span class="sxs-lookup"><span data-stu-id="9c0a0-122">Instantiate an [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) instance.</span></span>
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  <span data-ttu-id="9c0a0-123">Obtenga una instancia de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) mediante [**ISearchManager:: GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-123">Obtain an instance of [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) using [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span></span> <span data-ttu-id="9c0a0-124">El nombre del catálogo del sistema para Windows Search es `SYSTEMINDEX` .</span><span class="sxs-lookup"><span data-stu-id="9c0a0-124">The name of the system catalog for Windows Search is `SYSTEMINDEX`.</span></span>
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  <span data-ttu-id="9c0a0-125">Obtenga una instancia de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) mediante [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-125">Obtain an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) using [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span>
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  <span data-ttu-id="9c0a0-126">Después de tener una instancia de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), puede obtener la cadena de conexión utilizada para conectarse al conector de Windows Search OLE DB Connector.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-126">After you have an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), you can then get the connection string used to connect to the Windows Search index OLE DB connector.</span></span>
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a><span data-ttu-id="9c0a0-127">Usar el método GenerateSqlFromUserQuery</span><span class="sxs-lookup"><span data-stu-id="9c0a0-127">Using the GenerateSqlFromUserQuery Method</span></span>

<span data-ttu-id="9c0a0-128">El método [**ISearchQueryHelper:: GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) transforma la entrada del usuario en una cadena de consulta SQL, que se puede enviar a continuación al proveedor de OLE DB para la búsqueda de Windows.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-128">The [**ISearchQueryHelper::GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) method transforms user input into a SQL query string, which can then be submitted to the OLE DB provider for Windows Search.</span></span> <span data-ttu-id="9c0a0-129">Este método convierte la consulta de sintaxis de consulta [avanzada](-search-3x-advancedquerysyntax.md) (AQS) o la sintaxis de consulta natural (NQS) especificada por el usuario en SQL y permite agregar otros fragmentos de SQL según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-129">This method translates the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md) (AQS) or Natural Query Syntax (NQS) query entered by the user into SQL, and lets you add other SQL fragments as needed.</span></span>

<span data-ttu-id="9c0a0-130">La cadena de consulta SQL se devuelve de la forma siguiente:</span><span class="sxs-lookup"><span data-stu-id="9c0a0-130">The SQL query string is returned in the following form:</span></span>


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



<span data-ttu-id="9c0a0-131">El siguiente es un ejemplo de la cadena de SQL devuelta desde la llamada `GenerateSQLFromUserQuery("comput")` :</span><span class="sxs-lookup"><span data-stu-id="9c0a0-131">The following is an example of the SQL string returned from the call `GenerateSQLFromUserQuery("comput")`:</span></span>


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> <span data-ttu-id="9c0a0-132">El método genera los predicados FREETEXT y Contains porque Contains by by no genera una clasificación significativa.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-132">The method generates both the FREETEXT and the CONTAINS predicates because CONTAINS alone does not generate meaningful ranking.</span></span>

 

## <a name="working-with-locale-identifiers"></a><span data-ttu-id="9c0a0-133">Trabajar con identificadores de configuración regional</span><span class="sxs-lookup"><span data-stu-id="9c0a0-133">Working with Locale Identifiers</span></span>



| <span data-ttu-id="9c0a0-134">Método</span><span class="sxs-lookup"><span data-stu-id="9c0a0-134">Method</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="9c0a0-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c0a0-135">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c0a0-136">[**ISearchQueryHelper:: get \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span><span class="sxs-lookup"><span data-stu-id="9c0a0-136">[**ISearchQueryHelper::get\_QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span></span><br/> [<span data-ttu-id="9c0a0-137">**ISearchQueryHelper::p UT \_ QueryContentLocale**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-137">**ISearchQueryHelper::put\_QueryContentLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | <span data-ttu-id="9c0a0-138">Obtiene o coloca el identificador de código de idioma (LCID) de la consulta.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-138">Gets/Puts the language code identifier (LCID) of the query.</span></span> <span data-ttu-id="9c0a0-139">Esto ayuda a obtener el separador de palabrasización y el analizador correctos para comparar los términos de consulta con el índice inverso o el catálogo.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-139">This helps get the correct wordbreaker and stemmer to compare query terms against the catalog/inverted index.</span></span> <span data-ttu-id="9c0a0-140">El valor predeterminado es la configuración regional de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-140">The default is the current input locale.</span></span> |
| <span data-ttu-id="9c0a0-141">[**ISearchQueryHelper:: get \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span><span class="sxs-lookup"><span data-stu-id="9c0a0-141">[**ISearchQueryHelper::get\_QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span></span><br/> [<span data-ttu-id="9c0a0-142">**ISearchQueryHelper::p UT \_ QueryKeywordLocale**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-142">**ISearchQueryHelper::put\_QueryKeywordLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | <span data-ttu-id="9c0a0-143">Obtiene o coloca el LCID del idioma que se va a utilizar al analizar palabras clave de la sintaxis de consulta avanzada (AQS).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-143">Gets/Puts the LCID for the language to use when parsing Advanced Query Syntax (AQS) keywords.</span></span> <span data-ttu-id="9c0a0-144">El valor predeterminado es la configuración regional predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-144">The default is the default user locale.</span></span>                                                                              |



 

<span data-ttu-id="9c0a0-145">La configuración regional de **contenido** y de **palabras clave** son los identificadores de configuración regional (LCID) que ayudan al motor de búsqueda a usar los separadores de palabras correctos mediante la identificación del idioma de los términos de la consulta y el idioma de las palabras clave de AQS.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-145">The **content locale** and **keyword locale** are locale identifiers (LCID) that help the search engine use the correct word breakers by identifying the language of the query terms and the language the AQS keywords.</span></span> <span data-ttu-id="9c0a0-146">Estos no son siempre los mismos LCID porque Windows Search se ofrece en varias versiones internacionales y también incluye paquetes de interfaz de usuario multilingüe (MUI) para más idiomas.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-146">These are not always the same LCIDs because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="9c0a0-147">La configuración regional de contenido identifica el LCID para el idioma en el que los usuarios escriben su consulta de búsqueda en, mientras que la palabra clave regional identifica el LCID que el motor de búsqueda utiliza al analizar palabras clave de sintaxis de consulta avanzada (AQS).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-147">The content locale identifies the LCID for the language users input their search query in, while the keyword locale identifies the LCID the search engine uses when parsing Advanced Query Syntax (AQS) keywords.</span></span>

<span data-ttu-id="9c0a0-148">Por ejemplo, si tiene la versión en Inglés de Estados Unidos sin paquetes MUI, tanto la configuración regional de contenido como la configuración regional de palabra clave son 1033.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-148">For example, if you have the English-US version with no MUI packs, both the content locale and keyword locale are 1033.</span></span> <span data-ttu-id="9c0a0-149">Si tiene la versión alemana sin paquetes MUI, tanto la configuración regional de contenido como la configuración regional de palabra clave son 1031 (gr-gr).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-149">If you have the German version with no MUI packs, then both the content locale and keyword locale are 1031 (gr-gr).</span></span> <span data-ttu-id="9c0a0-150">Sin embargo, si tiene la versión en inglés con el paquete de MUI de rumano, la configuración regional de contenido es 2072 (RO) y la configuración regional de la palabra clave es 1033 (en-US).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-150">However, if you have the English version with the Romanian MUI pack, the content locale is 2072 (ro) and the keyword locale is 1033 (en-us).</span></span>

## <a name="working-with-properties-and-columns"></a><span data-ttu-id="9c0a0-151">Trabajar con propiedades y columnas</span><span class="sxs-lookup"><span data-stu-id="9c0a0-151">Working with Properties and Columns</span></span>



| <span data-ttu-id="9c0a0-152">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c0a0-152">Methods</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="9c0a0-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c0a0-153">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c0a0-154">[**ISearchQueryHelper:: get \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span><span class="sxs-lookup"><span data-stu-id="9c0a0-154">[**ISearchQueryHelper::get\_QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span></span><br/> [<span data-ttu-id="9c0a0-155">**ISearchQueryHelper::p UT \_ QueryContentProperties**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-155">**ISearchQueryHelper::put\_QueryContentProperties**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | <span data-ttu-id="9c0a0-156">Obtiene o establece las propiedades de contenido para la búsqueda (columna de propiedad enumerada en las cláusulas Contains o FREETEXT).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-156">Gets/Sets the content properties for the search (property column listed in the CONTAINS or FREETEXT clauses).</span></span>                                   |
| <span data-ttu-id="9c0a0-157">[**ISearchQueryHelper:: get \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span><span class="sxs-lookup"><span data-stu-id="9c0a0-157">[**ISearchQueryHelper::get\_QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span></span><br/> [<span data-ttu-id="9c0a0-158">**ISearchQueryHelper::p UT \_ QuerySelectColumns**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-158">**ISearchQueryHelper::put\_QuerySelectColumns**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | <span data-ttu-id="9c0a0-159">Obtiene o establece las columnas (o propiedades) solicitadas en la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-159">Gets/Sets the columns (or properties) requested in the SELECT statement.</span></span> <span data-ttu-id="9c0a0-160">El valor predeterminado es System. ItemUrl y las propiedades que se usan en la cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-160">The default is System.ItemUrl and properties used in the WHERE clause.</span></span> |



 

<span data-ttu-id="9c0a0-161">Los elementos se representan en el almacén de propiedades como una fila.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-161">Items are represented in the property store as a row.</span></span> <span data-ttu-id="9c0a0-162">Cada fila contiene un número de columnas que representan las propiedades de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-162">Each row contains a number of columns that represent properties for that item.</span></span> <span data-ttu-id="9c0a0-163">No todos los elementos tendrán un valor para una propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-163">Not all items will have a value for a given property.</span></span> <span data-ttu-id="9c0a0-164">Por ejemplo, un archivo de audio normalmente no contendría un valor para la propiedad System. Property. FromName, pero puede contener información relacionada con System. Music. artista.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-164">For example, an audio file would typically not contain a value for the System.Property.FromName property but may contain information regarding the System.Music.Artist.</span></span>

<span data-ttu-id="9c0a0-165">Con estos métodos, se tiene acceso o modificación de la propiedad con una cadena Unicode delimitada por comas, terminada en null que especifica uno o más nombres de columna del almacén de propiedades: "System.Document. Autor, System.Document. Título ".</span><span class="sxs-lookup"><span data-stu-id="9c0a0-165">With these methods, you access or modify the property with a comma delimited, null-terminated, Unicode string that specifies one or more column names of the property store: "System.Document.Author, System.Document.Title".</span></span>

## <a name="working-with-query-term-expansion"></a><span data-ttu-id="9c0a0-166">Trabajar con la expansión de términos de consulta</span><span class="sxs-lookup"><span data-stu-id="9c0a0-166">Working with Query Term Expansion</span></span>



| <span data-ttu-id="9c0a0-167">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c0a0-167">Methods</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="9c0a0-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c0a0-168">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="9c0a0-169">**ISearchQueryHelper:: get \_ QueryTermExpansion**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-169">**ISearchQueryHelper::get\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [<span data-ttu-id="9c0a0-170">**ISearchQueryHelper::p UT \_ QueryTermExpansion**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-170">**ISearchQueryHelper::put\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | <span data-ttu-id="9c0a0-171">Obtiene o establece la marca de expansión del término de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-171">Gets/Sets the search term expansion flag.</span></span> |



 

<span data-ttu-id="9c0a0-172">Este método permite la expansión de algunos términos de consulta con caracteres comodín, similar a la expansión de la expresión regular.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-172">This method enables the expansion of some query terms with wild card characters, similar to regular expression expansion.</span></span> <span data-ttu-id="9c0a0-173">La expansión de prefijo busca palabras con el mismo prefijo (diversión/embudo).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-173">Prefix expansion searches for words with the same prefix (fun/funnel).</span></span> <span data-ttu-id="9c0a0-174">Si no se establece, el valor predeterminado es el \_ Prefijo de término de búsqueda \_ \_ ALL.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-174">If not set, the default value is SEARCH\_TERM\_PREFIX\_ALL.</span></span> <span data-ttu-id="9c0a0-175">Los valores admitidos de la enumeración de [**\_ \_ expansión del término de búsqueda**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9c0a0-175">The supported values of the [**SEARCH\_TERM\_EXPANSION**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) enumeration are as follows:</span></span>

-   <span data-ttu-id="9c0a0-176">\_Prefijo \_ \_ de términos de búsqueda todos: todos los términos de búsqueda están expandidos</span><span class="sxs-lookup"><span data-stu-id="9c0a0-176">SEARCH\_TERM\_PREFIX\_ALL - All search terms are expanded</span></span>
-   <span data-ttu-id="9c0a0-177">\_Término \_ de búsqueda sin \_ expansión: no se expanden términos de búsqueda</span><span class="sxs-lookup"><span data-stu-id="9c0a0-177">SEARCH\_TERM\_NO\_EXPANSION - No search terms are expanded</span></span>

## <a name="working-with-other-isearchqueryhelper-methods"></a><span data-ttu-id="9c0a0-178">Trabajar con otros métodos de ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="9c0a0-178">Working with Other ISearchQueryHelper Methods</span></span>

<span data-ttu-id="9c0a0-179">Muchos de los métodos de la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) se usan para establecer argumentos de consulta o definir las propiedades devueltas.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-179">Many of the methods in the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface are used to set query arguments or define the properties returned.</span></span>



| <span data-ttu-id="9c0a0-180">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c0a0-180">Methods</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="9c0a0-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c0a0-181">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c0a0-182">**ISearchQueryHelper:: get \_ ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-182">**ISearchQueryHelper::get\_ConnectionString**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | <span data-ttu-id="9c0a0-183">Devuelve la cadena de conexión de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-183">Returns the OLE DB connection string.</span></span> <span data-ttu-id="9c0a0-184">Este es el método preferido para obtener una cadena de conexión correctamente formateada y correcta.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-184">This is the preferred method of getting a properly formatted and correct connection string.</span></span>                                  |
| [<span data-ttu-id="9c0a0-185">**ISearchQueryHelper:: get \_ QueryMaxResults**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-185">**ISearchQueryHelper::get\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [<span data-ttu-id="9c0a0-186">**ISearchQueryHelper::p UT \_ QueryMaxResults**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-186">**ISearchQueryHelper::put\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | <span data-ttu-id="9c0a0-187">Obtiene o establece el número máximo de resultados que debe devolver una consulta (es decir, SELECT TOP n).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-187">Gets/Sets the maximum number of results to be returned by a query (that is, SELECT TOP n).</span></span> <span data-ttu-id="9c0a0-188">El valor predeterminado es-1, lo que significa que no se genera ninguna cláusula de resultados máxima.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-188">The default is -1, meaning that no maximum results clause is generated.</span></span> |
| [<span data-ttu-id="9c0a0-189">**ISearchQueryHelper:: get \_ QuerySorting**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-189">**ISearchQueryHelper::get\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [<span data-ttu-id="9c0a0-190">**ISearchQueryHelper::p UT \_ QuerySorting**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-190">**ISearchQueryHelper::put\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | <span data-ttu-id="9c0a0-191">Obtiene o establece el criterio de ordenación para el conjunto de resultados de la consulta (ORDER BY).</span><span class="sxs-lookup"><span data-stu-id="9c0a0-191">Gets/Sets the sort order for the query result set (ORDER BY).</span></span> <span data-ttu-id="9c0a0-192">Si no existe ninguna cláusula ORDER BY, los resultados se devuelven en orden no determinista.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-192">If no ORDER BY clause exists, the results are returned in non-deterministic order.</span></span>                   |
| [<span data-ttu-id="9c0a0-193">**ISearchQueryHelper:: get \_ QuerySyntax**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-193">**ISearchQueryHelper::get\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [<span data-ttu-id="9c0a0-194">**ISearchQueryHelper::p UT \_ QuerySyntax**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-194">**ISearchQueryHelper::put\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | <span data-ttu-id="9c0a0-195">Obtiene o establece la sintaxis de la consulta: sintaxis de consulta avanzada o sintaxis de consulta natural.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-195">Gets/Sets the syntax of the query: Advanced Query Syntax or Natural Query Syntax.</span></span>                                                                                  |
| [<span data-ttu-id="9c0a0-196">**ISearchQueryHelper:: get \_ QueryWhereRestrictions**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-196">**ISearchQueryHelper::get\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [<span data-ttu-id="9c0a0-197">**ISearchQueryHelper::p UT \_ QueryWhereRestrictions**</span><span class="sxs-lookup"><span data-stu-id="9c0a0-197">**ISearchQueryHelper::put\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | <span data-ttu-id="9c0a0-198">Obtiene o establece las restricciones que se anexan a través de las cláusulas WHERE.</span><span class="sxs-lookup"><span data-stu-id="9c0a0-198">Gets/Sets the restrictions appended via WHERE clauses.</span></span>                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="9c0a0-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9c0a0-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c0a0-200">Consulta del índice mediante programación</span><span class="sxs-lookup"><span data-stu-id="9c0a0-200">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="9c0a0-201">Uso de enfoques de SQL y AQS para consultar el índice</span><span class="sxs-lookup"><span data-stu-id="9c0a0-201">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="9c0a0-202">Consultar el índice con el protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="9c0a0-202">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="9c0a0-203">Consultar el índice con la sintaxis SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="9c0a0-203">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="9c0a0-204">Usar la sintaxis de consulta avanzada mediante programación</span><span class="sxs-lookup"><span data-stu-id="9c0a0-204">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




