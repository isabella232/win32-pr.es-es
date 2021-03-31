---
description: '\_conversión de \_ multimedia de tipo de contenido de WPD \_ \_'
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2daafb381aac802b9add130aa97e9750f30e7847
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157048"
---
# <a name="wpd_content_type_media_cast"></a>\_conversión de \_ multimedia de tipo de contenido de WPD \_ \_

Objeto que describe su tipo como tipo de contenido de WPD la \_ \_ \_ \_ conversión multimedia representa una colección de contenido relacionado.

Un objeto Mediacast puede considerarse como un objeto contenedor que agrupa el contenido relacionado, al igual que una lista de reproducción agrupa música. A menudo, se usa un objeto Mediacast para agrupar el contenido multimedia que se publicó en línea. Por ejemplo, un canal RSS se puede representar como un objeto Mediacast cuyas referencias de objeto apuntan a objetos de contenido que representan cada elemento del canal.

Este tipo de objeto admite las siguientes propiedades.



|                                                                                                                       |                                                                       |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Nombre de la propiedad**                                                                                                     | **Obligatorio u opcional**                                              |
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Obligatorio.                                                             |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio.                                                             |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Es obligatorio si el objeto representa un archivo.                             |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Obligatorio.                                                             |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obligatorio.                                                             |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                           | Obligatorio.                                                             |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Es obligatorio si el objeto está oculto.                                     |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema). |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                     |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                              | Es obligatorio si el objeto representa un archivo.                             |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                       | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo. |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.               |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                             |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                             |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                           | Opcional.                                                             |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                         | Se recomienda su uso.                                                          |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                         | Opcional.                                                             |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                     | Se recomienda si otro objeto hace referencia al objeto.            |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                             |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                             |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                               | Obligatorio si el objeto se puede eliminar.                                |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                | Es obligatorio si no se puede eliminar el objeto.                             |
| [COPYRIGHT de los medios de WPD \_ \_](media-properties.md)                                                     | Opcional.                                                             |
| [\_ \_ clasificación parental de medios de \_ WPD](media-properties.md)                                        | Opcional.                                                             |
| [metagénero de multimedia de WPD \_ \_ \_](media-properties.md)                                                  | Opcional.                                                             |
| [subtítulo de medios de WPD \_ \_ \_](media-properties.md)                                                    | Opcional.                                                             |
| [\_fecha de \_ lanzamiento de medios de WPD \_](media-properties.md)                                              | Se recomienda su uso.                                                          |
| [título de los medios de WPD \_ \_](media-properties.md)                                                             | Se recomienda su uso.                                                          |
| [\_propietario de medios de WPD \_](media-properties.md)                                                             | Se recomienda su uso.                                                          |
| [\_Editor de \_ Administración de medios de WPD \_](media-properties.md)                                        | Se recomienda su uso.                                                          |
| [webmaster de multimedia de WPD \_ \_](media-properties.md)                                                     | Se recomienda su uso.                                                          |
| [\_URL de \_ origen de medios de WPD \_](media-properties.md)                                                  | Se recomienda su uso.                                                          |
| [\_URL de \_ destino de medios de WPD \_](media-properties.md)                                        | Se recomienda su uso.                                                          |
| [\_Descripción de medios de WPD \_](media-properties.md)                                                 | Opcional.                                                             |
| [\_género multimedia de WPD \_](media-properties.md)                                                             | Opcional.                                                             |
| [\_marcador de \_ objeto \_ multimedia WPD](media-properties.md)                                        | Recomendado                                                           |
| [\_fecha de \_ última \_ compilación \_ de los medios de WPD](media-properties.md)                                       | Se recomienda su uso.                                                          |
| [\_ \_ tiempo \_ de vida de los medios de WPD \_](media-properties.md)                                             | Opcional.                                                             |
| [subdescripción de los medios de WPD \_ \_ \_](object-properties.md)                                                                 | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                               | Obligatorio u opcional | Descripción                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**\_valor predeterminado del recurso WPD \_**](wpd-resource-default.md)      | Opcional.            | Contiene los datos del archivo mediacast. Por ejemplo, si este mediacast representa un canal RSS, podría tratarse del documento RSS. |
| [**\_miniatura de recursos de WPD \_**](wpd-resource-thumbnail.md)  | Opcional.            | Contiene la miniatura que representa este mediacast.                                                                         |
| [**\_carátula de \_ álbum de recursos de WPD \_**](wpd-resource-album-art.md) | Opcional.            | Contiene la ilustración de este mediacast.                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a>Asignación de elementos RSS y propiedades Mediacast

Un canal RSS se puede representar como un objeto Mediacast cuyas referencias apuntan a objetos de contenido que representan cada elemento de un canal determinado.

Los elementos de una fuente RSS tienen la jerarquía y los atributos siguientes.


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



En la tabla siguiente se enumeran los elementos de canal en una fuente RSS y las propiedades de conversión de multimedia correspondientes del tipo de contenido de WPD \_ \_ \_ \_ .



|                     |                          |                                                                                 |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| **Elemento Channel** | **Requisito de fuente RSS** | **Propiedad Mediacast correspondiente**                                            |
| category            | Opcional.                | [\_género multimedia de WPD \_](media-properties.md)                       |
| cloud               | No es aplicable.          | No es aplicable.                                                                 |
| copyright           | Opcional.                | [COPYRIGHT de los medios de WPD \_ \_](media-properties.md)               |
| description         | Obligatorio.                | [\_Descripción de medios de WPD \_](media-properties.md)           |
| Documentación                | No es aplicable.          | No es aplicable.                                                                 |
| generador           | No es aplicable.          | No es aplicable.                                                                 |
| language            | No es aplicable.          | No es aplicable.                                                                 |
| lastBuildDate       | Opcional.                | [\_fecha de \_ última \_ compilación \_ de los medios de WPD](media-properties.md) |
| link                | Obligatorio.                | [\_URL de \_ destino de medios de WPD \_](media-properties.md)  |
| managingEditor      | Opcional.                | [\_Editor de \_ Administración de medios de WPD \_](media-properties.md)  |
| pubDate             | Opcional.                | [\_fecha de \_ lanzamiento de medios de WPD \_](media-properties.md)        |
| rating              | No es aplicable.          | No es aplicable.                                                                 |
| skipDays            | No es aplicable.          | No es aplicable.                                                                 |
| skipHours           | No es aplicable.          | No es aplicable.                                                                 |
| textInput           | No es aplicable.          | No es aplicable.                                                                 |
| title               | Obligatorio.                | [\_nombre del objeto WPD \_](object-properties.md)                      |
| ttl                 | Opcional.                | [\_ \_ tiempo \_ de vida de los medios de WPD \_](media-properties.md)       |
| webmaster           | Opcional.                | [webmaster de multimedia de WPD \_ \_](media-properties.md)               |



 

En la tabla siguiente se enumeran los elementos de imagen de una fuente RSS y las propiedades de conversión de multimedia correspondientes del tipo de contenido de WPD \_ \_ \_ \_ .



|                   |                          |                                                                                |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| **Elemento Image** | **Requisito de fuente RSS** | **Propiedad Mediacast**                                                         |
| description       | Opcional.                | [\_Descripción de medios de WPD \_](media-properties.md)          |
| height            | Opcional.                | [altura de los medios de WPD \_ \_](media-properties.md)                    |
| link              | Opcional.                | [\_URL de \_ destino de medios de WPD \_](media-properties.md) |
| title             | Opcional.                | [\_nombre del objeto WPD \_](object-properties.md)                     |
| url               | Opcional.                | [\_URL de \_ origen de medios de WPD \_](media-properties.md)           |
| width             | Opcional.                | [\_ancho de medios de WPD \_](media-properties.md)                      |



 

En la tabla siguiente se enumeran los elementos de elemento de una fuente RSS y las propiedades de conversión de multimedia correspondientes del tipo de contenido de WPD \_ \_ \_ \_ .



|                  |               |                          |                                                                                |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| **Elemento Item** | **Atributo** | **Requisito de fuente RSS** | **Propiedad Mediacast**                                                         |
| autor           |               | Opcional.                | [\_intérprete multimedia de WPD \_](media-properties.md)                    |
| category         |               | Opcional.                | [\_género multimedia de WPD \_](media-properties.md)                      |
|                  | dominio        | No es aplicable.          | No es aplicable.                                                                |
| description      |               | Opcional.                | [\_Descripción de medios de WPD \_](media-properties.md)          |
| caja        |               | Opcional.                |                                                                                |
|                  | url           | Obligatorio.                | [\_URL de \_ origen de medios de WPD \_](media-properties.md)           |
|                  | length        | Obligatorio.                | [\_tamaño del objeto WPD \_](object-properties.md)                     |
|                  | type          | Obligatorio.                | (El tipo MIME debe asignarse al tipo de contenido de la propiedad).                 |
| guid             |               | Opcional.                | [\_GUID de medios de WPD \_](media-properties.md)                        |
|                  | isPermaLink   | No es aplicable.          | No es aplicable.                                                                |
| link             |               | Opcional.                | [\_URL de \_ destino de medios de WPD \_](media-properties.md) |
| pubDate          |               | Opcional.                | [\_fecha de \_ lanzamiento de medios de WPD \_](media-properties.md)       |
| source           |               | No es aplicable.          | No es aplicable.                                                                |
| title            |               | Opcional.                | [\_nombre del objeto WPD \_](object-properties.md)                     |



 

En el ejemplo siguiente se muestra una fuente RSS completa para un podcast ficticio proporcionado por el CEO de una empresa de publicación.


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past 5 years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



## <a name="mapping-rss-channel-elements-to-wpd-property-values"></a>Asignación de elementos de canal RSS a valores de propiedad de WPD

En la tabla siguiente se describe cómo se asignan los valores de los elementos de canal RSS en el ejemplo anterior a determinadas propiedades de WPD.



|                                                                                              |                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| **Propiedad WPD**                                                                             | **Valor**                                                                                     |
| [COPYRIGHT de los medios de WPD \_ \_](media-properties.md)                            | 2006 Lucerne Publishing LP, LLLP. All Rights Reserved.                                        |
| [\_Descripción de medios de WPD \_](media-properties.md)                        | Lucerne Publishing CEO Peter Bankov examina las últimas tendencias de las publicaciones en línea. |
| [\_URL de \_ destino de medios de WPD \_](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [\_género multimedia de WPD \_](media-properties.md)                                    | Noticias                                                                                          |
| [\_fecha de \_ última \_ compilación \_ de los medios de WPD](media-properties.md)              | Vie, 9 de junio 2006 14:00:28 EDT                                                                 |
| [\_Editor de \_ Administración de medios de WPD \_](media-properties.md)               | someone@example.com                                                                           |
| [\_fecha de \_ lanzamiento de medios de WPD \_](media-properties.md)                     | Vie, 9 de junio 2006 14:00:28 EDT                                                                 |
| [\_ \_ tiempo \_ de vida de los medios de WPD \_](media-properties.md)                    | 240                                                                                           |
| [título de los medios de WPD \_ \_](media-properties.md)                                    | La publicación digital                                                                       |
| [\_URL de \_ origen de medios de WPD \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [webmaster de multimedia de WPD \_ \_](media-properties.md)                            | someone@example.com                                                                           |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                  | \_conversión de \_ multimedia de tipo de contenido de WPD \_ \_                                                               |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                | Vie, 9 de junio 2006 14:00:28 EDT                                                                 |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                  | Vie, 9 de junio 2006 14:00:28 EDT                                                                 |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                | Vie, 9 de junio 2006 14:00:28 EDT                                                                 |
| [\_formato de objeto WPD \_](object-properties.md)                               | \_formato de objeto WPD \_ \_ conversión de medios abstractos \_ \_                                                    |
| [\_identificador de objeto de WPD \_](object-properties.md)                                       | Valor dependiente de la sesión.                                                                      |
| [\_nombre del objeto WPD \_](object-properties.md)                                   | La publicación digital                                                                       |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)     | La publicación digital                                                                       |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                        | Mis podcasts (una carpeta de podcast ficticia en el dispositivo). Asuma "0A0" en este ejemplo.        |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md) | Valor independiente de la sesión. (Asuma "0A1" en este ejemplo).                                   |
| [\_referencias a objetos de WPD \_](object-properties.md)                       | 0A2 para N elementos<br/>                                                                   |
| [\_tamaño del objeto WPD \_](object-properties.md)                                   | 13.790                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a>Asignar elementos de imagen RSS a valores de propiedad de WPD

En la tabla siguiente se describe cómo se asignan los valores de los elementos de imagen RSS en el ejemplo anterior a determinadas propiedades de WPD.



|                                                                                                                         |                                                     |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| **Propiedad WPD**                                                                                                        | **Valor**                                           |
| [\_Descripción de medios de WPD \_](media-properties.md)                                                   | Logotipo de Lucerne                                        |
| [\_URL de \_ destino de medios de WPD \_](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [altura de los medios de WPD \_ \_](media-properties.md)                                                             | 300                                                 |
| [\_URL de \_ origen de medios de WPD \_](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [\_ancho de medios de WPD \_](media-properties.md)                                                               | 300                                                 |
| [\_nombre del objeto WPD \_](object-properties.md)                                                              | Publicación de Lucerne                                  |
| [el \_ atributo de recurso de WPD \_ \_ puede \_ eliminar](attributes.md)                               | VARIANTE \_ true                                       |
| [el \_ atributo del recurso WPD \_ \_ puede \_ leer](attributes.md)                                   | VARIANTE \_ true                                       |
| [\_formato de \_ atributo de recurso de WPD \_](resource-attribute-properties.md)                     | \_formato de objeto WPD \_ \_ GIF                            |
| [\_tamaño de \_ \_ búfer de \_ lectura óptimo del \_ atributo \_ de recurso de WPD](attributes.md) | 1024                                                |
| [\_ \_ Tamaño total del atributo de recursos de \_ WPD \_](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>Asignar elementos RSS Item a valores de propiedad de WPD

En la tabla siguiente se describe cómo se asignan los valores de los elementos RSS item en el ejemplo anterior a determinadas propiedades de WPD.



|                                                                                              |                                                                                                                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **Propiedad WPD**<br/>                                                                  | **Valor**                                                                                                                        |
| [título de los medios de WPD \_ \_](media-properties.md)                                    | La publicación digital                                                                                                          |
| [duración de los medios de WPD \_ \_](media-properties.md)                              | 10329011                                                                                                                         |
| [\_intérprete multimedia de WPD \_](media-properties.md)                                  | Lucerne                                                                                                                          |
| [\_Descripción de medios de WPD \_](media-properties.md)                        | Las publicaciones en línea cambian rápidamente. El CEO de un centro de publicaciones examina las tendencias de los últimos cinco años y sus implicaciones. |
| [\_URL de \_ destino de medios de WPD \_](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_género multimedia de WPD \_](media-properties.md)                                    | Noticias                                                                                                                             |
| [\_GUID de medios de WPD \_](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_fecha de \_ lanzamiento de medios de WPD \_](media-properties.md)                     | Jue, 1 de junio 2006 14:00:28 EDT                                                                                                   |
| [\_URL de \_ origen de medios de WPD \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)            | 0A1                                                                                                                              |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                  | \_ \_ imagen multimedia del tipo de contenido de \_ WPD \_                                                                                                 |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                | Jue, 1 de junio 2006 14:00:28 EDT                                                                                                   |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                  | Jue, 1 de junio 2006 14:00:28 EDT                                                                                                   |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                | Jue, 1 de junio 2006 14:00:28 EDT                                                                                                   |
| [\_formato de objeto WPD \_](object-properties.md)                               | \_Formato de objeto WPD \_ \_ mp3                                                                                                         |
| [\_identificador de objeto de WPD \_](object-properties.md)                                       | Dependiente de la sesión. (Asuma "0A2" en este ejemplo).                                                                              |
| [\_nombre del objeto WPD \_](object-properties.md)                                   | La publicación digital                                                                                                          |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                        | 0A0                                                                                                                              |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md) | Independiente de la sesión.                                                                                                             |
| [\_tamaño del objeto WPD \_](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 




