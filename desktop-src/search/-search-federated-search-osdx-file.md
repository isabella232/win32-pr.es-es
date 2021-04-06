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
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a>Creación de un archivo de descripción de OpenSearch en Windows Federated Search

Describe cómo crear un archivo de descripción de OpenSearch (. osdx) para conectar los almacenes de datos externos al cliente de Windows a través del protocolo [OpenSearch](https://github.com/dewitt/opensearch) . La búsqueda federada permite a los usuarios buscar en un almacén de datos remoto y ver los resultados desde el explorador de Windows.

Este tema contiene las siguientes secciones:

-   [Archivo de descripción de OpenSearch](#opensearch-description-file)
    -   [Mínimo elementos secundarios requeridos](#mininum-required-child-elements)
-   [Elementos estándar en la búsqueda federada de Windows](#standard-elements-in-windows-federated-search)
    -   [Corto](#shortname)
    -   [Descripción](#description)
    -   [Plantilla de dirección URL para resultados de RSS/Atom](#url-template-for-rssatom-results)
    -   [Plantilla de dirección URL para resultados Web](#url-template-for-web-results)
    -   [Parámetros de plantilla de URL](#url-template-parameters)
    -   [Resultados paginados](#paged-results)
    -   [Paginación mediante el índice del elemento](#paging-using-the-item-index)
    -   [Paginación mediante el índice de página](#paging-using-the-page-index)
    -   [Tamaño de página](#page-size)
-   [Elementos extendidos en la búsqueda federada de Windows](#extended-elements-in-windows-federated-search)
    -   [Número máximo de resultados](#maximum-result-count)
    -   [Asignación de propiedades](#property-mapping)
-   [Vistas previas](#previews)
-   [Abrir el elemento de menú Ubicación del archivo](#open-file-location-menu-item)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="opensearch-description-file"></a>Archivo de descripción de OpenSearch

Un archivo de descripción de OpenSearch (. osdx) para la búsqueda federada de Windows debe cumplir las siguientes reglas:

-   Ser un documento de descripción de OpenSearch válido, tal y como se define en la especificación de [opensearch](https://github.com/dewitt/opensearch) 1,1.
-   Proporcione una plantilla de dirección URL con un tipo de formato RSS o Atom.
-   Use la extensión de nombre de archivo. osdx o asocie la extensión de nombre de archivo. osdx al descargar desde Internet. Por ejemplo, no es necesario que un servidor use. osdx. Un servidor puede devolver el archivo con cualquier extensión de nombre de archivo, como. XML por ejemplo, y tratarse como si fuera un archivo. Osdx Si usa el tipo MIME correcto para los documentos de descripción de OpenSearch (archivos. osdx).
-   Proporcione un valor de elemento **nombre_corto** (recomendado).

### <a name="mininum-required-child-elements"></a>Mínimo elementos secundarios requeridos

El siguiente archivo de ejemplo. osdx está compuesto por los elementos **nombre_corto** y `Url` , que son los elementos secundarios mínimos necesarios.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a>Elementos estándar en la búsqueda federada de Windows

Además de los elementos secundarios mínimos, la búsqueda federada admite los siguientes elementos estándar.

### <a name="shortname"></a>Corto

Windows usa el valor del elemento **nombre_corto** para asignar un nombre al archivo. searchconnector-MS (conector de búsqueda) que se crea cuando el usuario abre el archivo. osdx. Windows se asegura de que el nombre de archivo generado solo usa caracteres permitidos en los nombres de archivo de Windows. Si no se proporciona ningún valor de **ShortName** , el archivo. searchconnector-MS intenta usar el nombre de archivo del archivo. osdx en su lugar.

En el código siguiente se muestra cómo usar el elemento **nombre_corto** en un archivo. osdx.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a>Descripción

Windows usa el valor del elemento **Description** para rellenar la descripción del archivo que se muestra en el panel de detalles del explorador de Windows cuando un usuario selecciona un archivo. searchconnector-ms.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a>Plantilla de dirección URL para resultados de RSS/Atom

El archivo. osdx debe incluir un elemento de **formato de dirección URL** y un atributo de **plantilla** (una plantilla de dirección URL) que devuelva resultados en formato RSS o Atom. El atributo de formato debe establecerse en `application/rss+xml` para los resultados con formato RSS o en los `application/atom+xml` resultados con formato Atom, tal como se muestra en el código siguiente.

> [!Note]  
> El elemento de **formato de dirección URL** y el atributo de **plantilla** se conocen normalmente como una plantilla de dirección URL.

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a>Plantilla de dirección URL para resultados Web

Si hay una versión de los resultados de la búsqueda que se puede ver en un explorador Web, debe proporcionar un **formato de dirección URL =** `text/html` elemento y el atributo de **plantilla** , como se muestra en el código siguiente.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



Si proporciona un elemento de **formato de dirección URL = "text/html"** y un atributo de **plantilla** , aparece un botón en la barra de comandos del explorador de Windows, como se muestra en la siguiente captura de pantalla, que permite al usuario abrir un explorador Web para ver los resultados de la búsqueda cuando el usuario realiza una consulta.

![captura de pantalla que muestra el botón deshacer la búsqueda web.](images/websearchroll-overcommandbarbutton.png)

La reversión de la consulta de nuevo a la interfaz de usuario Web del almacén de datos es importante en algunos escenarios. Por ejemplo, puede que un usuario desee ver más de 100 resultados (el número predeterminado de elementos que solicita el proveedor de OpenSearch). Si es así, el usuario también puede usar características de búsqueda que solo están disponibles en el sitio web del almacén de datos, como volver a realizar consultas con un criterio de ordenación diferente o dinamizar y filtrar la consulta con los metadatos relacionados.

### <a name="url-template-parameters"></a>Parámetros de plantilla de URL

El proveedor de OpenSearch realiza siempre las siguientes acciones:

1.  Usa la plantilla de dirección URL para enviar la solicitud al servicio Web.
2.  Intenta reemplazar los tokens que se encuentran en la plantilla de dirección URL antes de enviar la solicitud al servicio Web, como se indica a continuación:
    -   Reemplaza los tokens de OpenSearch estándar que se enumeran en la tabla siguiente.
    -   Quita todos los tokens que no se muestran en la tabla siguiente.



| Token compatible  | Cómo lo usa el proveedor de OpenSearch                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| {searchTerms}    | Se reemplaza por los términos de búsqueda que el usuario escribe en el cuadro de entrada de búsqueda del explorador de Windows.<br/>                                         |
| Super     | Se usa al obtener resultados en "pages".<br/> Se reemplaza por el índice del primer elemento de resultado que se va a devolver.<br/>                        |
| StartPage      | Se usa al obtener resultados en "pages".<br/> Se reemplaza por el número de página del conjunto de resultados de búsqueda que se va a devolver.<br/>               |
| contabiliza          | Se usa al obtener resultados en "pages".<br/> Se reemplaza por el número de resultados de búsqueda por página que solicita el explorador de Windows.<br/> |
| módulo       | Se reemplaza por una cadena que indica el idioma de la consulta que se está enviando.<br/>                                                          |
| {inputEncoding}  | Se reemplaza por una cadena (por ejemplo, "UTF-16") que indica la codificación de caracteres de la consulta que se está enviando.<br/>                                |
| OutputEncoding | Se reemplaza por una cadena (como "UTF-16") que indica la codificación de caracteres deseada para la respuesta del servicio Web.<br/>       |



 

### <a name="paged-results"></a>Resultados paginados

Es posible que desee limitar el número de resultados que se devuelven por solicitud. Puede optar por devolver una "página" de los resultados a la vez, o bien para que el proveedor de OpenSearch obtenga páginas de resultados adicionales por número de elemento o número de página. Por ejemplo, si envía veinte resultados por página, la primera página que envíe comienza en el índice de elemento 1 y en la Página 1; la segunda página que envía comienza en el índice de elementos 21 y en la página 2. Puede definir cómo desea que el proveedor de OpenSearch solicite elementos mediante el `{startItem}` `{startPage}` token o en la plantilla de dirección URL.

### <a name="paging-using-the-item-index"></a>Paginación mediante el índice del elemento

Un índice de elemento identifica el primer elemento de resultado de una página de resultados. Si desea que los clientes envíen solicitudes mediante un índice de elemento, puede usar el `{startIndex}` token en el atributo de **plantilla** de elemento **URL** , tal como se muestra en el código siguiente.


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



A continuación, el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) reemplaza el token en la dirección URL con un valor de índice de inicio. La primera solicitud comienza con el primer elemento, como se muestra en el ejemplo siguiente:


```
https://example.com/rss.php?query=frogs&start=1
```



El proveedor de OpenSearch puede obtener elementos adicionales cambiando el `{startIndex}` valor del parámetro y emitiendo una nueva solicitud. El proveedor repite este proceso hasta que obtiene suficientes resultados para satisfacer su límite o alcanza el final de los resultados. El proveedor de OpenSearch examina el número de elementos devueltos por el servicio Web en la primera página de resultados y establece el tamaño de página esperado en ese número. Utiliza ese número para incrementar el `{startIndex}` valor de las solicitudes posteriores. Por ejemplo, si el servicio Web devuelve 20 resultados en la primera solicitud, el proveedor establece el tamaño de página esperado en 20. Para la solicitud siguiente, el proveedor reemplaza `{startIndex}` por el valor de 21 para obtener los 20 elementos siguientes.

> [!Note]  
> Si una página de resultados devuelta por el servicio Web tiene menos elementos que el tamaño de página esperado, el proveedor de OpenSearch supone que ha recibido la última página de resultados y detiene las solicitudes.

 

### <a name="paging-using-the-page-index"></a>Paginación mediante el índice de página

Un índice de página identifica la página de resultados especificada. Si desea que los clientes envíen solicitudes mediante un número de página, puede usar el `{startPage}` token en el atributo de **plantilla** de elemento de **formato de dirección URL** para indicar que, tal y como se muestra en el ejemplo siguiente:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



A continuación, el proveedor de OpenSearch reemplaza el token en la dirección URL con un parámetro de número de página. La primera solicitud comienza con la primera página, como se muestra en el ejemplo siguiente:


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> Si una página de resultados devuelta por el servicio Web tiene menos elementos que el tamaño de página esperado, el proveedor de OpenSearch supone que ha recibido la última página de resultados y detiene las solicitudes.

 

### <a name="page-size"></a>Tamaño de página

Es posible que desee configurar el servicio web para permitir que una solicitud especifique el tamaño de las páginas mediante el uso de algún parámetro en la dirección URL. Se debe especificar una solicitud en el archivo. osdx mediante el `{count}` token, como se indica a continuación:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



Después, el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) puede establecer el tamaño de página deseado, en número de resultados por página, como se muestra en el ejemplo siguiente:


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



De forma predeterminada, el proveedor de OpenSearch realiza solicitudes con un tamaño de página de 50. Si desea un tamaño de página diferente, no proporcione un `{count}` token y, en su lugar, coloque el número deseado directamente en el elemento de **plantilla de dirección URL** .

El proveedor de OpenSearch determina el tamaño de página en función del número de resultados que se devuelven en la primera solicitud. Si la primera página de resultados recibida tiene menos elementos que el número solicitado, el proveedor restablece el tamaño de página para las solicitudes de página posteriores. Si las solicitudes de página posteriores devuelven menos elementos de los solicitados, el proveedor de OpenSearch supone que ha alcanzado el final de los resultados.

## <a name="extended-elements-in-windows-federated-search"></a>Elementos extendidos en la búsqueda federada de Windows

Además de los elementos estándar, la búsqueda federada admite los siguientes elementos extendidos: **MaximumResultCount** y **ResultsProcessing**.

Dado que estos elementos secundarios extendidos no se admiten en la especificación de [OpenSearch](https://github.com/dewitt/opensearch) v 1.1, deben agregarse mediante el siguiente espacio de nombres:


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a>Número máximo de resultados

De forma predeterminada, los conectores de búsqueda se limitan a 100 resultados por consulta de usuario. Este límite se puede personalizar incluyendo el elemento **MaximumResultCount** en el archivo OSD, tal como se muestra en el ejemplo siguiente:


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



En el ejemplo anterior se declara el prefijo `ms-ose` de espacio de nombres en el elemento **OpenSearchDescription** de nivel superior y, a continuación, se usa como prefijo en el nombre del elemento. Esta declaración es necesaria porque no se admite **MaximumResultCount** en la especificación de [OpenSearch](https://github.com/dewitt/opensearch) v 1.1.

### <a name="property-mapping"></a>Asignación de propiedades

Cuando el servicio Web devuelve los resultados como una fuente RSS o Atom, el proveedor de OpenSearch debe asignar los metadatos de los elementos de las fuentes a las propiedades que el shell de Windows puede usar. En la captura de pantalla siguiente se muestra cómo el proveedor de OpenSearch asigna algunos de los elementos RSS predeterminados.

![captura de pantalla que muestra las asignaciones de propiedades integradas de RSS a Windows-Shell](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a>Asignaciones predeterminadas

En la tabla siguiente se enumeran las asignaciones predeterminadas de elementos XML de RSS a las propiedades del sistema de Shell de Windows. Las rutas XML son relativas al elemento Item. El `"media:"` prefijo está definido por el espacio de nombres del [espacio de nombres de búsqueda de Yahoo](https://www.rssboard.org/media-rss) .



| Ruta de acceso XML de RSS                  | Propiedad del shell de Windows (nombre canónico) |
|-------------------------------|-----------------------------------------|
| Link                          | System. ItemUrl                          |
| Title                         | System. ItemName                         |
| Autor                        | System.Author                           |
| pubDate                       | System. DateModified                     |
| Descripción                   | System. autosummary                      |
| Category                      | System.Keywords                         |
| enclosure/@type               | System. MIMEType                         |
| enclosure/@length             | System. Size                             |
| enclosure/@url                | System. ContentUrl                       |
| medio: categoría                | System.Keywords                         |
| media:content/@fileSize       | System. Size                             |
| media:content/@type           | System. MIMEType                         |
| media:content/@url            | System. ContentUrl                       |
| media:group/content/@fileSize | System. Size                             |
| media:group/content/@type     | System. MIMEType                         |
| media:group/content/@url      | System. ContentUrl                       |
| media:thumbnail/@url          | System. ItemThumbnailUrl                 |



 

> [!Note]  
> Además de las asignaciones predeterminadas de elementos RSS o Atom estándar, puede asignar otras propiedades del sistema de Shell de Windows incluyendo elementos XML adicionales en el espacio de nombres de Windows para cada una de las propiedades. También puede asignar elementos de otros espacios de nombres XML existentes, como MediaRSS, iTunes, etc., agregando la asignación de propiedades personalizadas en el archivo. osdx.

 

### <a name="custom-property-mappings"></a>Asignaciones de propiedades personalizadas

Puede personalizar la asignación de elementos de la salida RSS a las propiedades del sistema del shell de Windows especificando la asignación en el archivo. osdx.

La salida RSS especifica:

-   Un espacio de nombres XML y
-   Para cualquier elemento secundario de un elemento, un nombre de elemento que se va a asignar.

El archivo. osdx identifica una propiedad del shell de Windows para cada nombre de elemento de un espacio de nombres. Las asignaciones de propiedad que se definen en el archivo. osdx invalidan las asignaciones predeterminadas, si existen, para las propiedades especificadas.

En el diagrama siguiente se muestra cómo se asigna una extensión RSS a las propiedades de Windows (nombre canónico).

![diagrama que muestra que la combinación del espacio de nombres XML y la ruta XML genera el nombre canónico](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a>Resultados de RSS de ejemplo y asignación de propiedades OSD

La salida RSS de ejemplo siguiente identifica `https://example.com/schema/2009` como el espacio de nombres XML con el prefijo "example". Este prefijo debe aparecer de nuevo antes del elemento de **correo electrónico** .


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



En el siguiente archivo. osdx de ejemplo, el elemento de **correo electrónico** XML se asigna a la propiedad [System. contact. EmailAddress](../properties/props-system-contact-emailaddress.md)del shell de Windows.


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



Hay algunas propiedades que no se pueden asignar porque los valores para ellas se invalidan posteriormente o no se pueden editar. Por ejemplo, [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) o [System. ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) no se puede asignar porque se calculan a partir del valor de dirección URL proporcionado en los elementos del vínculo o del contenedor.

### <a name="thumbnails"></a>Miniaturas

Se pueden proporcionar direcciones URL de imagen en miniatura para cualquier elemento mediante el elemento **media: thumbnail URL = ""** . La solución ideal es de 150 x 150 píxeles. Las miniaturas más grandes admitidas son 256 x 256 píxeles. Proporcionar imágenes más grandes requiere más ancho de banda para que no haya más ventajas para el usuario.

### <a name="open-file-location-context-menu"></a>Abrir el menú contextual de ubicación del archivo

Windows proporciona un menú contextual denominado **Abrir archivo ubicación** para los elementos de resultados. Si el usuario selecciona un elemento de ese menú, se abre la dirección URL "principal" del elemento seleccionado. Si la dirección URL es una dirección URL Web, como `https://...` , el explorador Web se abre y se navega a esa dirección URL. La fuente debe proporcionar una dirección URL personalizada para cada elemento con el fin de asegurarse de que Windows abre una dirección URL válida. Esto puede realizarse incluyendo la dirección URL dentro de un elemento dentro del XML del elemento, como se muestra en el ejemplo siguiente:


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



Si esta propiedad no se establece explícitamente en el XML del elemento, el proveedor de OpenSearch lo establece en la carpeta primaria de la dirección URL del elemento. En el ejemplo anterior, el proveedor de OpenSearch usaría el valor del vínculo y establecería el valor de la propiedad del shell de Windows [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) en `"https://example.com/"` .

### <a name="customize-windows-explorer-views-with-property-description-lists"></a>Personalizar las vistas del explorador de Windows con las listas de descripción de propiedades

Algunos diseños de la vista del explorador de Windows se definen mediante listas de descripción de propiedades o provisores. Un proplist es una lista delimitada por punto y coma de propiedades, como `"prop:System.ItemName; System.Author"` , que se usa para controlar el modo en que los resultados aparecen en el explorador de Windows.

Las áreas de la interfaz de usuario del explorador de Windows que se pueden personalizar mediante el uso de proplists se muestran en la siguiente captura de pantalla:

![captura de pantalla que muestra las áreas de la interfaz de usuario del explorador de Windows que se pueden personalizar mediante el uso de proplists](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

Cada área del explorador de Windows tiene un conjunto asociado de proarchivos, que a su vez se especifican como propiedades. Puede especificar los valores predeterminados para los elementos individuales de los conjuntos de resultados o para todos los elementos de un conjunto de resultados.



| Área de la interfaz de usuario para personalizar               | Propiedad del shell de Windows que implementa la personalización |
|------------------------------------|----------------------------------------------------------|
| Modo de vista de contenido (al buscar) | System. proplist. ContentViewModeForSearch                 |
| Modo de vista de contenido (al examinar)  | System. proplist. ContentViewModeForBrowse                 |
| Modo de vista en mosaico                     | System. proplist. TileInfo                                 |
| Panel de detalles                       | System. proplist. PreviewDetails                           |
| Recuadro informativo (información sobre herramientas de desplazamiento del elemento)     | System. proplist. recuadro informativo                                  |



 

 

**Para especificar un único proplist para un elemento individual:**

1.  En la salida RSS, agregue un elemento personalizado que represente el proplist que desea personalizar. Por ejemplo, en el ejemplo siguiente se establece la lista del panel de detalles:
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  Para aplicar una propiedad a todos los elementos de los resultados de la búsqueda sin modificar la salida RSS, especifique un proplist dentro de un elemento **MS-OSE: PropertyDefaultValues** en el archivo. osdx, tal como se muestra en el ejemplo siguiente:

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a>Diseño de las propiedades del modo de vista de contenido

La lista de propiedades especificadas en los proarchivos **System. proplist. ContentViewModeForSearch** y **System. proplist. ContentViewModeForBrowse** determina lo que se muestra en el modo de vista de contenido. Para obtener más información sobre las listas de propiedades, consulte [proplist](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).

Las propiedades se disponen de acuerdo con los números que se muestran en el patrón de diseño siguiente:

![captura de pantalla que muestra el patrón de diseño predeterminado en la vista de contenido](images/propertiesnumberslayoutpattern.png)

Si usamos la siguiente lista de propiedades,


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



A continuación, vemos la siguiente pantalla:

![captura de pantalla que muestra el diseño de la propiedad de ejemplo.](images/samplepropertylayout.png)

> [!Note]  
> Para mejorar la legibilidad, se deben etiquetar las propiedades que se muestran en la columna situada más a la derecha.

 

### <a name="property-list-flags"></a>Marcas de la lista de propiedades

Solo una de las marcas definidas en la documentación de proplist se aplica a la presentación de los elementos en los diseños del modo de vista de contenido: ` "~"` . En los ejemplos anteriores, la vista del explorador de Windows etiqueta algunas de las propiedades, como `Tags: animals; zoo; lion` . Es el comportamiento predeterminado cuando se especifica una propiedad en la lista. Por ejemplo, el proplist tiene `"System.Author"` que se muestra como `"Authors: value"` . Si desea ocultar la etiqueta de la propiedad, coloque `"~"` delante del nombre de la propiedad. Por ejemplo, si el proplist tiene `"~System.Size"` , la propiedad se muestra como solo un valor, sin la etiqueta.

## <a name="previews"></a>Vistas previas

Cuando el usuario selecciona un elemento de resultados en el explorador de Windows y el panel de vista previa está abierto, se obtiene una vista previa del contenido del elemento.

El contenido que se muestra en la vista previa se especifica mediante una dirección URL, que se determina de la manera siguiente:

1.  Si se establece la propiedad del shell de Windows **System. WebPreviewUrl** para el elemento, use esa dirección URL.
    > [!Note]  
    > La propiedad debe proporcionarse en el RSS con el espacio de nombres del shell de Windows o asignarse explícitamente en el archivo. osdx.

     

2.  En caso contrario, utilice la dirección URL del vínculo en su lugar.

En el diagrama de flujo siguiente se muestra esta lógica.

![diagrama de flujo que muestra cómo el explorador de Windows selecciona la dirección URL que se usará para las versiones de vista previa](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

Es posible usar una dirección URL diferente para la versión preliminar que para el propio elemento. Esto significa que si proporciona direcciones URL diferentes para la dirección URL del vínculo y el contenedor o `media:content URL` , el explorador de Windows utiliza la dirección URL del vínculo para las vistas previas del elemento, pero usa la otra dirección URL para la detección de tipos de archivo, apertura, descarga, etc.

Cómo determina el explorador de Windows qué dirección URL usar:

1.  Si proporciona una asignación a [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), el explorador de Windows usa esa dirección URL
2.  Si no proporciona una asignación, el explorador de Windows identifica si las direcciones URL del vínculo y del contenedor son diferentes. Si es así, el explorador de Windows utiliza la dirección URL del vínculo.
3.  Si las direcciones URL son iguales o solo hay una dirección URL de vínculo, el explorador de Windows analiza el vínculo para buscar el contenedor primario quitando el nombre de archivo de la dirección URL completa.
    > [!Note]  
    > Si reconoce que el análisis de direcciones URL daría como resultado vínculos inactivos para su servicio, debe proporcionar una asignación explícita para la propiedad.

     

## <a name="open-file-location-menu-item"></a>Abrir el elemento de menú Ubicación del archivo

Cuando hace clic con el botón secundario en un elemento, aparece el comando de menú **abrir Ubicación del archivo** . Este comando toma el usuario en el contenedor de la ubicación o de ese elemento. Por ejemplo, en una búsqueda de SharePoint, si se selecciona esta opción para un archivo en una biblioteca de documentos, se abriría la raíz de la biblioteca de documentos en el explorador Web.

Cuando un usuario hace clic en **abrir ubicación de archivos**, el explorador de Windows intenta encontrar un contenedor primario mediante la lógica que se muestra en el siguiente diagrama de flujo:

![diagrama de flujo que muestra cómo el explorador de Windows identifica un contenedor primario](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a>Recursos adicionales

Para obtener información adicional sobre la implementación de la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, consulte "recursos adicionales" en [búsqueda federada en Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introducción con búsqueda federada en Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Conexión del servicio Web en la búsqueda federada de Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitación del almacén de datos en la búsqueda federada de Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Siguientes procedimientos recomendados en la búsqueda federada de Windows](-search-fedsearch-best.md)
</dt> <dt>

[Implementación de conectores de búsqueda en la búsqueda federada de Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
