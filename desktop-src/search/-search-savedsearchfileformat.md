---
description: Windows los usuarios pueden guardar las búsquedas como una carpeta de búsqueda generada por un archivo XML que almacena la consulta en un formulario que puede usar el subsistema de búsqueda Windows búsqueda.
ms.assetid: 1c73e220-a999-4243-879c-ac7310151def
title: Formato de archivo de búsqueda guardado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 614eb357a82d2c70e068a9fa5258974423d755c48e779d5f5fe8be184a864d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863728"
---
# <a name="saved-search-file-format"></a>Formato de archivo de búsqueda guardado

En Windows Vista y versiones posteriores, los usuarios pueden guardar búsquedas como una carpeta de búsqueda generada por un archivo XML que almacena la consulta en un formulario que puede usar el subsistema de búsqueda Windows búsqueda. En este tema se describe el formato de archivo \* (.search-ms) e incluye las secciones siguientes:

- [Introducción a las búsquedas guardadas](#overview-of-saved-searches)
- [Elemento \<viewInfo>](/windows)
  - [\<viewInfo> Atributos](/windows)
  - [\<viewInfo> Elementos secundarios](/windows)
- [Elemento \<query>](/windows)
  - [\<query> Elementos secundarios](/windows)
- [Elemento \<properties>](/windows)
- [Especificación completa del formato de archivo search-ms](#full-specification-of-the-search-ms-file-format)
- [Ejemplos de búsquedas guardadas](#examples-of-saved-searches)

## <a name="overview-of-saved-searches"></a>Introducción a las búsquedas guardadas

Los usuarios pueden guardar una consulta de búsqueda como una carpeta de búsqueda, una carpeta virtual que se muestra en Windows Explorer en la carpeta Búsquedas. Al abrir una carpeta de búsqueda, se ejecuta la búsqueda guardada y se muestran los resultados actualizados. El archivo de búsqueda guardado almacena la consulta en un formato en el que Windows Search puede actuar, especificando qué buscar, dónde buscar y cómo presentar los resultados.

La búsqueda guardada se genera a partir de un archivo XML \* (.search-ms) en la carpeta %userprofile% \\ Searches. Los datos se dividen en tres elementos principales del archivo XML:

- \<viewInfo> especifica información de presentación
- \<query> especifica (buscar información de consulta
- \<properties> especifica las propiedades del \* propio archivo .search-ms.

En el ejemplo siguiente se muestra la estructura de alto nivel de un archivo de búsqueda guardado.

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">

    <viewInfo ...>
        ...
    </viewInfo>

    <query>
        ...
    </query>

    <properties>
        ...
    </properties>

</persistedQuery>
```

## <a name="viewinfo-element"></a>\<viewInfo> (Elemento)

El \<viewInfo> elemento especifica cómo se presentan los resultados al usuario final. En el ejemplo siguiente se muestra la estructura del elemento .

```XML
...
    <viewInfo viewMode=""
              iconSize=""
              stackIconSize=""
              autoListFlags=""
              folderFlags=""
              taskFlags=""
              displayName="">

        <visibleColumns>
            <column viewField=""/>
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/>
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>
        </columnChooserColumns >

        <groupBy viewField=""
                 direction=""/>

        <stackList>
            <stack viewField=""/>
        </stackList>

        <sortList>
            <sort viewField=""
                  direction=""/>
        </sortList>
    </viewInfo>
...
```

### <a name="viewinfo-attributes"></a>\<viewInfo> Atributos

En la tabla siguiente se describen los atributos del elemento \<viewInfo>:

| Atributo     | Descripción                                                                     | Valores                     |
|---------------|---------------------------------------------------------------------------------|----------------------------|
| Viewmode      | Especifica la vista de carpeta.                                                      | Iconos de \| \| detalles Iconos  |
| iconSize      | Controla el tamaño predeterminado de los iconos y miniaturas de los elementos cuando no se apilan. | Entero entre 16 y 256 |
| stackIconSize | Solo para uso interno. No debe usarse.                                              | N/D                        |
| DisplayName   | Solo para uso interno. No debe usarse.                                              | N/D                        |
| autoListFlags | Solo para uso interno. No debe usarse.                                              | N/D                        |
| folderFlags   | Solo para uso interno. No debe usarse.                                              | N/D                        |
| taskFlags     | Solo para uso interno. No debe usarse.                                              | N/D                        |

### <a name="viewinfo-child-elements"></a>\<viewInfo> Elementos secundarios

Los elementos secundarios del elemento especifican qué columnas aparecen en los resultados de búsqueda del Explorador de Windows y cómo se agrupan y \<viewInfo> ordenan los resultados. Cada elemento secundario contiene un conjunto ordenado de columnas, identificado por nombres canónicos de propiedades del sistema (por ejemplo, System.DisplayName). Si no se definen en el archivo de búsqueda guardado, los resultados de la búsqueda se presentan con un conjunto predeterminado de columnas adecuado para los tipos de archivo mostrados.

| Elemento               | Descripción                                                                                        | Valores                                                       |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| visibleColumns        | Especifica una lista ordenada de columnas que aparecen en la vista de resultados. El usuario puede cambiar esta lista. | Cualquier propiedad del sistema.                                         |
| frequentlyUsedColumns | Solo para uso interno. No debe usarse.                                                                 | N/D                                                          |
| columnChooserColumns  | Solo para uso interno. No debe usarse.                                                                 | N/D                                                          |
| Groupby               | Especifica una única propiedad del sistema por la que se agrupan los resultados. El usuario puede cambiar este valor.  | Cualquier propiedad del sistema.                                         |
| sortList              | Especifica una lista ordenada de columnas por las que ordenar los resultados.                                       | Hasta cuatro propiedades del sistema. El usuario puede cambiar esta lista. |
| stackList             | Solo para uso interno. No debe usarse.                                                                 | N/D                                                          |

## <a name="query-element"></a>\<query> (Elemento)

El \<query> elemento especifica los atributos que definen cómo se consultan los resultados. En el ejemplo siguiente se muestra la estructura del elemento .

```XML
...
    <query>
        <providers>
            <provider clsid=""/>    <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

### <a name="query-child-elements"></a>\<query> Elementos secundarios

En la siguiente tabla se describen los elementos secundarios del elemento \<scope>.

| Elemento    | Descripción                                                                                                               | Valor                                                                                                                                                                                                                                                          |
|------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| providers  | Solo para uso interno. No debe usarse.                                                                                        | N/D                                                                                                                                                                                                                                                            |
| Subconsultas | Solo para uso interno. No debe usarse.                                                                                        | N/D                                                                                                                                                                                                                                                            |
| Ámbito      | Identifica las ubicaciones que se incluirán o excluirán en la búsqueda.                                                                 | Una ruta de acceso o [un identificador de carpeta conocido](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) de la ubicación que se va a incluir o excluir. Este elemento también puede especificar si la búsqueda debe incluir o excluir rutas de acceso secundarias (una búsqueda superficial o profunda). |
| kindList   | Identifica el tipo de archivo que se va a buscar.                                                                             | Cualquier valor System.Kind.                                                                                                                                                                                                                                         |
| condiciones | Especifica reglas para filtrar los resultados. Por ejemplo, los resultados podrían limitarse a los correos electrónicos enviados por o a una persona determinada. | andCondition, orCondition, notCondition, leafCondition.                                                                                                                                                                                                        |

### <a name="scope-element"></a>\<scope> (Elemento)

El \<scope> elemento identifica las ubicaciones que se incluirán o excluirán de la búsqueda. El \<scope> elemento debe contener al menos un elemento secundario presente y cero o más \<include> \<exclude> elementos. Las ubicaciones se pueden especificar como una ruta de acceso (se admiten variables de entorno) o como un [identificador de carpeta conocido.](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) Además, se puede especificar que cada una de estas ubicaciones se busque en profundidad o superficial estableciendo nonRecursive en "true" o "false" (el valor predeterminado es recursivo). Las partes de la lista de ubicaciones incluidas se pueden excluir especificando elementos exclude.

A continuación se muestra un elemento que buscará la carpeta especial de documentos, pero no sus elementos secundarios, el volumen "E:" y sus elementos secundarios, pero no el directorio "E: windows" ni ninguno de sus elementos \<scope> \\ secundarios:

```XML
...
    <query>
        ...
        <scope>
            <include knownFolder="{FDD39AD0-238F-46AF-ADB4-6C85480369C7}" nonRecursive="true"/>
            <include path="E:\"/>
            <exclude path="E:\Windows" nonRecursive="false"/>
        </scope>
        ...
    </query>
...
```

### <a name="kindlist-element"></a>\<kindList> (Elemento)

Estos elementos definen la unión del "tipo" de elementos que deben aparecer en la biblioteca. Los valores válidos son:

- calendario
- communication
- contact
- documento
- email
- feed
- folder
- Juego
- instantmessage
- Diario
- link
- Película
- music
- nota
- picture
- programa
- recordedtv
- searchfolder
- task
- video
- webhistory
- item
- Otros

### <a name="conditions-element"></a>\<conditions> (Elemento)

Las condiciones son filtros con los que se comparan los resultados de la búsqueda. Por ejemplo, puede filtrar los resultados que cumplan determinados criterios, como el nombre del autor o el tamaño del archivo. El conjunto de condiciones se basa en un único árbol de condiciones con bifurcaciones AND, OR y NOT lógicas.

En el ejemplo siguiente se muestra la estructura del \<condition> elemento .

```XML
...
    <query>
        ...
        <conditions>
            <condition type="" ...>
                <attributes>
                    <attribute attributeID="" .../>
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

El tipo de condición puede ser uno de los siguientes:

| Tipo          | Descripción                                 | Atributos disponibles                               |
|---------------|---------------------------------------------|----------------------------------------------------|
| yCondition  | Conjunción de dos o más condiciones secundarias | N/D                                                |
| orCondition   | Disyunción de dos condiciones secundarias más | N/D                                                |
| notCondition  | Negación de una condición secundaria               | N/D                                                |
| leafCondition | Compara una propiedad con un valor                | property, propertyType, operator, value, valuetype |

Los \<leafCondition> atributos del elemento identifican las propiedades y los valores con los que se filtran los resultados.

### <a name="example-conditions-element"></a>Ejemplo: \<conditions> Elemento

En el ejemplo siguiente se filtran los resultados de todos los elementos no leídos creados por John. Es decir, la propiedad System.IsRead es false y la cadena "john" aparece en las propiedades System.Author o System.ItemAuthors.

```XML
...
    <query>
        ...
        <conditions>

            <condition type="andCondition">

                <condition type="leafCondition"
                           property="System.IsRead"
                           operator="eq"
                           value="FALSE"/>

                <condition type="orCondition">

                    <condition type="leafCondition"
                               property="System.Author"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                    <condition type="leafCondition"
                               property="System.ItemAuthors"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                </condition>

            </condition>

        </conditions>

    </query>
...
```

## <a name="properties-element"></a>\<properties> (Elemento)

El \<properties> elemento describe las propiedades de la propia búsqueda guardada. Los archivos de búsqueda guardados admiten cuatro propiedades: \<author> \<kind> , , y \<description> \<tags> . Son solo para uso interno.

## <a name="full-specification-of-the-search-ms-file-format"></a>Especificación completa del formato de archivo search-ms

A continuación se muestra un ejemplo del XML completo para un archivo de búsqueda guardado.

```XML
<?xml version="1.0"?>

<persistedQuery version="1.0">

    <!-- The viewInfo section defines how results are displayed to the end user -->
    <viewInfo viewMode=""       <!-- details | icons | tiles -->
              iconSize=""       <!-- Integer -->
              stackIconSize=""  <!-- Do not use -->
              displayName=""    <!-- Do not use -->
              folderFlags=""    <!-- Do not use -->
              taskFlags=""      <!-- Do not use -->
              autoListFlags=""> <!-- Do not use -->

        <visibleColumns>
            <column viewField=""/>  <!-- System.[propertyname] -->
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/> <!-- Do not use -->
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>  <!-- Do not use -->
        </columnChooserColumns >

        <groupBy viewField=""       <!-- System.[propertyname] -->
                 direction=""/>     <!-- ascending | descending -->

        <stackList>
            <stack viewField=""/>   <!-- Do not use -->
        </stackList>

        <sortList>
            <sort viewField=""      <!-- System.[propertyname] -->
                  direction=""/>    <!-- ascending | descending -->
        </sortList>
    </viewInfo>

    <!-- The query section defines what gets searched (locations, file kinds) -->
    <query>
        <providers>
            <provider clsid=""/>          <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>

    <!-- The properties section identifies properties of the saved search file itself. -->
    <properties>
        ...             <!-- Do not use -->
    </properties>

</persistedQuery>
```

## <a name="examples-of-saved-searches"></a>Ejemplos de búsquedas guardadas

A continuación se muestran ejemplos \* de archivos .search-ms.

### <a name="recent-documentssearch-ms"></a>Documentos recientes.search-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUZZXD-30NU" propertyType="wstr" />
        </conditions>
        <kindList>
            <kind name="Document"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recent-musicsearch-ms"></a>Recientes Música.search-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUW-1WNNU" propertyType="wstr"/>
        </conditions>
        <kindList>
            <kind name="Music"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recently-shared-by-mesearch-ms"></a>Compartido recientemente por Me.search-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <visibleColumns>
            <column viewField="System.ItemNameDisplay"/>
            <column viewField="System.DateModified"/>
            <column viewField="System.Keywords"/>
            <column viewField="System.SharedWith"/>
            <column viewField="System.ItemFolderPathDisplayNarrow"/>
        </visibleColumns>
        <frequentlyUsedColumns>
            <column viewField="System.Author"/>
            <column viewField="System.Kind"/>
            <column viewField="System.Size"/>
            <column viewField="System.Title"/>
            <column viewField="System.Rating"/>
        </frequentlyUsedColumns>
        <sortList>
            <sort viewField="System.SharedWith" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="andCondition">
                <condition type="leafCondition" property="System.IsShared" operator="eq" value="true"/>
                <condition type="leafCondition" property="System.FileOwner" operator="eq" value="[Me]"/>
            </condition>
        </conditions>
        <kindList>
            <kind name="item"/>
        </kindList>
        <scope>
            <include knownFolder="{5E6C858F-0E22-4760-9AFE-EA3317B67173}"/>
            <include knownFolder="{DFDF76A2-C82A-4D63-906A-5644AC457385}"/>
        </scope>
    </query>
</persistedQuery>
```
