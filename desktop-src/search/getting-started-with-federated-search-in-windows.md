---
description: Obtenga información sobre la búsqueda federada, que permite a los usuarios acceder a sus datos remotos e interactuar con ellos desde Explorador de Windows.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: Tareas iniciales con la búsqueda federada en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de3fc42686e94f2edc1c5d45bbb0374afe79535
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119070"
---
# <a name="getting-started-with-federated-search-in-windows"></a><span data-ttu-id="0bb0a-103">Tareas iniciales con la búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="0bb0a-103">Getting Started with Federated Search in Windows</span></span>

<span data-ttu-id="0bb0a-104">La compatibilidad de Windows 7 con la federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch permite a los usuarios acceder a sus datos remotos e interactuar con ellos desde dentro Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span> <span data-ttu-id="0bb0a-105">Puede crear un almacén de datos basado en web que se pueda buscar mediante la búsqueda federada de Windows y habilitar la integración enriquecida de los orígenes de datos remotos con Explorador de Windows sin tener que escribir ni implementar ningún código del lado cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-105">You can build a web-based data store that can be searched using Windows federated search and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="0bb0a-106">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="0bb0a-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="0bb0a-107">¿Qué es la búsqueda federada?</span><span class="sxs-lookup"><span data-stu-id="0bb0a-107">What is Federated Search?</span></span>](#what-is-federated-search)
-   [<span data-ttu-id="0bb0a-108">Pasos para compilar la búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="0bb0a-108">Steps for Building Federated Search</span></span>](#steps-for-building-federated-search)
-   [<span data-ttu-id="0bb0a-109">Funcionamiento de la búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="0bb0a-109">How Federated Search Works</span></span>](#how-federated-search-works)
-   [<span data-ttu-id="0bb0a-110">Envío de consultas y devolución de resultados de búsqueda en RSS o Atom</span><span class="sxs-lookup"><span data-stu-id="0bb0a-110">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [<span data-ttu-id="0bb0a-111">Ejemplos de búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="0bb0a-111">Federated Search Examples</span></span>](#federated-search-examples)
-   [<span data-ttu-id="0bb0a-112">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="0bb0a-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="0bb0a-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bb0a-113">Related topics</span></span>](#related-topics)

## <a name="what-is-federated-search"></a><span data-ttu-id="0bb0a-114">¿Qué es la búsqueda federada?</span><span class="sxs-lookup"><span data-stu-id="0bb0a-114">What is Federated Search?</span></span>

<span data-ttu-id="0bb0a-115">Windows 7 admite la conexión de orígenes externos al cliente de Windows a través del [protocolo OpenSearch.](https://github.com/dewitt/opensearch)</span><span class="sxs-lookup"><span data-stu-id="0bb0a-115">Windows 7 supports the connection of external sources to the Windows client through the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="0bb0a-116">Esto permite a los usuarios buscar en un almacén de datos remoto y ver los resultados desde dentro Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-116">This enables users to search a remote data store and view results from within Windows Explorer.</span></span> <span data-ttu-id="0bb0a-117">El estándar [OpenSearch](https://github.com/dewitt/opensearch) v1.1 define formatos de archivo simples que se pueden usar para describir cómo un cliente debe consultar el servicio web para el almacén de datos y cómo el servicio debe devolver los resultados que el cliente debe representar.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-117">The [OpenSearch](https://github.com/dewitt/opensearch) v1.1 standard defines simple file formats that can be used to describe how a client should query the web service for the data store and how the service should return results to be rendered by the client.</span></span> <span data-ttu-id="0bb0a-118">La búsqueda federada de Windows se conecta a los servicios web que reciben consultas [de OpenSearch](https://github.com/dewitt/opensearch) y devuelve resultados en formato RSS o ATOM XML.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-118">Windows federated search connects to web services that receive [OpenSearch](https://github.com/dewitt/opensearch) queries, and returns results in either the RSS or Atom XML format.</span></span>

<span data-ttu-id="0bb0a-119">En la siguiente captura de pantalla se muestran los resultados de búsqueda obtenidos después de buscar de forma remota en un sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-119">The following screen shot illustrates the search results obtained after remotely searching a SharePoint site.</span></span>

![captura de pantalla que muestra los resultados de la búsqueda desde un sitio de SharePoint como se muestra en el Explorador de Windows](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a><span data-ttu-id="0bb0a-121">Pasos para compilar la búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="0bb0a-121">Steps for Building Federated Search</span></span>

<span data-ttu-id="0bb0a-122">Para compilar la búsqueda federada, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0bb0a-122">To build federated search, perform the following steps:</span></span>

1.  <span data-ttu-id="0bb0a-123">Habilite la búsqueda del almacén de datos desde Explorador de Windows proporcionando un servicio web compatible con [OpenSearch](https://github.com/dewitt/opensearch)que pueda devolver resultados en formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-123">Enable your data store to be searched from Windows Explorer by providing an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service that can return results in RSS or Atom format.</span></span>
2.  <span data-ttu-id="0bb0a-124">Cree un archivo de descripción de OpenSearch (.osdx) que describa cómo conectarse al servicio web y cómo asignar elementos personalizados en RSS o ATOM XML.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-124">Create an OpenSearch Description (.osdx) file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML.</span></span>
3.  <span data-ttu-id="0bb0a-125">Implemente los conectores de búsqueda en equipos cliente windows con un archivo .osdx.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-125">Deploy the search connectors to Windows client computers with an .osdx file.</span></span>

<span data-ttu-id="0bb0a-126">En el diagrama siguiente se muestran los pasos para crear búsquedas federadas.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-126">The following diagram illustrates the steps for building federated search.</span></span>

![diagrama del proceso de creación de búsqueda federada](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a><span data-ttu-id="0bb0a-128">Funcionamiento de la búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="0bb0a-128">How Federated Search Works</span></span>

<span data-ttu-id="0bb0a-129">La comunicación entre Explorador de Windows y el servicio web [de OpenSearch](https://github.com/dewitt/opensearch) se realiza a través de la capa de datos de Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-129">Communication between Windows Explorer and your [OpenSearch](https://github.com/dewitt/opensearch) web service is performed through the Windows Data Layer.</span></span> <span data-ttu-id="0bb0a-130">La capa de datos de Windows puede comunicarse con diferentes tipos de almacenes de datos a través de proveedores de la Tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-130">The Windows Data Layer can communicate with different types of data stores through Windows Store Providers.</span></span> <span data-ttu-id="0bb0a-131">Cada proveedor se especializa en comunicarse con almacenes de datos que admiten un protocolo determinado y tienen funcionalidades específicas.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-131">Each provider specializes in communicating with data stores that support a particular protocol and have specific capabilities.</span></span> <span data-ttu-id="0bb0a-132">Por ejemplo, en la ilustración siguiente se explica cómo el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) se comunica con los almacenes de datos que proporcionan un servicio web que admite el [estándar OpenSearch.](https://github.com/dewitt/opensearch)</span><span class="sxs-lookup"><span data-stu-id="0bb0a-132">For example, the following illustration sows how the [OpenSearch](https://github.com/dewitt/opensearch) provider communicates with data stores that provide a web service that supports the [OpenSearch](https://github.com/dewitt/opensearch) standard.</span></span>

![diagrama que muestra la comunicación desde el Explorador de Windows en el cliente a través del almacén de datos opensearch en el servidor remoto](images/windowssearchfederationfunctionality.png)

<span data-ttu-id="0bb0a-134">Para permitir que el almacén de datos admita la búsqueda federada en Windows 7, debe realizar una serie de tareas.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-134">To enable your data store to support federated search in Windows 7, you must perform a number of tasks.</span></span> <span data-ttu-id="0bb0a-135">En la tabla siguiente se enumeran las tareas para habilitar el almacén de datos, lo que se necesita para realizar cada tarea y dónde encontrar documentación.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-135">The following table lists tasks for enabling your data store, what is required to accomplish each task, and where to find documentation.</span></span>



| <span data-ttu-id="0bb0a-136">Tarea</span><span class="sxs-lookup"><span data-stu-id="0bb0a-136">Task</span></span>                                                                                                     | <span data-ttu-id="0bb0a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bb0a-137">Requirement</span></span>                                                                                                                                                                                            | <span data-ttu-id="0bb0a-138">Documentación</span><span class="sxs-lookup"><span data-stu-id="0bb0a-138">Documentation</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb0a-139">Habilite el almacén de datos para que lo busquen Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-139">Enable your data store to be searched by Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="0bb0a-140">Cree un servicio web compatible con OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-140">Build an OpenSearch-compatible web service.</span></span><br/> <span data-ttu-id="0bb0a-141">Cree un archivo de descripción de OpenSearch (.osdx).</span><span class="sxs-lookup"><span data-stu-id="0bb0a-141">Create an OpenSearch Description (.osdx) file.</span></span><br/>                                                                                       | [<span data-ttu-id="0bb0a-142">Conexión del servicio web en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="0bb0a-142">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/> [<span data-ttu-id="0bb0a-143">Habilitación del almacén de datos en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="0bb0a-143">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/> |
| <span data-ttu-id="0bb0a-144">Implemente activamente el servicio web para los usuarios de una empresa.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-144">Actively deploy your web service to users within an enterprise.</span></span><br/>                               | <span data-ttu-id="0bb0a-145">Proporcione un archivo .osdx a los usuarios, cópielo localmente y haga que sea accesible para el usuario a través de un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-145">Supply an .osdx file to your users, copy it locally, and make it accessible to the user via a shortcut.</span></span><br/>                                                                                     | [<span data-ttu-id="0bb0a-146">Implementación de conectores de búsqueda en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="0bb0a-146">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)<br/>                                                                                                              |
| <span data-ttu-id="0bb0a-147">Enumerar los resultados de la búsqueda Explorador de Windows respuesta a una consulta.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-147">Enumerate search results in Windows Explorer in response to a query.</span></span><br/>                          | <span data-ttu-id="0bb0a-148">Implemente un servicio web que acepte una cadena de consulta y devuelva resultados en formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-148">Implement a web service that accepts a query string and returns results in RSS or Atom format.</span></span><br/>                                                                                              | [<span data-ttu-id="0bb0a-149">Conexión del servicio web en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="0bb0a-149">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/>                                                                                                            |
| <span data-ttu-id="0bb0a-150">Permitir que los usuarios agreguen el almacén de datos a sus Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-150">Enable users to add your data store to their Windows Explorer.</span></span><br/>                                | <span data-ttu-id="0bb0a-151">Cree un archivo .osdx y proporcionelo a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-151">Create an .osdx file and supply it to your users.</span></span><br/>                                                                                                                                           | [<span data-ttu-id="0bb0a-152">Habilitación del almacén de datos en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="0bb0a-152">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="0bb0a-153">Muestre los elementos como elementos similares a archivos en Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-153">Display your items as file-like items in Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="0bb0a-154">Devolver una dirección URL al archivo o flujo de contenido mediante elementos **enclosure** o **media:content**</span><span class="sxs-lookup"><span data-stu-id="0bb0a-154">Return a URL to the file or content stream by using **enclosure** or **media:content** elements</span></span><br/> <span data-ttu-id="0bb0a-155">Proporcione una extensión de nombre de archivo o un tipo MIME que reconozca el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-155">Supply a file name extension or a MIME type that the client computer recognizes.</span></span><br/> | [<span data-ttu-id="0bb0a-156">Habilitación del almacén de datos en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="0bb0a-156">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="0bb0a-157">Mostrar propiedades personalizadas en Explorador de Windows, más allá de las definidas en estándares RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-157">Display custom properties in Windows Explorer, beyond those defined in RSS or Atom standards.</span></span><br/> | <span data-ttu-id="0bb0a-158">Proporcione metadatos adicionales mediante otro espacio de nombres XML en la salida RSS/Atom.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-158">Provide additional metadata by using another XML namespace in your RSS/Atom output.</span></span><br/> <span data-ttu-id="0bb0a-159">Agregue un mapa de propiedades al archivo .osdx.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-159">Add a property map to your .osdx file.</span></span><br/>                                                       | [<span data-ttu-id="0bb0a-160">Creación de un archivo de descripción de OpenSearch en La búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="0bb0a-160">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="0bb0a-161">Personalice las propiedades que se muestran para los elementos de Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-161">Customize the properties that are displayed for your items in Windows Explorer.</span></span><br/>               | <span data-ttu-id="0bb0a-162">Agregue asignaciones proplist al archivo .osdx.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-162">Add proplist mappings to your .osdx file.</span></span><br/>                                                                                                                                                   | [<span data-ttu-id="0bb0a-163">Creación de un archivo de descripción de OpenSearch en La búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="0bb0a-163">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="0bb0a-164">Mostrar una vista de página web personalizada de los elementos en el panel de vista previa.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-164">Display a custom webpage view of your items in the preview pane.</span></span><br/>                              | <span data-ttu-id="0bb0a-165">Devuelve distintos valores de vínculo y alojamiento.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-165">Return distinct link and enclosure values.</span></span><br/> <span data-ttu-id="0bb0a-166">Asigne un valor de dirección URL a **la propiedad System.WebPreviewUrl** del Shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-166">Map a URL value to the **System.WebPreviewUrl** Windows Shell property.</span></span><br/>                                                               | [<span data-ttu-id="0bb0a-167">Creación de un archivo de descripción de OpenSearch en La búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="0bb0a-167">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="0bb0a-168">Muestre un botón de la barra de comandos Explorador de Windows que revierte la consulta al sitio web.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-168">Display a command bar button in Windows Explorer that rolls the query over to your website.</span></span><br/>   | <span data-ttu-id="0bb0a-169">Proporcione una `Url format="text/html"` plantilla en el archivo .osdx.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-169">Provide a `Url format="text/html"` template in the .osdx file.</span></span><br/>                                                                                                                              | [<span data-ttu-id="0bb0a-170">Creación de un archivo de descripción de OpenSearch en La búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="0bb0a-170">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="0bb0a-171">Envío de consultas y devolución de resultados de búsqueda en RSS o Atom</span><span class="sxs-lookup"><span data-stu-id="0bb0a-171">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="0bb0a-172">Cuando el usuario escriba un término en el cuadro de búsqueda de la esquina superior derecha de Explorador de Windows, la consulta se envía al proveedor [de OpenSearch,](https://github.com/dewitt/opensearch) que envía la consulta al almacén de datos remoto.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-172">When the user types a term into the search box in the upper-right corner of Windows Explorer, the query is sent to the [OpenSearch](https://github.com/dewitt/opensearch) provider, which then sends the query to the remote data store.</span></span> <span data-ttu-id="0bb0a-173">El servicio web remoto responde a la consulta proporcionando resultados en un documento XML, normalmente denominado fuente, en uno de los dos formatos admitidos (RSS o Atom).</span><span class="sxs-lookup"><span data-stu-id="0bb0a-173">The remote web service responds to the query by providing results in an XML document, typically referred to as a feed, in one of two supported formats (RSS or Atom).</span></span> <span data-ttu-id="0bb0a-174">Cada elemento de resultado de la fuente incluye elementos secundarios XML para representar o describir metadatos de elementos, como el título, la dirección URL, la descripción, la imagen en miniatura, etc.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-174">Each result item in the feed includes XML child elements to represent or describe item metadata, such as the title, URL, description, thumbnail image, and so forth.</span></span> <span data-ttu-id="0bb0a-175">El [proveedor de OpenSearch](https://github.com/dewitt/opensearch) es responsable de asignar los valores de elemento XML a las propiedades del sistema de Windows Shell que pueden usar las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-175">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span>

## <a name="federated-search-examples"></a><span data-ttu-id="0bb0a-176">Ejemplos de búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="0bb0a-176">Federated Search Examples</span></span>

<span data-ttu-id="0bb0a-177">El siguiente archivo de descripción de OpenSearch (.osdx) de ejemplo consta de elementos y , que son los elementos secundarios mínimos necesarios para conectar un almacén de datos externo al cliente de Windows a través del protocolo `ShortName` `Url` OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="0bb0a-177">The following example OpenSearch Description (.osdx) file consists of `ShortName` and `Url` elements, which are the minimum required child elements to connect an external data store to the Windows client through the OpenSearch protocol.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



<span data-ttu-id="0bb0a-178">En el ejemplo siguiente se muestra cómo hacer que un almacén de datos habilitado para web pueda realizar búsquedas en formato RSS y cómo especificar que se devuelva un elemento de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="0bb0a-178">The following example illustrates how to make a web-enabled data store searchable in RSS format, and how to specify that one search item be returned:</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, then you would be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="0bb0a-179">En el ejemplo siguiente se muestra cómo asignar propiedades a las propiedades predeterminadas del sistema para que los elementos mostrados se ordenan y agrupan:</span><span class="sxs-lookup"><span data-stu-id="0bb0a-179">The following example illustrates how to map properties to default system properties so that displayed items are sorted and grouped:</span></span>


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



<span data-ttu-id="0bb0a-180">En el ejemplo siguiente se muestra cómo agregar una presentación de imagen en miniatura a cada elemento de Explorador de Windows:</span><span class="sxs-lookup"><span data-stu-id="0bb0a-180">The following example illustrates how to adds a thumbnail image display to each item in Windows Explorer:</span></span>


```
<media:thumbnail>    
```



## <a name="additional-resources"></a><span data-ttu-id="0bb0a-181">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="0bb0a-181">Additional Resources</span></span>

<span data-ttu-id="0bb0a-182">Para obtener información adicional sobre cómo implementar la federación de búsqueda en almacenes de datos remotos mediante tecnologías OpenSearch en Windows 7 y versiones posteriores, vea "Recursos adicionales" en Búsqueda federada [en Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0bb0a-182">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bb0a-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bb0a-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bb0a-184">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="0bb0a-184">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="0bb0a-185">Conexión del servicio web en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="0bb0a-185">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="0bb0a-186">Habilitación del almacén de datos en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="0bb0a-186">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="0bb0a-187">Creación de un archivo de descripción de OpenSearch en La búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="0bb0a-187">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="0bb0a-188">Procedimientos recomendados siguientes en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="0bb0a-188">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="0bb0a-189">Implementación de conectores de búsqueda en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="0bb0a-189">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 




