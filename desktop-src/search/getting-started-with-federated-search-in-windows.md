---
description: Compatibilidad de Windows 7 con la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch permite a los usuarios tener acceso a sus datos remotos e interactuar con ellos desde el explorador de Windows.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: Introducción con búsqueda federada en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c1f887ff2bdba279cdd25e4910162dd9263d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540651"
---
# <a name="getting-started-with-federated-search-in-windows"></a><span data-ttu-id="ae645-103">Introducción con búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-103">Getting Started with Federated Search in Windows</span></span>

<span data-ttu-id="ae645-104">Compatibilidad de Windows 7 con la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch permite a los usuarios tener acceso a sus datos remotos e interactuar con ellos desde el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae645-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span> <span data-ttu-id="ae645-105">Puede crear un almacén de datos basado en Web en el que se pueda buscar mediante la búsqueda federada de Windows y habilitar la integración enriquecida de los orígenes de datos remotos con el explorador de Windows sin tener que escribir ni implementar ningún código del lado cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae645-105">You can build a web-based data store that can be searched using Windows federated search and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="ae645-106">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ae645-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="ae645-107">¿Qué es la búsqueda federada?</span><span class="sxs-lookup"><span data-stu-id="ae645-107">What is Federated Search?</span></span>](#what-is-federated-search)
-   [<span data-ttu-id="ae645-108">Pasos para crear la búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="ae645-108">Steps for Building Federated Search</span></span>](#steps-for-building-federated-search)
-   [<span data-ttu-id="ae645-109">Cómo funciona la búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="ae645-109">How Federated Search Works</span></span>](#how-federated-search-works)
-   [<span data-ttu-id="ae645-110">Enviar consultas y devolver resultados de búsqueda en RSS o Atom</span><span class="sxs-lookup"><span data-stu-id="ae645-110">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [<span data-ttu-id="ae645-111">Ejemplos de búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="ae645-111">Federated Search Examples</span></span>](#federated-search-examples)
-   [<span data-ttu-id="ae645-112">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ae645-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="ae645-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae645-113">Related topics</span></span>](#related-topics)

## <a name="what-is-federated-search"></a><span data-ttu-id="ae645-114">¿Qué es la búsqueda federada?</span><span class="sxs-lookup"><span data-stu-id="ae645-114">What is Federated Search?</span></span>

<span data-ttu-id="ae645-115">Windows 7 admite la conexión de orígenes externos al cliente de Windows a través del protocolo [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="ae645-115">Windows 7 supports the connection of external sources to the Windows client through the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="ae645-116">Esto permite a los usuarios buscar en un almacén de datos remoto y ver los resultados desde el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae645-116">This enables users to search a remote data store and view results from within Windows Explorer.</span></span> <span data-ttu-id="ae645-117">El estándar de [OpenSearch](https://github.com/dewitt/opensearch) v 1.1 define formatos de archivo simples que se pueden usar para describir cómo un cliente debe consultar el servicio web para el almacén de datos y cómo el servicio debe devolver los resultados que el cliente va a representar.</span><span class="sxs-lookup"><span data-stu-id="ae645-117">The [OpenSearch](https://github.com/dewitt/opensearch) v1.1 standard defines simple file formats that can be used to describe how a client should query the web service for the data store and how the service should return results to be rendered by the client.</span></span> <span data-ttu-id="ae645-118">Windows Federated Search se conecta a los servicios web que reciben consultas de [OpenSearch](https://github.com/dewitt/opensearch) y devuelve los resultados en formato XML de RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="ae645-118">Windows federated search connects to web services that receive [OpenSearch](https://github.com/dewitt/opensearch) queries, and returns results in either the RSS or Atom XML format.</span></span>

<span data-ttu-id="ae645-119">En la captura de pantalla siguiente se muestran los resultados de la búsqueda obtenidos después de buscar un sitio de SharePoint de forma remota.</span><span class="sxs-lookup"><span data-stu-id="ae645-119">The following screen shot illustrates the search results obtained after remotely searching a SharePoint site.</span></span>

![captura de pantalla que muestra los resultados de la búsqueda desde un sitio de SharePoint, tal como se muestra en el explorador de Windows](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a><span data-ttu-id="ae645-121">Pasos para crear la búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="ae645-121">Steps for Building Federated Search</span></span>

<span data-ttu-id="ae645-122">Para generar la búsqueda federada, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ae645-122">To build federated search, perform the following steps:</span></span>

1.  <span data-ttu-id="ae645-123">Habilite la búsqueda en el almacén de datos desde el explorador de Windows proporcionando un servicio Web compatible con [OpenSearch](https://github.com/dewitt/opensearch)que puede devolver resultados en formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="ae645-123">Enable your data store to be searched from Windows Explorer by providing an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service that can return results in RSS or Atom format.</span></span>
2.  <span data-ttu-id="ae645-124">Cree un archivo de descripción de OpenSearch (. osdx) que describa cómo conectarse al servicio Web y cómo asignar cualquier elemento personalizado en el XML de RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="ae645-124">Create an OpenSearch Description (.osdx) file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML.</span></span>
3.  <span data-ttu-id="ae645-125">Implemente los conectores de búsqueda en los equipos cliente de Windows con un archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="ae645-125">Deploy the search connectors to Windows client computers with an .osdx file.</span></span>

<span data-ttu-id="ae645-126">En el diagrama siguiente se muestran los pasos para crear la búsqueda federada.</span><span class="sxs-lookup"><span data-stu-id="ae645-126">The following diagram illustrates the steps for building federated search.</span></span>

![diagrama del proceso de creación de una búsqueda federada](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a><span data-ttu-id="ae645-128">Cómo funciona la búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="ae645-128">How Federated Search Works</span></span>

<span data-ttu-id="ae645-129">La comunicación entre el explorador de Windows y el servicio Web de [OpenSearch](https://github.com/dewitt/opensearch) se realiza a través de la capa de datos de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae645-129">Communication between Windows Explorer and your [OpenSearch](https://github.com/dewitt/opensearch) web service is performed through the Windows Data Layer.</span></span> <span data-ttu-id="ae645-130">El nivel de datos de Windows puede comunicarse con distintos tipos de almacenes de datos a través de los proveedores de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="ae645-130">The Windows Data Layer can communicate with different types of data stores through Windows Store Providers.</span></span> <span data-ttu-id="ae645-131">Cada proveedor se especializa en la comunicación con almacenes de datos que admiten un protocolo determinado y tienen funciones específicas.</span><span class="sxs-lookup"><span data-stu-id="ae645-131">Each provider specializes in communicating with data stores that support a particular protocol and have specific capabilities.</span></span> <span data-ttu-id="ae645-132">Por ejemplo, en la siguiente ilustración se SOWS la forma en que el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) se comunica con almacenes de datos que proporcionan un servicio Web que admite el estándar de [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="ae645-132">For example, the following illustration sows how the [OpenSearch](https://github.com/dewitt/opensearch) provider communicates with data stores that provide a web service that supports the [OpenSearch](https://github.com/dewitt/opensearch) standard.</span></span>

![diagrama que muestra la comunicación desde el explorador de Windows en el cliente a través del almacén de datos de OpenSearch en el servidor remoto](images/windowssearchfederationfunctionality.png)

<span data-ttu-id="ae645-134">Para habilitar el almacén de datos para que admita la búsqueda federada en Windows 7, debe realizar una serie de tareas.</span><span class="sxs-lookup"><span data-stu-id="ae645-134">To enable your data store to support federated search in Windows 7, you must perform a number of tasks.</span></span> <span data-ttu-id="ae645-135">En la tabla siguiente se enumeran las tareas para habilitar el almacén de datos, lo que se necesita para realizar cada tarea y dónde encontrar la documentación.</span><span class="sxs-lookup"><span data-stu-id="ae645-135">The following table lists tasks for enabling your data store, what is required to accomplish each task, and where to find documentation.</span></span>



| <span data-ttu-id="ae645-136">Tarea</span><span class="sxs-lookup"><span data-stu-id="ae645-136">Task</span></span>                                                                                                     | <span data-ttu-id="ae645-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae645-137">Requirement</span></span>                                                                                                                                                                                            | <span data-ttu-id="ae645-138">Documentación</span><span class="sxs-lookup"><span data-stu-id="ae645-138">Documentation</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae645-139">Permite que el explorador de Windows busque en el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="ae645-139">Enable your data store to be searched by Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="ae645-140">Cree un servicio Web compatible con OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="ae645-140">Build an OpenSearch-compatible web service.</span></span><br/> <span data-ttu-id="ae645-141">Cree un archivo de descripción de OpenSearch (. osdx).</span><span class="sxs-lookup"><span data-stu-id="ae645-141">Create an OpenSearch Description (.osdx) file.</span></span><br/>                                                                                       | [<span data-ttu-id="ae645-142">Conexión del servicio Web en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-142">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/> [<span data-ttu-id="ae645-143">Habilitación del almacén de datos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-143">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/> |
| <span data-ttu-id="ae645-144">Implemente activamente el servicio Web en los usuarios de una empresa.</span><span class="sxs-lookup"><span data-stu-id="ae645-144">Actively deploy your web service to users within an enterprise.</span></span><br/>                               | <span data-ttu-id="ae645-145">Proporcione un archivo. osdx a los usuarios, cópielo localmente y haga que sea accesible para el usuario a través de un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="ae645-145">Supply an .osdx file to your users, copy it locally, and make it accessible to the user via a shortcut.</span></span><br/>                                                                                     | [<span data-ttu-id="ae645-146">Implementación de conectores de búsqueda en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-146">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)<br/>                                                                                                              |
| <span data-ttu-id="ae645-147">Enumerar los resultados de la búsqueda en el explorador de Windows como respuesta a una consulta.</span><span class="sxs-lookup"><span data-stu-id="ae645-147">Enumerate search results in Windows Explorer in response to a query.</span></span><br/>                          | <span data-ttu-id="ae645-148">Implemente un servicio Web que acepte una cadena de consulta y devuelva resultados en formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="ae645-148">Implement a web service that accepts a query string and returns results in RSS or Atom format.</span></span><br/>                                                                                              | [<span data-ttu-id="ae645-149">Conexión del servicio Web en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-149">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/>                                                                                                            |
| <span data-ttu-id="ae645-150">Permitir a los usuarios agregar el almacén de datos al explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae645-150">Enable users to add your data store to their Windows Explorer.</span></span><br/>                                | <span data-ttu-id="ae645-151">Cree un archivo. osdx y proporcione a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ae645-151">Create an .osdx file and supply it to your users.</span></span><br/>                                                                                                                                           | [<span data-ttu-id="ae645-152">Habilitación del almacén de datos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-152">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="ae645-153">Mostrar los elementos como elementos de tipo archivo en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae645-153">Display your items as file-like items in Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="ae645-154">Devolver una dirección URL al archivo o la secuencia de contenido mediante los elementos de **contenedor** o **multimedia: contenido**</span><span class="sxs-lookup"><span data-stu-id="ae645-154">Return a URL to the file or content stream by using **enclosure** or **media:content** elements</span></span><br/> <span data-ttu-id="ae645-155">Proporcione una extensión de nombre de archivo o un tipo MIME que el equipo cliente reconozca.</span><span class="sxs-lookup"><span data-stu-id="ae645-155">Supply a file name extension or a MIME type that the client computer recognizes.</span></span><br/> | [<span data-ttu-id="ae645-156">Habilitación del almacén de datos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-156">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="ae645-157">Mostrar propiedades personalizadas en el explorador de Windows, más allá de las definidas en los estándares RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="ae645-157">Display custom properties in Windows Explorer, beyond those defined in RSS or Atom standards.</span></span><br/> | <span data-ttu-id="ae645-158">Proporcione metadatos adicionales mediante el uso de otro espacio de nombres XML en la salida RSS/Atom.</span><span class="sxs-lookup"><span data-stu-id="ae645-158">Provide additional metadata by using another XML namespace in your RSS/Atom output.</span></span><br/> <span data-ttu-id="ae645-159">Agregue una asignación de propiedad al archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="ae645-159">Add a property map to your .osdx file.</span></span><br/>                                                       | [<span data-ttu-id="ae645-160">Creación de un archivo de descripción de OpenSearch en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="ae645-160">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="ae645-161">Personalizar las propiedades que se muestran para los elementos en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae645-161">Customize the properties that are displayed for your items in Windows Explorer.</span></span><br/>               | <span data-ttu-id="ae645-162">Agregue asignaciones de proplist al archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="ae645-162">Add proplist mappings to your .osdx file.</span></span><br/>                                                                                                                                                   | [<span data-ttu-id="ae645-163">Creación de un archivo de descripción de OpenSearch en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="ae645-163">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="ae645-164">Mostrar una vista de página web personalizada de los elementos en el panel de vista previa.</span><span class="sxs-lookup"><span data-stu-id="ae645-164">Display a custom webpage view of your items in the preview pane.</span></span><br/>                              | <span data-ttu-id="ae645-165">Devolver valores de vínculo y de contenedor distintos.</span><span class="sxs-lookup"><span data-stu-id="ae645-165">Return distinct link and enclosure values.</span></span><br/> <span data-ttu-id="ae645-166">Asigne un valor de dirección URL a la propiedad del shell de Windows **System. WebPreviewUrl** .</span><span class="sxs-lookup"><span data-stu-id="ae645-166">Map a URL value to the **System.WebPreviewUrl** Windows Shell property.</span></span><br/>                                                               | [<span data-ttu-id="ae645-167">Creación de un archivo de descripción de OpenSearch en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="ae645-167">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="ae645-168">Mostrar un botón de la barra de comandos en el explorador de Windows que revierta la consulta en el sitio Web.</span><span class="sxs-lookup"><span data-stu-id="ae645-168">Display a command bar button in Windows Explorer that rolls the query over to your website.</span></span><br/>   | <span data-ttu-id="ae645-169">Proporcione una `Url format="text/html"` plantilla en el archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="ae645-169">Provide a `Url format="text/html"` template in the .osdx file.</span></span><br/>                                                                                                                              | [<span data-ttu-id="ae645-170">Creación de un archivo de descripción de OpenSearch en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="ae645-170">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="ae645-171">Enviar consultas y devolver resultados de búsqueda en RSS o Atom</span><span class="sxs-lookup"><span data-stu-id="ae645-171">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="ae645-172">Cuando el usuario escribe un término en el cuadro de búsqueda en la esquina superior derecha del explorador de Windows, la consulta se envía al proveedor de [OpenSearch](https://github.com/dewitt/opensearch) , que, a continuación, envía la consulta al almacén de datos remoto.</span><span class="sxs-lookup"><span data-stu-id="ae645-172">When the user types a term into the search box in the upper-right corner of Windows Explorer, the query is sent to the [OpenSearch](https://github.com/dewitt/opensearch) provider, which then sends the query to the remote data store.</span></span> <span data-ttu-id="ae645-173">El servicio Web remoto responde a la consulta proporcionando los resultados en un documento XML, normalmente denominado fuente, en uno de los dos formatos admitidos (RSS o Atom).</span><span class="sxs-lookup"><span data-stu-id="ae645-173">The remote web service responds to the query by providing results in an XML document, typically referred to as a feed, in one of two supported formats (RSS or Atom).</span></span> <span data-ttu-id="ae645-174">Cada elemento de resultado de la fuente incluye elementos secundarios XML para representar o describir metadatos de elementos, como el título, la dirección URL, la descripción, la imagen en miniatura, etc.</span><span class="sxs-lookup"><span data-stu-id="ae645-174">Each result item in the feed includes XML child elements to represent or describe item metadata, such as the title, URL, description, thumbnail image, and so forth.</span></span> <span data-ttu-id="ae645-175">El proveedor de [OpenSearch](https://github.com/dewitt/opensearch) es responsable de asignar los valores del elemento XML a las propiedades del sistema del shell de Windows que pueden usar las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae645-175">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span>

## <a name="federated-search-examples"></a><span data-ttu-id="ae645-176">Ejemplos de búsqueda federada</span><span class="sxs-lookup"><span data-stu-id="ae645-176">Federated Search Examples</span></span>

<span data-ttu-id="ae645-177">En el ejemplo siguiente, el archivo de descripción de OpenSearch (. osdx) consta de los `ShortName` `Url` elementos y, que son los elementos secundarios mínimos necesarios para conectar un almacén de datos externo al cliente de Windows a través del protocolo OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="ae645-177">The following example OpenSearch Description (.osdx) file consists of `ShortName` and `Url` elements, which are the minimum required child elements to connect an external data store to the Windows client through the OpenSearch protocol.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



<span data-ttu-id="ae645-178">En el ejemplo siguiente se muestra cómo hacer que un almacén de datos habilitado para web se pueda buscar en formato RSS y cómo especificar que se devuelva un elemento de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="ae645-178">The following example illustrates how to make a web-enabled data store searchable in RSS format, and how to specify that one search item be returned:</span></span>


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



<span data-ttu-id="ae645-179">En el ejemplo siguiente se muestra cómo asignar propiedades a las propiedades del sistema predeterminadas para que los elementos mostrados se ordenen y agrupen:</span><span class="sxs-lookup"><span data-stu-id="ae645-179">The following example illustrates how to map properties to default system properties so that displayed items are sorted and grouped:</span></span>


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



<span data-ttu-id="ae645-180">En el ejemplo siguiente se muestra cómo agregar una pantalla de imagen en miniatura a cada elemento en el explorador de Windows:</span><span class="sxs-lookup"><span data-stu-id="ae645-180">The following example illustrates how to adds a thumbnail image display to each item in Windows Explorer:</span></span>


```
<media:thumbnail>    
```



## <a name="additional-resources"></a><span data-ttu-id="ae645-181">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ae645-181">Additional Resources</span></span>

<span data-ttu-id="ae645-182">Para obtener información adicional sobre la implementación de la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, consulte "recursos adicionales" en [búsqueda federada en Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ae645-182">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae645-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae645-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae645-184">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-184">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="ae645-185">Conexión del servicio Web en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-185">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="ae645-186">Habilitación del almacén de datos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-186">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="ae645-187">Creación de un archivo de descripción de OpenSearch en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="ae645-187">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="ae645-188">Siguientes procedimientos recomendados en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-188">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="ae645-189">Implementación de conectores de búsqueda en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="ae645-189">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 




