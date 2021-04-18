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
# <a name="enabling-your-data-store-in-windows-federated-search"></a>Habilitación del almacén de datos en la búsqueda federada de Windows

Explica cómo habilitar el acceso al almacén de datos a través de un servicio Web de [OpenSearch](https://github.com/dewitt/opensearch) y cómo evitar posibles barreras para hacerlo.

Este tema se organiza de la siguiente manera:

-   [Condiciones para la aceptación de la solicitud de búsqueda](#conditions-for-search-request-acceptance)
    -   [Sintaxis de consulta admitida](#supported-query-syntax)
    -   [Protocolos de autenticación admitidos](#supported-authentication-protocols)
-   [Enviar consultas y devolver resultados de búsqueda en RSS o Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [Ejemplo de una salida de fuente RSS](#example-of-an-rss-feed-output)
-   [Asignación automática a las propiedades del shell de Windows](#automatic-mapping-to-windows-shell-properties)
-   [Descripción de cómo Windows asigna elementos a tipos de archivo](#understanding-how-windows-maps-items-to-file-types)
-   [Evitar posibles barreras para habilitar un almacén de datos](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a>Condiciones para la aceptación de la solicitud de búsqueda

El servicio Web de [OpenSearch](https://github.com/dewitt/opensearch) que cree en el servidor Web **debe** cumplir los dos requisitos siguientes:

-   Poder aceptar una `GET URL` consulta del cliente.
-   Permite que los términos de búsqueda se incrusten en la dirección URL.

    En el ejemplo siguiente se muestra cómo se puede incrustar un término de búsqueda en una dirección URL.

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> La búsqueda federada no admite `POST` el envío de solicitudes a un servicio Web.

 

Para obtener más información sobre cómo construir una dirección URL, vea "parámetros de plantilla de dirección URL" en [creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md).

### <a name="supported-query-syntax"></a>Sintaxis de consulta admitida

No se espera ninguna sintaxis de consulta específica en Windows 7. El proveedor de OpenSearch acepta cualquier término que el usuario escriba en el cuadro de entrada en el explorador de Windows y lo codifica en la dirección URL. Lo hace según la plantilla de dirección URL que se describe en "parámetros de plantilla de dirección URL" en [creación de un archivo de descripción de OpenSearch en la búsqueda federada de Windows](-search-federated-search-osdx-file.md).

Los usuarios esperan que los términos independientes se traten conjuntamente como intercadenas de forma implícita. Por ejemplo, una consulta de "Microsoft Windows" solo debe devolver resultados que contengan "Windows" y "Microsoft".

### <a name="supported-authentication-protocols"></a>Protocolos de autenticación admitidos

Windows Federated Search admite la autenticación basada en Windows y puede proporcionar credenciales a los servicios web a través de los protocolos siguientes:

-   NTLM.
-   Kerberos.
-   Básico (solo a través de HTTPS).
-   Otros proveedores de compatibilidad para seguridad (SSP) instalados en Windows que proporcionan capacidad de consulta adicional. Consulte la documentación del SDK de la [interfaz SSP](../secauthn/sspi.md) para mantenerse al día de la posible adición de otros SSP.

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Enviar consultas y devolver resultados de búsqueda en RSS o Atom

El proveedor de [OpenSearch](https://github.com/dewitt/opensearch) es responsable de asignar los valores del elemento XML a las propiedades del sistema del shell de Windows que pueden usar las aplicaciones de Windows. Pero no se limita a las asignaciones predeterminadas de elementos RSS o Atom estándar, y puede incluir elementos XML personalizados en el espacio de nombres de Windows para cada una de las propiedades. Por ejemplo, puede agregar sus propios elementos XML personalizados dentro del elemento **Item** para proporcionar metadatos adicionales a Windows. También puede asignar elementos de otros espacios de nombres XML, como iTunes.

### <a name="example-of-an-rss-feed-output"></a>Ejemplo de una salida de fuente RSS

El siguiente ejemplo de salida de fuente RSS devuelve un elemento.


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



Para obtener información más detallada sobre la asignación de propiedades, consulte las secciones "elementos extendidos en la búsqueda federada de WIndows" y "asignaciones de propiedades personalizadas" en [creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md).

## <a name="automatic-mapping-to-windows-shell-properties"></a>Asignación automática a las propiedades del shell de Windows

Dentro de los elementos de la fuente RSS, puede incluir otros elementos XML que se asignan automáticamente a las propiedades del sistema del shell de Windows. Para ello, incluya un elemento con el nombre de la propiedad del shell de Windows y el prefijo del espacio de nombres System del shell de Windows. En el ejemplo siguiente se muestra la declaración de espacio de nombres `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` y la inclusión de un elemento para la asignación de propiedades `win:System.Contact.PrimaryEmailAddress` :


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



El prefijo de espacio de nombres usado aquí ( `"win"` ) es una sugerencia; puede usar cualquier prefijo. Sin embargo, debe usar los nombres de propiedad del shell de Windows exactos y debe incluir el identificador uniforme de recursos (URI) exacto, tal como se muestra en el ejemplo siguiente:


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



**Acerca de las propiedades del sistema Shell de Windows**

Windows define una lista completa de [propiedades del sistema](../properties/props.md) y el formato de tipo de valor necesario para cada propiedad. La documentación de la propiedad del shell de la ventana [System. FileExtension](../properties/props-system-fileextension.md) , por ejemplo, especifica que el valor debe contener el punto inicial (". docx" y no "docx").

**Valores de fecha y hora**

El formato de fecha y hora preferido es ISO-8601, como se muestra en el ejemplo siguiente:


```
2008-01-16T 19:20:30:.45+01:00
```



Los desarrolladores de .NET deben usar la clase DateTime con `ToString("R") ` para generar el formato correcto.

Para obtener información más detallada sobre la asignación de propiedades, consulte "elementos extendidos en la búsqueda federada de Windows" en [creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md).

## <a name="understanding-how-windows-maps-items-to-file-types"></a>Descripción de cómo Windows asigna elementos a tipos de archivo

La búsqueda en la interfaz de usuario del explorador de Windows permite a los usuarios tratar los resultados como archivos cuando un elemento RSS señala a un archivo almacenado de forma remota. El usuario puede arrastrar y colocar elementos en el escritorio, y la interfaz de usuario del explorador de Windows muestra el icono correcto y proporciona el menú contextual adecuado. Si el elemento RSS no apunta a un archivo almacenado de forma remota, el archivo se trata como un vínculo y los usuarios pueden realizar acciones en él, como crear un acceso directo o abrirlo en el explorador.

En el diagrama de flujo siguiente se muestra cómo Windows determina el tipo de archivo de un elemento.

![diagrama de flujo que muestra las rutas de acceso de un elemento a decisiones para tratarlo como un elemento de tipo de vínculo Web o como un tipo de archivo](images/determineanitemfiletype.png)

El proveedor de [OpenSearch](https://github.com/dewitt/opensearch) realiza los pasos siguientes para asignar un elemento a un tipo de archivo:

-   Identifique si el elemento se debe tratar como un archivo o como un vínculo Web.
-   Identifique la extensión de nombre de archivo correcta que se va a usar.

Por ejemplo, si el elemento tiene una dirección URL de vínculo que usa una ruta de acceso del sistema de archivos (como `file:///\\server\share\etc\item.ext` ), el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) trata el vínculo como un archivo y determina el tipo mediante la extensión de nombre de archivo usada en la ruta de acceso (. ext en este ejemplo).

Si el elemento utiliza el elemento contenedor de RSS estándar o **MediaRSS: Content** , el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) supone que el elemento es un archivo e identifica la extensión de nombre de archivo de la siguiente manera:

-   Si la propiedad del shell de Windows [System. FileExtension](../properties/props-system-fileextension.md) se ha asignado para el elemento, el proveedor utiliza esa extensión de nombre de archivo.
-   Si no se ha asignado la propiedad del shell de Windows [System. FileExtension](../properties/props-system-fileextension.md) , el proveedor usa el atributo **Type** especificado en el contenedor o el elemento de contenido. Este elemento debe contener una `MIMEType` cadena, como `"image/jpeg"` . Si `MIMEType` está asociado a una extensión de nombre de archivo que está registrada en el equipo cliente, el elemento se considera como un archivo de ese tipo. Si el `MIMEType` no está asociado a una extensión de nombre de archivo registrada en el equipo cliente, el elemento se trata como un tipo de vínculo Web. El proveedor de [OpenSearch](https://github.com/dewitt/opensearch) no intenta analizar el atributo de **dirección URL** para buscar la extensión de nombre de archivo.
-   Si el `MIMEType` está asociado a una extensión de nombre de archivo que está registrada en el equipo cliente, el proveedor determina si la extensión de nombre de archivo es un tipo de archivo Web conocido (. htm,. html,. asp,. aspx,. php,. SWF,. STM). Si es así, el tipo de archivo se considera un tipo de vínculo Web; de lo contrario, se considera como un tipo de archivo. Por ejemplo, si `MIMEType "text/html"` está asociado con la extensión de nombre de archivo. htm, ese elemento se considera un vínculo Web en lugar de un tipo de archivo. htm.

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a>Evitar posibles barreras para habilitar un almacén de datos

Algunos almacenes de datos no proporcionan un servicio Web compatible con [OpenSearch](https://github.com/dewitt/opensearch), pero todavía pueden estar conectados a la búsqueda federada de Windows. Estos almacenes de datos incluyen:

-   Índices remotos con métodos de autenticación que no se admiten en la búsqueda federada de Windows 7.

    Algunos ejemplos son la autenticación basada en formularios y otros métodos de autenticación personalizados.

-   Si un almacén público de alto valor tiene API web públicas, cualquier usuario puede escribir otro servicio Web compatible con [OpenSearch](https://github.com/dewitt/opensearch)y llama a esas API en segundo plano.

    Algunos ejemplos son la biblioteca de las bases de datos del Congreso y de investigación médica.

-   Almacenes de datos empresariales de propiedad o índices, y almacenes de administración de contenido heredados, para los que es posible que no se pueda implementar un front-end.

Sin embargo, hay alternativas que pueden evitar barreras para habilitar un almacén de datos. A continuación se muestran algunas de esas alternativas:

**Para escribir un servicio Web de intermediario intermedio cuando no se puede modificar el servicio web para el origen de datos existente, o el servicio web proporciona una API personalizada:**

1.  Escriba un servicio web central de Man que pueda aceptar una consulta de Windows 7.
2.  Conéctese al origen de datos y recupere los resultados de la consulta.
3.  Vuelva a dar formato a los resultados en formato RSS o Atom.
4.  Devuelva los resultados al cliente de Windows 7.
5.  Tenga en cuenta que para los servicios de datos empresariales y muchos servicios de datos de Internet, es posible que tenga que pasar las credenciales de usuario mediante en nombre del servicio web para realizar el recorte de resultados en función de los permisos del usuario.

**Para usar un motor de búsqueda existente cuando no se puede habilitar un almacén de datos público:**

1.  Use un motor de búsqueda público que ya sea compatible con [OpenSearch](https://github.com/dewitt/opensearch) con RSS. Puede hacerlo si proporciona a los usuarios un archivo. osdx con una plantilla de dirección URL que restringe los resultados solo a los de su dominio específico.
2.  Vea el ejemplo siguiente de una descripción de [OpenSearch](https://github.com/dewitt/opensearch) para buscar solo el contenido de la ayuda de Windows mediante una consulta en Live.com.

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

    

**Para usar un servidor de indexación existente que admita OpenSearch cuando no pueda habilitar los índices o almacenes de datos empresariales de su propiedad:**

1.  Seleccione un servidor de indexación existente que admita [OpenSearch](https://github.com/dewitt/opensearch) para indizar el contenido, como el servidor de búsqueda de SharePoint.
2.  Cree un archivo. osdx que restrinja los resultados del índice de SharePoint a solo los del servidor mediante el uso de su sintaxis de palabra clave dentro de la plantilla de dirección URL.

**Para escribir un almacén de datos del lado cliente si una solución solo del servidor no funciona:**

1.  Escribir un origen de datos de [OpenSearch](https://github.com/dewitt/opensearch) de cliente que se encuentre entre el proveedor de Windows [OpenSearch](https://github.com/dewitt/opensearch) y el origen de datos externo.
2.  Use la API de la [interfaz IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) en la Windows SDK para crear un archivo. searchconnector-MS configurado correctamente a través del cual el explorador de Windows puede llamar a su implementación con los parámetros de la consulta. A continuación, la implementación puede devolver resultados con formato RSS o Atom. Esto permite que la implementación proporcione una interfaz de usuario de autenticación personalizada y que se conecte al origen de datos mediante su propia API.

> [!Note]  
> Al abrir un archivo. osdx, se crea un archivo. searchconnector-MS (conector de búsqueda) en el directorio% userprofile%/searches y se le coloca un vínculo en el directorio% userprofile%/links

 

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

[Creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md)
</dt> <dt>

[Siguientes procedimientos recomendados en la búsqueda federada de Windows](-search-fedsearch-best.md)
</dt> <dt>

[Implementación de conectores de búsqueda en la búsqueda federada de Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
