---
description: Presenta el esquema de Descripción del conector de búsqueda que usan las bibliotecas del explorador de Windows y los proveedores de búsquedas federadas.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Esquema de Descripción del conector de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f502f67cdc933bf4d27a3475cd6adef70c00fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705471"
---
# <a name="search-connector-description-schema"></a>Esquema de Descripción del conector de búsqueda

Presenta el esquema de Descripción del conector de búsqueda que usan las bibliotecas del explorador de Windows y los proveedores de búsquedas federadas. El esquema especifica la estructura y los requisitos para los archivos de Descripción del conector de búsqueda ( \* . searchConnector-MS) y para los elementos **searchConnectorDescriptionType** de los archivos de descripción de la biblioteca de Shell ( \* . Library-MS).

En este tema se describe el esquema en relación con los conectores de búsqueda federada. Para obtener más información sobre las bibliotecas y el esquema de descripción de la biblioteca, vea [esquema de Descripción](../shell/library-schema-entry.md)de la biblioteca.

Este tema incluye las siguientes secciones:

-   [¿Qué son los conectores de búsqueda?](#what-are-search-connectors)
-   [¿Cómo funcionan los archivos de Descripción del conector de búsqueda?](#search-connector-description-schema)
-   [¿Qué es el esquema de Descripción del conector de búsqueda?](#what-is-the-search-connector-description-schema)
-   [¿Cuáles son las partes principales del esquema?](#what-are-the-major-parts-of-the-schema)
-   [Ejemplos de archivos de Descripción del conector de búsqueda](#examples-of-search-connector-description-files)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="what-are-search-connectors"></a>¿Qué son los conectores de búsqueda?

Los conectores de búsqueda conectan a los usuarios con los datos almacenados en servicios web o ubicaciones de almacenamiento remoto. Con Windows 7, los usuarios pueden instalar conectores de búsqueda para ubicaciones, como los servicios Web, de modo que busquen esas ubicaciones directamente desde el explorador de Windows. Los conectores de búsqueda son archivos de Descripción \* del conector de búsqueda (. searchConnector-MS) que especifican cómo conectarse a, enviar consultas a y recibir los resultados de la ubicación.

Además de los servicios Web, los conectores de búsqueda se pueden usar para buscar ámbitos de índice locales creados por los controladores de protocolo. Por ejemplo, los usuarios pueden buscar correo electrónico indexado localmente con el controlador de protocolo MAPI mediante el uso de un conector de búsqueda para ese almacén de correo electrónico.

## <a name="how-do-search-connector-description-files-work"></a>¿Cómo funcionan los archivos de Descripción del conector de búsqueda?

Cuando los archivos de Descripción del conector de búsqueda se instalan en los sistemas de los usuarios, los usuarios pueden abrir el explorador de Windows, hacer clic en el conector de búsqueda en el panel de navegación y especificar una consulta de búsqueda. El explorador de Windows envía la consulta con información del archivo de Descripción del conector de búsqueda, como el proveedor que se va a utilizar y el ámbito de la búsqueda. Los resultados se devuelven como elementos de fuente RSS o Atom y se muestran a los usuarios como si fueran elementos de Shell normales.

La forma de implementar el archivo de Descripción del conector de búsqueda depende del tipo de ubicación que admita el conector de búsqueda:

-   En un archivo de configuración de OpenSearch ( \* . osdx) para el servicio Web
-   Como parte de la instalación del controlador de protocolo

Debe asegurarse de que se producen las siguientes acciones cuando un usuario abre el archivo. osdx o instala el controlador de protocolo:

-   El archivo. searchconnector-MS se crea en la carpeta de **búsquedas de Windows** de los usuarios (% userprofile%/searches).
-   Se crea un acceso directo al archivo. searchconnector-MS en la carpeta de **vínculos** de los usuarios (% userprofile%/links).

## <a name="what-is-the-search-connector-description-schema"></a>¿Qué es el esquema de Descripción del conector de búsqueda?

El esquema de Descripción del conector de búsqueda es un esquema XML que define la estructura de los archivos de Descripción del conector de búsqueda ( \* . searchConnector-MS). Cada conector de búsqueda debe tener un archivo de Descripción del conector de búsqueda que especifique cómo conectarse a, enviar consultas a y recibir los resultados de la ubicación.

## <a name="what-are-the-major-parts-of-the-schema"></a>¿Cuáles son las partes principales del esquema?

En la tabla siguiente se enumeran las partes principales del esquema.



| Elementos secundarios                                                                         | Descripción                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isSearchOnlyItem](search-schema-sconn-issearchonlyitem.md)                           | Identifica si las ubicaciones admitidas por el conector de búsqueda son de solo búsqueda o buscar y examinar.                                                                                |
| [isDefaultSaveLocation](search-schema-sconn-isdefaultsavelocation.md)                 | Solo para uso de la biblioteca.                                                                                                                                                                   |
| [isDefaultNonOwnerSaveLocation](search-schema-sconn-isdefaultnonownersavelocation.md) | Solo para uso de la biblioteca.                                                                                                                                                                   |
| [description](search-schema-sconn-description.md)                                     | Describe el conector de búsqueda.                                                                                                                                                         |
| [iconReference](search-schema-sconn-iconreference.md)                                 | Identifica la ubicación de un icono personalizado para el conector de búsqueda.                                                                                                                      |
| [imageLink](search-schema-sconn-imagelink.md)                                         | Identifica la ubicación de una miniatura personalizada para el conector de búsqueda.                                                                                                                 |
| [frente](search-schema-sconn-author.md)                                               | Identifica al autor del conector de búsqueda.                                                                                                                                          |
| [dateCreated](search-schema-sconn-datecreated.md)                                     | Identifica la fecha en que se creó el conector de búsqueda.                                                                                                                              |
| [templateInfo](search-schema-sconn-templateinfo.md)                                   | Especifica un tipo de carpeta para el conector de búsqueda.                                                                                                                                       |
| [locationProvider](search-schema-sconn-locationprovider.md)                           | Especifica el proveedor de búsquedas que va a usar este conector de búsqueda.                                                                                                                      |
| [scope](search-schema-sconn-scope.md)                                                 | Especifica las ubicaciones que se van a incluir y excluir del ámbito de búsqueda.                                                                                                                |
| [propertyStore](search-schema-sconn-propertystore.md)                                 | Especifica la ubicación de un [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) basado en XML para este conector de búsqueda. **IPropertyStore** admite los metadatos abiertos del conector de búsqueda. |
| [includeInStartMenuScope](search-schema-sconn-includeinstartmenuscope.md)             | Especifica si la ubicación representada por el conector de búsqueda debe incluirse en el ámbito de búsqueda del menú Inicio.                                                                 |
| [dominio](search-schema-sconn-domain.md)                                               | Identifica el dominio de nivel superior del conector de búsqueda.                                                                                                                                     |
| [supportsAdvancedQuerySyntax](search-schema-sconn-supportsadvancedquerysyntax.md)     | Especifica si el conector de búsqueda admite la sintaxis de consulta avanzada (AQS).                                                                                                            |
| [isIndexed](search-schema-sconn-isindexed.md)                                         | Especifica si la ubicación representada por el conector de búsqueda está indizada.                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a>Ejemplos de archivos de Descripción del conector de búsqueda

El siguiente es un ejemplo de un archivo de Descripción del conector de búsqueda para un servicio Web de búsqueda federada.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



El siguiente es un ejemplo de un archivo de Descripción del conector de búsqueda para un controlador de protocolo MAPI.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener más información sobre el esquema de descripción de la biblioteca, vea [esquema de Descripción](../shell/library-schema-entry.md)de la biblioteca.
-   Para obtener más información sobre la instalación de un conector de búsqueda, consulte [Federated Search in Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[OpenSearch](http://www.opensearch.org/Home)
</dt> <dt>

[Centro de descarga de Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
