---
description: Describe cómo crear un archivo OpenSearch Description (.osdx) para conectar almacenes de datos externos al cliente de Windows a través del protocolo OpenSearch.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Crear un archivo OpenSearch descripción en Windows búsqueda federada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363259"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a>Crear un archivo OpenSearch descripción en Windows búsqueda federada

Describe cómo crear un archivo OpenSearch Description (.osdx) para conectar almacenes de datos externos al cliente de Windows a través [del protocolo OpenSearch](https://github.com/dewitt/opensearch) datos. La búsqueda federada permite a los usuarios buscar en un almacén de datos remoto y ver los resultados desde Windows Explorer.

Este tema contiene las siguientes secciones:

-   [OpenSearch Archivo de descripción](#opensearch-description-file)
    -   [Elementos secundarios mínimos necesarios](#mininum-required-child-elements)
-   [Elementos estándar en Windows búsqueda federada](#standard-elements-in-windows-federated-search)
    -   [Shortname](#shortname)
    -   [Descripción](#description)
    -   [Plantilla de dirección URL para resultados RSS/Atom](#url-template-for-rssatom-results)
    -   [Plantilla de dirección URL para resultados web](#url-template-for-web-results)
    -   [Parámetros de plantilla de dirección URL](#url-template-parameters)
    -   [Resultados paginados](#paged-results)
    -   [Paginación mediante el índice de elementos](#paging-using-the-item-index)
    -   [Paginación mediante el índice de página](#paging-using-the-page-index)
    -   [Tamaño de página](#page-size)
-   [Elementos extendidos en Windows búsqueda federada](#extended-elements-in-windows-federated-search)
    -   [Recuento máximo de resultados](#maximum-result-count)
    -   [Asignación de propiedades](#property-mapping)
-   [Vistas previas](#previews)
-   [Abrir el elemento de menú Ubicación del archivo](#open-file-location-menu-item)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="opensearch-description-file"></a>OpenSearch Archivo de descripción

Un OpenSearch description (.osdx) para Windows búsqueda federada debe cumplir las reglas siguientes:

-   Ser un documento OpenSearch descripción, tal como se define en la [especificación OpenSearch](https://github.com/dewitt/opensearch) 1.1.
-   Proporcione una plantilla de dirección URL con un tipo de formato RSS o Atom.
-   Use la extensión de nombre de archivo .osdx o asocie con la extensión de nombre de archivo .osdx al descargar desde la web. Por ejemplo, no es necesario que un servidor use .osdx. Un servidor puede devolver el archivo con cualquier extensión de nombre de archivo, como .xml por ejemplo, y tratarlo como si fuera un archivo .osdx si usa el tipo MIME correcto para los documentos de descripción de OpenSearch (archivos .osdx).
-   Proporcione un **valor de elemento ShortName** (recomendado).

### <a name="mininum-required-child-elements"></a>Elementos secundarios mínimos necesarios

El siguiente archivo .osdx de ejemplo consta de **ShortName** y `Url` elementos , que son los elementos secundarios mínimos necesarios.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a>Elementos estándar en Windows búsqueda federada

Además de los elementos secundarios mínimos, la búsqueda federada admite los siguientes elementos estándar.

### <a name="shortname"></a>Shortname

Windows el valor del elemento **ShortName** para dar nombre al archivo .searchconnector-ms (conector de búsqueda) que se crea cuando el usuario abre el archivo .osdx. Windows garantiza que el nombre de archivo generado use solo los caracteres que se permiten en Windows nombres de archivo. Si no se proporciona ningún valor **ShortName,** el archivo .searchconnector-ms intenta usar el nombre de archivo del archivo .osdx en su lugar.

En el código siguiente se muestra cómo usar el **elemento ShortName** en un archivo .osdx.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a>Descripción

Windows el valor del elemento **Description** para rellenar la descripción del archivo que se muestra en el panel de detalles del Explorador de Windows cuando un usuario selecciona un archivo .searchconnector-ms.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a>Plantilla de dirección URL para resultados RSS/Atom

El archivo .osdx debe incluir  un elemento de formato **URL** y un atributo de plantilla (una plantilla de dirección URL) que devuelva resultados en formato RSS o Atom. El atributo format debe establecerse en para los resultados con formato RSS o para los resultados con formato Atom, como se muestra `application/rss+xml` `application/atom+xml` en el código siguiente.

> [!Note]  
> El **elemento de formato** url y el atributo **de** plantilla se conocen normalmente como plantilla de dirección URL.

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a>Plantilla de dirección URL para resultados web

Si hay una versión de los resultados de la búsqueda que se puede ver en un explorador web, debe proporcionar un elemento **Url format=** y un atributo de plantilla, como se muestra en el `text/html` código siguiente. 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



Si proporciona un elemento **Url format="text/html"** y un atributo de plantilla, aparece un botón en la barra de comandos de Windows Explorer, como se muestra en la siguiente captura de pantalla, que permite al usuario abrir un explorador web para ver los resultados de la búsqueda cuando el usuario realiza una consulta. 

![captura de pantalla que muestra el botón de succión de búsqueda web.](images/websearchroll-overcommandbarbutton.png)

La reversión de la consulta a la interfaz de usuario web del almacén de datos es importante en algunos escenarios. Por ejemplo, es posible que un usuario quiera ver más de 100 resultados (el número predeterminado de elementos que OpenSearch proveedor). Si es así, es posible que el usuario también quiera usar características de búsqueda que solo están disponibles en el sitio web del almacén de datos, como volver a consultar con un criterio de ordenación diferente, o dinamr y filtrar la consulta con metadatos relacionados.

### <a name="url-template-parameters"></a>Parámetros de plantilla de dirección URL

El OpenSearch realiza siempre las siguientes acciones:

1.  Usa la plantilla de dirección URL para enviar la solicitud al servicio web.
2.  Intenta reemplazar los tokens encontrados en la plantilla de dirección URL antes de enviar la solicitud al servicio web, como se muestra a continuación:
    -   Reemplaza los tokens de OpenSearch estándar que se enumeran en la tabla siguiente.
    -   Quita los tokens que no aparecen en la tabla siguiente.



| Token admitido  | Uso por parte del OpenSearch proveedor                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| {searchTerms}    | Se reemplaza por los términos de búsqueda que el usuario escriba en el cuadro Windows entrada de búsqueda del Explorador.<br/>                                         |
| {startIndex}     | Se usa al obtener resultados en "páginas".<br/> Se reemplaza por el índice del primer elemento de resultado que se devuelve.<br/>                        |
| {startPage}      | Se usa al obtener resultados en "páginas".<br/> Se reemplaza por el número de página del conjunto de resultados de búsqueda que se devolverán.<br/>               |
| {count}          | Se usa al obtener resultados en "páginas".<br/> Se reemplaza por el número de resultados de búsqueda por página que Windows explorer.<br/> |
| {language}       | Se reemplaza por una cadena que indica el idioma de la consulta que se envía.<br/>                                                          |
| {inputEncoding}  | Se reemplaza por una cadena (como "UTF-16") que indica la codificación de caracteres de la consulta que se envía.<br/>                                |
| {outputEncoding} | Se reemplaza por una cadena (como "UTF-16") que indica la codificación de caracteres deseada para la respuesta del servicio web.<br/>       |



 

### <a name="paged-results"></a>Resultados paginados

Es posible que desee limitar el número de resultados devueltos por solicitud. Puede optar por devolver una "página" de resultados a la vez o hacer que el proveedor de OpenSearch obtenga páginas de resultados adicionales por número de elemento o número de página. Por ejemplo, si envía veinte resultados por página, la primera página que envíe se iniciará en el índice de elemento 1 y en la página 1. la segunda página que envía comienza en el índice de elemento 21 y en la página 2. Puede definir cómo desea que el proveedor de OpenSearch solicite elementos mediante o el `{startItem}` token en la plantilla de dirección `{startPage}` URL.

### <a name="paging-using-the-item-index"></a>Paginación mediante el índice de elementos

Un índice de elemento identifica el primer elemento de resultado en una página de resultados. Si desea que los clientes envíen solicitudes mediante un índice de elemento, puede usar el token en el atributo de plantilla de elemento Url, como se muestra `{startIndex}` en el código siguiente.  


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



El [OpenSearch](https://github.com/dewitt/opensearch) a continuación reemplaza el token de la dirección URL por un valor de índice inicial. La primera solicitud comienza con el primer elemento, como se muestra en el ejemplo siguiente:


```
https://example.com/rss.php?query=frogs&start=1
```



El OpenSearch puede obtener elementos adicionales cambiando el valor `{startIndex}` del parámetro y emitiendo una nueva solicitud. El proveedor repite este proceso hasta que obtiene suficientes resultados para satisfacer su límite o alcanza el final de los resultados. El OpenSearch consulta el número de elementos devueltos por el servicio web en la primera página de resultados y establece el tamaño de página esperado en ese número. Usa ese número para incrementar el `{startIndex}` valor de las solicitudes posteriores. Por ejemplo, si el servicio web devuelve 20 resultados en la primera solicitud, el proveedor establece el tamaño de página esperado en 20. Para la siguiente solicitud, el proveedor reemplaza `{startIndex}` por el valor de 21 para obtener los 20 elementos siguientes.

> [!Note]  
> Si una página de resultados devuelta por el servicio web tiene menos elementos que el tamaño de página esperado, el proveedor de OpenSearch asume que ha recibido la última página de resultados y deja de realizar solicitudes.

 

### <a name="paging-using-the-page-index"></a>Paginación mediante el índice de página

Un índice de página identifica la página de resultados especificada. Si desea que los clientes envíen solicitudes mediante un número de página, puede usar el token en el atributo de plantilla del elemento de formato URL para indicarlo, como se muestra en `{startPage}` el ejemplo siguiente:  


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



Después, OpenSearch proveedor reemplaza el token de la dirección URL por un parámetro de número de página. La primera solicitud comienza con la primera página, como se muestra en el ejemplo siguiente:


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> Si una página de resultados devuelta por el servicio web tiene menos elementos que el tamaño de página esperado, el proveedor de OpenSearch asume que ha recibido la última página de resultados y deja de realizar solicitudes.

 

### <a name="page-size"></a>Tamaño de página

Es posible que desee configurar el servicio web para permitir que una solicitud especifique el tamaño de las páginas mediante algún parámetro en la dirección URL. Una solicitud debe especificarse en el archivo .osdx mediante el `{count}` token , como se indica a continuación:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



El [OpenSearch](https://github.com/dewitt/opensearch) puede establecer el tamaño de página deseado, en número de resultados por página, como se muestra en el ejemplo siguiente:


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



De forma predeterminada, OpenSearch proveedor realiza solicitudes con un tamaño de página de 50. Si desea un tamaño de página diferente, no proporcione un token y, en su lugar, coloque el número deseado `{count}` directamente en el elemento de plantilla **Url.**

El OpenSearch determina el tamaño de página en función del número de resultados devueltos en la primera solicitud. Si la primera página de resultados recibidos tiene menos elementos que el recuento solicitado, el proveedor restablece el tamaño de página para las solicitudes de página posteriores. Si las solicitudes de página posteriores devuelven menos elementos de los solicitados, OpenSearch proveedor da por supuesto que ha llegado al final de los resultados.

## <a name="extended-elements-in-windows-federated-search"></a>Elementos extendidos en Windows búsqueda federada

Además de los elementos estándar, la búsqueda federada admite los siguientes elementos extendidos: **MaximumResultCount** y **ResultsProcessing.**

Dado que estos elementos secundarios extendidos no se admiten en la [especificación OpenSearch](https://github.com/dewitt/opensearch) v1.1, deben agregarse mediante el siguiente espacio de nombres:


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a>Recuento máximo de resultados

De forma predeterminada, los conectores de búsqueda están limitados a 100 resultados por consulta de usuario. Este límite se puede personalizar incluyendo el **elemento MaximumResultCount** en el archivo OSD, como se muestra en el ejemplo siguiente:


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



En el ejemplo anterior se declara el prefijo de espacio de nombres en el elemento OpenSearchDescription de nivel superior y, a continuación, se usa como prefijo `ms-ose` en el nombre del elemento.  Esta declaración es necesaria porque **MaximumResultCount** no se admite en la [especificación OpenSearch](https://github.com/dewitt/opensearch) v1.1.

### <a name="property-mapping"></a>Asignación de propiedades

Cuando el servicio web devuelve los resultados como una fuente RSS o Atom, el proveedor de OpenSearch debe asignar los metadatos de elemento de las fuentes a las propiedades que el shell de Windows puede usar. En la siguiente captura de pantalla se muestra cómo el OpenSearch asigna algunos de los elementos RSS predeterminados.

![captura de pantalla que muestra las asignaciones de propiedades integradas de rss a windows-shell](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a>Asignaciones predeterminadas

En la tabla siguiente se enumeran las asignaciones predeterminadas de elementos XML RSS Windows propiedades del sistema shell. Las rutas de acceso XML son relativas al elemento de elemento. El prefijo se define mediante el espacio de nombres `"media:"` [Yahoo Search Namespace.](https://www.rssboard.org/media-rss)



| Ruta de acceso XML RSS                  | Windows Propiedad shell (nombre canónico) |
|-------------------------------|-----------------------------------------|
| Vínculo                          | System.ItemUrl                          |
| Título                         | System.ItemName                         |
| Autor                        | System.Author                           |
| pubDate                       | System.DateModified                     |
| Descripción                   | System.AutoSummary                      |
| Category                      | System.Keywords                         |
| enclosure/@type               | System.MIMEType                         |
| enclosure/@length             | System.Size                             |
| enclosure/@url                | System.ContentUrl                       |
| media:category                | System.Keywords                         |
| media:content/@fileSize       | System.Size                             |
| media:content/@type           | System.MIMEType                         |
| media:content/@url            | System.ContentUrl                       |
| media:group/content/@fileSize | System.Size                             |
| media:group/content/@type     | System.MIMEType                         |
| media:group/content/@url      | System.ContentUrl                       |
| media:thumbnail/@url          | System.ItemThumbnailUrl                 |



 

> [!Note]  
> Además de las asignaciones predeterminadas de elementos ESTÁNDAR RSS o Atom, puede asignar otras propiedades del sistema de Windows Shell mediante la inclusión de elementos XML adicionales en el espacio de nombres Windows para cada una de las propiedades. También puede asignar elementos de otros espacios de nombres XML existentes, como MediaRSS, iTunes, etc., agregando la asignación de propiedades personalizadas en el archivo .osdx.

 

### <a name="custom-property-mappings"></a>Asignaciones de propiedades personalizadas

Puede personalizar la asignación de elementos de la salida RSS para Windows Shell mediante la especificación de la asignación en el archivo .osdx.

La salida RSS especifica:

-   Un espacio de nombres XML y
-   Para cualquier elemento secundario de un elemento, un nombre de elemento al que asignar.

El archivo .osdx identifica una propiedad Windows Shell para cada nombre de elemento de un espacio de nombres. Las asignaciones de propiedades que defina en el archivo .osdx invalidan las asignaciones predeterminadas, si existen, para esas propiedades especificadas.

En el diagrama siguiente se muestra cómo se asigna una extensión RSS a Windows propiedades (nombre canónico).

![diagrama que muestra que la combinación de espacio de nombres xml y ruta de acceso xml genera el nombre canónico](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a>Resultados RSS de ejemplo y asignación de propiedades OSD

La siguiente salida RSS de ejemplo identifica `https://example.com/schema/2009` como el espacio de nombres XML con el prefijo "example". Este prefijo debe aparecer de nuevo antes del elemento **de correo** electrónico.


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



En el archivo .osdx de ejemplo siguiente, el elemento **de** correo electrónico XML se asigna a la propiedad [System.Contact.EmailAddress](../properties/props-system-contact-emailaddress.md)de Shell de Windows .


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



Hay algunas propiedades que no se pueden asignar porque los valores para ellas se invalidan más adelante o no son editables. Por ejemplo, [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) o [System.ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) no se pueden asignar porque se calculan a partir del valor de dirección URL proporcionado en los elementos de vínculo o de alojamiento.

### <a name="thumbnails"></a>Miniaturas

Las direcciones URL de imagen en miniatura se pueden proporcionar para cualquier elemento mediante el **elemento media:thumbnail url=""".** La resolución ideal es de 150 x 150 píxeles. Las miniaturas más grandes admitidas son de 256 x 256 píxeles. Proporcionar imágenes más grandes toma más ancho de banda sin ninguna ventaja adicional para el usuario.

### <a name="open-file-location-context-menu"></a>Menú contextual Abrir ubicación de archivo

Windows un menú contextual denominado **Abrir ubicación de archivo para** los elementos de resultado. Si el usuario selecciona un elemento de ese menú, se abre la dirección URL "primaria" del elemento seleccionado. Si la dirección URL es una dirección URL web, como , el explorador web se abre y `https://...` navega a esa dirección URL. La fuente debe proporcionar una dirección URL personalizada para cada elemento para asegurarse de que Windows abre una dirección URL válida. Esto se puede lograr mediante la inclusión de la dirección URL dentro de un elemento dentro del XML del elemento, como se muestra en el ejemplo siguiente:


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



Si esta propiedad no se establece explícitamente en el XML del elemento, el proveedor de OpenSearch la establece en la carpeta primaria de la dirección URL del elemento. En el ejemplo anterior, el proveedor OpenSearch usaría el valor de vínculo y establecería el valor de la propiedad [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell en `"https://example.com/"` .

### <a name="customize-windows-explorer-views-with-property-description-lists"></a>Personalizar vistas Windows Explorer con listas de descripción de propiedades

Algunos Windows diseños de vista del Explorador de propiedades se definen mediante listas de descripción de propiedades o listas de propiedades. Una lista proplist es una lista delimitada por punto y coma de propiedades, como , que se usa para controlar cómo aparecen los resultados en `"prop:System.ItemName; System.Author"` Windows Explorer.

Las áreas de interfaz de usuario Windows Explorer que se pueden personalizar mediante proplists se muestran en la siguiente captura de pantalla:

![captura de pantalla que muestra las áreas de interfaz de usuario del Explorador de Windows que se pueden personalizar mediante proplists](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

Cada área de Windows Explorer tiene un conjunto asociado de proplists, que se especifican a sí mismos como propiedades. Puede especificar listas de propiedades personalizadas para elementos individuales en los conjuntos de resultados o para todos los elementos de un conjunto de resultados.



| Área de interfaz de usuario para personalizar               | Windows Propiedad de shell que implementa la personalización |
|------------------------------------|----------------------------------------------------------|
| Modo de vista de contenido (al buscar) | System.PropList.ContentViewModeForSearch                 |
| Modo de vista de contenido (al examinar)  | System.PropList.ContentViewModeForBrowse                 |
| Modo de vista de mosaico                     | System.PropList.TileInfo                                 |
| Panel de detalles                       | System.PropList.PreviewDetails                           |
| Información sobre herramientas (información sobre herramientas del elemento)     | System.PropList.Infotip                                  |



 

 

**Para especificar una lista de propiedades única para un elemento individual:**

1.  En la salida RSS, agregue un elemento personalizado que represente la lista de propiedades que desea personalizar. Por ejemplo, en el ejemplo siguiente se establece la lista del panel de detalles:
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  Para aplicar una propiedad a todos los elementos de los resultados de búsqueda sin modificar la salida RSS, especifique una lista proplist dentro de un **elemento ms-ose:PropertyDefaultValues** en el archivo .osdx, como se muestra en el ejemplo siguiente:

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a>Diseño de propiedades del modo de vista de contenido

La lista de propiedades especificadas en las listas de propiedades **System.PropList.ContentViewModeForSearch** y **System.PropList.ContentViewModeForBrowse** determina lo que se muestra en el modo de vista Contenido. Para obtener más información sobre las listas de propiedades, [vea PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).

Las propiedades se establecen según los números que se muestran en el siguiente patrón de diseño:

![captura de pantalla que muestra el patrón de diseño predeterminado en la vista de contenido](images/propertiesnumberslayoutpattern.png)

Si usamos la siguiente lista de propiedades,


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



A continuación, se muestra lo siguiente:

![captura de pantalla que muestra el diseño de la propiedad de ejemplo.](images/samplepropertylayout.png)

> [!Note]  
> Para obtener la mejor legibilidad, las propiedades que se muestran en la columna más a la derecha deben estar etiquetadas.

 

### <a name="property-list-flags"></a>Marcas de lista de propiedades

Solo una de las marcas definidas en la documentación de proplists se aplica a la presentación de elementos en los diseños del modo vista de contenido: ` "~"` . En los ejemplos anteriores, el explorador Windows etiqueta algunas de las propiedades, como `Tags: animals; zoo; lion` . Este es el comportamiento predeterminado cuando se especifica una propiedad en la lista. Por ejemplo, la lista proplist `"System.Author"` tiene que se muestra como `"Authors: value"` . Si desea ocultar la etiqueta de propiedad, coloque un delante `"~"` del nombre de propiedad. Por ejemplo, si la lista de propiedades tiene , la propiedad se muestra como simplemente `"~System.Size"` un valor, sin la etiqueta .

## <a name="previews"></a>Vistas previas

Cuando el usuario selecciona un elemento de resultado en Windows Explorer y el panel de vista previa está abierto, se muestra la vista previa del contenido del elemento.

El contenido que se va a mostrar en la versión preliminar se especifica mediante una dirección URL, que se determina de la siguiente manera:

1.  Si la **propiedad System.WebPreviewUrl** Windows Shell está establecida para el elemento, use esa dirección URL.
    > [!Note]  
    > La propiedad debe proporcionarse en RSS mediante el espacio de nombres Windows Shell o asignarse explícitamente en el archivo .osdx.

     

2.  Si no es así, use la dirección URL del vínculo en su lugar.

En el diagrama de flujo siguiente se muestra esta lógica.

![diagrama de flujo que muestra cómo el Explorador de Windows selecciona la dirección URL que se va a usar para las versiones preliminares](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

Es posible usar una dirección URL diferente para la versión preliminar que para el propio elemento. Esto significa que si proporciona direcciones URL diferentes para la dirección URL del vínculo y el gabinete o , Windows Explorer usa la dirección URL del vínculo para las vistas previas del elemento, pero usa la otra dirección URL para la detección de tipos de archivo, la apertura, la `media:content URL` descarga, etc.

Cómo Windows explorer determina qué dirección URL usar:

1.  Si proporciona una asignación a [System.ItemFolderPathDisplay,](../properties/props-system-itemfolderpathdisplay.md)Windows Explorer usa esa dirección URL.
2.  Si no proporciona una asignación, Windows Explorer identifica si las direcciones URL del vínculo y del receptábulo son diferentes. Si es así, Windows Explorer usa la dirección URL del vínculo.
3.  Si las direcciones URL son las mismas o si solo hay una dirección URL de vínculo, Windows Explorer analiza el vínculo para buscar el contenedor primario quitando el nombre de archivo de la dirección URL completa.
    > [!Note]  
    > Si reconoce que el análisis de direcciones URL daría lugar a vínculos no encontrados para el servicio, debe proporcionar una asignación explícita para la propiedad .

     

## <a name="open-file-location-menu-item"></a>Elemento de menú Abrir ubicación del archivo

Cuando un elemento hace clic con el botón derecho en un elemento, aparece el comando **de** menú Abrir ubicación de archivo. Este comando lleva al usuario al contenedor para o la ubicación de ese elemento. Por ejemplo, en una SharePoint, al seleccionar esta opción para un archivo en una biblioteca de documentos se abriría la raíz de la biblioteca de documentos en el explorador web.

Cuando un usuario hace clic en **Abrir** ubicación de archivo , Windows Explorer intenta encontrar un contenedor primario, mediante la lógica que se muestra en el siguiente diagrama de flujo:

![diagrama de flujo que muestra cómo el Explorador de Windows identifica un contenedor primario](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a>Recursos adicionales

Para obtener más información sobre cómo implementar la federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, vea "Recursos adicionales" en Búsqueda federada [en Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Tareas iniciales con la búsqueda federada en Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Conexión del servicio web en Windows búsqueda federada](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitar el almacén de datos en Windows búsqueda federada](-search-federated-search-data-store.md)
</dt> <dt>

[Seguir los procedimientos recomendados en Windows búsqueda federada](-search-fedsearch-best.md)
</dt> <dt>

[Implementación de conectores de búsqueda en Windows búsqueda federada](-search-federated-search-deploying.md)
</dt> </dl>

 

 
