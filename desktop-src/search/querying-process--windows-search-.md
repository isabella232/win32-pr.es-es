---
description: .
ms.assetid: 0e5a633e-1703-4b72-8a04-6da71aec0ae2
title: Consulta del proceso en Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d92d868cb843e96b04d6b4bd575284638b6652ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808911"
---
# <a name="querying-process-in-windows-search"></a>Consulta del proceso en Windows Search

Este tema se organiza de la siguiente manera:

-   [Acerca de las consultas en Windows Search](#about-querying-in-windows-search)
    -   [Consultas locales y remotas](#local-and-remote-queries)
    -   [Información general sobre la API de consulta estructurada](#structured-query-api-overview)
-   [Consultar escenarios](#querying-scenarios)
    -   [Extracción de condiciones y análisis de consultas](#condition-extraction-and-query-parsing)
    -   [Consultar el índice](#querying-the-index)
-   [Temas relacionados](#related-topics)

## <a name="about-querying-in-windows-search"></a>Acerca de las consultas en Windows Search

La consulta en Windows Search se basa en los cuatro métodos siguientes:

-   [Sintaxis de consulta avanzada](-search-3x-advancedquerysyntax.md) (AQS)
-   Sintaxis de consulta natural (NQS)
-   Lenguaje de consulta estructurado (SQL)
-   Interfaces de consulta estructuradas

AQS es la sintaxis de consulta predeterminada que usa Windows Search para consultar el índice y para refinar y restringir los parámetros de búsqueda. AQS es principalmente orientada al usuario y puede ser utilizada por los usuarios para compilar consultas AQS, pero también pueden ser usadas por los desarrolladores para compilar consultas mediante programación. En Windows 7, se presentó una AQS canónica y se debe usar para generar consultas AQS mediante programación. En Windows 7 y versiones posteriores, una opción de menú contextual puede estar disponible en función de si se cumple una condición de AQS. Para obtener más información, vea "obtener el comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada" en [crear controladores de menú contextuales](../shell/context-menu-handlers.md). Las consultas AQS se pueden limitar a tipos específicos de archivos, que se conocen como tipos de archivo. Para obtener más información, vea [tipos de archivo y asociaciones](../shell/fa-intro.md). Para obtener documentación de referencia sobre las propiedades pertinentes, vea [System. Kind](../properties/props-system-kind.md)y [System. KindText](../properties/props-system-kindtext.md).

NQS es una sintaxis de consulta que es más relajada que AQS y es similar a la lengua humana. La búsqueda de Windows puede usar NQS para consultar el índice si se selecciona NQS en lugar del valor predeterminado, AQS.

SQL es un lenguaje de texto que define las consultas. SQL es común en muchas tecnologías de base de datos diferentes. Windows Search usa SQL, implementa un subconjunto del mismo y lo amplía agregando elementos al lenguaje. Windows Search SQL amplía la sintaxis de consulta de base de datos SQL-92 y SQL-99 para mejorar su utilidad con las búsquedas basadas en texto. Todas las características de Windows Search SQL son compatibles con Windows Search en Windows XP y Windows Server 2003 y versiones posteriores. Para obtener más información sobre SQL Search, vea [consultar el índice con la sintaxis de SQL](-search-sql-windowssearch-entry.md)de Windows Search e [información general sobre la sintaxis SQL de Windows Search](-search-sql-ovwofsearchquery.md).

Las API de consulta estructurada se describen más adelante en este tema. Para obtener documentación de referencia sobre las API de consulta estructurada, vea [consultar interfaces](-search-querying-interfaces-entry-page.md). Las interfaces como [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) ayudan a construir cadenas SQL a partir de un conjunto de valores de entrada. Esta interfaz convierte las consultas de usuario AQS en SQL de búsqueda de Windows y especifica restricciones de consulta que se pueden expresar en SQL, pero no en AQS. [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) también obtiene una cadena de conexión OLE DB para conectarse a la base de datos de Windows Search.

### <a name="local-and-remote-queries"></a>Consultas locales y remotas

Puede ejecutar las consultas de forma local o remota. En el ejemplo siguiente se muestra una consulta local con la [cláusula FROM](-search-sql-from.md) . Una consulta local solo consulta el catálogo SystemIndex local.


```
FROM SystemIndex
```



En el ejemplo siguiente se muestra una consulta remota con la [cláusula FROM](-search-sql-from.md) . Al agregar ComputerName, se transforma el ejemplo anterior en una consulta remota.


```
FROM [<ComputerName>.]SystemIndex
```



De forma predeterminada, Windows XP y Windows Server 2003 no tienen instalado Windows Search. Solo Windows Search 4 (WS4) proporciona compatibilidad con consultas remotas. Las versiones anteriores de la búsqueda de escritorio de Windows (WDS), como 3,01 y versiones anteriores, no admiten las consultas remotas. Con el explorador de Windows puede consultar el índice local de un equipo remoto para los elementos del sistema de archivos (elementos administrados por el protocolo "File:").

Para recuperar un elemento mediante una consulta remota, el elemento debe cumplir los siguientes requisitos:

-   Ser accesible a través de la ruta de acceso UNC (Convención de nomenclatura universal).
-   Existe en el equipo remoto al que el cliente tiene acceso.
-   Tenga su seguridad establecida para permitir que el cliente tenga acceso de lectura.

El explorador de Windows tiene características para compartir elementos, incluido un recurso compartido "público" ( \\ \\ equipo \\ público \\ ...) en el **centro de redes y recursos compartidos**, y un recurso compartido de "usuarios" ( \\ \\ \\ usuarios de la máquina \\ ...) para elementos compartidos mediante el Asistente para compartir. Después de compartir las carpetas, puede consultar el índice local especificando el nombre del equipo del equipo remoto en la cláusula FROM y una ruta de acceso UNC en el equipo remoto en la cláusula SCOPE. En el ejemplo siguiente se muestra una consulta remota con las cláusulas FROM y SCOPE.


```
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>' 
```



Los ejemplos que se proporcionan aquí usan SQL.

### <a name="structured-query-api-overview"></a>Información general sobre la API de consulta estructurada

Una consulta estructurada proporciona la capacidad de buscar información por combinaciones booleanas de consultas sobre propiedades individuales. En este tema se describe la funcionalidad de las API y los métodos de consulta estructurados más importantes. Para obtener documentación de referencia sobre las API de consulta estructurada, vea [consultar interfaces](-search-querying-interfaces-entry-page.md).

### <a name="iqueryparser"></a>IQueryParser

El método [**IQueryParser::P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) analiza una cadena de entrada del usuario y genera una interpretación en forma de [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution). Si el parámetro *pCustomProperties* de ese método no es null, es una enumeración de objetos [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) (uno para cada propiedad personalizada reconocida). Los otros métodos de [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) permiten que la aplicación establezca varias opciones, como la configuración regional, un esquema, un separador de palabras y controladores para varios tipos de entidades con nombre. [**IQueryParser:: GetSchemaProvider**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-getschemaprovider) devuelve una interfaz [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) para examinar el esquema cargado.

### <a name="iquerysolution--iconditionfactory"></a>IQuerySolution : IConditionFactory

La interfaz [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) proporciona toda la información sobre el resultado del análisis de una cadena de entrada. Dado que **IQuerySolution** también es una interfaz [**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) , se pueden crear nodos de árbol de condiciones adicionales. El método [**IQuerySolution:: GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) genera un árbol de condiciones para la interpretación. **IQuerySolution:: GetQuery** también devuelve el tipo semántico.

### <a name="iconditionfactory"></a>IConditionFactory

[**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) crea nodos de árbol de condiciones. Si el parámetro de *simplificación* de [**IConditionFactory:: MakeNot**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makenot) es **Variant \_ true**, se simplifica la [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) resultante y no es necesario que sea un nodo de negación. Si el parámetro *pSubConditions* de [**IConditionFactory:: MakeAndOr**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeandor) no es null, ese parámetro debe ser una enumeración de los objetos [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) y convertirse en subárboles. [**IConditionFactory:: MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf) crea un nodo hoja con un nombre de propiedad, una operación y un valor especificados. La cadena del parámetro *pValueType* debe ser el nombre de un tipo semántico del esquema. Si el parámetro *Expand* es **Variant \_ true** y la propiedad es virtual, el árbol de condiciones resultante suele ser una disyunción derivada de expandir la propiedad a sus componentes definidos. Si no es null, los parámetros *pPropertyNameTerm*, *pOperatorTerm* y *pValueTerm* deben identificar los términos que indican la propiedad, la operación y el valor.

### <a name="icondition--ipersiststream"></a>ICondition: IPersistStream

La interfaz [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) es un nodo único en un árbol de condiciones. El nodo puede ser un nodo de negación, un nodo, un nodo o un nodo hoja. Para un nodo no hoja [**ICondition:: GetSubConditions**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getsubconditions) devuelve una enumeración de los subárboles. Para un nodo hoja, los siguientes métodos de [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) devuelven los siguientes valores:

-   [**GetComparisonInfo**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo) devuelve el nombre, la operación y el valor de la propiedad.
-   [**GetValueType**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluetype) devuelve el tipo semántico del valor, que se specificied en el parámetro *pszValueType* de [**IConditionFactory:: MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf).
-   [**GetValueNormalization**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluenormalization) devuelve una forma de cadena del valor. (Si el valor ya era una cadena, este formulario se normalizará con respecto a mayúsculas y minúsculas, etc.)
-   [**GetInputTerms**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms) devuelve información sobre qué partes de la oración de entrada generaron el nombre de la propiedad, la operación y el valor.
-   [**Clone**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone) devuelve una copia en profundidad de un árbol de condiciones.

### <a name="irichchunk"></a>IRichChunk

Cada objeto [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) identifica un intervalo de token y una cadena. **IRichChunk** es una interfaz de utilidad que representa información sobre un intervalo (normalmente un intervalo de tokens) identificado por una posición inicial y una longitud. Esta información de intervalo incluye una cadena o una **variante**.

### <a name="iconditiongenerator"></a>IConditionGenerator

La aplicación proporciona la interfaz [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) para controlar el reconocimiento y la generación del árbol de condiciones para un tipo de entidad con nombre. Se asigna un generador de condiciones a un [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) a través de [**IQueryParser:: SetMultiOption**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-setmultioption). [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) llama a [**IConditionGenerator:: Initialize**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-initialize) con un [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) para el esquema cargado actualmente. Esto permite a [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) obtener cualquier información de esquema necesaria. Al analizar una cadena de entrada, **IQueryParser** llama al método [**IConditionGenerator:: RecognizeNamedEntities**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-recognizenamedentities) de cada [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator), de modo que se puede informar de la aparición de entidades con nombre que reconoce en la cadena de entrada. **IQueryParser** puede usar la configuración regional actual y debe hacer uso de la tokenización de la entrada, ya que necesita informar de los intervalos de token de las entidades con nombre.

Cuando [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) está a punto de emitir un nodo hoja y el tipo semántico del valor coincide con el tipo de entidad con nombre para un [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator), **IQueryParser** llama a [**IConditionGenerator:: GenerateforLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf) con la información del nodo que se va a generar. Si [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) devuelve S \_ OK, debe devolver un árbol de condiciones (que no tiene que ser un nodo hoja) e informar a **IQueryParser** de si se debe suprimir la interpretación de cadena alternativa que normalmente generaría como precaución.

### <a name="itokencollection"></a>ITokenCollection

El método [**ITokenCollection:: NumberOfTokens**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-numberoftokens) devuelve el número de tokens. [**ITokenCollection:: GetToken**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-gettoken) devuelve información sobre el token *i*. El principio y la longitud son posiciones de caracteres en la cadena de entrada. El texto devuelto no será null solo si hay un texto que invalide los caracteres de la cadena de entrada. Esto se usa, por ejemplo, para reemplazar un guión de la cadena de entrada con NOT cuando ese guión está en un contexto donde se debe interpretar como una negación.

### <a name="inamedentitycollector"></a>INamedEntityCollector

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) llama a [**INamedEntityCollector:: Add**](/windows/desktop/api/Structuredquery/nf-structuredquery-inamedentitycollector-add) para cada entidad con nombre que reconoció. Los intervalos son intervalos de tokens. Siempre debe ser el caso de *beginSpan* ? *beginActual*  <  *endActual* ? *endSpan*. *beginSpan* y *endSpan* pueden diferir de *beginActual* y *endActual* si la entidad con nombre comienza o termina con tokens semánticamente insignificantes, como comillas (que no están incluidas en la entidad con nombre). El valor se debe expresar como una cadena y aparecerá posteriormente en una llamada a [**IConditionGenerator:: GenerateForLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf).

### <a name="ischemaprovider"></a>ISchemaProvider

La interfaz [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) se puede usar para examinar un esquema cargado para entidades (tipos) y relaciones (propiedades). Estos son los métodos individuales:

-   [**Entidades**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-entities) devuelve una enumeración de todas las entidades ([**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity)) del esquema.
-   [**RootEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-rootentity) devuelve la entidad raíz del esquema. Para un esquema plano, se devuelve el tipo principal de cada [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) .
-   [**GetEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-getentity) busca una entidad por su nombre y devuelve S \_ false si no hay ninguna entidad en el esquema.
-   [**Metadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-metadata) devuelve una enumeración de las interfaces [**IMetaData**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) .

### <a name="ientity"></a>IEntity

La interfaz [**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity) es una entidad de esquema que representa un tipo que tiene un nombre, tiene varias relaciones con nombre para otros tipos (propiedades) y se deriva de una entidad base. Estos son los métodos individuales:

-   [**IEntity:: Relationships**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-relationships) devuelve una enumeración de objetos [**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) , uno para cada relación de salida de este tipo. Cada relación saliente de una entidad tiene un nombre.
-   [**IEntity:: GetRelationship**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-getrelationship) busca una relación por nombre y devuelve S \_ false si no hay ninguna relación de este tipo para esta entidad.
-   [**IEntity:: Metadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-metadata) devuelve una enumeración de interfaces [**IMetaData**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) , una para cada par de metadatos de esta entidad.
-   [**IEntity::D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-defaultphrase) devuelve una frase predeterminada para facilitar la generación de una reexpresión AQS o NQS de un árbol de condiciones.

### <a name="irelationship"></a>IRelationship

La interfaz [**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) representa una relación entre dos entidades: un origen y un destino. Estos son los métodos individuales:

-   [**IRelationship:: IsReal**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-isreal) informa de si una relación es real. Por ejemplo, si la entidad A deriva de la entidad B y hereda una relación denominada R de ella, todavía puede tener su propia relación denominada R. Sin embargo, la relación beween A y R debe tener el mismo tipo de destino que el de B, y la única razón para que exista es almacenar los metadatos específicos de B. Se dice que una relación de B no es real.
-   [**IRelationship:: metadatos**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-metadata) devuelve una enumeración de interfaces [**IMetaData**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) , una para cada par de metadatos de esta entidad.
-   [**IRelationship::D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-defaultphrase) devuelve la frase predeterminada que se va a usar para esta relación en las reinstrucciones. Cada relación tiene una frase predeterminada que indica que facilite la generación de una reexpresión AQS o NQS de un árbol de condiciones.

### <a name="imetadata"></a>IMetaData

Los metadatos son pares clave-valor que están asociados a una entidad, una relación o todo el esquema. Dado que las claves no son necesariamente únicas, una colección de metadatos se puede considerar como un mapa múltiple. Se llama a [**IMetaData:: GetData**](/windows/desktop/api/Structuredquery/nf-structuredquery-imetadata-getdata) para recuperar la clave y el valor de un par metatdata.

## <a name="querying-scenarios"></a>Consultar escenarios

En los escenarios siguientes se describe el uso de las API de consulta estructuradas en la búsqueda de Windows en escenarios comunes de consulta, como la creación de un árbol de condiciones y la consulta del índice.

### <a name="condition-extraction-and-query-parsing"></a>Extracción de condiciones y análisis de consultas

Cuando se crea una consulta, su ámbito se define indicando al sistema dónde debe realizarse la búsqueda. Esto restringe los resultados de la búsqueda. Una vez definido el ámbito, se aplica un filtro y se devuelve un conjunto de filtros. Los resultados de la búsqueda se restringen mediante la creación de un árbol de condiciones con nodos hoja, similar a un gráfico. Después se extraen esas condiciones. Un árbol de condiciones es una combinación booleana (AND, OR, NOT) de las condiciones hoja, cada una de las cuales relaciona una propiedad, a través de una operación, con un valor. Un nodo hoja representa una restricción de una sola propiedad a un valor a través de algunas operaciones.

Una restricción de filtro requiere una expresión lógica que describa la restricción. La definición de esta expresión se inicia con la interfaz [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) , que se usa para crear un nodo único en un árbol de condiciones. Dado que solo hay una condición en el ejemplo siguiente, el árbol no cambia.


```C++
    
    [
        object,
        uuid(0FC988D4-C935-4b97-A973-46282EA175C8),
        pointer_default(unique)
    ]
    interface ICondition : IPersistStream
    {
        HRESULT GetConditionType([out, retval] CONDITION_TYPE* pNodeType);
        HRESULT GetSubConditions([in] REFIID riid, [out, retval, iid_is(riid)] void** ppv);
        [local] HRESULT GetComparisonInfo([out, annotation("__deref_opt_out")] LPWSTR *ppszPropertyName, [out, annotation("__out_opt")] CONDITION_OPERATION *pOperation, [out, annotation("__out_opt")] PROPVARIANT *pValue);
        HRESULT GetValueType([out, retval] LPWSTR* ppszValueTypeName);
        HRESULT GetValueNormalization([out, retval] LPWSTR* ppszNormalization);
        [local] HRESULT GetInputTerms([out, annotation("__out_opt")] IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] IRichChunk** ppValueTerm);
        HRESULT Clone([out, retval] ICondition** ppc);
    };


```



Si hay más de una condición de filtro, se usan y y otros operadores booleanos para lograr un único árbol. Y-los árboles y o-árboles representan conjunciones y desuniones de sus subárboles. Un árbol NOT representa la negación de su único subárbol. AQS proporciona un enfoque de texto para lograr expresiones lógicas con operadores booleanos y, a menudo, es más sencillo.

En el ejemplo siguiente, se convierte el árbol de condición ([**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)) en un formulario visual. El analizador de consultas, mediante la interfaz [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) , convierte el [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) en una cadena de consulta con formato de texto enriquecido (RTF). El método [**IQueryParser:: RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) devuelve el texto de la consulta, mientras que el método [**IQueryParser::P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) genera una interfaz [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) . En el ejemplo siguiente se muestra cómo hacer todo eso.


```C++
    [
        object,
        uuid(2EBDEE67-3505-43f8-9946-EA44ABC8E5B0),
        pointer_default(unique)
    ]
    interface IQueryParser : IUnknown
    {
        HRESULT Parse([in] LPCWSTR pszInputString, [in] IEnumUnknown* pCustomProperties, [out, retval] IQuerySolution** ppSolution);
        HRESULT SetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [out, retval] PROPVARIANT* pOptionValue);
        HRESULT SetMultiOption([in] STRUCTURED_QUERY_MULTIOPTION option, [in] LPCWSTR pszOptionKey, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetSchemaProvider([out, retval] ISchemaProvider** ppSchemaProvider);
        HRESULT RestateToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszQueryString);
        HRESULT ParsePropertyValue([in] LPCWSTR pszPropertyName, [in] LPCWSTR pszInputString, [out, retval] IQuerySolution** ppSolution);
        HRESULT RestatePropertyValueToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszPropertyName, [out] LPWSTR* ppszQueryString);
    };

```



La entrada principal de [**IQueryParser::P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) es una cadena de entrada de usuario que se va a analizar, pero la aplicación también puede informar al analizador de consultas de las propiedades que reconoce en la entrada (desde la sintaxis específica de la aplicación). La salida de **IQueryParser::P arse** es un [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution), que proporciona toda la información relativa a esa invocación del análisis. Existen métodos para obtener la cadena de entrada, el modo en que se ha acortado la cadena de entrada, los errores de análisis y la consulta analizada como árbol de condiciones, representada por un [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition). En el ejemplo siguiente se muestra...


```C++
    [
        object,
        uuid(D6EBC66B-8921-4193-AFDD-A1789FB7FF57),
        pointer_default(unique)
    ]
    interface IQuerySolution : IConditionFactory
    {
        [local] HRESULT GetQuery([out, annotation("__out_opt")] ICondition** ppQueryNode, [out, annotation("__out_opt")] IEntity** ppMainType);
        HRESULT GetErrors([in] REFIID riid, [out, retval, iid_is(riid)] void** ppParseErrors);
        [local] HRESULT GetLexicalData([out, annotation("__deref_opt_out")] LPWSTR* ppszInputString, [out, annotation("__out_opt")] ITokenCollection** ppTokens, [out, annotation("__out_opt")] LCID* pLocale, [out, annotation("__out_opt")] IUnknown** ppWordBreaker);
    }    

    

```



En el ejemplo anterior, [**IQuerySolution:: GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) podría obtener cualquier información sobre la consulta, incluido el texto original, los tokens que componen el texto o el árbol de condiciones. En la tabla siguiente se muestran ejemplos de posibles valores de consulta devueltos.



| Ejemplos de valores de consulta devueltos                        | Descripción                                                                                               |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `  author:relja OR author:tyler`                         | El texto de la consulta que [**IQueryParser:: RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) devuelve |
| `?author?, ?:?, ?relja?, ?OR?, ?author?, ?:?, ?tyler?`   | La división de tokens                                                                                  |
| ![un árbol de condiciones sin resolver](images/queryvalues1.png) | Un árbol de condiciones sin resolver                                                                              |



 

El árbol de condiciones inicial que se devuelve no se resuelve. En un árbol de condiciones sin resolver, las referencias de fecha y hora, como `date:yesterday` , no se convierten en tiempo absoluto. Además, las propiedades virtuales no se expanden. Las propiedades virtuales son propiedades que actúan como agregados de varias propiedades.

Por ejemplo, la consulta `kind:email from:reljai` genera los siguientes árboles de condiciones sin resolver y resueltos. El árbol de condiciones sin resolver está a la izquierda y el árbol de condición resuelto está a la derecha.

![árboles de condiciones sin resolver y resueltos](images/conditiontree.png)

El árbol resuelto se puede obtener llamando a [**IConditionFactory:: Resolve**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-resolve). Sin embargo, si se pasa [**SQRO not \_ \_ Resolve \_ DateTime**](/windows/desktop/api/Structuredquery/ne-structuredquery-structured_query_resolve_option) , la fecha y hora no se resuelven. Hay ventajas en un árbol de condiciones sin resolver, porque un árbol de condiciones sin resolver contiene información sobre la consulta. Cada nodo hoja apunta a los tokens devueltos por [**IQuerySolution:: GetLexicalData**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getlexicaldata), que corresponden a la propiedad, el operador y el valor cuando se usa la interfaz [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) . En el ejemplo siguiente se muestra...


```C++
    interface ITokenCollection : IUnknown
    {
        HRESULT NumberOfTokens(ULONG* pCount);
        HRESULT GetToken([in] ULONG i, [out, annotation("__out_opt")] ULONG* pBegin, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz);
    };

ICondition:: GetInputTerms([out, annotation("__out_opt")] 
IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] 
IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] 
IRichChunk** ppValueTerm);

    interface IRichChunk : IUnknown
    {
        HRESULT GetData([out, annotation("__out_opt")] ULONG* pFirstPos, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz, [out, annotation("__out_opt")] PROPVARIANT* pValue);
    }
```



### <a name="querying-the-index"></a>Consultar el índice

Hay varios enfoques para consultar el índice. Algunas se basan en SQL y otras se basan en AQS. También puede consultar el índice de búsqueda de Windows mediante programación con las [interfaces de consulta](./-search-querying-interfaces-entry-page.md). Hay tres interfaces que son específicas de la consulta del índice: [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)y [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents). Para obtener información conceptual, consulte [consultar el índice mediante programación](-search-3x-wds-qryidx-overview.md).

Puede desarrollar un componente o una clase auxiliar para consultar el índice mediante la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) . Esta interfaz se implementa como una clase auxiliar para [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (y [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) y se obtiene llamando a [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Para obtener información conceptual, consulte [consultar el índice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md).

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) le permite:

-   Obtenga una cadena de conexión OLE DB para conectarse a la base de datos de Windows Search.
-   Convertir consultas de usuario AQS en SQL de Windows Search.
-   Especifique restricciones de consulta que se pueden expresar en SQL, pero no en AQS.

En Windows 7 y versiones posteriores se admiten los eventos de indización y priorización de indexación. Con [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) hay una pila de prioridades que permite al cliente solicitar que los ámbitos utilizados en una consulta determinada se proporcionen más alto que la prioridad normal. [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) proporciona una notificación de los cambios en los elementos de los conjuntos de filas, incluida la adición de nuevos elementos, la eliminación de elementos y la modificación de los datos de los elementos. El uso de notificaciones de eventos de conjunto de filas garantiza que los resultados de las consultas existentes estén tan actualizados como sea posible. Para obtener información conceptual, consulte [Indexing Priority and Rowset Events in Windows 7](indexing-prioritization-and-rowset-events.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Indexación, consulta y notificaciones en Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Qué se incluye en el índice](-search-indexing-process-overview.md)
</dt> <dt>

[Proceso de indexación en Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Proceso de notificaciones en Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Requisitos de formato de dirección URL](url-formatting-requirements.md)
</dt> </dl>

 

 
