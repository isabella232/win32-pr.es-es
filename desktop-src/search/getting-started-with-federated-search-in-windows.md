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
# <a name="getting-started-with-federated-search-in-windows"></a>Tareas iniciales con la búsqueda federada en Windows

La compatibilidad de Windows 7 con la federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch permite a los usuarios acceder a sus datos remotos e interactuar con ellos desde dentro Explorador de Windows. Puede crear un almacén de datos basado en web que se pueda buscar mediante la búsqueda federada de Windows y habilitar la integración enriquecida de los orígenes de datos remotos con Explorador de Windows sin tener que escribir ni implementar ningún código del lado cliente de Windows.

Este tema se organiza de la siguiente manera:

-   [¿Qué es la búsqueda federada?](#what-is-federated-search)
-   [Pasos para compilar la búsqueda federada](#steps-for-building-federated-search)
-   [Funcionamiento de la búsqueda federada](#how-federated-search-works)
-   [Envío de consultas y devolución de resultados de búsqueda en RSS o Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [Ejemplos de búsqueda federada](#federated-search-examples)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="what-is-federated-search"></a>¿Qué es la búsqueda federada?

Windows 7 admite la conexión de orígenes externos al cliente de Windows a través del [protocolo OpenSearch.](https://github.com/dewitt/opensearch) Esto permite a los usuarios buscar en un almacén de datos remoto y ver los resultados desde dentro Explorador de Windows. El estándar [OpenSearch](https://github.com/dewitt/opensearch) v1.1 define formatos de archivo simples que se pueden usar para describir cómo un cliente debe consultar el servicio web para el almacén de datos y cómo el servicio debe devolver los resultados que el cliente debe representar. La búsqueda federada de Windows se conecta a los servicios web que reciben consultas [de OpenSearch](https://github.com/dewitt/opensearch) y devuelve resultados en formato RSS o ATOM XML.

En la siguiente captura de pantalla se muestran los resultados de búsqueda obtenidos después de buscar de forma remota en un sitio de SharePoint.

![captura de pantalla que muestra los resultados de la búsqueda desde un sitio de SharePoint como se muestra en el Explorador de Windows](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a>Pasos para compilar la búsqueda federada

Para compilar la búsqueda federada, realice los pasos siguientes:

1.  Habilite la búsqueda del almacén de datos desde Explorador de Windows proporcionando un servicio web compatible con [OpenSearch](https://github.com/dewitt/opensearch)que pueda devolver resultados en formato RSS o Atom.
2.  Cree un archivo de descripción de OpenSearch (.osdx) que describa cómo conectarse al servicio web y cómo asignar elementos personalizados en RSS o ATOM XML.
3.  Implemente los conectores de búsqueda en equipos cliente windows con un archivo .osdx.

En el diagrama siguiente se muestran los pasos para crear búsquedas federadas.

![diagrama del proceso de creación de búsqueda federada](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a>Funcionamiento de la búsqueda federada

La comunicación entre Explorador de Windows y el servicio web [de OpenSearch](https://github.com/dewitt/opensearch) se realiza a través de la capa de datos de Windows. La capa de datos de Windows puede comunicarse con diferentes tipos de almacenes de datos a través de proveedores de la Tienda Windows. Cada proveedor se especializa en comunicarse con almacenes de datos que admiten un protocolo determinado y tienen funcionalidades específicas. Por ejemplo, en la ilustración siguiente se explica cómo el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) se comunica con los almacenes de datos que proporcionan un servicio web que admite el [estándar OpenSearch.](https://github.com/dewitt/opensearch)

![diagrama que muestra la comunicación desde el Explorador de Windows en el cliente a través del almacén de datos opensearch en el servidor remoto](images/windowssearchfederationfunctionality.png)

Para permitir que el almacén de datos admita la búsqueda federada en Windows 7, debe realizar una serie de tareas. En la tabla siguiente se enumeran las tareas para habilitar el almacén de datos, lo que se necesita para realizar cada tarea y dónde encontrar documentación.



| Tarea                                                                                                     | Requisito                                                                                                                                                                                            | Documentación                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Habilite el almacén de datos para que lo busquen Explorador de Windows.<br/>                                    | Cree un servicio web compatible con OpenSearch.<br/> Cree un archivo de descripción de OpenSearch (.osdx).<br/>                                                                                       | [Conexión del servicio web en Windows Federated Search](-search-federated-search-web-service.md)<br/> [Habilitación del almacén de datos en Windows Federated Search](-search-federated-search-data-store.md)<br/> |
| Implemente activamente el servicio web para los usuarios de una empresa.<br/>                               | Proporcione un archivo .osdx a los usuarios, cópielo localmente y haga que sea accesible para el usuario a través de un acceso directo.<br/>                                                                                     | [Implementación de conectores de búsqueda en Windows Federated Search](-search-federated-search-deploying.md)<br/>                                                                                                              |
| Enumerar los resultados de la búsqueda Explorador de Windows respuesta a una consulta.<br/>                          | Implemente un servicio web que acepte una cadena de consulta y devuelva resultados en formato RSS o Atom.<br/>                                                                                              | [Conexión del servicio web en Windows Federated Search](-search-federated-search-web-service.md)<br/>                                                                                                            |
| Permitir que los usuarios agreguen el almacén de datos a sus Explorador de Windows.<br/>                                | Cree un archivo .osdx y proporcionelo a los usuarios.<br/>                                                                                                                                           | [Habilitación del almacén de datos en Windows Federated Search](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Muestre los elementos como elementos similares a archivos en Explorador de Windows.<br/>                                    | Devolver una dirección URL al archivo o flujo de contenido mediante elementos **enclosure** o **media:content**<br/> Proporcione una extensión de nombre de archivo o un tipo MIME que reconozca el equipo cliente.<br/> | [Habilitación del almacén de datos en Windows Federated Search](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Mostrar propiedades personalizadas en Explorador de Windows, más allá de las definidas en estándares RSS o Atom.<br/> | Proporcione metadatos adicionales mediante otro espacio de nombres XML en la salida RSS/Atom.<br/> Agregue un mapa de propiedades al archivo .osdx.<br/>                                                       | [Creación de un archivo de descripción de OpenSearch en La búsqueda federada de Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Personalice las propiedades que se muestran para los elementos de Explorador de Windows.<br/>               | Agregue asignaciones proplist al archivo .osdx.<br/>                                                                                                                                                   | [Creación de un archivo de descripción de OpenSearch en La búsqueda federada de Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Mostrar una vista de página web personalizada de los elementos en el panel de vista previa.<br/>                              | Devuelve distintos valores de vínculo y alojamiento.<br/> Asigne un valor de dirección URL a **la propiedad System.WebPreviewUrl** del Shell de Windows.<br/>                                                               | [Creación de un archivo de descripción de OpenSearch en La búsqueda federada de Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Muestre un botón de la barra de comandos Explorador de Windows que revierte la consulta al sitio web.<br/>   | Proporcione una `Url format="text/html"` plantilla en el archivo .osdx.<br/>                                                                                                                              | [Creación de un archivo de descripción de OpenSearch en La búsqueda federada de Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Envío de consultas y devolución de resultados de búsqueda en RSS o Atom

Cuando el usuario escriba un término en el cuadro de búsqueda de la esquina superior derecha de Explorador de Windows, la consulta se envía al proveedor [de OpenSearch,](https://github.com/dewitt/opensearch) que envía la consulta al almacén de datos remoto. El servicio web remoto responde a la consulta proporcionando resultados en un documento XML, normalmente denominado fuente, en uno de los dos formatos admitidos (RSS o Atom). Cada elemento de resultado de la fuente incluye elementos secundarios XML para representar o describir metadatos de elementos, como el título, la dirección URL, la descripción, la imagen en miniatura, etc. El [proveedor de OpenSearch](https://github.com/dewitt/opensearch) es responsable de asignar los valores de elemento XML a las propiedades del sistema de Windows Shell que pueden usar las aplicaciones de Windows.

## <a name="federated-search-examples"></a>Ejemplos de búsqueda federada

El siguiente archivo de descripción de OpenSearch (.osdx) de ejemplo consta de elementos y , que son los elementos secundarios mínimos necesarios para conectar un almacén de datos externo al cliente de Windows a través del protocolo `ShortName` `Url` OpenSearch.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



En el ejemplo siguiente se muestra cómo hacer que un almacén de datos habilitado para web pueda realizar búsquedas en formato RSS y cómo especificar que se devuelva un elemento de búsqueda:


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



En el ejemplo siguiente se muestra cómo asignar propiedades a las propiedades predeterminadas del sistema para que los elementos mostrados se ordenan y agrupan:


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



En el ejemplo siguiente se muestra cómo agregar una presentación de imagen en miniatura a cada elemento de Explorador de Windows:


```
<media:thumbnail>    
```



## <a name="additional-resources"></a>Recursos adicionales

Para obtener información adicional sobre cómo implementar la federación de búsqueda en almacenes de datos remotos mediante tecnologías OpenSearch en Windows 7 y versiones posteriores, vea "Recursos adicionales" en Búsqueda federada [en Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Conexión del servicio web en Windows Federated Search](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitación del almacén de datos en Windows Federated Search](-search-federated-search-data-store.md)
</dt> <dt>

[Creación de un archivo de descripción de OpenSearch en La búsqueda federada de Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Procedimientos recomendados siguientes en la búsqueda federada de Windows](-search-fedsearch-best.md)
</dt> <dt>

[Implementación de conectores de búsqueda en Windows Federated Search](-search-federated-search-deploying.md)
</dt> </dl>

 

 




