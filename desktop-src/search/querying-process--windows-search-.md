---
description: Proceso de consulta en Windows Búsqueda
ms.assetid: 0e5a633e-1703-4b72-8a04-6da71aec0ae2
title: Proceso de consulta en Windows Búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffec01c7b85b54d56e4e1092004be7e18e318b736cb591a10db0973153471cd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680265"
---
# <a name="querying-process-in-windows-search"></a>Proceso de consulta en Windows Búsqueda

Este tema se organiza de la siguiente manera:

-   [Acerca de las consultas en Windows Search](#about-querying-in-windows-search)
    -   [Consultas locales y remotas](#local-and-remote-queries)
    -   [Información general sobre structured query API](#structured-query-api-overview)
-   [Escenarios de consulta](#querying-scenarios)
    -   [Extracción de condiciones y análisis de consultas](#condition-extraction-and-query-parsing)
    -   [Consulta del índice](#querying-the-index)
-   [Temas relacionados](#related-topics)

## <a name="about-querying-in-windows-search"></a>Acerca de las consultas en Windows Search

Las consultas en Windows Search se basan en los cuatro enfoques siguientes:

-   [Sintaxis de consulta](-search-3x-advancedquerysyntax.md) avanzada (AQS)
-   Sintaxis de consulta natural (NQS)
-   Lenguaje de consulta estructurado (SQL)
-   Interfaces de consulta estructurada

AQS es la sintaxis de consulta predeterminada que usa Windows Search para consultar el índice y para restringir y restringir los parámetros de búsqueda. AQS está orientado principalmente al usuario y lo pueden usar los usuarios para crear consultas de AQS, pero los desarrolladores también pueden usarlas para compilar consultas mediante programación. En Windows 7, se introdujo AQS canónico y debe usarse para generar consultas de AQS mediante programación. En Windows 7 y versiones posteriores, una opción de menú contextual puede estar disponible en función de si se cumple una condición de AQS. Para obtener más información, vea "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" (Obtener comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada) en [Creating Context Menu Handlers](../shell/context-menu-handlers.md). Las consultas de AQS se pueden limitar a tipos específicos de archivos, que se conocen como tipos de archivo. Para obtener más información, vea [Tipos de archivo y asociaciones](../shell/fa-intro.md). Para obtener documentación de referencia sobre las propiedades pertinentes, [vea System.Kind](../properties/props-system-kind.md)y [System.KindText](../properties/props-system-kindtext.md).

NQS es una sintaxis de consulta que es más relajada que AQS y es similar al lenguaje humano. NQS se puede usar Windows Search para consultar el índice si NQS está seleccionado en lugar del valor predeterminado, AQS.

SQL es un lenguaje de texto que define las consultas. SQL es común en muchas tecnologías de base de datos diferentes. Windows La búsqueda SQL, implementa un subconjunto de él y lo extiende agregando elementos al lenguaje. Windows Search SQL amplía la sintaxis de consulta de base de datos estándar SQL-92 y SQL-99 para mejorar su utilidad con las búsquedas basadas en texto. Todas las características de Windows Search SQL son compatibles con Windows Search en Windows XP y Windows Server 2003 y versiones posteriores. Para obtener más información sobre Windows Search SQL, vea Consultar el índice con la sintaxis SQL de Windows [Search](-search-sql-windowssearch-entry.md)e Información general de Windows [Search SQL Syntax](-search-sql-ovwofsearchquery.md).

Las API de consulta estructuradas se describen más adelante en este tema. Para obtener documentación de referencia sobre las API de consulta estructuradas, vea [Querying Interfaces](-search-querying-interfaces-entry-page.md). Interfaces como [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) ayudan a construir SQL cadenas a partir de un conjunto de valores de entrada. Esta interfaz convierte las consultas de usuario de AQS en Windows Search SQL y especifica restricciones de consulta que se pueden expresar en SQL pero no en AQS. [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) también obtiene una cadena OLE DB conexión para conectarse a la base de datos Windows Search.

### <a name="local-and-remote-queries"></a>Consultas locales y remotas

Puede ejecutar las consultas de forma local o remota. En el ejemplo siguiente se [muestra una consulta](-search-sql-from.md) local que usa la cláusula FROM. Una consulta local solo consulta el catálogo SystemIndex local.


```
FROM SystemIndex
```



En el ejemplo siguiente se [muestra una consulta](-search-sql-from.md) remota con la cláusula FROM. Al agregar ComputerName, se transforma el ejemplo anterior en una consulta remota.


```
FROM [<ComputerName>.]SystemIndex
```



De forma predeterminada, Windows XP y Windows Server 2003 no tienen Windows Search instalado. Solo Windows Search 4 (WS4) proporciona compatibilidad con consultas remotas. Las versiones anteriores de Windows Desktop Search (WDS), como 3.01 y versiones anteriores, no admiten consultas remotas. Con Windows explorer puede consultar el índice local de un equipo remoto para los elementos del sistema de archivos (elementos que controla el protocolo "archivo:").

Para recuperar un elemento por consulta remota, el elemento debe cumplir los siguientes requisitos:

-   Se puede acceder a través de la ruta de acceso de convención de nomenclatura universal (UNC).
-   Existe en el equipo remoto al que el cliente tiene acceso.
-   Tenga su seguridad establecida para permitir que el cliente tenga acceso de lectura.

Windows El Explorador tiene características para compartir elementos, incluido un recurso compartido "Público" (Público de la máquina ...) en el Centro de redes y recursos compartidos y un recurso compartido \\ \\ \\ \\ "Usuarios" (Usuarios  \\ \\ \\ de la \\ máquina...) para los elementos compartidos a través del Asistente para uso compartido. Después de compartir las carpetas, puede consultar el índice local especificando el nombre del equipo remoto en la cláusula FROM y una ruta de acceso UNC en el equipo remoto en la cláusula SCOPE. En el ejemplo siguiente se muestra una consulta remota con las cláusulas FROM y SCOPE.


```
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>' 
```



Los ejemplos que se proporcionan aquí usan SQL.

### <a name="structured-query-api-overview"></a>Información general sobre structured query API

Una consulta estructurada proporciona la capacidad de buscar información por combinaciones booleanas de consultas sobre propiedades individuales. En este tema se describe la funcionalidad de las API y los métodos de consulta estructurados más importantes. Para obtener documentación de referencia sobre las API de consulta estructuradas, vea [Querying Interfaces](-search-querying-interfaces-entry-page.md).

### <a name="iqueryparser"></a>IQueryParser

El [**método IQueryParser::P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) analiza una cadena de entrada del usuario y genera una interpretación en forma de [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution). Si el *parámetro pCustomProperties* de ese método no es NULL, es una enumeración de objetos [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) (uno para cada propiedad personalizada reconocida). Los otros [**métodos IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) permiten a la aplicación establecer varias opciones, como la configuración regional, un esquema, un separador de palabras y controladores para varios tipos de entidades con nombre. [**IQueryParser::GetSchemaProvider devuelve**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-getschemaprovider) una [**interfaz ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) para examinar el esquema cargado.

### <a name="iquerysolution--iconditionfactory"></a>IQuerySolution: IConditionFactory

La [**interfaz IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) proporciona toda la información sobre el resultado del análisis de una cadena de entrada. Dado **que IQuerySolution también** es una interfaz [**IConditionFactory,**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) se pueden crear nodos de árbol de condiciones adicionales. El [**método IQuerySolution::GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) genera un árbol de condiciones para la interpretación. **IQuerySolution::GetQuery** también devuelve el tipo semántico.

### <a name="iconditionfactory"></a>IConditionFactory

[**IConditionFactory crea**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) nodos de árbol de condiciones. Si el *parámetro simplify* de [**IConditionFactory::MakeNot**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makenot) es **VARIANT \_ TRUE,** la [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) resultante se simplifica y no necesita ser un nodo de negación. Si el *parámetro pSubConditions* de [**IConditionFactory::MakeAndOr**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeandor) no es NULL, ese parámetro debe ser una enumeración de objetos [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) y convertirse en subárboles. [**IConditionFactory::MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf) construye un nodo hoja con un nombre de propiedad, operación y valor especificados. La cadena del *parámetro pValueType* debe ser el nombre de un tipo semántico del esquema. Si el *parámetro expand* es **VARIANT \_ TRUE** y la propiedad es virtual, el árbol de condiciones resultante suele ser una disyunción resultante de expandir la propiedad a sus constituyentes definidos. Si no es NULL, los parámetros *pPropertyNameTerm*, *pOperatorTerm* y *pValueTerm* deben identificar los términos que indican la propiedad, la operación y el valor.

### <a name="icondition--ipersiststream"></a>ICondition : IPersistStream

La [**interfaz ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) es un único nodo en un árbol de condiciones. El nodo puede ser un nodo de negación, un nodo AND, un nodo OR o un nodo hoja. Para un nodo no hoja [**ICondition::GetSubConditions**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getsubconditions) devuelve una enumeración de los subárboles. Para un nodo hoja, los métodos siguientes [**de ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) devuelven los valores siguientes:

-   [**GetComparisonInfo devuelve**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo) el nombre, la operación y el valor de la propiedad.
-   [**GetValueType**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluetype) devuelve el tipo semántico del valor, que se especificó en el parámetro *pszValueType* [**de IConditionFactory::MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf).
-   [**GetValueNormalization**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluenormalization) devuelve una forma de cadena del valor. (Si el valor ya era una cadena, este formulario se normalizará con respecto a mayúsculas y minúsculas, acentos, etc.).
-   [**GetInputTerms**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms) devuelve información sobre qué partes de la oración de entrada generaron el nombre de propiedad, la operación y el valor.
-   [**Clone**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone) devuelve una copia en profundidad de un árbol de condiciones.

### <a name="irichchunk"></a>IRichChunk

Cada [**objeto IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) identifica un intervalo de token y una cadena. **IRichChunk es** una interfaz de utilidad que representa información sobre un intervalo (normalmente un intervalo de tokens) identificado por una posición inicial y una longitud. Esta información de intervalo incluye una cadena o **variant.**

### <a name="iconditiongenerator"></a>IConditionGenerator

La [**aplicación proporciona la interfaz IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) para controlar la generación de árbol de reconocimiento y condición para un tipo de entidad con nombre. Se da un generador de condiciones a [**un IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) a través [**de IQueryParser::SetMultiOption**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-setmultioption). [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) llama [**a IConditionGenerator::Initialize**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-initialize) con [**un ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) para el esquema cargado actualmente. Esto permite a [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) obtener la información de esquema necesaria. Al analizar una cadena de entrada, **IQueryParser** llama al método [**IConditionGenerator::RecognizeNamedEntities**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-recognizenamedentities) de cada [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)para que se puedan notifica las apariciones de las entidades con nombre que reconoce en la cadena de entrada. **IQueryParser** puede hacer uso de la configuración regional actual y debe usar la tokenización de la entrada, ya que necesita notificar los intervalos de tokens de cualquier entidad con nombre.

Cuando [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) está a punto de emitir un nodo hoja y el tipo semántico del valor coincide con el tipo de entidad con nombre de un [**IConditionGenerator,**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) **IQueryParser** llama a [**IConditionGenerator::GenerateforLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf) con la información del nodo que se va a generar. Si [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) devuelve S OK, debe devolver un árbol de condiciones (que no tiene que ser un nodo hoja) e informar \_ a **IQueryParser** de si se debe suprimir la interpretación de cadena alternativa que se generaría normalmente como precaución.

### <a name="itokencollection"></a>ITokenCollection

El [**método ITokenCollection::NumberOfTokens**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-numberoftokens) devuelve el número de tokens. [**ITokenCollection::GetToken**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-gettoken) devuelve información sobre *el token ith.* El principio y la longitud son posiciones de caracteres en la cadena de entrada. El texto devuelto será distinto de NULL solo si hay un texto que reemplaza los caracteres de la cadena de entrada. Esto se usa, por ejemplo, para invalidar un guión en la cadena de entrada con NOT cuando ese guión está en un contexto donde se debe interpretar como una negación.

### <a name="inamedentitycollector"></a>INamedEntityCollector

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) llama [**a INamedEntityCollector::Add**](/windows/desktop/api/Structuredquery/nf-structuredquery-inamedentitycollector-add) para cada entidad con nombre que ha reconocido. Los intervalos son intervalos de tokens. Siempre debe ser el caso en el que *beginSpan* ? *beginActual*  <  *endActual* ? *endSpan*. *beginSpan* y *endSpan* pueden diferir de *beginActual* y *endActual* si la entidad con nombre comienza o termina con tokens semánticamente insignificantes, como comillas (que, sin embargo, están cubiertos por la entidad con nombre). El valor debe expresarse como una cadena y aparecerá posteriormente en una llamada a [**IConditionGenerator::GenerateForLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf).

### <a name="ischemaprovider"></a>ISchemaProvider

La [**interfaz ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) se puede usar para examinar un esquema cargado de entidades (tipos) y relaciones (propiedades). Esto es lo que hacen los métodos individuales:

-   [**Las entidades**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-entities) devuelven una enumeración de cada entidad ([**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity)) del esquema.
-   [**RootEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-rootentity) devuelve la entidad raíz del esquema. Para un esquema plano, se devuelve el tipo principal de [**cada IQuerySolution.**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)
-   [**GetEntity busca**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-getentity) una entidad por nombre y devuelve S \_ FALSE si no hay ninguna entidad de este tipo en el esquema.
-   [**MetaData**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-metadata) devuelve una enumeración de [**interfaces IMetaData.**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata)

### <a name="ientity"></a>IEntity

La [**interfaz IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity) es una entidad de esquema que representa un tipo que tiene un nombre, tiene una serie de relaciones con nombre con otros tipos (propiedades) y deriva de una entidad base. Esto es lo que hacen sus métodos individuales:

-   [**IEntity::Relationships**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-relationships) devuelve una enumeración de [**objetos IRelationship,**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) uno para cada relación saliente de este tipo. Cada relación saliente de una entidad tiene un nombre.
-   [**IEntity::GetRelationship**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-getrelationship) busca una relación por nombre y devuelve S FALSE si no hay ninguna relación de este tipo \_ para esta entidad.
-   [**IEntity::MetaData devuelve**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-metadata) una enumeración de interfaces [**IMetaData,**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) una para cada par de metadatos de esta entidad.
-   [**IEntity::D efaultPhrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-defaultphrase) devuelve una frase predeterminada para facilitar la generación de una nueva instrucción de AQS o NQS de un árbol de condiciones.

### <a name="irelationship"></a>IRelationship

La [**interfaz IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) representa una relación entre dos entidades: un origen y un destino. Esto es lo que hacen los métodos individuales:

-   [**IRelationship::IsReal**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-isreal) informa de si una relación es real. Por ejemplo, si la entidad A deriva de la entidad B y hereda de ella una relación denominada R, A todavía puede tener su propia relación denominada R. Sin embargo, la relación entre A y R debe tener el mismo tipo de destino que B y la única razón para que exista es almacenar metadatos específicos de B. Se dice que esta relación de B no es real.
-   [**IRelationship::Medadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-metadata) devuelve una enumeración de interfaces [**IMetaData,**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) una para cada par de metadatos de esta entidad.
-   [**IRelationship::D efaultPhrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-defaultphrase) devuelve la frase predeterminada que se va a usar para esta relación en las reevaluaciones. Cada relación tiene una frase predeterminada que la denota para facilitar la generación de una nueva instrucción de AQS o NQS de un árbol de condiciones.

### <a name="imetadata"></a>IMetaData

Los metadatos son pares clave-valor que están asociados a una entidad, una relación o todo el esquema. Dado que las claves no son necesariamente únicas, una colección de metadatos se puede pensar en un mapa múltiple. [**Se llama a IMetaData::GetData**](/windows/desktop/api/Structuredquery/nf-structuredquery-imetadata-getdata) para recuperar la clave y el valor de un par de metadatos.

## <a name="querying-scenarios"></a>Escenarios de consulta

En los escenarios siguientes se describe el uso de API de consulta estructuradas en Windows Search en escenarios de consulta comunes, como la creación de un árbol de condiciones y la consulta del índice.

### <a name="condition-extraction-and-query-parsing"></a>Extracción de condiciones y análisis de consultas

Cuando se crea una consulta, su ámbito se define al decir al sistema dónde buscar. Esto restringe los resultados de la búsqueda. Una vez definido el ámbito, se aplica un filtro y se devuelve un conjunto de filtros. Los resultados de la búsqueda se restringen mediante la creación de un árbol de condiciones con nodos hoja, similar a un gráfico. A continuación, se extraen esas condiciones. Un árbol de condiciones es una combinación booleana (AND, OR, NOT) de condiciones hoja, cada una de las cuales relaciona una propiedad, a través de una operación, con un valor. Un nodo hoja representa una restricción de una sola propiedad a un valor a través de algunas operaciones.

Una restricción de filtro requiere una expresión lógica que describa la restricción. La definición de esta expresión comienza con [**la interfaz ICondition,**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) que se usa para crear un único nodo en un árbol de condiciones. Dado que solo hay una condición en el ejemplo siguiente, el árbol no cambia.


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



Si hay más de una condición de filtro, se usan AND y otros operadores booleanos para lograr un único árbol. Los árboles AND y OR representan conjunciones y disyunciones de sus subárboles. Un árbol NOT representa la negación de su único subárbol. AQS proporciona un enfoque de texto para lograr expresiones lógicas con operadores booleanos y, a menudo, es más sencillo.

En el ejemplo siguiente se convierte el árbol de condiciones ([**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)) en forma visual. El analizador de consultas, mediante la interfaz [**IQueryParser,**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) convierte [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) en una cadena de consulta con formato de texto enriquecido (RTF). El [**método IQueryParser::RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) devuelve el texto de la consulta, mientras que el método [**IQueryParser::P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) genera una [**interfaz IQuerySolution.**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) En el ejemplo siguiente se muestra cómo hacer todo eso.


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



La entrada principal de [**IQueryParser::P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) es una cadena de entrada del usuario que se va a analizar, pero la aplicación también puede informar al analizador de consultas de las propiedades que ha reconocido en la entrada (a partir de la sintaxis específica de la aplicación). La salida **de IQueryParser::P arse** es [**una IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution), que proporciona toda la información relativa a esa invocación de análisis. Hay métodos para obtener la cadena de entrada, cómo se ha tokenizado la cadena de entrada, los errores de análisis y la consulta analizada como árbol de condición, representado por una [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition). En el ejemplo siguiente se muestra ...


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



En el ejemplo anterior, [**IQuerySolution::GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) podría obtener cualquier información sobre la consulta, incluido el texto original, los tokens que componen el texto o el árbol de condiciones. En la tabla siguiente se muestran ejemplos de posibles valores de consulta devueltos.



| Ejemplos de valores de consulta devueltos                        | Descripción                                                                                               |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `  author:relja OR author:tyler`                         | Texto de consulta que [**devuelve IQueryParser::RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) |
| `?author?, ?:?, ?relja?, ?OR?, ?author?, ?:?, ?tyler?`   | La interrupción de tokens                                                                                  |
| ![un árbol de condiciones sin resolver](images/queryvalues1.png) | Un árbol de condiciones sin resolver                                                                              |



 

El árbol de condición inicial que se devuelve no está resuelto. En un árbol de condiciones sin resolver, las referencias de fecha y hora, como `date:yesterday` , no se convierten a hora absoluta. Además, las propiedades virtuales no se expanden. Las propiedades virtuales son propiedades que actúan como agregados de varias propiedades.

Por ejemplo, la consulta genera los siguientes árboles de condición sin `kind:email from:reljai` resolver y resueltos. El árbol de condiciones sin resolver está a la izquierda y el árbol de condiciones resuelto está a la derecha.

![árboles de condiciones resueltos y sin resolver](images/conditiontree.png)

El árbol resuelto se puede obtener llamando a [**IConditionFactory::Resolve**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-resolve). Sin embargo, [**pasar SQRO \_ DONT \_ RESOLVE \_ DATETIME**](/windows/desktop/api/Structuredquery/ne-structuredquery-structured_query_resolve_option) deja sin resolver la fecha y hora. Hay ventajas para un árbol de condiciones sin resolver, porque un árbol de condiciones sin resolver contiene información sobre la consulta. Cada nodo hoja apunta a los tokens devueltos por [**IQuerySolution::GetLexicalData**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getlexicaldata), que se corresponden con la propiedad, el operador y el valor cuando se usa la interfaz [**IRichChunk.**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) En el ejemplo siguiente se muestra ...


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



### <a name="querying-the-index"></a>Consulta del índice

Hay varios enfoques para consultar el índice. Algunas se basan en la SQL y otras se basan en AQS. También puede consultar el índice Windows search mediante programación mediante [interfaces de consulta](./-search-querying-interfaces-entry-page.md). Hay tres interfaces específicas para consultar el índice: [**ISearchQueryHelper,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)e [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents). Para obtener información conceptual, [vea Consultar el índice mediante programación.](-search-3x-wds-qryidx-overview.md)

Puede desarrollar un componente o una clase auxiliar para consultar el índice mediante la [**interfaz ISearchQueryHelper.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) Esta interfaz se implementa como una clase auxiliar para [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) y se obtiene mediante una llamada a [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Para obtener información conceptual, vea [Consulta del índice con ISearchQueryHelper.](-search-3x-wds-qryidx-searchqueryhelper.md)

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) le permite:

-   Obtenga una cadena OLE DB conexión para conectarse a la base de datos Windows Search.
-   Convierta las consultas de usuario de AQS en Windows search SQL.
-   Especifique restricciones de consulta que se pueden expresar en SQL pero no en AQS.

Los eventos de priorización de indexación y de conjunto de filas se admiten en Windows 7 y versiones posteriores. Con [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) hay una pila de prioridad que permite al cliente solicitar que los ámbitos usados en una consulta determinada se den una prioridad superior a la normal. [**IRowsetEvents proporciona**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) notificación de los cambios en los elementos de los conjuntos de filas, incluida la adición de nuevos elementos, la eliminación de elementos y la modificación de los datos de los elementos. El uso de notificaciones de eventos de conjunto de filas garantiza que los resultados de las consultas existentes estén lo más actualizados posible. Para obtener información conceptual, vea [Indexing Prioritization and Rowset Events in Windows 7](indexing-prioritization-and-rowset-events.md).

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

 

 
