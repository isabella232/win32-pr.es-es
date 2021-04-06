---
description: Describe cómo crear un archivo de descripción de OpenSearch (. osdx) para conectar los almacenes de datos externos al cliente de Windows a través del protocolo OpenSearch.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Creación de un archivo de descripción de OpenSearch en Windows Federated Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000998"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a><span data-ttu-id="582ee-103">Creación de un archivo de descripción de OpenSearch en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="582ee-103">Creating an OpenSearch Description File in Windows Federated Search</span></span>

<span data-ttu-id="582ee-104">Describe cómo crear un archivo de descripción de OpenSearch (. osdx) para conectar los almacenes de datos externos al cliente de Windows a través del protocolo [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="582ee-104">Describes how to create an OpenSearch Description (.osdx) file to connect external data stores to the Windows Client via the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="582ee-105">La búsqueda federada permite a los usuarios buscar en un almacén de datos remoto y ver los resultados desde el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="582ee-105">Federated search enables users to search a remote data store and view the results from within Windows Explorer.</span></span>

<span data-ttu-id="582ee-106">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="582ee-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="582ee-107">Archivo de descripción de OpenSearch</span><span class="sxs-lookup"><span data-stu-id="582ee-107">OpenSearch Description File</span></span>](#opensearch-description-file)
    -   [<span data-ttu-id="582ee-108">Mínimo elementos secundarios requeridos</span><span class="sxs-lookup"><span data-stu-id="582ee-108">Mininum Required Child Elements</span></span>](#mininum-required-child-elements)
-   [<span data-ttu-id="582ee-109">Elementos estándar en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="582ee-109">Standard Elements in Windows Federated Search</span></span>](#standard-elements-in-windows-federated-search)
    -   [<span data-ttu-id="582ee-110">Corto</span><span class="sxs-lookup"><span data-stu-id="582ee-110">Shortname</span></span>](#shortname)
    -   [<span data-ttu-id="582ee-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="582ee-111">Description</span></span>](#description)
    -   [<span data-ttu-id="582ee-112">Plantilla de dirección URL para resultados de RSS/Atom</span><span class="sxs-lookup"><span data-stu-id="582ee-112">URL Template for RSS/Atom Results</span></span>](#url-template-for-rssatom-results)
    -   [<span data-ttu-id="582ee-113">Plantilla de dirección URL para resultados Web</span><span class="sxs-lookup"><span data-stu-id="582ee-113">URL Template for web Results</span></span>](#url-template-for-web-results)
    -   [<span data-ttu-id="582ee-114">Parámetros de plantilla de URL</span><span class="sxs-lookup"><span data-stu-id="582ee-114">URL Template Parameters</span></span>](#url-template-parameters)
    -   [<span data-ttu-id="582ee-115">Resultados paginados</span><span class="sxs-lookup"><span data-stu-id="582ee-115">Paged Results</span></span>](#paged-results)
    -   [<span data-ttu-id="582ee-116">Paginación mediante el índice del elemento</span><span class="sxs-lookup"><span data-stu-id="582ee-116">Paging Using the Item Index</span></span>](#paging-using-the-item-index)
    -   [<span data-ttu-id="582ee-117">Paginación mediante el índice de página</span><span class="sxs-lookup"><span data-stu-id="582ee-117">Paging Using the Page Index</span></span>](#paging-using-the-page-index)
    -   [<span data-ttu-id="582ee-118">Tamaño de página</span><span class="sxs-lookup"><span data-stu-id="582ee-118">Page Size</span></span>](#page-size)
-   [<span data-ttu-id="582ee-119">Elementos extendidos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="582ee-119">Extended Elements in Windows Federated Search</span></span>](#extended-elements-in-windows-federated-search)
    -   [<span data-ttu-id="582ee-120">Número máximo de resultados</span><span class="sxs-lookup"><span data-stu-id="582ee-120">Maximum Result Count</span></span>](#maximum-result-count)
    -   [<span data-ttu-id="582ee-121">Asignación de propiedades</span><span class="sxs-lookup"><span data-stu-id="582ee-121">Property Mapping</span></span>](#property-mapping)
-   [<span data-ttu-id="582ee-122">Vistas previas</span><span class="sxs-lookup"><span data-stu-id="582ee-122">Previews</span></span>](#previews)
-   [<span data-ttu-id="582ee-123">Abrir el elemento de menú Ubicación del archivo</span><span class="sxs-lookup"><span data-stu-id="582ee-123">Open File Location Menu Item</span></span>](#open-file-location-menu-item)
-   [<span data-ttu-id="582ee-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="582ee-124">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="582ee-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="582ee-125">Related topics</span></span>](#related-topics)

## <a name="opensearch-description-file"></a><span data-ttu-id="582ee-126">Archivo de descripción de OpenSearch</span><span class="sxs-lookup"><span data-stu-id="582ee-126">OpenSearch Description File</span></span>

<span data-ttu-id="582ee-127">Un archivo de descripción de OpenSearch (. osdx) para la búsqueda federada de Windows debe cumplir las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="582ee-127">An OpenSearch Description (.osdx) file for Windows Federated Search must abide by the following rules:</span></span>

-   <span data-ttu-id="582ee-128">Ser un documento de descripción de OpenSearch válido, tal y como se define en la especificación de [opensearch](https://github.com/dewitt/opensearch) 1,1.</span><span class="sxs-lookup"><span data-stu-id="582ee-128">Be a valid OpenSearch Description document, as defined by the [OpenSearch](https://github.com/dewitt/opensearch) 1.1 specification.</span></span>
-   <span data-ttu-id="582ee-129">Proporcione una plantilla de dirección URL con un tipo de formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="582ee-129">Provide a URL template with either an RSS or an Atom format type.</span></span>
-   <span data-ttu-id="582ee-130">Use la extensión de nombre de archivo. osdx o asocie la extensión de nombre de archivo. osdx al descargar desde Internet.</span><span class="sxs-lookup"><span data-stu-id="582ee-130">Use the .osdx file name extension, or be associated with the .osdx file name extension when downloading from the web.</span></span> <span data-ttu-id="582ee-131">Por ejemplo, no es necesario que un servidor use. osdx.</span><span class="sxs-lookup"><span data-stu-id="582ee-131">For example, a server is not required to use .osdx.</span></span> <span data-ttu-id="582ee-132">Un servidor puede devolver el archivo con cualquier extensión de nombre de archivo, como. XML por ejemplo, y tratarse como si fuera un archivo. Osdx Si usa el tipo MIME correcto para los documentos de descripción de OpenSearch (archivos. osdx).</span><span class="sxs-lookup"><span data-stu-id="582ee-132">A server can return the file with any file name extension, such as .xml for example, and treated as if it were an .osdx file if it uses the correct MIME Type for OpenSearch Description documents (.osdx files).</span></span>
-   <span data-ttu-id="582ee-133">Proporcione un valor de elemento **nombre_corto** (recomendado).</span><span class="sxs-lookup"><span data-stu-id="582ee-133">Provide a **ShortName** element value (recommended).</span></span>

### <a name="mininum-required-child-elements"></a><span data-ttu-id="582ee-134">Mínimo elementos secundarios requeridos</span><span class="sxs-lookup"><span data-stu-id="582ee-134">Mininum Required Child Elements</span></span>

<span data-ttu-id="582ee-135">El siguiente archivo de ejemplo. osdx está compuesto por los elementos **nombre_corto** y `Url` , que son los elementos secundarios mínimos necesarios.</span><span class="sxs-lookup"><span data-stu-id="582ee-135">The following example .osdx file consists of **ShortName** and `Url` elements, which are the minimum required child elements.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a><span data-ttu-id="582ee-136">Elementos estándar en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="582ee-136">Standard Elements in Windows Federated Search</span></span>

<span data-ttu-id="582ee-137">Además de los elementos secundarios mínimos, la búsqueda federada admite los siguientes elementos estándar.</span><span class="sxs-lookup"><span data-stu-id="582ee-137">In addition to the minimum child elements, federated search supports the following standard elements.</span></span>

### <a name="shortname"></a><span data-ttu-id="582ee-138">Corto</span><span class="sxs-lookup"><span data-stu-id="582ee-138">Shortname</span></span>

<span data-ttu-id="582ee-139">Windows usa el valor del elemento **nombre_corto** para asignar un nombre al archivo. searchconnector-MS (conector de búsqueda) que se crea cuando el usuario abre el archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="582ee-139">Windows uses the **ShortName** element value to name the .searchconnector-ms (search connector) file that is created when the user opens the .osdx file.</span></span> <span data-ttu-id="582ee-140">Windows se asegura de que el nombre de archivo generado solo usa caracteres permitidos en los nombres de archivo de Windows.</span><span class="sxs-lookup"><span data-stu-id="582ee-140">Windows ensures that the generated file name uses only characters that are allowed in Windows file names.</span></span> <span data-ttu-id="582ee-141">Si no se proporciona ningún valor de **ShortName** , el archivo. searchconnector-MS intenta usar el nombre de archivo del archivo. osdx en su lugar.</span><span class="sxs-lookup"><span data-stu-id="582ee-141">If no **ShortName** value is provided, the .searchconnector-ms file tries to use the file name of the .osdx file instead.</span></span>

<span data-ttu-id="582ee-142">En el código siguiente se muestra cómo usar el elemento **nombre_corto** en un archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="582ee-142">The following code illustrates how to use the **ShortName** element in an .osdx file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a><span data-ttu-id="582ee-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="582ee-143">Description</span></span>

<span data-ttu-id="582ee-144">Windows usa el valor del elemento **Description** para rellenar la descripción del archivo que se muestra en el panel de detalles del explorador de Windows cuando un usuario selecciona un archivo. searchconnector-ms.</span><span class="sxs-lookup"><span data-stu-id="582ee-144">Windows uses the **Description** element value to populate the file description shown in the Windows Explorer details pane when a user selects a .searchconnector-ms file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a><span data-ttu-id="582ee-145">Plantilla de dirección URL para resultados de RSS/Atom</span><span class="sxs-lookup"><span data-stu-id="582ee-145">URL Template for RSS/Atom Results</span></span>

<span data-ttu-id="582ee-146">El archivo. osdx debe incluir un elemento de **formato de dirección URL** y un atributo de **plantilla** (una plantilla de dirección URL) que devuelva resultados en formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="582ee-146">The .osdx file must include one **Url format** element and **template** attribute (a URL template) that returns results in either RSS or Atom format.</span></span> <span data-ttu-id="582ee-147">El atributo de formato debe establecerse en `application/rss+xml` para los resultados con formato RSS o en los `application/atom+xml` resultados con formato Atom, tal como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="582ee-147">The format attribute must be set to `application/rss+xml` for RSS formatted results, or `application/atom+xml` for Atom formatted results, as shown in the following code.</span></span>

> [!Note]  
> <span data-ttu-id="582ee-148">El elemento de **formato de dirección URL** y el atributo de **plantilla** se conocen normalmente como una plantilla de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="582ee-148">The **Url format** element and **template** attribute are commonly known as a URL template.</span></span>

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a><span data-ttu-id="582ee-149">Plantilla de dirección URL para resultados Web</span><span class="sxs-lookup"><span data-stu-id="582ee-149">URL Template for web Results</span></span>

<span data-ttu-id="582ee-150">Si hay una versión de los resultados de la búsqueda que se puede ver en un explorador Web, debe proporcionar un **formato de dirección URL =** `text/html` elemento y el atributo de **plantilla** , como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="582ee-150">If there is a version of the search results that can be viewed in a web browser, you should provide a **Url format=**`text/html` element, and **template** attribute, as shown in the following code.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



<span data-ttu-id="582ee-151">Si proporciona un elemento de **formato de dirección URL = "text/html"** y un atributo de **plantilla** , aparece un botón en la barra de comandos del explorador de Windows, como se muestra en la siguiente captura de pantalla, que permite al usuario abrir un explorador Web para ver los resultados de la búsqueda cuando el usuario realiza una consulta.</span><span class="sxs-lookup"><span data-stu-id="582ee-151">If you provide a **Url format="text/html"** element and **template** attribute, a button appears in the Windows Explorer command bar, as shown in the following screen shot, that enables the user to open a web browser to view the search results when the user performs a query.</span></span>

![captura de pantalla que muestra el botón deshacer la búsqueda web.](images/websearchroll-overcommandbarbutton.png)

<span data-ttu-id="582ee-153">La reversión de la consulta de nuevo a la interfaz de usuario Web del almacén de datos es importante en algunos escenarios.</span><span class="sxs-lookup"><span data-stu-id="582ee-153">The roll-over of the query back to the data store's web UI is important in some scenarios.</span></span> <span data-ttu-id="582ee-154">Por ejemplo, puede que un usuario desee ver más de 100 resultados (el número predeterminado de elementos que solicita el proveedor de OpenSearch).</span><span class="sxs-lookup"><span data-stu-id="582ee-154">For example, a user may want to view more than 100 results (the default number of items the OpenSearch provider requests).</span></span> <span data-ttu-id="582ee-155">Si es así, el usuario también puede usar características de búsqueda que solo están disponibles en el sitio web del almacén de datos, como volver a realizar consultas con un criterio de ordenación diferente o dinamizar y filtrar la consulta con los metadatos relacionados.</span><span class="sxs-lookup"><span data-stu-id="582ee-155">If so, the user may also want to use search features that are available only on the data store's website, such as re-querying with a different sort order, or pivoting and filtering the query with related metadata.</span></span>

### <a name="url-template-parameters"></a><span data-ttu-id="582ee-156">Parámetros de plantilla de URL</span><span class="sxs-lookup"><span data-stu-id="582ee-156">URL Template Parameters</span></span>

<span data-ttu-id="582ee-157">El proveedor de OpenSearch realiza siempre las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="582ee-157">The OpenSearch provider performs always the following actions:</span></span>

1.  <span data-ttu-id="582ee-158">Usa la plantilla de dirección URL para enviar la solicitud al servicio Web.</span><span class="sxs-lookup"><span data-stu-id="582ee-158">Uses the URL template to send the request to the web service.</span></span>
2.  <span data-ttu-id="582ee-159">Intenta reemplazar los tokens que se encuentran en la plantilla de dirección URL antes de enviar la solicitud al servicio Web, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="582ee-159">Attempts to replace the tokens found in the URL template before sending the request to the web service, as follows:</span></span>
    -   <span data-ttu-id="582ee-160">Reemplaza los tokens de OpenSearch estándar que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="582ee-160">Replaces the standard OpenSearch tokens that are listed in the following table.</span></span>
    -   <span data-ttu-id="582ee-161">Quita todos los tokens que no se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="582ee-161">Removes any tokens that are not listed in the following table.</span></span>



| <span data-ttu-id="582ee-162">Token compatible</span><span class="sxs-lookup"><span data-stu-id="582ee-162">Supported token</span></span>  | <span data-ttu-id="582ee-163">Cómo lo usa el proveedor de OpenSearch</span><span class="sxs-lookup"><span data-stu-id="582ee-163">How used by OpenSearch provider</span></span>                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582ee-164">{searchTerms}</span><span class="sxs-lookup"><span data-stu-id="582ee-164">{searchTerms}</span></span>    | <span data-ttu-id="582ee-165">Se reemplaza por los términos de búsqueda que el usuario escribe en el cuadro de entrada de búsqueda del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="582ee-165">Replaced with the search terms that the user types in the Windows Explorer search input box.</span></span><br/>                                         |
| <span data-ttu-id="582ee-166">Super</span><span class="sxs-lookup"><span data-stu-id="582ee-166">{startIndex}</span></span>     | <span data-ttu-id="582ee-167">Se usa al obtener resultados en "pages".</span><span class="sxs-lookup"><span data-stu-id="582ee-167">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="582ee-168">Se reemplaza por el índice del primer elemento de resultado que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="582ee-168">Replaced with the index for the first result item to return.</span></span><br/>                        |
| <span data-ttu-id="582ee-169">StartPage</span><span class="sxs-lookup"><span data-stu-id="582ee-169">{startPage}</span></span>      | <span data-ttu-id="582ee-170">Se usa al obtener resultados en "pages".</span><span class="sxs-lookup"><span data-stu-id="582ee-170">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="582ee-171">Se reemplaza por el número de página del conjunto de resultados de búsqueda que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="582ee-171">Replaced with the page number of the set of search results to return.</span></span><br/>               |
| <span data-ttu-id="582ee-172">contabiliza</span><span class="sxs-lookup"><span data-stu-id="582ee-172">{count}</span></span>          | <span data-ttu-id="582ee-173">Se usa al obtener resultados en "pages".</span><span class="sxs-lookup"><span data-stu-id="582ee-173">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="582ee-174">Se reemplaza por el número de resultados de búsqueda por página que solicita el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="582ee-174">Replaced with the number of search results per page that Windows Explorer requests.</span></span><br/> |
| <span data-ttu-id="582ee-175">módulo</span><span class="sxs-lookup"><span data-stu-id="582ee-175">{language}</span></span>       | <span data-ttu-id="582ee-176">Se reemplaza por una cadena que indica el idioma de la consulta que se está enviando.</span><span class="sxs-lookup"><span data-stu-id="582ee-176">Replaced with a string that indicates the language of the query being sent.</span></span><br/>                                                          |
| <span data-ttu-id="582ee-177">{inputEncoding}</span><span class="sxs-lookup"><span data-stu-id="582ee-177">{inputEncoding}</span></span>  | <span data-ttu-id="582ee-178">Se reemplaza por una cadena (por ejemplo, "UTF-16") que indica la codificación de caracteres de la consulta que se está enviando.</span><span class="sxs-lookup"><span data-stu-id="582ee-178">Replaced with a string (such "UTF-16") that indicates the character encoding of the query being sent.</span></span><br/>                                |
| <span data-ttu-id="582ee-179">OutputEncoding</span><span class="sxs-lookup"><span data-stu-id="582ee-179">{outputEncoding}</span></span> | <span data-ttu-id="582ee-180">Se reemplaza por una cadena (como "UTF-16") que indica la codificación de caracteres deseada para la respuesta del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="582ee-180">Replaced with a string (such as "UTF-16") that indicates the desired character encoding for the response from the web service.</span></span><br/>       |



 

### <a name="paged-results"></a><span data-ttu-id="582ee-181">Resultados paginados</span><span class="sxs-lookup"><span data-stu-id="582ee-181">Paged Results</span></span>

<span data-ttu-id="582ee-182">Es posible que desee limitar el número de resultados que se devuelven por solicitud.</span><span class="sxs-lookup"><span data-stu-id="582ee-182">You may want to limit the number of results returned per request.</span></span> <span data-ttu-id="582ee-183">Puede optar por devolver una "página" de los resultados a la vez, o bien para que el proveedor de OpenSearch obtenga páginas de resultados adicionales por número de elemento o número de página.</span><span class="sxs-lookup"><span data-stu-id="582ee-183">You can opt to return a "page" of results at a time, or to have the OpenSearch provider get additional pages of results either by item number or page number.</span></span> <span data-ttu-id="582ee-184">Por ejemplo, si envía veinte resultados por página, la primera página que envíe comienza en el índice de elemento 1 y en la Página 1; la segunda página que envía comienza en el índice de elementos 21 y en la página 2.</span><span class="sxs-lookup"><span data-stu-id="582ee-184">For example, if you send twenty results per page, the first page you send starts at item index 1 and at page 1; the second page you send starts at item index 21 and at page 2.</span></span> <span data-ttu-id="582ee-185">Puede definir cómo desea que el proveedor de OpenSearch solicite elementos mediante el `{startItem}` `{startPage}` token o en la plantilla de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="582ee-185">You can define how you want the OpenSearch provider to request items by using either the `{startItem}` or the `{startPage}` token in the URL template.</span></span>

### <a name="paging-using-the-item-index"></a><span data-ttu-id="582ee-186">Paginación mediante el índice del elemento</span><span class="sxs-lookup"><span data-stu-id="582ee-186">Paging Using the Item Index</span></span>

<span data-ttu-id="582ee-187">Un índice de elemento identifica el primer elemento de resultado de una página de resultados.</span><span class="sxs-lookup"><span data-stu-id="582ee-187">An item index identifies the first result item in a page of results.</span></span> <span data-ttu-id="582ee-188">Si desea que los clientes envíen solicitudes mediante un índice de elemento, puede usar el `{startIndex}` token en el atributo de **plantilla** de elemento **URL** , tal como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="582ee-188">If you want clients to send requests using an item index, you can use the `{startIndex}` token in your **Url** element **template** attribute, as shown in the following code.</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



<span data-ttu-id="582ee-189">A continuación, el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) reemplaza el token en la dirección URL con un valor de índice de inicio.</span><span class="sxs-lookup"><span data-stu-id="582ee-189">The [OpenSearch](https://github.com/dewitt/opensearch) provider then replaces the token in the URL with a starting index value.</span></span> <span data-ttu-id="582ee-190">La primera solicitud comienza con el primer elemento, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="582ee-190">The first request starts with the first item, as illustrated in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1
```



<span data-ttu-id="582ee-191">El proveedor de OpenSearch puede obtener elementos adicionales cambiando el `{startIndex}` valor del parámetro y emitiendo una nueva solicitud.</span><span class="sxs-lookup"><span data-stu-id="582ee-191">The OpenSearch provider can get additional items by changing the `{startIndex}` parameter value and issuing a new request.</span></span> <span data-ttu-id="582ee-192">El proveedor repite este proceso hasta que obtiene suficientes resultados para satisfacer su límite o alcanza el final de los resultados.</span><span class="sxs-lookup"><span data-stu-id="582ee-192">The provider repeats this process until it gets enough results to satisfy its limit, or reaches the end of the results.</span></span> <span data-ttu-id="582ee-193">El proveedor de OpenSearch examina el número de elementos devueltos por el servicio Web en la primera página de resultados y establece el tamaño de página esperado en ese número.</span><span class="sxs-lookup"><span data-stu-id="582ee-193">The OpenSearch provider looks at the number of items returned by the web service in the first page of results, and sets the expected page size to that number.</span></span> <span data-ttu-id="582ee-194">Utiliza ese número para incrementar el `{startIndex}` valor de las solicitudes posteriores.</span><span class="sxs-lookup"><span data-stu-id="582ee-194">It uses that number to increment the `{startIndex}` value for subsequent requests.</span></span> <span data-ttu-id="582ee-195">Por ejemplo, si el servicio Web devuelve 20 resultados en la primera solicitud, el proveedor establece el tamaño de página esperado en 20.</span><span class="sxs-lookup"><span data-stu-id="582ee-195">For example, if the web service returns 20 results in the first request, then the provider sets the expected page size to 20.</span></span> <span data-ttu-id="582ee-196">Para la solicitud siguiente, el proveedor reemplaza `{startIndex}` por el valor de 21 para obtener los 20 elementos siguientes.</span><span class="sxs-lookup"><span data-stu-id="582ee-196">For the next request, the provider replaces `{startIndex}` with the value of 21 to get the next 20 items.</span></span>

> [!Note]  
> <span data-ttu-id="582ee-197">Si una página de resultados devuelta por el servicio Web tiene menos elementos que el tamaño de página esperado, el proveedor de OpenSearch supone que ha recibido la última página de resultados y detiene las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="582ee-197">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="paging-using-the-page-index"></a><span data-ttu-id="582ee-198">Paginación mediante el índice de página</span><span class="sxs-lookup"><span data-stu-id="582ee-198">Paging Using the Page Index</span></span>

<span data-ttu-id="582ee-199">Un índice de página identifica la página de resultados especificada.</span><span class="sxs-lookup"><span data-stu-id="582ee-199">A page index identifies the specified page of results.</span></span> <span data-ttu-id="582ee-200">Si desea que los clientes envíen solicitudes mediante un número de página, puede usar el `{startPage}` token en el atributo de **plantilla** de elemento de **formato de dirección URL** para indicar que, tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="582ee-200">If you want clients to send requests using a page number, you can use the `{startPage}` token in your **Url format** element **template** attribute to indicate that, as illustrated in the following example:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



<span data-ttu-id="582ee-201">A continuación, el proveedor de OpenSearch reemplaza el token en la dirección URL con un parámetro de número de página.</span><span class="sxs-lookup"><span data-stu-id="582ee-201">The OpenSearch provider then replaces the token in the URL with a page number parameter.</span></span> <span data-ttu-id="582ee-202">La primera solicitud comienza con la primera página, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="582ee-202">The first request starts with the first page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> <span data-ttu-id="582ee-203">Si una página de resultados devuelta por el servicio Web tiene menos elementos que el tamaño de página esperado, el proveedor de OpenSearch supone que ha recibido la última página de resultados y detiene las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="582ee-203">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="page-size"></a><span data-ttu-id="582ee-204">Tamaño de página</span><span class="sxs-lookup"><span data-stu-id="582ee-204">Page Size</span></span>

<span data-ttu-id="582ee-205">Es posible que desee configurar el servicio web para permitir que una solicitud especifique el tamaño de las páginas mediante el uso de algún parámetro en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="582ee-205">You may want to configure your web service to permit a request to specify the size of the pages by using some parameter in the URL.</span></span> <span data-ttu-id="582ee-206">Se debe especificar una solicitud en el archivo. osdx mediante el `{count}` token, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="582ee-206">A request must be specified in the .osdx file by using the `{count}` token, as follows:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



<span data-ttu-id="582ee-207">Después, el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) puede establecer el tamaño de página deseado, en número de resultados por página, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="582ee-207">The [OpenSearch](https://github.com/dewitt/opensearch) provider can then set the desired page size, in number of results per page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



<span data-ttu-id="582ee-208">De forma predeterminada, el proveedor de OpenSearch realiza solicitudes con un tamaño de página de 50.</span><span class="sxs-lookup"><span data-stu-id="582ee-208">By default the OpenSearch provider makes requests using a page size of 50.</span></span> <span data-ttu-id="582ee-209">Si desea un tamaño de página diferente, no proporcione un `{count}` token y, en su lugar, coloque el número deseado directamente en el elemento de **plantilla de dirección URL** .</span><span class="sxs-lookup"><span data-stu-id="582ee-209">If you want a different page size, then do not provide a `{count}` token, and instead place the desired number directly in the **Url template** element.</span></span>

<span data-ttu-id="582ee-210">El proveedor de OpenSearch determina el tamaño de página en función del número de resultados que se devuelven en la primera solicitud.</span><span class="sxs-lookup"><span data-stu-id="582ee-210">The OpenSearch provider determines the page size based on the number of results returned on the first request.</span></span> <span data-ttu-id="582ee-211">Si la primera página de resultados recibida tiene menos elementos que el número solicitado, el proveedor restablece el tamaño de página para las solicitudes de página posteriores.</span><span class="sxs-lookup"><span data-stu-id="582ee-211">If the first page of results received has fewer items than the count requested, the provider resets the page size for any subsequent page requests.</span></span> <span data-ttu-id="582ee-212">Si las solicitudes de página posteriores devuelven menos elementos de los solicitados, el proveedor de OpenSearch supone que ha alcanzado el final de los resultados.</span><span class="sxs-lookup"><span data-stu-id="582ee-212">If subsequent page requests return fewer items than requested, the OpenSearch provider assumes that it has reached the end of the results.</span></span>

## <a name="extended-elements-in-windows-federated-search"></a><span data-ttu-id="582ee-213">Elementos extendidos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="582ee-213">Extended Elements in Windows Federated Search</span></span>

<span data-ttu-id="582ee-214">Además de los elementos estándar, la búsqueda federada admite los siguientes elementos extendidos: **MaximumResultCount** y **ResultsProcessing**.</span><span class="sxs-lookup"><span data-stu-id="582ee-214">In addition to the standard elements, federated search supports the following extended elements: **MaximumResultCount** and **ResultsProcessing**.</span></span>

<span data-ttu-id="582ee-215">Dado que estos elementos secundarios extendidos no se admiten en la especificación de [OpenSearch](https://github.com/dewitt/opensearch) v 1.1, deben agregarse mediante el siguiente espacio de nombres:</span><span class="sxs-lookup"><span data-stu-id="582ee-215">Because these extended child elements are not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification, they must be added by using the following namespace:</span></span>


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a><span data-ttu-id="582ee-216">Número máximo de resultados</span><span class="sxs-lookup"><span data-stu-id="582ee-216">Maximum Result Count</span></span>

<span data-ttu-id="582ee-217">De forma predeterminada, los conectores de búsqueda se limitan a 100 resultados por consulta de usuario.</span><span class="sxs-lookup"><span data-stu-id="582ee-217">By default, search connectors are limited to 100 results per user query.</span></span> <span data-ttu-id="582ee-218">Este límite se puede personalizar incluyendo el elemento **MaximumResultCount** en el archivo OSD, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="582ee-218">This limit can be customized by including the **MaximumResultCount** element within the OSD file as shown in the following example:</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



<span data-ttu-id="582ee-219">En el ejemplo anterior se declara el prefijo `ms-ose` de espacio de nombres en el elemento **OpenSearchDescription** de nivel superior y, a continuación, se usa como prefijo en el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="582ee-219">The preceding example declares the namespace prefix `ms-ose` in the top-level **OpenSearchDescription** element, and then uses it as a prefix in the element name.</span></span> <span data-ttu-id="582ee-220">Esta declaración es necesaria porque no se admite **MaximumResultCount** en la especificación de [OpenSearch](https://github.com/dewitt/opensearch) v 1.1.</span><span class="sxs-lookup"><span data-stu-id="582ee-220">This declaration is required because the **MaximumResultCount** is not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification.</span></span>

### <a name="property-mapping"></a><span data-ttu-id="582ee-221">Asignación de propiedades</span><span class="sxs-lookup"><span data-stu-id="582ee-221">Property Mapping</span></span>

<span data-ttu-id="582ee-222">Cuando el servicio Web devuelve los resultados como una fuente RSS o Atom, el proveedor de OpenSearch debe asignar los metadatos de los elementos de las fuentes a las propiedades que el shell de Windows puede usar.</span><span class="sxs-lookup"><span data-stu-id="582ee-222">When results are returned by the web service as an RSS or Atom feed, the OpenSearch provider must map the item metadata in the feeds to properties that the Windows Shell can use.</span></span> <span data-ttu-id="582ee-223">En la captura de pantalla siguiente se muestra cómo el proveedor de OpenSearch asigna algunos de los elementos RSS predeterminados.</span><span class="sxs-lookup"><span data-stu-id="582ee-223">The following screen shot illustrates how the OpenSearch provider maps some of the default RSS elements.</span></span>

![captura de pantalla que muestra las asignaciones de propiedades integradas de RSS a Windows-Shell](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a><span data-ttu-id="582ee-225">Asignaciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="582ee-225">Default Mappings</span></span>

<span data-ttu-id="582ee-226">En la tabla siguiente se enumeran las asignaciones predeterminadas de elementos XML de RSS a las propiedades del sistema de Shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="582ee-226">The default mappings of RSS XML elements to Windows Shell system properties, are listed in the following table.</span></span> <span data-ttu-id="582ee-227">Las rutas XML son relativas al elemento Item.</span><span class="sxs-lookup"><span data-stu-id="582ee-227">XML paths are relative to the item element.</span></span> <span data-ttu-id="582ee-228">El `"media:"` prefijo está definido por el espacio de nombres del [espacio de nombres de búsqueda de Yahoo](https://www.rssboard.org/media-rss) .</span><span class="sxs-lookup"><span data-stu-id="582ee-228">The `"media:"` prefix is defined by the [Yahoo Search Namespace](https://www.rssboard.org/media-rss) namespace.</span></span>



| <span data-ttu-id="582ee-229">Ruta de acceso XML de RSS</span><span class="sxs-lookup"><span data-stu-id="582ee-229">RSS XML path</span></span>                  | <span data-ttu-id="582ee-230">Propiedad del shell de Windows (nombre canónico)</span><span class="sxs-lookup"><span data-stu-id="582ee-230">Windows Shell property (canonical name)</span></span> |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="582ee-231">Link</span><span class="sxs-lookup"><span data-stu-id="582ee-231">Link</span></span>                          | <span data-ttu-id="582ee-232">System. ItemUrl</span><span class="sxs-lookup"><span data-stu-id="582ee-232">System.ItemUrl</span></span>                          |
| <span data-ttu-id="582ee-233">Title</span><span class="sxs-lookup"><span data-stu-id="582ee-233">Title</span></span>                         | <span data-ttu-id="582ee-234">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="582ee-234">System.ItemName</span></span>                         |
| <span data-ttu-id="582ee-235">Autor</span><span class="sxs-lookup"><span data-stu-id="582ee-235">Author</span></span>                        | <span data-ttu-id="582ee-236">System.Author</span><span class="sxs-lookup"><span data-stu-id="582ee-236">System.Author</span></span>                           |
| <span data-ttu-id="582ee-237">pubDate</span><span class="sxs-lookup"><span data-stu-id="582ee-237">pubDate</span></span>                       | <span data-ttu-id="582ee-238">System. DateModified</span><span class="sxs-lookup"><span data-stu-id="582ee-238">System.DateModified</span></span>                     |
| <span data-ttu-id="582ee-239">Descripción</span><span class="sxs-lookup"><span data-stu-id="582ee-239">Description</span></span>                   | <span data-ttu-id="582ee-240">System. autosummary</span><span class="sxs-lookup"><span data-stu-id="582ee-240">System.AutoSummary</span></span>                      |
| <span data-ttu-id="582ee-241">Category</span><span class="sxs-lookup"><span data-stu-id="582ee-241">Category</span></span>                      | <span data-ttu-id="582ee-242">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="582ee-242">System.Keywords</span></span>                         |
| enclosure/@type               | <span data-ttu-id="582ee-243">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="582ee-243">System.MIMEType</span></span>                         |
| enclosure/@length             | <span data-ttu-id="582ee-244">System. Size</span><span class="sxs-lookup"><span data-stu-id="582ee-244">System.Size</span></span>                             |
| enclosure/@url                | <span data-ttu-id="582ee-245">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="582ee-245">System.ContentUrl</span></span>                       |
| <span data-ttu-id="582ee-246">medio: categoría</span><span class="sxs-lookup"><span data-stu-id="582ee-246">media:category</span></span>                | <span data-ttu-id="582ee-247">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="582ee-247">System.Keywords</span></span>                         |
| media:content/@fileSize       | <span data-ttu-id="582ee-248">System. Size</span><span class="sxs-lookup"><span data-stu-id="582ee-248">System.Size</span></span>                             |
| media:content/@type           | <span data-ttu-id="582ee-249">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="582ee-249">System.MIMEType</span></span>                         |
| media:content/@url            | <span data-ttu-id="582ee-250">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="582ee-250">System.ContentUrl</span></span>                       |
| media:group/content/@fileSize | <span data-ttu-id="582ee-251">System. Size</span><span class="sxs-lookup"><span data-stu-id="582ee-251">System.Size</span></span>                             |
| media:group/content/@type     | <span data-ttu-id="582ee-252">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="582ee-252">System.MIMEType</span></span>                         |
| media:group/content/@url      | <span data-ttu-id="582ee-253">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="582ee-253">System.ContentUrl</span></span>                       |
| media:thumbnail/@url          | <span data-ttu-id="582ee-254">System. ItemThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="582ee-254">System.ItemThumbnailUrl</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="582ee-255">Además de las asignaciones predeterminadas de elementos RSS o Atom estándar, puede asignar otras propiedades del sistema de Shell de Windows incluyendo elementos XML adicionales en el espacio de nombres de Windows para cada una de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="582ee-255">In addition to the default mappings of standard RSS or Atom elements, you can map other Windows Shell system properties by including additional XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="582ee-256">También puede asignar elementos de otros espacios de nombres XML existentes, como MediaRSS, iTunes, etc., agregando la asignación de propiedades personalizadas en el archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="582ee-256">You can also map elements from other existing XML namespaces such as MediaRSS, iTunes, and so forth, by adding custom property mapping in the .osdx file.</span></span>

 

### <a name="custom-property-mappings"></a><span data-ttu-id="582ee-257">Asignaciones de propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="582ee-257">Custom Property Mappings</span></span>

<span data-ttu-id="582ee-258">Puede personalizar la asignación de elementos de la salida RSS a las propiedades del sistema del shell de Windows especificando la asignación en el archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="582ee-258">You can customize the mapping of elements from your RSS output to Windows Shell system properties by specifying the mapping in the .osdx file.</span></span>

<span data-ttu-id="582ee-259">La salida RSS especifica:</span><span class="sxs-lookup"><span data-stu-id="582ee-259">The RSS output specifies:</span></span>

-   <span data-ttu-id="582ee-260">Un espacio de nombres XML y</span><span class="sxs-lookup"><span data-stu-id="582ee-260">An XML namespace, and</span></span>
-   <span data-ttu-id="582ee-261">Para cualquier elemento secundario de un elemento, un nombre de elemento que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="582ee-261">For any child element of an item, an element name to map against.</span></span>

<span data-ttu-id="582ee-262">El archivo. osdx identifica una propiedad del shell de Windows para cada nombre de elemento de un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="582ee-262">The .osdx file identifies a Windows Shell property for each element name in a namespace.</span></span> <span data-ttu-id="582ee-263">Las asignaciones de propiedad que se definen en el archivo. osdx invalidan las asignaciones predeterminadas, si existen, para las propiedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="582ee-263">The property mappings that you define in your .osdx file override the default mappings, if they exist, for those specified properties.</span></span>

<span data-ttu-id="582ee-264">En el diagrama siguiente se muestra cómo se asigna una extensión RSS a las propiedades de Windows (nombre canónico).</span><span class="sxs-lookup"><span data-stu-id="582ee-264">The following diagram illustrates how an RSS extension maps to Windows properties (canonical name).</span></span>

![diagrama que muestra que la combinación del espacio de nombres XML y la ruta XML genera el nombre canónico](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a><span data-ttu-id="582ee-266">Resultados de RSS de ejemplo y asignación de propiedades OSD</span><span class="sxs-lookup"><span data-stu-id="582ee-266">Example RSS results and OSD Property Mapping</span></span>

<span data-ttu-id="582ee-267">La salida RSS de ejemplo siguiente identifica `https://example.com/schema/2009` como el espacio de nombres XML con el prefijo "example".</span><span class="sxs-lookup"><span data-stu-id="582ee-267">The following example RSS output identifies `https://example.com/schema/2009` as the XML namespace with the prefix "example".</span></span> <span data-ttu-id="582ee-268">Este prefijo debe aparecer de nuevo antes del elemento de **correo electrónico** .</span><span class="sxs-lookup"><span data-stu-id="582ee-268">This prefix must appear again before the **email** element.</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



<span data-ttu-id="582ee-269">En el siguiente archivo. osdx de ejemplo, el elemento de **correo electrónico** XML se asigna a la propiedad [System. contact. EmailAddress](../properties/props-system-contact-emailaddress.md)del shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="582ee-269">In the following example .osdx file, the XML **email** element maps to the Windows Shell property [System.Contact.EmailAddress](../properties/props-system-contact-emailaddress.md).</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



<span data-ttu-id="582ee-270">Hay algunas propiedades que no se pueden asignar porque los valores para ellas se invalidan posteriormente o no se pueden editar.</span><span class="sxs-lookup"><span data-stu-id="582ee-270">There are some properties that cannot be mapped because values for them are either overridden later or are not editable.</span></span> <span data-ttu-id="582ee-271">Por ejemplo, [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) o [System. ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) no se puede asignar porque se calculan a partir del valor de dirección URL proporcionado en los elementos del vínculo o del contenedor.</span><span class="sxs-lookup"><span data-stu-id="582ee-271">For example, [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) or [System.ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) cannot be mapped because they are calculated from the URL value provided in either the link or enclosure elements.</span></span>

### <a name="thumbnails"></a><span data-ttu-id="582ee-272">Miniaturas</span><span class="sxs-lookup"><span data-stu-id="582ee-272">Thumbnails</span></span>

<span data-ttu-id="582ee-273">Se pueden proporcionar direcciones URL de imagen en miniatura para cualquier elemento mediante el elemento **media: thumbnail URL = ""** .</span><span class="sxs-lookup"><span data-stu-id="582ee-273">Thumbnail image URLs can be provided for any item by using the **media:thumbnail url=""** element.</span></span> <span data-ttu-id="582ee-274">La solución ideal es de 150 x 150 píxeles.</span><span class="sxs-lookup"><span data-stu-id="582ee-274">The ideal resolution is 150 x 150 pixels.</span></span> <span data-ttu-id="582ee-275">Las miniaturas más grandes admitidas son 256 x 256 píxeles.</span><span class="sxs-lookup"><span data-stu-id="582ee-275">The largest thumbnails supported are 256 x 256 pixels.</span></span> <span data-ttu-id="582ee-276">Proporcionar imágenes más grandes requiere más ancho de banda para que no haya más ventajas para el usuario.</span><span class="sxs-lookup"><span data-stu-id="582ee-276">Providing larger images takes more bandwidth for no extra benefit to the user.</span></span>

### <a name="open-file-location-context-menu"></a><span data-ttu-id="582ee-277">Abrir el menú contextual de ubicación del archivo</span><span class="sxs-lookup"><span data-stu-id="582ee-277">Open File Location Context Menu</span></span>

<span data-ttu-id="582ee-278">Windows proporciona un menú contextual denominado **Abrir archivo ubicación** para los elementos de resultados.</span><span class="sxs-lookup"><span data-stu-id="582ee-278">Windows provides a shortcut menu named **Open file location** for result items.</span></span> <span data-ttu-id="582ee-279">Si el usuario selecciona un elemento de ese menú, se abre la dirección URL "principal" del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="582ee-279">If the user selects an item from that menu, the "parent" URL for the selected item is opened.</span></span> <span data-ttu-id="582ee-280">Si la dirección URL es una dirección URL Web, como `https://...` , el explorador Web se abre y se navega a esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="582ee-280">If the URL is a web URL, such as `https://...`, the web browser is opened and navigated to that URL.</span></span> <span data-ttu-id="582ee-281">La fuente debe proporcionar una dirección URL personalizada para cada elemento con el fin de asegurarse de que Windows abre una dirección URL válida.</span><span class="sxs-lookup"><span data-stu-id="582ee-281">Your feed should provide a custom URL for each item to ensure that Windows opens a valid URL.</span></span> <span data-ttu-id="582ee-282">Esto puede realizarse incluyendo la dirección URL dentro de un elemento dentro del XML del elemento, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="582ee-282">This can be accomplished by including the URL within an element inside the item's XML, as illustrated in the following example:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



<span data-ttu-id="582ee-283">Si esta propiedad no se establece explícitamente en el XML del elemento, el proveedor de OpenSearch lo establece en la carpeta primaria de la dirección URL del elemento.</span><span class="sxs-lookup"><span data-stu-id="582ee-283">If this property is not explicitly set in the item's XML, the OpenSearch provider sets it to the parent folder of the URL of the item.</span></span> <span data-ttu-id="582ee-284">En el ejemplo anterior, el proveedor de OpenSearch usaría el valor del vínculo y establecería el valor de la propiedad del shell de Windows [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) en `"https://example.com/"` .</span><span class="sxs-lookup"><span data-stu-id="582ee-284">In the example above, the OpenSearch provider would use the link value, and set the [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell property value to `"https://example.com/"`.</span></span>

### <a name="customize-windows-explorer-views-with-property-description-lists"></a><span data-ttu-id="582ee-285">Personalizar las vistas del explorador de Windows con las listas de descripción de propiedades</span><span class="sxs-lookup"><span data-stu-id="582ee-285">Customize Windows Explorer Views with Property Description Lists</span></span>

<span data-ttu-id="582ee-286">Algunos diseños de la vista del explorador de Windows se definen mediante listas de descripción de propiedades o provisores.</span><span class="sxs-lookup"><span data-stu-id="582ee-286">Some Windows Explorer view layouts are defined by property description lists, or proplists.</span></span> <span data-ttu-id="582ee-287">Un proplist es una lista delimitada por punto y coma de propiedades, como `"prop:System.ItemName; System.Author"` , que se usa para controlar el modo en que los resultados aparecen en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="582ee-287">A proplist is a semicolon-delimited list of properties, such as `"prop:System.ItemName; System.Author"`, that is used to control how your results appear in Windows Explorer.</span></span>

<span data-ttu-id="582ee-288">Las áreas de la interfaz de usuario del explorador de Windows que se pueden personalizar mediante el uso de proplists se muestran en la siguiente captura de pantalla:</span><span class="sxs-lookup"><span data-stu-id="582ee-288">The UI areas of Windows Explorer that can be customized by using proplists are illustrated in the following screen shot:</span></span>

![captura de pantalla que muestra las áreas de la interfaz de usuario del explorador de Windows que se pueden personalizar mediante el uso de proplists](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

<span data-ttu-id="582ee-290">Cada área del explorador de Windows tiene un conjunto asociado de proarchivos, que a su vez se especifican como propiedades.</span><span class="sxs-lookup"><span data-stu-id="582ee-290">Each area of Windows Explorer has an associated set of proplists, which themselves are specified as properties.</span></span> <span data-ttu-id="582ee-291">Puede especificar los valores predeterminados para los elementos individuales de los conjuntos de resultados o para todos los elementos de un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="582ee-291">You can specify custom proplists for individual items in your result sets or for all items in a set of results.</span></span>



| <span data-ttu-id="582ee-292">Área de la interfaz de usuario para personalizar</span><span class="sxs-lookup"><span data-stu-id="582ee-292">UI Area to customize</span></span>               | <span data-ttu-id="582ee-293">Propiedad del shell de Windows que implementa la personalización</span><span class="sxs-lookup"><span data-stu-id="582ee-293">Windows Shell property that implements the customization</span></span> |
|------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="582ee-294">Modo de vista de contenido (al buscar)</span><span class="sxs-lookup"><span data-stu-id="582ee-294">Content view mode (when searching)</span></span> | <span data-ttu-id="582ee-295">System. proplist. ContentViewModeForSearch</span><span class="sxs-lookup"><span data-stu-id="582ee-295">System.PropList.ContentViewModeForSearch</span></span>                 |
| <span data-ttu-id="582ee-296">Modo de vista de contenido (al examinar)</span><span class="sxs-lookup"><span data-stu-id="582ee-296">Content view mode (when browsing)</span></span>  | <span data-ttu-id="582ee-297">System. proplist. ContentViewModeForBrowse</span><span class="sxs-lookup"><span data-stu-id="582ee-297">System.PropList.ContentViewModeForBrowse</span></span>                 |
| <span data-ttu-id="582ee-298">Modo de vista en mosaico</span><span class="sxs-lookup"><span data-stu-id="582ee-298">Tile view mode</span></span>                     | <span data-ttu-id="582ee-299">System. proplist. TileInfo</span><span class="sxs-lookup"><span data-stu-id="582ee-299">System.PropList.TileInfo</span></span>                                 |
| <span data-ttu-id="582ee-300">Panel de detalles</span><span class="sxs-lookup"><span data-stu-id="582ee-300">Details pane</span></span>                       | <span data-ttu-id="582ee-301">System. proplist. PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="582ee-301">System.PropList.PreviewDetails</span></span>                           |
| <span data-ttu-id="582ee-302">Recuadro informativo (información sobre herramientas de desplazamiento del elemento)</span><span class="sxs-lookup"><span data-stu-id="582ee-302">Infotip (item's hover tooltip)</span></span>     | <span data-ttu-id="582ee-303">System. proplist. recuadro informativo</span><span class="sxs-lookup"><span data-stu-id="582ee-303">System.PropList.Infotip</span></span>                                  |



 

 

<span data-ttu-id="582ee-304">**Para especificar un único proplist para un elemento individual:**</span><span class="sxs-lookup"><span data-stu-id="582ee-304">**To specify a unique proplist for an individual item:**</span></span>

1.  <span data-ttu-id="582ee-305">En la salida RSS, agregue un elemento personalizado que represente el proplist que desea personalizar.</span><span class="sxs-lookup"><span data-stu-id="582ee-305">In your RSS output, add a custom element representing the proplist you want to customize.</span></span> <span data-ttu-id="582ee-306">Por ejemplo, en el ejemplo siguiente se establece la lista del panel de detalles:</span><span class="sxs-lookup"><span data-stu-id="582ee-306">For example, the following example sets the list for the details pane:</span></span>
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  <span data-ttu-id="582ee-307">Para aplicar una propiedad a todos los elementos de los resultados de la búsqueda sin modificar la salida RSS, especifique un proplist dentro de un elemento **MS-OSE: PropertyDefaultValues** en el archivo. osdx, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="582ee-307">To apply a property to every item in the search results without modifying the RSS output, specify a proplist within an **ms-ose:PropertyDefaultValues** element in the .osdx file, as shown in the following example:</span></span>

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a><span data-ttu-id="582ee-308">Diseño de las propiedades del modo de vista de contenido</span><span class="sxs-lookup"><span data-stu-id="582ee-308">Content View Mode Layout of Properties</span></span>

<span data-ttu-id="582ee-309">La lista de propiedades especificadas en los proarchivos **System. proplist. ContentViewModeForSearch** y **System. proplist. ContentViewModeForBrowse** determina lo que se muestra en el modo de vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="582ee-309">The list of properties specified in the **System.PropList.ContentViewModeForSearch** and **System.PropList.ContentViewModeForBrowse** proplists determines what is shown in Content view mode.</span></span> <span data-ttu-id="582ee-310">Para obtener más información sobre las listas de propiedades, consulte [proplist](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span><span class="sxs-lookup"><span data-stu-id="582ee-310">For more information about property lists, see [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span></span>

<span data-ttu-id="582ee-311">Las propiedades se disponen de acuerdo con los números que se muestran en el patrón de diseño siguiente:</span><span class="sxs-lookup"><span data-stu-id="582ee-311">The properties are laid out according to the numbers shown in the following layout pattern:</span></span>

![captura de pantalla que muestra el patrón de diseño predeterminado en la vista de contenido](images/propertiesnumberslayoutpattern.png)

<span data-ttu-id="582ee-313">Si usamos la siguiente lista de propiedades,</span><span class="sxs-lookup"><span data-stu-id="582ee-313">If we use the following list of properties,</span></span>


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



<span data-ttu-id="582ee-314">A continuación, vemos la siguiente pantalla:</span><span class="sxs-lookup"><span data-stu-id="582ee-314">Then we see the following display:</span></span>

![captura de pantalla que muestra el diseño de la propiedad de ejemplo.](images/samplepropertylayout.png)

> [!Note]  
> <span data-ttu-id="582ee-316">Para mejorar la legibilidad, se deben etiquetar las propiedades que se muestran en la columna situada más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="582ee-316">For the best readability, the properties shown in the right-most column should be labeled.</span></span>

 

### <a name="property-list-flags"></a><span data-ttu-id="582ee-317">Marcas de la lista de propiedades</span><span class="sxs-lookup"><span data-stu-id="582ee-317">Property List Flags</span></span>

<span data-ttu-id="582ee-318">Solo una de las marcas definidas en la documentación de proplist se aplica a la presentación de los elementos en los diseños del modo de vista de contenido: ` "~"` .</span><span class="sxs-lookup"><span data-stu-id="582ee-318">Only one of the flags defined in the proplists documentation applies to the display of items in Content View mode layouts:` "~"`.</span></span> <span data-ttu-id="582ee-319">En los ejemplos anteriores, la vista del explorador de Windows etiqueta algunas de las propiedades, como `Tags: animals; zoo; lion` .</span><span class="sxs-lookup"><span data-stu-id="582ee-319">In the previous examples, the Windows Explorer view labels some of the properties, such as `Tags: animals; zoo; lion`.</span></span> <span data-ttu-id="582ee-320">Es el comportamiento predeterminado cuando se especifica una propiedad en la lista.</span><span class="sxs-lookup"><span data-stu-id="582ee-320">That is the default behavior when you specify a property in the list.</span></span> <span data-ttu-id="582ee-321">Por ejemplo, el proplist tiene `"System.Author"` que se muestra como `"Authors: value"` .</span><span class="sxs-lookup"><span data-stu-id="582ee-321">For example, the proplist has `"System.Author"` which is displayed as `"Authors: value"`.</span></span> <span data-ttu-id="582ee-322">Si desea ocultar la etiqueta de la propiedad, coloque `"~"` delante del nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="582ee-322">When you want to hide the property label, place a `"~"` in front of the property name.</span></span> <span data-ttu-id="582ee-323">Por ejemplo, si el proplist tiene `"~System.Size"` , la propiedad se muestra como solo un valor, sin la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="582ee-323">For example, if the proplist has `"~System.Size"`, the property is displayed as just a value, without the label.</span></span>

## <a name="previews"></a><span data-ttu-id="582ee-324">Vistas previas</span><span class="sxs-lookup"><span data-stu-id="582ee-324">Previews</span></span>

<span data-ttu-id="582ee-325">Cuando el usuario selecciona un elemento de resultados en el explorador de Windows y el panel de vista previa está abierto, se obtiene una vista previa del contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="582ee-325">When the user selects a result item in Windows Explorer and the preview pane is open, the content of the item is previewed.</span></span>

<span data-ttu-id="582ee-326">El contenido que se muestra en la vista previa se especifica mediante una dirección URL, que se determina de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="582ee-326">The content to show in the preview is specified by a URL, that is determined as follows:</span></span>

1.  <span data-ttu-id="582ee-327">Si se establece la propiedad del shell de Windows **System. WebPreviewUrl** para el elemento, use esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="582ee-327">If the **System.WebPreviewUrl** Windows Shell property is set for the item, then use that URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="582ee-328">La propiedad debe proporcionarse en el RSS con el espacio de nombres del shell de Windows o asignarse explícitamente en el archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="582ee-328">The property needs to be provided in the RSS by using the Windows Shell namespace, or explicitly mapped in the .osdx file.</span></span>

     

2.  <span data-ttu-id="582ee-329">En caso contrario, utilice la dirección URL del vínculo en su lugar.</span><span class="sxs-lookup"><span data-stu-id="582ee-329">If not, then use the link URL instead.</span></span>

<span data-ttu-id="582ee-330">En el diagrama de flujo siguiente se muestra esta lógica.</span><span class="sxs-lookup"><span data-stu-id="582ee-330">The following flowchart shows this logic.</span></span>

![diagrama de flujo que muestra cómo el explorador de Windows selecciona la dirección URL que se usará para las versiones de vista previa](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

<span data-ttu-id="582ee-332">Es posible usar una dirección URL diferente para la versión preliminar que para el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="582ee-332">It is possible to use a different URL for the preview than for the item itself.</span></span> <span data-ttu-id="582ee-333">Esto significa que si proporciona direcciones URL diferentes para la dirección URL del vínculo y el contenedor o `media:content URL` , el explorador de Windows utiliza la dirección URL del vínculo para las vistas previas del elemento, pero usa la otra dirección URL para la detección de tipos de archivo, apertura, descarga, etc.</span><span class="sxs-lookup"><span data-stu-id="582ee-333">This means that if you provide different URLs for the link URL and the enclosure or `media:content URL`, Windows Explorer uses the link URL for previews of the item but uses the other URL for file type detection, opening, downloading, and so forth.</span></span>

<span data-ttu-id="582ee-334">Cómo determina el explorador de Windows qué dirección URL usar:</span><span class="sxs-lookup"><span data-stu-id="582ee-334">How Windows Explorer determines what URL to use:</span></span>

1.  <span data-ttu-id="582ee-335">Si proporciona una asignación a [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), el explorador de Windows usa esa dirección URL</span><span class="sxs-lookup"><span data-stu-id="582ee-335">If you provide a mapping to [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), then Windows Explorer uses that URL</span></span>
2.  <span data-ttu-id="582ee-336">Si no proporciona una asignación, el explorador de Windows identifica si las direcciones URL del vínculo y del contenedor son diferentes.</span><span class="sxs-lookup"><span data-stu-id="582ee-336">If you do not provide a mapping, then Windows Explorer identifies whether the link and enclosure URLs are different.</span></span> <span data-ttu-id="582ee-337">Si es así, el explorador de Windows utiliza la dirección URL del vínculo.</span><span class="sxs-lookup"><span data-stu-id="582ee-337">If so, then Windows Explorer uses the link URL.</span></span>
3.  <span data-ttu-id="582ee-338">Si las direcciones URL son iguales o solo hay una dirección URL de vínculo, el explorador de Windows analiza el vínculo para buscar el contenedor primario quitando el nombre de archivo de la dirección URL completa.</span><span class="sxs-lookup"><span data-stu-id="582ee-338">If the URLs are the same or if there is only a link URL, then Windows Explorer parses the link to find the parent container by removing the file name from the full URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="582ee-339">Si reconoce que el análisis de direcciones URL daría como resultado vínculos inactivos para su servicio, debe proporcionar una asignación explícita para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="582ee-339">If you recognize that the URL parsing would result in dead links for your service, you should provide an explicit mapping for the property.</span></span>

     

## <a name="open-file-location-menu-item"></a><span data-ttu-id="582ee-340">Abrir el elemento de menú Ubicación del archivo</span><span class="sxs-lookup"><span data-stu-id="582ee-340">Open File Location Menu Item</span></span>

<span data-ttu-id="582ee-341">Cuando hace clic con el botón secundario en un elemento, aparece el comando de menú **abrir Ubicación del archivo** .</span><span class="sxs-lookup"><span data-stu-id="582ee-341">When a right-clicks an item, the **Open file location** menu command appears.</span></span> <span data-ttu-id="582ee-342">Este comando toma el usuario en el contenedor de la ubicación o de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="582ee-342">This command takes the user to the container for or location of that item.</span></span> <span data-ttu-id="582ee-343">Por ejemplo, en una búsqueda de SharePoint, si se selecciona esta opción para un archivo en una biblioteca de documentos, se abriría la raíz de la biblioteca de documentos en el explorador Web.</span><span class="sxs-lookup"><span data-stu-id="582ee-343">For example, in a SharePoint search, selecting this option for a file in a document library would open the document library root in the web browser.</span></span>

<span data-ttu-id="582ee-344">Cuando un usuario hace clic en **abrir ubicación de archivos**, el explorador de Windows intenta encontrar un contenedor primario mediante la lógica que se muestra en el siguiente diagrama de flujo:</span><span class="sxs-lookup"><span data-stu-id="582ee-344">When a user clicks **Open file location**, Windows Explorer attempts to find a parent container, by using the logic shown in the following flowchart:</span></span>

![diagrama de flujo que muestra cómo el explorador de Windows identifica un contenedor primario](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a><span data-ttu-id="582ee-346">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="582ee-346">Additional Resources</span></span>

<span data-ttu-id="582ee-347">Para obtener información adicional sobre la implementación de la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, consulte "recursos adicionales" en [búsqueda federada en Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="582ee-347">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="582ee-348">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="582ee-348">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="582ee-349">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="582ee-349">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="582ee-350">Introducción con búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="582ee-350">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="582ee-351">Conexión del servicio Web en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="582ee-351">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="582ee-352">Habilitación del almacén de datos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="582ee-352">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="582ee-353">Siguientes procedimientos recomendados en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="582ee-353">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="582ee-354">Implementación de conectores de búsqueda en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="582ee-354">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
