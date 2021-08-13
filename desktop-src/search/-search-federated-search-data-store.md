---
description: Explica cómo habilitar el acceso al almacén de datos mediante un servicio web OpenSearch y cómo evitar posibles barreras para hacerlo.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Habilitación del almacén de datos en Windows búsqueda federada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26feb231f17dbaacb9656f2ef91e1cdb64bc598831a1e4808327dff7e5787bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456765"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a>Habilitación del almacén de datos en Windows búsqueda federada

Explica cómo habilitar el acceso al almacén de datos mediante un [servicio](https://github.com/dewitt/opensearch) web OpenSearch y cómo evitar posibles barreras para hacerlo.

Este tema se organiza de la siguiente manera:

-   [Condiciones para la aceptación de la solicitud de búsqueda](#conditions-for-search-request-acceptance)
    -   [Sintaxis de consulta admitida](#supported-query-syntax)
    -   [Protocolos de autenticación admitidos](#supported-authentication-protocols)
-   [Envío de consultas y devolución de resultados de búsqueda en RSS o Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [Ejemplo de una salida de fuente RSS](#example-of-an-rss-feed-output)
-   [Asignación automática a Windows shell](#automatic-mapping-to-windows-shell-properties)
-   [Descripción de cómo Mapas de Windows elementos a tipos de archivo](#understanding-how-windows-maps-items-to-file-types)
-   [Evitar posibles barreras para habilitar un almacén de datos](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a>Condiciones para la aceptación de la solicitud de búsqueda

El [OpenSearch](https://github.com/dewitt/opensearch) web que cree en el servidor web **debe cumplir** los dos requisitos siguientes:

-   Poder aceptar una `GET URL` consulta del cliente.
-   Permitir que los términos de búsqueda se inserte en la dirección URL.

    En el ejemplo siguiente se muestra cómo se puede incrustar un término de búsqueda en una dirección URL.

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> La búsqueda federada no admite el envío `POST` de solicitudes a un servicio web.

 

Para obtener más información sobre cómo construir una dirección URL, vea "Parámetros de plantilla de dirección URL" en [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).

### <a name="supported-query-syntax"></a>Sintaxis de consulta admitida

No se espera ninguna sintaxis de consulta específica en Windows 7. El OpenSearch acepta los términos que el usuario escribe en el cuadro de entrada en Windows Explorer y lo codifica en la dirección URL. Lo hace según la plantilla de dirección URL descrita en "Parámetros de plantilla de dirección URL" en Creación de un archivo de descripción de OpenSearch en [Windows búsqueda federada.](-search-federated-search-osdx-file.md)

Los usuarios esperan que los términos independientes se traten como ANDed implícitamente juntos. Por ejemplo, una consulta para "Microsoft Windows" solo debe devolver resultados que contengan "Windows" y "Microsoft".

### <a name="supported-authentication-protocols"></a>Protocolos de autenticación admitidos

Windows Federated Search admite Windows autenticación basada en aplicaciones y puede proporcionar credenciales a los servicios web a través de los protocolos siguientes:

-   NTLM.
-   Kerberos.
-   Básico (solo a través de https).
-   Otros proveedores de soporte técnico de seguridad (SSP) instalados en Windows que proporcionan capacidad de consulta adicional. Consulte la documentación del SDK [de la interfaz SSP](../secauthn/sspi.md) para mantenerse al día de la posible adición de otros SSP.

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Envío de consultas y devolución de resultados de búsqueda en RSS o Atom

El [OpenSearch](https://github.com/dewitt/opensearch) es responsable de asignar los valores de elemento XML a las propiedades del sistema Windows Shell que pueden usar Windows aplicaciones. Pero no está limitado a las asignaciones predeterminadas de elementos ESTÁNDAR RSS o Atom, y puede incluir elementos XML personalizados en el espacio de nombres Windows para cada una de las propiedades. Por ejemplo, puede agregar sus propios elementos XML personalizados dentro del elemento **de** elemento para proporcionar metadatos adicionales a Windows. También puede asignar elementos de otros espacios de nombres XML, como iTunes.

### <a name="example-of-an-rss-feed-output"></a>Ejemplo de una salida de fuente RSS

La siguiente salida de fuente RSS de ejemplo devuelve un elemento.


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



Para obtener información más detallada sobre la asignación de propiedades, vea las secciones "Extended Elements in WIndows Federated Search" y "Custom Property Mappings" en [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).

## <a name="automatic-mapping-to-windows-shell-properties"></a>Asignación automática a Windows shell

Dentro de los elementos de la fuente RSS, puede elegir incluir otros elementos XML que se asignan automáticamente a Windows del sistema shell. Para ello, incluya un elemento denominado después de la propiedad Windows Shell y con el prefijo Windows espacio de nombres del sistema shell. En el ejemplo siguiente se muestra la declaración de espacio de `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` nombres y la inclusión de un elemento para la asignación de propiedades `win:System.Contact.PrimaryEmailAddress` :


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



El prefijo de espacio de nombres que se usa aquí ( `"win"` ) es una sugerencia; puede usar cualquier prefijo. Sin embargo, debe usar los nombres de propiedad Windows Shell exactos y debe incluir el identificador uniforme de recursos (URI) exacto, como se muestra en el ejemplo siguiente:


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



**Acerca de Windows del sistema shell**

Windows define una lista completa de propiedades [del sistema](../properties/props.md) y el formato de tipo de valor necesario para cada propiedad. La documentación de la propiedad Shell de ventana [System.FileExtension,](../properties/props-system-fileextension.md) por ejemplo, especifica que el valor debe contener el punto inicial (".docx" y no "docx").

**Valores de fecha y hora**

El formato de fecha y hora preferido es ISO-8601, como se muestra en el ejemplo siguiente:


```
2008-01-16T 19:20:30:.45+01:00
```



Los desarrolladores de .NET deben usar la clase DateTime con `ToString("R") ` para generar el formato correcto.

Para obtener información más detallada sobre la asignación de propiedades, vea "Elementos extendidos en la búsqueda federada de Windows" en [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).

## <a name="understanding-how-windows-maps-items-to-file-types"></a>Descripción de cómo Mapas de Windows elementos a tipos de archivo

La búsqueda en la interfaz Windows Explorer permite a los usuarios tratar los resultados como archivos cuando un elemento RSS apunta a un archivo almacenado de forma remota. El usuario puede arrastrar y colocar elementos en el escritorio, y la interfaz de usuario de Windows Explorer muestra el icono correcto y proporciona el menú contextual adecuado. Si el elemento RSS no apunta a un archivo almacenado de forma remota, el archivo se trata como un vínculo y los usuarios pueden realizar acciones en él, como crear un acceso directo o abrirlo en el explorador.

En el diagrama de flujo siguiente se muestra Windows determina el tipo de archivo de un elemento.

![diagrama de flujo que muestra las rutas de acceso de un elemento a las decisiones para tratarlo como un elemento de tipo de vínculo web o como un tipo de archivo](images/determineanitemfiletype.png)

El [OpenSearch](https://github.com/dewitt/opensearch) realiza los pasos siguientes para asignar un elemento a un tipo de archivo:

-   Identifique si el elemento debe tratarse como un archivo o un vínculo web.
-   Identifique la extensión de nombre de archivo correcta que se usará.

Por ejemplo, si el elemento tiene una dirección URL de vínculo que usa una ruta de acceso del sistema de archivos (como ), el proveedor de OpenSearch trata el vínculo como un archivo y determina el tipo por la extensión de nombre de archivo utilizada en la ruta `file:///\\server\share\etc\item.ext` de acceso (.ext en este ejemplo). [](https://github.com/dewitt/opensearch)

Si el elemento usa el gabinete RSS estándar o el elemento **media:content de MediaRSS,** el proveedor [de OpenSearch](https://github.com/dewitt/opensearch) asume que el elemento es un archivo e identifica la extensión de nombre de archivo de la siguiente manera:

-   Si la [propiedad System.FileExtension](../properties/props-system-fileextension.md) Windows Shell se ha asignado para el elemento, el proveedor usa esa extensión de nombre de archivo.
-   Si no se ha asignado la propiedad [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell, el proveedor usa el atributo **Type** especificado en el gabinete o elemento content. Este elemento debe contener una `MIMEType` cadena, como `"image/jpeg"` . Si está asociado a una extensión de nombre de archivo registrada en el equipo cliente, el elemento se considera `MIMEType` un archivo de ese tipo. Si no está asociado a una extensión de nombre de archivo registrada en el equipo cliente, el elemento `MIMEType` se trata como un tipo de vínculo web. El [OpenSearch](https://github.com/dewitt/opensearch) no intenta analizar el atributo **Url** para buscar la extensión de nombre de archivo.
-   Si está asociado a una extensión de nombre de archivo registrada en el equipo cliente, el proveedor determina si la extensión de nombre de archivo es un tipo de archivo web conocido `MIMEType` (.htm, .html, .asp, .aspx, .php, .mq, .stm). Si es así, el tipo de archivo se considera un tipo de vínculo web; de lo contrario, se considera un tipo de archivo. Por ejemplo, si está asociado .htm la extensión de nombre de archivo, ese elemento se considera un vínculo web en lugar de como un tipo .htm `MIMEType "text/html"` archivo.

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a>Evitar posibles barreras para habilitar un almacén de datos

Algunos almacenes de datos no proporcionan un servicio web [compatible OpenSearch,](https://github.com/dewitt/opensearch)pero todavía se pueden conectar a Windows búsqueda federada. Estos almacenes de datos incluyen:

-   Índices remotos con métodos de autenticación que no se admiten Windows 7 Federated Search.

    Algunos ejemplos son la autenticación basada en formularios y otros métodos de autenticación personalizados.

-   Si un almacén público de gran valor tiene API web públicas, cualquiera puede escribir otro servicio web que sea compatible con OpenSearch y llame a esas API en segundo plano. [](https://github.com/dewitt/opensearch)

    Algunos ejemplos son la Biblioteca del Congreso y las bases de datos de investigación médica.

-   Almacenes de datos o índices empresariales propietarios y almacenes de administración de contenido heredados para los que podría ser imposible implementar un front-end.

Sin embargo, hay alternativas que pueden evitar barreras para habilitar un almacén de datos. Estas son algunas de estas alternativas:

**Para escribir un servicio web de intermediario cuando no se puede modificar el servicio web para el origen de datos existente, o el servicio web proporciona una API personalizada:**

1.  Escriba un servicio web de intermediario que pueda aceptar una consulta Windows 7.
2.  Conectar al origen de datos y recupere los resultados de la consulta.
3.  Vuelva a formatear los resultados en formato RSS o Atom.
4.  Devuelve los resultados al Windows 7.
5.  Tenga en cuenta que para los servicios de datos empresariales y muchos servicios de datos de Internet, es posible que tenga que pasar las credenciales de usuario a través en nombre del servicio web para realizar el recorte de resultados en función de los permisos del usuario.

**Para usar un motor de búsqueda existente cuando no se puede habilitar un almacén de datos público:**

1.  Use un motor de búsqueda público que ya [admita OpenSearch](https://github.com/dewitt/opensearch) con RSS. Para ello, proporcione a los usuarios un archivo .osdx que tenga una plantilla de dirección URL que restrinja los resultados solo a los del dominio específico.
2.  Vea el ejemplo siguiente de una [OpenSearch](https://github.com/dewitt/opensearch) para buscar solo el contenido de la Ayuda para Windows mediante una consulta en live.com.

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

    

**Para usar un servidor de indexación existente que admita OpenSearch cuando no se puedan habilitar los índices o almacenes de datos empresariales propietarios:**

1.  Seleccione un servidor de indexación existente que [admita OpenSearch](https://github.com/dewitt/opensearch) indexar el contenido, como SharePoint Search Server.
2.  Cree un archivo .osdx que restrinja los resultados del índice SharePoint a solo los del servidor mediante su sintaxis KeyWord dentro de la plantilla de dirección URL.

**Para escribir un almacén de datos del lado cliente si una solución solo del lado servidor no funciona:**

1.  Escriba un origen de datos [OpenSearch](https://github.com/dewitt/opensearch) cliente que se encuentra entre el proveedor Windows [OpenSearch](https://github.com/dewitt/opensearch) y el origen de datos externo.
2.  Use la API de interfaz [IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) en el SDK de Windows para crear un archivo .searchconnector-ms configurado correctamente a través del cual Windows Explorer puede llamar a la implementación con los parámetros de consulta. A continuación, la implementación puede devolver resultados con formato RSS o Atom. Esto permite a la implementación proporcionar una interfaz de usuario de autenticación personalizada y conectarse al origen de datos mediante su API propietaria.

> [!Note]  
> Al abrir un archivo .osdx, se crea un archivo .searchconnector-ms (conector de búsqueda) en el directorio %userprofile%/searches y se coloca un vínculo a él en el directorio %userprofile%/links.

 

## <a name="additional-resources"></a>Recursos adicionales

Para obtener información adicional sobre cómo implementar la federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, vea "Recursos adicionales" en Búsqueda federada [en Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Tareas iniciales con la búsqueda federada en Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Conexión del servicio web en Windows búsqueda federada](-search-federated-search-web-service.md)
</dt> <dt>

[Crear un archivo OpenSearch descripción en Windows búsqueda federada](-search-federated-search-osdx-file.md)
</dt> <dt>

[Seguir los procedimientos recomendados en Windows búsqueda federada](-search-fedsearch-best.md)
</dt> <dt>

[Implementación de conectores de búsqueda en Windows búsqueda federada](-search-federated-search-deploying.md)
</dt> </dl>

 

 
