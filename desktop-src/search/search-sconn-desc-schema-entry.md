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
# <a name="search-connector-description-schema"></a><span data-ttu-id="d65b5-103">Esquema de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="d65b5-103">Search Connector Description Schema</span></span>

<span data-ttu-id="d65b5-104">Presenta el esquema de Descripción del conector de búsqueda que usan las bibliotecas del explorador de Windows y los proveedores de búsquedas federadas.</span><span class="sxs-lookup"><span data-stu-id="d65b5-104">Introduces the Search Connector Description schema that is used by Windows Explorer libraries and federated search providers.</span></span> <span data-ttu-id="d65b5-105">El esquema especifica la estructura y los requisitos para los archivos de Descripción del conector de búsqueda ( \* . searchConnector-MS) y para los elementos **searchConnectorDescriptionType** de los archivos de descripción de la biblioteca de Shell ( \* . Library-MS).</span><span class="sxs-lookup"><span data-stu-id="d65b5-105">The schema specifies the structure and requirements for Search Connector Description files (\*.searchConnector-ms) and for **searchConnectorDescriptionType** elements of the Shell Library Description (\*.library-ms) files.</span></span>

<span data-ttu-id="d65b5-106">En este tema se describe el esquema en relación con los conectores de búsqueda federada.</span><span class="sxs-lookup"><span data-stu-id="d65b5-106">This topic describes the schema as it relates to federated search connectors.</span></span> <span data-ttu-id="d65b5-107">Para obtener más información sobre las bibliotecas y el esquema de descripción de la biblioteca, vea [esquema de Descripción](../shell/library-schema-entry.md)de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d65b5-107">For more information about libraries and the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>

<span data-ttu-id="d65b5-108">Este tema incluye las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="d65b5-108">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="d65b5-109">¿Qué son los conectores de búsqueda?</span><span class="sxs-lookup"><span data-stu-id="d65b5-109">What Are Search Connectors?</span></span>](#what-are-search-connectors)
-   [<span data-ttu-id="d65b5-110">¿Cómo funcionan los archivos de Descripción del conector de búsqueda?</span><span class="sxs-lookup"><span data-stu-id="d65b5-110">How Do Search Connector Description Files Work?</span></span>](#search-connector-description-schema)
-   [<span data-ttu-id="d65b5-111">¿Qué es el esquema de Descripción del conector de búsqueda?</span><span class="sxs-lookup"><span data-stu-id="d65b5-111">What Is the Search Connector Description Schema?</span></span>](#what-is-the-search-connector-description-schema)
-   [<span data-ttu-id="d65b5-112">¿Cuáles son las partes principales del esquema?</span><span class="sxs-lookup"><span data-stu-id="d65b5-112">What Are the Major Parts of the Schema?</span></span>](#what-are-the-major-parts-of-the-schema)
-   [<span data-ttu-id="d65b5-113">Ejemplos de archivos de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="d65b5-113">Examples of Search Connector Description Files</span></span>](#examples-of-search-connector-description-files)
-   [<span data-ttu-id="d65b5-114">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d65b5-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="d65b5-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d65b5-115">Related topics</span></span>](#related-topics)

## <a name="what-are-search-connectors"></a><span data-ttu-id="d65b5-116">¿Qué son los conectores de búsqueda?</span><span class="sxs-lookup"><span data-stu-id="d65b5-116">What Are Search Connectors?</span></span>

<span data-ttu-id="d65b5-117">Los conectores de búsqueda conectan a los usuarios con los datos almacenados en servicios web o ubicaciones de almacenamiento remoto.</span><span class="sxs-lookup"><span data-stu-id="d65b5-117">Search connectors connect users with data stored in web services or remote storage locations.</span></span> <span data-ttu-id="d65b5-118">Con Windows 7, los usuarios pueden instalar conectores de búsqueda para ubicaciones, como los servicios Web, de modo que busquen esas ubicaciones directamente desde el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="d65b5-118">With Windows 7, users can install search connectors for locations, like web services, so that they search those locations directly from Windows Explorer.</span></span> <span data-ttu-id="d65b5-119">Los conectores de búsqueda son archivos de Descripción \* del conector de búsqueda (. searchConnector-MS) que especifican cómo conectarse a, enviar consultas a y recibir los resultados de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="d65b5-119">Search connectors are Search Connector Description files (\*.searchConnector-ms) that specify how to connect to, send queries to, and receive results from the location.</span></span>

<span data-ttu-id="d65b5-120">Además de los servicios Web, los conectores de búsqueda se pueden usar para buscar ámbitos de índice locales creados por los controladores de protocolo.</span><span class="sxs-lookup"><span data-stu-id="d65b5-120">In addition to web services, search connectors can be used to search local index scopes created by protocol handlers.</span></span> <span data-ttu-id="d65b5-121">Por ejemplo, los usuarios pueden buscar correo electrónico indexado localmente con el controlador de protocolo MAPI mediante el uso de un conector de búsqueda para ese almacén de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="d65b5-121">For example, users can search email indexed locally with the MAPI protocol handler by using a search connector for that email store.</span></span>

## <a name="how-do-search-connector-description-files-work"></a><span data-ttu-id="d65b5-122">¿Cómo funcionan los archivos de Descripción del conector de búsqueda?</span><span class="sxs-lookup"><span data-stu-id="d65b5-122">How Do Search Connector Description Files Work?</span></span>

<span data-ttu-id="d65b5-123">Cuando los archivos de Descripción del conector de búsqueda se instalan en los sistemas de los usuarios, los usuarios pueden abrir el explorador de Windows, hacer clic en el conector de búsqueda en el panel de navegación y especificar una consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-123">When Search Connector Description files are installed on users' systems, users can open Windows Explorer, click the search connector in the navigation pane, and enter a search query.</span></span> <span data-ttu-id="d65b5-124">El explorador de Windows envía la consulta con información del archivo de Descripción del conector de búsqueda, como el proveedor que se va a utilizar y el ámbito de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-124">Windows Explorer sends the query using information from the Search Connector Description file, such as which provider to use and the scope of the search.</span></span> <span data-ttu-id="d65b5-125">Los resultados se devuelven como elementos de fuente RSS o Atom y se muestran a los usuarios como si fueran elementos de Shell normales.</span><span class="sxs-lookup"><span data-stu-id="d65b5-125">The results are returned as RSS or Atom feed items and displayed to users as if they were regular Shell items.</span></span>

<span data-ttu-id="d65b5-126">La forma de implementar el archivo de Descripción del conector de búsqueda depende del tipo de ubicación que admita el conector de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="d65b5-126">How you deploy your Search Connector Description file depends on the type of location the search connector supports:</span></span>

-   <span data-ttu-id="d65b5-127">En un archivo de configuración de OpenSearch ( \* . osdx) para el servicio Web</span><span class="sxs-lookup"><span data-stu-id="d65b5-127">In an OpenSearch configuration (\*.osdx) file for your web service</span></span>
-   <span data-ttu-id="d65b5-128">Como parte de la instalación del controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="d65b5-128">As part of your protocol handler installation</span></span>

<span data-ttu-id="d65b5-129">Debe asegurarse de que se producen las siguientes acciones cuando un usuario abre el archivo. osdx o instala el controlador de protocolo:</span><span class="sxs-lookup"><span data-stu-id="d65b5-129">You should ensure that the following things happen when a user opens the .osdx file or installs the protocol handler:</span></span>

-   <span data-ttu-id="d65b5-130">El archivo. searchconnector-MS se crea en la carpeta de **búsquedas de Windows** de los usuarios (% userprofile%/searches).</span><span class="sxs-lookup"><span data-stu-id="d65b5-130">The .searchconnector-ms file is created in the users' **Windows Searches** folder (%userprofile%/Searches).</span></span>
-   <span data-ttu-id="d65b5-131">Se crea un acceso directo al archivo. searchconnector-MS en la carpeta de **vínculos** de los usuarios (% userprofile%/links).</span><span class="sxs-lookup"><span data-stu-id="d65b5-131">A shortcut to the .searchconnector-ms file is created in the users' **Links** folder (%userprofile%/Links).</span></span>

## <a name="what-is-the-search-connector-description-schema"></a><span data-ttu-id="d65b5-132">¿Qué es el esquema de Descripción del conector de búsqueda?</span><span class="sxs-lookup"><span data-stu-id="d65b5-132">What Is the Search Connector Description Schema?</span></span>

<span data-ttu-id="d65b5-133">El esquema de Descripción del conector de búsqueda es un esquema XML que define la estructura de los archivos de Descripción del conector de búsqueda ( \* . searchConnector-MS).</span><span class="sxs-lookup"><span data-stu-id="d65b5-133">The Search Connector Description schema is an XML schema that defines the structure of Search Connector Description files (\*.searchConnector-ms).</span></span> <span data-ttu-id="d65b5-134">Cada conector de búsqueda debe tener un archivo de Descripción del conector de búsqueda que especifique cómo conectarse a, enviar consultas a y recibir los resultados de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="d65b5-134">Each search connector must have a Search Connector Description file that specifies how to connect to, send queries to, and receive results from the location.</span></span>

## <a name="what-are-the-major-parts-of-the-schema"></a><span data-ttu-id="d65b5-135">¿Cuáles son las partes principales del esquema?</span><span class="sxs-lookup"><span data-stu-id="d65b5-135">What Are the Major Parts of the Schema?</span></span>

<span data-ttu-id="d65b5-136">En la tabla siguiente se enumeran las partes principales del esquema.</span><span class="sxs-lookup"><span data-stu-id="d65b5-136">The following table lists the major parts of the schema.</span></span>



| <span data-ttu-id="d65b5-137">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d65b5-137">Child elements</span></span>                                                                         | <span data-ttu-id="d65b5-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="d65b5-138">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d65b5-139">isSearchOnlyItem</span><span class="sxs-lookup"><span data-stu-id="d65b5-139">isSearchOnlyItem</span></span>](search-schema-sconn-issearchonlyitem.md)                           | <span data-ttu-id="d65b5-140">Identifica si las ubicaciones admitidas por el conector de búsqueda son de solo búsqueda o buscar y examinar.</span><span class="sxs-lookup"><span data-stu-id="d65b5-140">Identifies whether the locations supported by the search connector are search-only or search and browse.</span></span>                                                                                |
| [<span data-ttu-id="d65b5-141">isDefaultSaveLocation</span><span class="sxs-lookup"><span data-stu-id="d65b5-141">isDefaultSaveLocation</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 | <span data-ttu-id="d65b5-142">Solo para uso de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d65b5-142">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="d65b5-143">isDefaultNonOwnerSaveLocation</span><span class="sxs-lookup"><span data-stu-id="d65b5-143">isDefaultNonOwnerSaveLocation</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) | <span data-ttu-id="d65b5-144">Solo para uso de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d65b5-144">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="d65b5-145">description</span><span class="sxs-lookup"><span data-stu-id="d65b5-145">description</span></span>](search-schema-sconn-description.md)                                     | <span data-ttu-id="d65b5-146">Describe el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-146">Describes the search connector.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="d65b5-147">iconReference</span><span class="sxs-lookup"><span data-stu-id="d65b5-147">iconReference</span></span>](search-schema-sconn-iconreference.md)                                 | <span data-ttu-id="d65b5-148">Identifica la ubicación de un icono personalizado para el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-148">Identifies the location of a custom icon for the search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="d65b5-149">imageLink</span><span class="sxs-lookup"><span data-stu-id="d65b5-149">imageLink</span></span>](search-schema-sconn-imagelink.md)                                         | <span data-ttu-id="d65b5-150">Identifica la ubicación de una miniatura personalizada para el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-150">Identifies the location of a custom thumbnail for the search connector.</span></span>                                                                                                                 |
| [<span data-ttu-id="d65b5-151">frente</span><span class="sxs-lookup"><span data-stu-id="d65b5-151">author</span></span>](search-schema-sconn-author.md)                                               | <span data-ttu-id="d65b5-152">Identifica al autor del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-152">Identifies the author of the search connector.</span></span>                                                                                                                                          |
| [<span data-ttu-id="d65b5-153">dateCreated</span><span class="sxs-lookup"><span data-stu-id="d65b5-153">dateCreated</span></span>](search-schema-sconn-datecreated.md)                                     | <span data-ttu-id="d65b5-154">Identifica la fecha en que se creó el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-154">Identifies the date that the search connector was created.</span></span>                                                                                                                              |
| [<span data-ttu-id="d65b5-155">templateInfo</span><span class="sxs-lookup"><span data-stu-id="d65b5-155">templateInfo</span></span>](search-schema-sconn-templateinfo.md)                                   | <span data-ttu-id="d65b5-156">Especifica un tipo de carpeta para el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-156">Specifies a folder type for the search connector.</span></span>                                                                                                                                       |
| [<span data-ttu-id="d65b5-157">locationProvider</span><span class="sxs-lookup"><span data-stu-id="d65b5-157">locationProvider</span></span>](search-schema-sconn-locationprovider.md)                           | <span data-ttu-id="d65b5-158">Especifica el proveedor de búsquedas que va a usar este conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-158">Specifies the search provider to be used by this search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="d65b5-159">scope</span><span class="sxs-lookup"><span data-stu-id="d65b5-159">scope</span></span>](search-schema-sconn-scope.md)                                                 | <span data-ttu-id="d65b5-160">Especifica las ubicaciones que se van a incluir y excluir del ámbito de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-160">Specifies the locations to include in and exclude from the search scope.</span></span>                                                                                                                |
| [<span data-ttu-id="d65b5-161">propertyStore</span><span class="sxs-lookup"><span data-stu-id="d65b5-161">propertyStore</span></span>](search-schema-sconn-propertystore.md)                                 | <span data-ttu-id="d65b5-162">Especifica la ubicación de un [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) basado en XML para este conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-162">Specifies the location of an XML-based [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) for this search connector.</span></span> <span data-ttu-id="d65b5-163">**IPropertyStore** admite los metadatos abiertos del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-163">The **IPropertyStore** supports the search connector's open metadata.</span></span> |
| [<span data-ttu-id="d65b5-164">includeInStartMenuScope</span><span class="sxs-lookup"><span data-stu-id="d65b5-164">includeInStartMenuScope</span></span>](search-schema-sconn-includeinstartmenuscope.md)             | <span data-ttu-id="d65b5-165">Especifica si la ubicación representada por el conector de búsqueda debe incluirse en el ámbito de búsqueda del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="d65b5-165">Specifies whether the location represented by the search connector should be included in the Start menu's search scope.</span></span>                                                                 |
| [<span data-ttu-id="d65b5-166">dominio</span><span class="sxs-lookup"><span data-stu-id="d65b5-166">domain</span></span>](search-schema-sconn-domain.md)                                               | <span data-ttu-id="d65b5-167">Identifica el dominio de nivel superior del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d65b5-167">Identifies the search connector's top-level domain.</span></span>                                                                                                                                     |
| [<span data-ttu-id="d65b5-168">supportsAdvancedQuerySyntax</span><span class="sxs-lookup"><span data-stu-id="d65b5-168">supportsAdvancedQuerySyntax</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     | <span data-ttu-id="d65b5-169">Especifica si el conector de búsqueda admite la sintaxis de consulta avanzada (AQS).</span><span class="sxs-lookup"><span data-stu-id="d65b5-169">Specifies whether the search connector supports Advanced Query Syntax (AQS).</span></span>                                                                                                            |
| [<span data-ttu-id="d65b5-170">isIndexed</span><span class="sxs-lookup"><span data-stu-id="d65b5-170">isIndexed</span></span>](search-schema-sconn-isindexed.md)                                         | <span data-ttu-id="d65b5-171">Especifica si la ubicación representada por el conector de búsqueda está indizada.</span><span class="sxs-lookup"><span data-stu-id="d65b5-171">Specifies whether the location represented by the search connector is indexed.</span></span>                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a><span data-ttu-id="d65b5-172">Ejemplos de archivos de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="d65b5-172">Examples of Search Connector Description Files</span></span>

<span data-ttu-id="d65b5-173">El siguiente es un ejemplo de un archivo de Descripción del conector de búsqueda para un servicio Web de búsqueda federada.</span><span class="sxs-lookup"><span data-stu-id="d65b5-173">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


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



<span data-ttu-id="d65b5-174">El siguiente es un ejemplo de un archivo de Descripción del conector de búsqueda para un controlador de protocolo MAPI.</span><span class="sxs-lookup"><span data-stu-id="d65b5-174">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


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



## <a name="additional-resources"></a><span data-ttu-id="d65b5-175">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d65b5-175">Additional Resources</span></span>

-   <span data-ttu-id="d65b5-176">Para obtener más información sobre el esquema de descripción de la biblioteca, vea [esquema de Descripción](../shell/library-schema-entry.md)de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d65b5-176">For more information about the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>
-   <span data-ttu-id="d65b5-177">Para obtener más información sobre la instalación de un conector de búsqueda, consulte [Federated Search in Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d65b5-177">For more information on installing a search connector, see [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d65b5-178">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d65b5-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d65b5-179">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d65b5-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d65b5-180">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="d65b5-180">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md)
</dt> <dt>

<span data-ttu-id="d65b5-181">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="d65b5-181">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d65b5-182">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="d65b5-182">OpenSearch</span></span>](http://www.opensearch.org/Home)
</dt> <dt>

[<span data-ttu-id="d65b5-183">Centro de descarga de Microsoft</span><span class="sxs-lookup"><span data-stu-id="d65b5-183">Microsoft Download Center</span></span>](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
