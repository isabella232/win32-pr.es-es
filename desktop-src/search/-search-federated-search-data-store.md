---
description: Explica cómo habilitar el acceso al almacén de datos a través de un servicio Web de OpenSearch y cómo evitar posibles barreras para hacerlo.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Habilitación del almacén de datos en la búsqueda federada de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cef227cb82c64f391ec61b2a7fef0fe35acf131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720340"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a><span data-ttu-id="76798-103">Habilitación del almacén de datos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="76798-103">Enabling Your Data Store in Windows Federated Search</span></span>

<span data-ttu-id="76798-104">Explica cómo habilitar el acceso al almacén de datos a través de un servicio Web de [OpenSearch](https://github.com/dewitt/opensearch) y cómo evitar posibles barreras para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="76798-104">Explains how to enable your data store to be accessed by an [OpenSearch](https://github.com/dewitt/opensearch) web service, and how to avoid potential barriers for doing so.</span></span>

<span data-ttu-id="76798-105">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="76798-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="76798-106">Condiciones para la aceptación de la solicitud de búsqueda</span><span class="sxs-lookup"><span data-stu-id="76798-106">Conditions for Search Request Acceptance</span></span>](#conditions-for-search-request-acceptance)
    -   [<span data-ttu-id="76798-107">Sintaxis de consulta admitida</span><span class="sxs-lookup"><span data-stu-id="76798-107">Supported Query Syntax</span></span>](#supported-query-syntax)
    -   [<span data-ttu-id="76798-108">Protocolos de autenticación admitidos</span><span class="sxs-lookup"><span data-stu-id="76798-108">Supported Authentication Protocols</span></span>](#supported-authentication-protocols)
-   [<span data-ttu-id="76798-109">Enviar consultas y devolver resultados de búsqueda en RSS o Atom</span><span class="sxs-lookup"><span data-stu-id="76798-109">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [<span data-ttu-id="76798-110">Ejemplo de una salida de fuente RSS</span><span class="sxs-lookup"><span data-stu-id="76798-110">Example of an RSS Feed Output</span></span>](#example-of-an-rss-feed-output)
-   [<span data-ttu-id="76798-111">Asignación automática a las propiedades del shell de Windows</span><span class="sxs-lookup"><span data-stu-id="76798-111">Automatic Mapping to Windows Shell Properties</span></span>](#automatic-mapping-to-windows-shell-properties)
-   [<span data-ttu-id="76798-112">Descripción de cómo Windows asigna elementos a tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="76798-112">Understanding How Windows Maps Items to File Types</span></span>](#understanding-how-windows-maps-items-to-file-types)
-   [<span data-ttu-id="76798-113">Evitar posibles barreras para habilitar un almacén de datos</span><span class="sxs-lookup"><span data-stu-id="76798-113">Avoiding Potential Barriers to Enabling a Data Store</span></span>](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [<span data-ttu-id="76798-114">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="76798-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="76798-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76798-115">Related topics</span></span>](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a><span data-ttu-id="76798-116">Condiciones para la aceptación de la solicitud de búsqueda</span><span class="sxs-lookup"><span data-stu-id="76798-116">Conditions for Search Request Acceptance</span></span>

<span data-ttu-id="76798-117">El servicio Web de [OpenSearch](https://github.com/dewitt/opensearch) que cree en el servidor Web **debe** cumplir los dos requisitos siguientes:</span><span class="sxs-lookup"><span data-stu-id="76798-117">The [OpenSearch](https://github.com/dewitt/opensearch) web service you create on your web server **must** fulfill the following two requirements:</span></span>

-   <span data-ttu-id="76798-118">Poder aceptar una `GET URL` consulta del cliente.</span><span class="sxs-lookup"><span data-stu-id="76798-118">Be able to accept a `GET URL` query from the client.</span></span>
-   <span data-ttu-id="76798-119">Permite que los términos de búsqueda se incrusten en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="76798-119">Permit the search terms to be embedded in the URL.</span></span>

    <span data-ttu-id="76798-120">En el ejemplo siguiente se muestra cómo se puede incrustar un término de búsqueda en una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="76798-120">The following example shows how a search term can be embedded in a URL.</span></span>

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> <span data-ttu-id="76798-121">La búsqueda federada no admite `POST` el envío de solicitudes a un servicio Web.</span><span class="sxs-lookup"><span data-stu-id="76798-121">Federated search does not support sending `POST` requests to a web service.</span></span>

 

<span data-ttu-id="76798-122">Para obtener más información sobre cómo construir una dirección URL, vea "parámetros de plantilla de dirección URL" en [creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="76798-122">For more information about constructing a URL, see "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

### <a name="supported-query-syntax"></a><span data-ttu-id="76798-123">Sintaxis de consulta admitida</span><span class="sxs-lookup"><span data-stu-id="76798-123">Supported Query Syntax</span></span>

<span data-ttu-id="76798-124">No se espera ninguna sintaxis de consulta específica en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="76798-124">There is no specific query syntax expected in Windows 7.</span></span> <span data-ttu-id="76798-125">El proveedor de OpenSearch acepta cualquier término que el usuario escriba en el cuadro de entrada en el explorador de Windows y lo codifica en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="76798-125">The OpenSearch provider accepts whatever terms the user enters in the input box in Windows Explorer, and encodes it into the URL.</span></span> <span data-ttu-id="76798-126">Lo hace según la plantilla de dirección URL que se describe en "parámetros de plantilla de dirección URL" en [creación de un archivo de descripción de OpenSearch en la búsqueda federada de Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="76798-126">It does so according to the URL template described in "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

<span data-ttu-id="76798-127">Los usuarios esperan que los términos independientes se traten conjuntamente como intercadenas de forma implícita.</span><span class="sxs-lookup"><span data-stu-id="76798-127">Users expect that separate terms are treated as implicitly ANDed together.</span></span> <span data-ttu-id="76798-128">Por ejemplo, una consulta de "Microsoft Windows" solo debe devolver resultados que contengan "Windows" y "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="76798-128">For example, a query for "Microsoft Windows" should return only results that contain both "Windows" and "Microsoft".</span></span>

### <a name="supported-authentication-protocols"></a><span data-ttu-id="76798-129">Protocolos de autenticación admitidos</span><span class="sxs-lookup"><span data-stu-id="76798-129">Supported Authentication Protocols</span></span>

<span data-ttu-id="76798-130">Windows Federated Search admite la autenticación basada en Windows y puede proporcionar credenciales a los servicios web a través de los protocolos siguientes:</span><span class="sxs-lookup"><span data-stu-id="76798-130">Windows Federated Search supports Windows-based authentication, and can provide credentials to web services via the following protocols:</span></span>

-   <span data-ttu-id="76798-131">NTLM.</span><span class="sxs-lookup"><span data-stu-id="76798-131">NTLM.</span></span>
-   <span data-ttu-id="76798-132">Kerberos.</span><span class="sxs-lookup"><span data-stu-id="76798-132">Kerberos.</span></span>
-   <span data-ttu-id="76798-133">Básico (solo a través de HTTPS).</span><span class="sxs-lookup"><span data-stu-id="76798-133">Basic (only over https).</span></span>
-   <span data-ttu-id="76798-134">Otros proveedores de compatibilidad para seguridad (SSP) instalados en Windows que proporcionan capacidad de consulta adicional.</span><span class="sxs-lookup"><span data-stu-id="76798-134">Other Security Support Providers (SSPs) installed on Windows that provide additional querying capacity.</span></span> <span data-ttu-id="76798-135">Consulte la documentación del SDK de la [interfaz SSP](../secauthn/sspi.md) para mantenerse al día de la posible adición de otros SSP.</span><span class="sxs-lookup"><span data-stu-id="76798-135">See the [SSP Interface](../secauthn/sspi.md) SDK documentation to keep abreast of the potential addition of other SSPs.</span></span>

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="76798-136">Enviar consultas y devolver resultados de búsqueda en RSS o Atom</span><span class="sxs-lookup"><span data-stu-id="76798-136">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="76798-137">El proveedor de [OpenSearch](https://github.com/dewitt/opensearch) es responsable de asignar los valores del elemento XML a las propiedades del sistema del shell de Windows que pueden usar las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="76798-137">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span> <span data-ttu-id="76798-138">Pero no se limita a las asignaciones predeterminadas de elementos RSS o Atom estándar, y puede incluir elementos XML personalizados en el espacio de nombres de Windows para cada una de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="76798-138">But you are not limited to the default mappings of standard RSS or Atom elements, and can include custom XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="76798-139">Por ejemplo, puede agregar sus propios elementos XML personalizados dentro del elemento **Item** para proporcionar metadatos adicionales a Windows.</span><span class="sxs-lookup"><span data-stu-id="76798-139">For example, you can add your own custom XML elements within the **item** element to provide additional metadata to Windows.</span></span> <span data-ttu-id="76798-140">También puede asignar elementos de otros espacios de nombres XML, como iTunes.</span><span class="sxs-lookup"><span data-stu-id="76798-140">You can also map elements from other XML namespaces, such as iTunes</span></span>

### <a name="example-of-an-rss-feed-output"></a><span data-ttu-id="76798-141">Ejemplo de una salida de fuente RSS</span><span class="sxs-lookup"><span data-stu-id="76798-141">Example of an RSS Feed Output</span></span>

<span data-ttu-id="76798-142">El siguiente ejemplo de salida de fuente RSS devuelve un elemento.</span><span class="sxs-lookup"><span data-stu-id="76798-142">The following example RSS feed output returns one item.</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, you'd be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="76798-143">Para obtener información más detallada sobre la asignación de propiedades, consulte las secciones "elementos extendidos en la búsqueda federada de WIndows" y "asignaciones de propiedades personalizadas" en [creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="76798-143">For more detailed information about property mapping, see the "Extended Elements in WIndows Federated Search" and "Custom Property Mappings" sections in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="automatic-mapping-to-windows-shell-properties"></a><span data-ttu-id="76798-144">Asignación automática a las propiedades del shell de Windows</span><span class="sxs-lookup"><span data-stu-id="76798-144">Automatic Mapping to Windows Shell Properties</span></span>

<span data-ttu-id="76798-145">Dentro de los elementos de la fuente RSS, puede incluir otros elementos XML que se asignan automáticamente a las propiedades del sistema del shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="76798-145">Within the items in your RSS feed, you can choose to include other XML elements that automatically map to Windows Shell system properties.</span></span> <span data-ttu-id="76798-146">Para ello, incluya un elemento con el nombre de la propiedad del shell de Windows y el prefijo del espacio de nombres System del shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="76798-146">To do so, include an element named after the Windows Shell property and prefixed with the Windows Shell system namespace.</span></span> <span data-ttu-id="76798-147">En el ejemplo siguiente se muestra la declaración de espacio de nombres `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` y la inclusión de un elemento para la asignación de propiedades `win:System.Contact.PrimaryEmailAddress` :</span><span class="sxs-lookup"><span data-stu-id="76798-147">The following example illustrates the namespace declaration `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` and the inclusion of an element for the property mapping `win:System.Contact.PrimaryEmailAddress`:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



<span data-ttu-id="76798-148">El prefijo de espacio de nombres usado aquí ( `"win"` ) es una sugerencia; puede usar cualquier prefijo.</span><span class="sxs-lookup"><span data-stu-id="76798-148">The namespace prefix used here (`"win"`) is a suggestion; you can use any prefix.</span></span> <span data-ttu-id="76798-149">Sin embargo, debe usar los nombres de propiedad del shell de Windows exactos y debe incluir el identificador uniforme de recursos (URI) exacto, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="76798-149">However, you must use the exact Windows Shell property names, and must include the exact Uniform Resource Identifier (URI), as shown in the following example:</span></span>


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



<span data-ttu-id="76798-150">**Acerca de las propiedades del sistema Shell de Windows**</span><span class="sxs-lookup"><span data-stu-id="76798-150">**About Windows Shell System Properties**</span></span>

<span data-ttu-id="76798-151">Windows define una lista completa de [propiedades del sistema](../properties/props.md) y el formato de tipo de valor necesario para cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="76798-151">Windows defines a complete list of [System Properties](../properties/props.md) and the value type format required for each property.</span></span> <span data-ttu-id="76798-152">La documentación de la propiedad del shell de la ventana [System. FileExtension](../properties/props-system-fileextension.md) , por ejemplo, especifica que el valor debe contener el punto inicial (". docx" y no "docx").</span><span class="sxs-lookup"><span data-stu-id="76798-152">The documentation for the [System.FileExtension](../properties/props-system-fileextension.md) Window Shell property, for example, specifies that the value must contain the leading dot (".docx" and not "docx").</span></span>

<span data-ttu-id="76798-153">**Valores de fecha y hora**</span><span class="sxs-lookup"><span data-stu-id="76798-153">**Date and Time Values**</span></span>

<span data-ttu-id="76798-154">El formato de fecha y hora preferido es ISO-8601, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="76798-154">The preferred date and time format is ISO-8601, as shown in the following example:</span></span>


```
2008-01-16T 19:20:30:.45+01:00
```



<span data-ttu-id="76798-155">Los desarrolladores de .NET deben usar la clase DateTime con `ToString("R") ` para generar el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="76798-155">.NET developers should use the DateTime class with `ToString("R") `to output the correct format.</span></span>

<span data-ttu-id="76798-156">Para obtener información más detallada sobre la asignación de propiedades, consulte "elementos extendidos en la búsqueda federada de Windows" en [creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="76798-156">For more detailed information about property mapping, see "Extended Elements in Windows Federated Search" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="understanding-how-windows-maps-items-to-file-types"></a><span data-ttu-id="76798-157">Descripción de cómo Windows asigna elementos a tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="76798-157">Understanding How Windows Maps Items to File Types</span></span>

<span data-ttu-id="76798-158">La búsqueda en la interfaz de usuario del explorador de Windows permite a los usuarios tratar los resultados como archivos cuando un elemento RSS señala a un archivo almacenado de forma remota.</span><span class="sxs-lookup"><span data-stu-id="76798-158">Searching within the Windows Explorer UI permits users to treat results as files when an RSS item points to a file stored remotely.</span></span> <span data-ttu-id="76798-159">El usuario puede arrastrar y colocar elementos en el escritorio, y la interfaz de usuario del explorador de Windows muestra el icono correcto y proporciona el menú contextual adecuado.</span><span class="sxs-lookup"><span data-stu-id="76798-159">The user can drag and drop items to the desktop, and the Windows Explorer UI displays the correct icon and provides the appropriate shortcut menu.</span></span> <span data-ttu-id="76798-160">Si el elemento RSS no apunta a un archivo almacenado de forma remota, el archivo se trata como un vínculo y los usuarios pueden realizar acciones en él, como crear un acceso directo o abrirlo en el explorador.</span><span class="sxs-lookup"><span data-stu-id="76798-160">If the RSS item does not point to a remotely stored file, the file is treated as a link, and users can perform actions on it such as creating a shortcut or opening it in the browser.</span></span>

<span data-ttu-id="76798-161">En el diagrama de flujo siguiente se muestra cómo Windows determina el tipo de archivo de un elemento.</span><span class="sxs-lookup"><span data-stu-id="76798-161">The following flowchart shows how Windows determines an item's file type.</span></span>

![diagrama de flujo que muestra las rutas de acceso de un elemento a decisiones para tratarlo como un elemento de tipo de vínculo Web o como un tipo de archivo](images/determineanitemfiletype.png)

<span data-ttu-id="76798-163">El proveedor de [OpenSearch](https://github.com/dewitt/opensearch) realiza los pasos siguientes para asignar un elemento a un tipo de archivo:</span><span class="sxs-lookup"><span data-stu-id="76798-163">The [OpenSearch](https://github.com/dewitt/opensearch) provider performs the following steps to map an item to a file type:</span></span>

-   <span data-ttu-id="76798-164">Identifique si el elemento se debe tratar como un archivo o como un vínculo Web.</span><span class="sxs-lookup"><span data-stu-id="76798-164">Identify whether the item should be treated as a file or a web link.</span></span>
-   <span data-ttu-id="76798-165">Identifique la extensión de nombre de archivo correcta que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="76798-165">Identify the correct file name extension to use.</span></span>

<span data-ttu-id="76798-166">Por ejemplo, si el elemento tiene una dirección URL de vínculo que usa una ruta de acceso del sistema de archivos (como `file:///\\server\share\etc\item.ext` ), el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) trata el vínculo como un archivo y determina el tipo mediante la extensión de nombre de archivo usada en la ruta de acceso (. ext en este ejemplo).</span><span class="sxs-lookup"><span data-stu-id="76798-166">For example, if the item has a link URL that uses a file system path (such as `file:///\\server\share\etc\item.ext`), the [OpenSearch](https://github.com/dewitt/opensearch) provider treats the link as a file and determines the type by the file name extension used in the path (.ext in this example).</span></span>

<span data-ttu-id="76798-167">Si el elemento utiliza el elemento contenedor de RSS estándar o **MediaRSS: Content** , el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) supone que el elemento es un archivo e identifica la extensión de nombre de archivo de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="76798-167">If the item uses the standard RSS enclosure or **MediaRSS media:content** element, the [OpenSearch](https://github.com/dewitt/opensearch) provider assumes that the item is a file and identifies the file name extension as follows:</span></span>

-   <span data-ttu-id="76798-168">Si la propiedad del shell de Windows [System. FileExtension](../properties/props-system-fileextension.md) se ha asignado para el elemento, el proveedor utiliza esa extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="76798-168">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has been mapped for the item, the provider uses that file name extension.</span></span>
-   <span data-ttu-id="76798-169">Si no se ha asignado la propiedad del shell de Windows [System. FileExtension](../properties/props-system-fileextension.md) , el proveedor usa el atributo **Type** especificado en el contenedor o el elemento de contenido.</span><span class="sxs-lookup"><span data-stu-id="76798-169">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has not been mapped, the provider uses the **Type** attribute specified in the enclosure or content element.</span></span> <span data-ttu-id="76798-170">Este elemento debe contener una `MIMEType` cadena, como `"image/jpeg"` .</span><span class="sxs-lookup"><span data-stu-id="76798-170">This element should contain a `MIMEType` string, such as `"image/jpeg"`.</span></span> <span data-ttu-id="76798-171">Si `MIMEType` está asociado a una extensión de nombre de archivo que está registrada en el equipo cliente, el elemento se considera como un archivo de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="76798-171">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the item is regarded as a file of that type.</span></span> <span data-ttu-id="76798-172">Si el `MIMEType` no está asociado a una extensión de nombre de archivo registrada en el equipo cliente, el elemento se trata como un tipo de vínculo Web.</span><span class="sxs-lookup"><span data-stu-id="76798-172">If the `MIMEType` is not associated with a file name extension registered on the client computer, the item is treated as a web link type.</span></span> <span data-ttu-id="76798-173">El proveedor de [OpenSearch](https://github.com/dewitt/opensearch) no intenta analizar el atributo de **dirección URL** para buscar la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="76798-173">The [OpenSearch](https://github.com/dewitt/opensearch) provider does not attempt to parse the **Url** attribute to locate the file name extension.</span></span>
-   <span data-ttu-id="76798-174">Si el `MIMEType` está asociado a una extensión de nombre de archivo que está registrada en el equipo cliente, el proveedor determina si la extensión de nombre de archivo es un tipo de archivo Web conocido (. htm,. html,. asp,. aspx,. php,. SWF,. STM).</span><span class="sxs-lookup"><span data-stu-id="76798-174">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the provider determines whether the file name extension is a known web file type (.htm, .html, .asp, .aspx, .php, .swf, .stm).</span></span> <span data-ttu-id="76798-175">Si es así, el tipo de archivo se considera un tipo de vínculo Web; de lo contrario, se considera como un tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="76798-175">If so, the file type is regarded as a web link type; otherwise, it is regarded as a file type.</span></span> <span data-ttu-id="76798-176">Por ejemplo, si `MIMEType "text/html"` está asociado con la extensión de nombre de archivo. htm, ese elemento se considera un vínculo Web en lugar de un tipo de archivo. htm.</span><span class="sxs-lookup"><span data-stu-id="76798-176">For example, if the `MIMEType "text/html"` is associated with the .htm file name extension, that item is regarded as a web link instead of as an .htm file type.</span></span>

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a><span data-ttu-id="76798-177">Evitar posibles barreras para habilitar un almacén de datos</span><span class="sxs-lookup"><span data-stu-id="76798-177">Avoiding Potential Barriers to Enabling a Data Store</span></span>

<span data-ttu-id="76798-178">Algunos almacenes de datos no proporcionan un servicio Web compatible con [OpenSearch](https://github.com/dewitt/opensearch), pero todavía pueden estar conectados a la búsqueda federada de Windows.</span><span class="sxs-lookup"><span data-stu-id="76798-178">Some data stores do not provide an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service but can still be connected to Windows Federated Search.</span></span> <span data-ttu-id="76798-179">Estos almacenes de datos incluyen:</span><span class="sxs-lookup"><span data-stu-id="76798-179">Such data stores include:</span></span>

-   <span data-ttu-id="76798-180">Índices remotos con métodos de autenticación que no se admiten en la búsqueda federada de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="76798-180">Remote indexes with authentication methods that are not supported in Windows 7 Federated Search.</span></span>

    <span data-ttu-id="76798-181">Algunos ejemplos son la autenticación basada en formularios y otros métodos de autenticación personalizados.</span><span class="sxs-lookup"><span data-stu-id="76798-181">Examples include forms-based authentication and other custom authentication methods.</span></span>

-   <span data-ttu-id="76798-182">Si un almacén público de alto valor tiene API web públicas, cualquier usuario puede escribir otro servicio Web compatible con [OpenSearch](https://github.com/dewitt/opensearch)y llama a esas API en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="76798-182">If a high-value public store has public web APIs, anyone can write another web service that is [OpenSearch](https://github.com/dewitt/opensearch)-compatible and calls those APIs behind the scenes.</span></span>

    <span data-ttu-id="76798-183">Algunos ejemplos son la biblioteca de las bases de datos del Congreso y de investigación médica.</span><span class="sxs-lookup"><span data-stu-id="76798-183">Examples include the Library of Congress, and medical research databases.</span></span>

-   <span data-ttu-id="76798-184">Almacenes de datos empresariales de propiedad o índices, y almacenes de administración de contenido heredados, para los que es posible que no se pueda implementar un front-end.</span><span class="sxs-lookup"><span data-stu-id="76798-184">Proprietary enterprise data stores or indexes, and legacy content management stores, for which it might be impossible to implement a front end.</span></span>

<span data-ttu-id="76798-185">Sin embargo, hay alternativas que pueden evitar barreras para habilitar un almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="76798-185">However, there are alternatives that can avoid barriers to enabling a data store.</span></span> <span data-ttu-id="76798-186">A continuación se muestran algunas de esas alternativas:</span><span class="sxs-lookup"><span data-stu-id="76798-186">The following are some of those alternatives:</span></span>

<span data-ttu-id="76798-187">**Para escribir un servicio Web de intermediario intermedio cuando no se puede modificar el servicio web para el origen de datos existente, o el servicio web proporciona una API personalizada:**</span><span class="sxs-lookup"><span data-stu-id="76798-187">**To write a middle-man web service when you cannot modify the web service for the existing data source, or the web service provides a custom API:**</span></span>

1.  <span data-ttu-id="76798-188">Escriba un servicio web central de Man que pueda aceptar una consulta de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="76798-188">Write a middle-man web service that can accept a Windows 7 query.</span></span>
2.  <span data-ttu-id="76798-189">Conéctese al origen de datos y recupere los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="76798-189">Connect to your data source, and retrieve the query results.</span></span>
3.  <span data-ttu-id="76798-190">Vuelva a dar formato a los resultados en formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="76798-190">Reformat the results in RSS or Atom format.</span></span>
4.  <span data-ttu-id="76798-191">Devuelva los resultados al cliente de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="76798-191">Return the results to the Windows 7 client.</span></span>
5.  <span data-ttu-id="76798-192">Tenga en cuenta que para los servicios de datos empresariales y muchos servicios de datos de Internet, es posible que tenga que pasar las credenciales de usuario mediante en nombre del servicio web para realizar el recorte de resultados en función de los permisos del usuario.</span><span class="sxs-lookup"><span data-stu-id="76798-192">Note that for enterprise data services and many Internet data services, you may need to pass the user credentials through on behalf of the web service to perform result trimming based on the user's permissions.</span></span>

<span data-ttu-id="76798-193">**Para usar un motor de búsqueda existente cuando no se puede habilitar un almacén de datos público:**</span><span class="sxs-lookup"><span data-stu-id="76798-193">**To use an existing search engine when you cannot enable a public data store:**</span></span>

1.  <span data-ttu-id="76798-194">Use un motor de búsqueda público que ya sea compatible con [OpenSearch](https://github.com/dewitt/opensearch) con RSS.</span><span class="sxs-lookup"><span data-stu-id="76798-194">Use a public search engine that already supports [OpenSearch](https://github.com/dewitt/opensearch) with RSS.</span></span> <span data-ttu-id="76798-195">Puede hacerlo si proporciona a los usuarios un archivo. osdx con una plantilla de dirección URL que restringe los resultados solo a los de su dominio específico.</span><span class="sxs-lookup"><span data-stu-id="76798-195">You can do so by providing your users with an .osdx file that has a URL template that restricts results to only those for your specific domain.</span></span>
2.  <span data-ttu-id="76798-196">Vea el ejemplo siguiente de una descripción de [OpenSearch](https://github.com/dewitt/opensearch) para buscar solo el contenido de la ayuda de Windows mediante una consulta en Live.com.</span><span class="sxs-lookup"><span data-stu-id="76798-196">See the following example of an [OpenSearch](https://github.com/dewitt/opensearch) description for searching only the Help content for Windows by using a query against live.com.</span></span>

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
      <ShortName>Windows Help</ShortName>
      <Description>Search Windows Help using the live.com search engine</Description>
      <Language></Language>
      <Url type="text/html" template="https://windowshelp.microsoft.com/windows/search.aspx?=&amp;qu={searchTerms}"/>
      <Url type="application/rss+xml" template="https://api.search.live.com/rss.aspx?source=web&amp;query={searchTerms} site:windowshelp.microsoft.com&amp;web.count=50"/>
    </OpenSearchDescription>
    ```

    

<span data-ttu-id="76798-197">**Para usar un servidor de indexación existente que admita OpenSearch cuando no pueda habilitar los índices o almacenes de datos empresariales de su propiedad:**</span><span class="sxs-lookup"><span data-stu-id="76798-197">**To use an existing indexing server that supports OpenSearch when you cannot enable proprietary enterprise data stores or indexes:**</span></span>

1.  <span data-ttu-id="76798-198">Seleccione un servidor de indexación existente que admita [OpenSearch](https://github.com/dewitt/opensearch) para indizar el contenido, como el servidor de búsqueda de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="76798-198">Select an existing indexing server that supports [OpenSearch](https://github.com/dewitt/opensearch) to index your content, such as the SharePoint Search Server.</span></span>
2.  <span data-ttu-id="76798-199">Cree un archivo. osdx que restrinja los resultados del índice de SharePoint a solo los del servidor mediante el uso de su sintaxis de palabra clave dentro de la plantilla de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="76798-199">Create an .osdx file that restricts the results from the SharePoint index to only those from your server by using their KeyWord syntax within the URL template.</span></span>

<span data-ttu-id="76798-200">**Para escribir un almacén de datos del lado cliente si una solución solo del servidor no funciona:**</span><span class="sxs-lookup"><span data-stu-id="76798-200">**To write a client-side data store if a server-side-only solution does not work:**</span></span>

1.  <span data-ttu-id="76798-201">Escribir un origen de datos de [OpenSearch](https://github.com/dewitt/opensearch) de cliente que se encuentre entre el proveedor de Windows [OpenSearch](https://github.com/dewitt/opensearch) y el origen de datos externo.</span><span class="sxs-lookup"><span data-stu-id="76798-201">Write a client-side [OpenSearch](https://github.com/dewitt/opensearch) data source that sits between the Windows [OpenSearch](https://github.com/dewitt/opensearch) provider and the external data source.</span></span>
2.  <span data-ttu-id="76798-202">Use la API de la [interfaz IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) en la Windows SDK para crear un archivo. searchconnector-MS configurado correctamente a través del cual el explorador de Windows puede llamar a su implementación con los parámetros de la consulta.</span><span class="sxs-lookup"><span data-stu-id="76798-202">Use the [IOpenSearchSource Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) API in the Windows SDK to create an appropriately configured .searchconnector-ms file through which Windows Explorer can call your implementation with the query parameters.</span></span> <span data-ttu-id="76798-203">A continuación, la implementación puede devolver resultados con formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="76798-203">Your implementation can then return results formatted in RSS or Atom format.</span></span> <span data-ttu-id="76798-204">Esto permite que la implementación proporcione una interfaz de usuario de autenticación personalizada y que se conecte al origen de datos mediante su propia API.</span><span class="sxs-lookup"><span data-stu-id="76798-204">Doing so enables your implementation to provide custom authentication UI and to connect to the data source using its proprietary API.</span></span>

> [!Note]  
> <span data-ttu-id="76798-205">Al abrir un archivo. osdx, se crea un archivo. searchconnector-MS (conector de búsqueda) en el directorio% userprofile%/searches y se le coloca un vínculo en el directorio% userprofile%/links</span><span class="sxs-lookup"><span data-stu-id="76798-205">Opening an .osdx file creates a .searchconnector-ms file (search connector) in the %userprofile%/searches directory and places a link to it in the %userprofile%/links directory.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="76798-206">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="76798-206">Additional Resources</span></span>

<span data-ttu-id="76798-207">Para obtener información adicional sobre la implementación de la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, consulte "recursos adicionales" en [búsqueda federada en Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76798-207">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76798-208">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76798-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76798-209">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="76798-209">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="76798-210">Introducción con búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="76798-210">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="76798-211">Conexión del servicio Web en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="76798-211">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="76798-212">Creación de un archivo de descripción de OpenSearch en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="76798-212">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="76798-213">Siguientes procedimientos recomendados en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="76798-213">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="76798-214">Implementación de conectores de búsqueda en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="76798-214">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
