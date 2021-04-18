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
# <a name="getting-started-with-federated-search-in-windows"></a>Introducción con búsqueda federada en Windows

Compatibilidad de Windows 7 con la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch permite a los usuarios tener acceso a sus datos remotos e interactuar con ellos desde el explorador de Windows. Puede crear un almacén de datos basado en Web en el que se pueda buscar mediante la búsqueda federada de Windows y habilitar la integración enriquecida de los orígenes de datos remotos con el explorador de Windows sin tener que escribir ni implementar ningún código del lado cliente de Windows.

Este tema se organiza de la siguiente manera:

-   [¿Qué es la búsqueda federada?](#what-is-federated-search)
-   [Pasos para crear la búsqueda federada](#steps-for-building-federated-search)
-   [Cómo funciona la búsqueda federada](#how-federated-search-works)
-   [Enviar consultas y devolver resultados de búsqueda en RSS o Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [Ejemplos de búsqueda federada](#federated-search-examples)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="what-is-federated-search"></a>¿Qué es la búsqueda federada?

Windows 7 admite la conexión de orígenes externos al cliente de Windows a través del protocolo [OpenSearch](https://github.com/dewitt/opensearch) . Esto permite a los usuarios buscar en un almacén de datos remoto y ver los resultados desde el explorador de Windows. El estándar de [OpenSearch](https://github.com/dewitt/opensearch) v 1.1 define formatos de archivo simples que se pueden usar para describir cómo un cliente debe consultar el servicio web para el almacén de datos y cómo el servicio debe devolver los resultados que el cliente va a representar. Windows Federated Search se conecta a los servicios web que reciben consultas de [OpenSearch](https://github.com/dewitt/opensearch) y devuelve los resultados en formato XML de RSS o Atom.

En la captura de pantalla siguiente se muestran los resultados de la búsqueda obtenidos después de buscar un sitio de SharePoint de forma remota.

![captura de pantalla que muestra los resultados de la búsqueda desde un sitio de SharePoint, tal como se muestra en el explorador de Windows](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a>Pasos para crear la búsqueda federada

Para generar la búsqueda federada, realice los pasos siguientes:

1.  Habilite la búsqueda en el almacén de datos desde el explorador de Windows proporcionando un servicio Web compatible con [OpenSearch](https://github.com/dewitt/opensearch)que puede devolver resultados en formato RSS o Atom.
2.  Cree un archivo de descripción de OpenSearch (. osdx) que describa cómo conectarse al servicio Web y cómo asignar cualquier elemento personalizado en el XML de RSS o Atom.
3.  Implemente los conectores de búsqueda en los equipos cliente de Windows con un archivo. osdx.

En el diagrama siguiente se muestran los pasos para crear la búsqueda federada.

![diagrama del proceso de creación de una búsqueda federada](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a>Cómo funciona la búsqueda federada

La comunicación entre el explorador de Windows y el servicio Web de [OpenSearch](https://github.com/dewitt/opensearch) se realiza a través de la capa de datos de Windows. El nivel de datos de Windows puede comunicarse con distintos tipos de almacenes de datos a través de los proveedores de la tienda Windows. Cada proveedor se especializa en la comunicación con almacenes de datos que admiten un protocolo determinado y tienen funciones específicas. Por ejemplo, en la siguiente ilustración se SOWS la forma en que el proveedor de [OpenSearch](https://github.com/dewitt/opensearch) se comunica con almacenes de datos que proporcionan un servicio Web que admite el estándar de [OpenSearch](https://github.com/dewitt/opensearch) .

![diagrama que muestra la comunicación desde el explorador de Windows en el cliente a través del almacén de datos de OpenSearch en el servidor remoto](images/windowssearchfederationfunctionality.png)

Para habilitar el almacén de datos para que admita la búsqueda federada en Windows 7, debe realizar una serie de tareas. En la tabla siguiente se enumeran las tareas para habilitar el almacén de datos, lo que se necesita para realizar cada tarea y dónde encontrar la documentación.



| Tarea                                                                                                     | Requisito                                                                                                                                                                                            | Documentación                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Permite que el explorador de Windows busque en el almacén de datos.<br/>                                    | Cree un servicio Web compatible con OpenSearch.<br/> Cree un archivo de descripción de OpenSearch (. osdx).<br/>                                                                                       | [Conexión del servicio Web en la búsqueda federada de Windows](-search-federated-search-web-service.md)<br/> [Habilitación del almacén de datos en la búsqueda federada de Windows](-search-federated-search-data-store.md)<br/> |
| Implemente activamente el servicio Web en los usuarios de una empresa.<br/>                               | Proporcione un archivo. osdx a los usuarios, cópielo localmente y haga que sea accesible para el usuario a través de un acceso directo.<br/>                                                                                     | [Implementación de conectores de búsqueda en la búsqueda federada de Windows](-search-federated-search-deploying.md)<br/>                                                                                                              |
| Enumerar los resultados de la búsqueda en el explorador de Windows como respuesta a una consulta.<br/>                          | Implemente un servicio Web que acepte una cadena de consulta y devuelva resultados en formato RSS o Atom.<br/>                                                                                              | [Conexión del servicio Web en la búsqueda federada de Windows](-search-federated-search-web-service.md)<br/>                                                                                                            |
| Permitir a los usuarios agregar el almacén de datos al explorador de Windows.<br/>                                | Cree un archivo. osdx y proporcione a los usuarios.<br/>                                                                                                                                           | [Habilitación del almacén de datos en la búsqueda federada de Windows](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Mostrar los elementos como elementos de tipo archivo en el explorador de Windows.<br/>                                    | Devolver una dirección URL al archivo o la secuencia de contenido mediante los elementos de **contenedor** o **multimedia: contenido**<br/> Proporcione una extensión de nombre de archivo o un tipo MIME que el equipo cliente reconozca.<br/> | [Habilitación del almacén de datos en la búsqueda federada de Windows](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Mostrar propiedades personalizadas en el explorador de Windows, más allá de las definidas en los estándares RSS o Atom.<br/> | Proporcione metadatos adicionales mediante el uso de otro espacio de nombres XML en la salida RSS/Atom.<br/> Agregue una asignación de propiedad al archivo. osdx.<br/>                                                       | [Creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Personalizar las propiedades que se muestran para los elementos en el explorador de Windows.<br/>               | Agregue asignaciones de proplist al archivo. osdx.<br/>                                                                                                                                                   | [Creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Mostrar una vista de página web personalizada de los elementos en el panel de vista previa.<br/>                              | Devolver valores de vínculo y de contenedor distintos.<br/> Asigne un valor de dirección URL a la propiedad del shell de Windows **System. WebPreviewUrl** .<br/>                                                               | [Creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Mostrar un botón de la barra de comandos en el explorador de Windows que revierta la consulta en el sitio Web.<br/>   | Proporcione una `Url format="text/html"` plantilla en el archivo. osdx.<br/>                                                                                                                              | [Creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Enviar consultas y devolver resultados de búsqueda en RSS o Atom

Cuando el usuario escribe un término en el cuadro de búsqueda en la esquina superior derecha del explorador de Windows, la consulta se envía al proveedor de [OpenSearch](https://github.com/dewitt/opensearch) , que, a continuación, envía la consulta al almacén de datos remoto. El servicio Web remoto responde a la consulta proporcionando los resultados en un documento XML, normalmente denominado fuente, en uno de los dos formatos admitidos (RSS o Atom). Cada elemento de resultado de la fuente incluye elementos secundarios XML para representar o describir metadatos de elementos, como el título, la dirección URL, la descripción, la imagen en miniatura, etc. El proveedor de [OpenSearch](https://github.com/dewitt/opensearch) es responsable de asignar los valores del elemento XML a las propiedades del sistema del shell de Windows que pueden usar las aplicaciones de Windows.

## <a name="federated-search-examples"></a>Ejemplos de búsqueda federada

En el ejemplo siguiente, el archivo de descripción de OpenSearch (. osdx) consta de los `ShortName` `Url` elementos y, que son los elementos secundarios mínimos necesarios para conectar un almacén de datos externo al cliente de Windows a través del protocolo OpenSearch.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



En el ejemplo siguiente se muestra cómo hacer que un almacén de datos habilitado para web se pueda buscar en formato RSS y cómo especificar que se devuelva un elemento de búsqueda:


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



En el ejemplo siguiente se muestra cómo asignar propiedades a las propiedades del sistema predeterminadas para que los elementos mostrados se ordenen y agrupen:


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



En el ejemplo siguiente se muestra cómo agregar una pantalla de imagen en miniatura a cada elemento en el explorador de Windows:


```
<media:thumbnail>    
```



## <a name="additional-resources"></a>Recursos adicionales

Para obtener información adicional sobre la implementación de la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, consulte "recursos adicionales" en [búsqueda federada en Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Conexión del servicio Web en la búsqueda federada de Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitación del almacén de datos en la búsqueda federada de Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md)
</dt> <dt>

[Siguientes procedimientos recomendados en la búsqueda federada de Windows](-search-fedsearch-best.md)
</dt> <dt>

[Implementación de conectores de búsqueda en la búsqueda federada de Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 




