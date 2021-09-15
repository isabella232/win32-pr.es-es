---
description: CONVERSIÓN MULTIMEDIA \_ DE TIPO DE CONTENIDO \_ \_ WPD \_
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d45c9bc1e8e41bae526f02102d341ef00fad435
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571157"
---
# <a name="wpd_content_type_media_cast"></a>CONVERSIÓN MULTIMEDIA \_ DE TIPO DE CONTENIDO \_ \_ WPD \_

Un objeto que describe su tipo como WPD \_ CONTENT TYPE MEDIA CAST representa una colección de contenido \_ \_ \_ relacionado.

Un objeto Mediacast se puede pensar en un objeto contenedor que agrupa contenido relacionado, igual que una lista de reproducción que agrupa música. A menudo, un objeto Mediacast se usa para agrupar el contenido multimedia que se publicó en línea. Por ejemplo, un canal RSS se puede representar como un objeto Mediacast cuyas referencias de objeto apuntan a objetos de contenido que representan cada elemento del canal.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad             |  Obligatorio u opcional         |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                | Necesario.                                                             |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Necesario.                                                             |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto representa un archivo.                             |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                          | Necesario.                                                             |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Necesario.                                                             |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Necesario.                                                             |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                     |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema). |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                     |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                             |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo. |
| [REFERENCIAS DE OBJETOS \_ WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.               |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                             |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                                           | Opcional.                                                             |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                                         | Se recomienda su uso.                                                          |
| [FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Opcional.                                                             |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                     | Se recomienda si otro objeto hace referencia al objeto.            |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                             |
| [WPD \_ OBJECT \_ GENERATE \_ THUMBNAIL \_ FROM \_ RESOURCE](object-properties.md) | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ SE PUEDE \_ ELIMINAR](object-properties.md)                                               | Obligatorio si el objeto se puede eliminar.                                |
| [CONFIGURACIÓN REGIONAL \_ DEL LENGUAJE DE OBJETOS \_ \_ WPD](object-properties.md)                                                                | Obligatorio si no se puede eliminar el objeto.                             |
| [COPYRIGHT DE \_ WPD \_ MEDIA](media-properties.md)                                                     | Opcional.                                                             |
| [CLASIFICACIÓN PARENTAL \_ DE WPD \_ MEDIA \_](media-properties.md)                                        | Opcional.                                                             |
| [WPD \_ MEDIA \_ META \_ GENRE](media-properties.md)                                                  | Opcional.                                                             |
| [SUB TÍTULO DE \_ \_ WPD \_ MEDIA](media-properties.md)                                                    | Opcional.                                                             |
| [FECHA DE LANZAMIENTO \_ DE WPD \_ \_ MEDIA](media-properties.md)                                              | Se recomienda su uso.                                                          |
| [TÍTULO MULTIMEDIA \_ DE \_ WPD](media-properties.md)                                                             | Se recomienda su uso.                                                          |
| [PROPIETARIO DE \_ WPD \_ MEDIA](media-properties.md)                                                             | Se recomienda su uso.                                                          |
| [EDITOR DE \_ ADMINISTRACIÓN DE \_ MEDIOS DE WPD \_](media-properties.md)                                        | Se recomienda su uso.                                                          |
| [WPD \_ MEDIA \_ WEBMASTER](media-properties.md)                                                     | Se recomienda su uso.                                                          |
| [DIRECCIÓN URL DE \_ ORIGEN \_ DE \_ WPD MEDIA](media-properties.md)                                                  | Se recomienda su uso.                                                          |
| [DIRECCIÓN URL DE \_ DESTINO DE \_ \_ WPD MEDIA](media-properties.md)                                        | Se recomienda su uso.                                                          |
| [DESCRIPCIÓN DE LOS \_ MEDIOS DE \_ WPD](media-properties.md)                                                 | Opcional.                                                             |
| [GÉNERO MULTIMEDIA DE WPD \_ \_](media-properties.md)                                                             | Opcional.                                                             |
| [MARCADOR DE \_ OBJETOS MULTIMEDIA WPD \_ \_](media-properties.md)                                        | Recomendado                                                           |
| [FECHA DE ÚLTIMA COMPILACIÓN DE WPD \_ \_ \_ \_ MEDIA](media-properties.md)                                       | Se recomienda su uso.                                                          |
| [PERÍODO DE \_ VIDA \_ DE WPD \_ \_ MEDIA](media-properties.md)                                             | Opcional.                                                             |
| [SUB DESCRIPTION DE \_ WPD MEDIA \_ \_](object-properties.md)                                                                 | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                               | Obligatorio u opcional | Descripción                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)      | Opcional.            | Contiene los datos del archivo de difusión multimedia. Por ejemplo, si este mediacast representa un canal RSS, podría ser el documento RSS. |
| [**MINIATURA DE RECURSOS DE WPD \_ \_**](wpd-resource-thumbnail.md)  | Opcional.            | Contiene la miniatura que representa esta difusión multimedia.                                                                         |
| [**WPD \_ RESOURCE \_ ALBUM \_ ART**](wpd-resource-album-art.md) | Opcional.            | Contiene las ilustraciones de esta difusión multimedia.                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a>Asignación de elementos RSS y propiedades de Mediacast

Un canal RSS se puede representar como un objeto Mediacast cuyas referencias apuntan a objetos de contenido que representan cada elemento de un canal determinado.

Los elementos de una fuente RSS tienen la siguiente jerarquía y atributos.


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



En la tabla siguiente se enumeran los elementos de canal de una fuente RSS y las propiedades MEDIA CAST correspondientes de WPD \_ CONTENT \_ \_ \_ TYPE.



| Elemento Channel | Requisito de fuente RSS | Propiedad Mediacast correspondiente      |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| category            | Opcional.                | [GÉNERO MULTIMEDIA DE WPD \_ \_](media-properties.md)                       |
| cloud               | No es aplicable.          | No es aplicable.                                                                 |
| copyright           | Opcional.                | [COPYRIGHT DE \_ WPD \_ MEDIA](media-properties.md)               |
| description         | Necesario.                | [DESCRIPCIÓN DE LOS \_ MEDIOS DE \_ WPD](media-properties.md)           |
| Documentación                | No es aplicable.          | No es aplicable.                                                                 |
| generador           | No es aplicable.          | No es aplicable.                                                                 |
| language            | No es aplicable.          | No es aplicable.                                                                 |
| lastBuildDate       | Opcional.                | [FECHA DE ÚLTIMA COMPILACIÓN DE WPD \_ \_ \_ \_ MEDIA](media-properties.md) |
| link                | Necesario.                | [DIRECCIÓN URL DE \_ DESTINO DE \_ \_ WPD MEDIA](media-properties.md)  |
| managingEditor      | Opcional.                | [EDITOR DE \_ ADMINISTRACIÓN DE \_ MEDIOS DE WPD \_](media-properties.md)  |
| pubDate             | Opcional.                | [FECHA DE LANZAMIENTO \_ DE WPD \_ \_ MEDIA](media-properties.md)        |
| rating              | No es aplicable.          | No es aplicable.                                                                 |
| skipDays            | No es aplicable.          | No es aplicable.                                                                 |
| skipHours           | No es aplicable.          | No es aplicable.                                                                 |
| Textinput           | No es aplicable.          | No es aplicable.                                                                 |
| title               | Necesario.                | [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                      |
| ttl                 | Opcional.                | [PERÍODO DE \_ VIDA \_ DE WPD \_ \_ MEDIA](media-properties.md)       |
| Webmaster           | Opcional.                | [WPD \_ MEDIA \_ WEBMASTER](media-properties.md)               |



 

En la tabla siguiente se enumeran los elementos de imagen de una fuente RSS y las propiedades \_ MEDIA \_ CAST \_ correspondientes de WPD CONTENT \_ TYPE.



| Elemento de imagen | Requisito de fuente RSS | Mediacast (propiedad)                     |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| description       | Opcional.                | [DESCRIPCIÓN DE LOS \_ MEDIOS DE \_ WPD](media-properties.md)          |
| height            | Opcional.                | [ALTURA DEL \_ MEDIO WPD \_](media-properties.md)                    |
| link              | Opcional.                | [DIRECCIÓN URL DE \_ DESTINO DE \_ \_ WPD MEDIA](media-properties.md) |
| title             | Opcional.                | [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                     |
| url               | Opcional.                | [DIRECCIÓN URL DE \_ ORIGEN \_ DE \_ WPD MEDIA](media-properties.md)           |
| width             | Opcional.                | [ANCHO DE MEDIOS \_ WPD \_](media-properties.md)                      |



 

En la tabla siguiente se enumeran los elementos de una fuente RSS y las propiedades \_ MEDIA \_ CAST \_ correspondientes de WPD CONTENT \_ TYPE.



| Elemento Item | Atributo | Requisito de fuente RSS | Mediacast (propiedad)  |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| autor           |               | Opcional.                | [WPD \_ MEDIA \_ ARTIST](media-properties.md)                    |
| category         |               | Opcional.                | [GÉNERO MULTIMEDIA DE WPD \_ \_](media-properties.md)                      |
|                  | dominio        | No es aplicable.          | No es aplicable.                                                                |
| description      |               | Opcional.                | [DESCRIPCIÓN DE LOS \_ MEDIOS DE \_ WPD](media-properties.md)          |
| Recinto        |               | Opcional.                |                                                                                |
|                  | url           | Necesario.                | [DIRECCIÓN URL DE \_ ORIGEN \_ DE \_ WPD MEDIA](media-properties.md)           |
|                  | length        | Necesario.                | [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                     |
|                  | type          | Necesario.                | (El tipo MIME debe asignarse al tipo de contenido de propiedad).                 |
| guid             |               | Opcional.                | [GUID DE \_ MEDIOS DE \_ WPD](media-properties.md)                        |
|                  | isPermaLink   | No es aplicable.          | No es aplicable.                                                                |
| link             |               | Opcional.                | [DIRECCIÓN URL DE \_ DESTINO DE \_ \_ WPD MEDIA](media-properties.md) |
| pubDate          |               | Opcional.                | [FECHA DE LANZAMIENTO \_ DE WPD \_ \_ MEDIA](media-properties.md)       |
| source           |               | No es aplicable.          | No es aplicable.                                                                |
| title            |               | Opcional.                | [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                     |



 

En el ejemplo siguiente se muestra una fuente RSS completa para un podcast ficticio proporcionado por el director general de una empresa de publicación.


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



## <a name="mapping-rss-channel-elements-to-wpd-property-values"></a>Asignación de elementos de canal RSS a valores de propiedad WPD

En la tabla siguiente se describe cómo se asignan los valores de los elementos del canal RSS del ejemplo anterior a propiedades de WPD concretas.



| Propiedad WPD | Value |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [COPYRIGHT DE \_ WPD \_ MEDIA](media-properties.md)                            | 2006 Lucerne Publishing LP, LLLP. All Rights Reserved.                                        |
| [DESCRIPCIÓN DE LOS \_ MEDIOS DE \_ WPD](media-properties.md)                        | El director general de publicación de Lucerne, Peter Bankov, se fija en las tendencias más recientes de las publicaciones en línea. |
| [DIRECCIÓN URL DE \_ DESTINO DE \_ \_ WPD MEDIA](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [GÉNERO MULTIMEDIA DE WPD \_ \_](media-properties.md)                                    | Noticias                                                                                          |
| [FECHA DE ÚLTIMA COMPILACIÓN DE WPD \_ \_ \_ \_ MEDIA](media-properties.md)              | Viernes, 9 de junio de 2006 14:00:28 EDT                                                                 |
| [EDITOR DE \_ ADMINISTRACIÓN DE \_ MEDIOS DE WPD \_](media-properties.md)               | someone@example.com                                                                           |
| [FECHA DE LANZAMIENTO \_ DE WPD \_ \_ MEDIA](media-properties.md)                     | Viernes, 9 de junio de 2006 14:00:28 EDT                                                                 |
| [PERÍODO DE \_ VIDA \_ DE WPD \_ \_ MEDIA](media-properties.md)                    | 240                                                                                           |
| [TÍTULO MULTIMEDIA \_ DE \_ WPD](media-properties.md)                                    | La publicación digital                                                                       |
| [DIRECCIÓN URL DE \_ ORIGEN \_ DE \_ WPD MEDIA](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [WPD \_ MEDIA \_ WEBMASTER](media-properties.md)                            | someone@example.com                                                                           |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                  | CONVERSIÓN MULTIMEDIA \_ DE TIPO DE CONTENIDO \_ \_ WPD \_                                                               |
| [FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD](object-properties.md)                | Viernes, 9 de junio de 2006 14:00:28 EDT                                                                 |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                  | Viernes, 9 de junio de 2006 14:00:28 EDT                                                                 |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                | Viernes, 9 de junio de 2006 14:00:28 EDT                                                                 |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                               | CONVERSIÓN MULTIMEDIA \_ ABSTRACTA \_ DE FORMATO DE \_ OBJETO \_ WPD \_                                                    |
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                       | Valor dependiente de la sesión.                                                                      |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                   | La publicación digital                                                                       |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)     | La publicación digital                                                                       |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                        | MyPodcasts (una carpeta de podcasts ficticia en el dispositivo). Suponga "0A0" en este ejemplo.        |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md) | Valor independiente de la sesión. (Suponga "0A1" para este ejemplo).                                   |
| [REFERENCIAS DE OBJETOS \_ WPD \_](object-properties.md)                       | 0A2 para N elementos<br/>                                                                   |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                   | 13,790                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a>Asignación de elementos de imagen RSS a valores de propiedad WPD

En la tabla siguiente se describe cómo los valores de los elementos RSS Image del ejemplo anterior se asignan a propiedades de WPD concretas.



| Propiedad WPD               |                         Value                                           |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [DESCRIPCIÓN DE LOS \_ MEDIOS DE \_ WPD](media-properties.md)                                                   | Logotipo de Lucerne                                        |
| [DIRECCIÓN URL DE \_ DESTINO DE \_ \_ WPD MEDIA](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [ALTURA DEL \_ MEDIO WPD \_](media-properties.md)                                                             | 300                                                 |
| [DIRECCIÓN URL DE \_ ORIGEN \_ DE \_ WPD MEDIA](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [ANCHO DE MEDIOS \_ WPD \_](media-properties.md)                                                               | 300                                                 |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                              | Publicación de Lucerne                                  |
| [EL ATRIBUTO \_ DE RECURSO WPD \_ SE \_ PUEDE \_ ELIMINAR](attributes.md)                               | VARIANT \_ TRUE                                       |
| [EL ATRIBUTO \_ DE RECURSO WPD \_ PUEDE \_ \_ LEER](attributes.md)                                   | VARIANT \_ TRUE                                       |
| [FORMATO DE ATRIBUTO \_ DE \_ RECURSO \_ WPD](resource-attribute-properties.md)                     | GIF CON \_ FORMATO DE \_ OBJETO \_ WPD                            |
| [TAMAÑO ÓPTIMO DEL BÚFER DE \_ LECTURA DEL ATRIBUTO DE RECURSO \_ \_ \_ \_ \_ WPD](attributes.md) | 1024                                                |
| [TAMAÑO TOTAL DEL \_ ATRIBUTO \_ DE RECURSO \_ WPD \_](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>Asignación de elementos de elemento RSS a valores de propiedad WPD

En la tabla siguiente se describe cómo se asignan los valores de los elementos elemento RSS del ejemplo anterior a propiedades de WPD concretas.



| Propiedad WPD  | Value                   |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [TÍTULO MULTIMEDIA \_ DE \_ WPD](media-properties.md)                                    | La publicación digital                                                                                                          |
| [DURACIÓN MULTIMEDIA \_ DE \_ WPD](media-properties.md)                              | 10329011                                                                                                                         |
| [WPD \_ MEDIA \_ ARTIST](media-properties.md)                                  | Lucerna                                                                                                                          |
| [DESCRIPCIÓN DE LOS \_ MEDIOS DE \_ WPD](media-properties.md)                        | Las publicaciones en línea cambian rápidamente. Un director general de una casa de publicación examina las tendencias de los últimos 5 años y sus implicaciones. |
| [DIRECCIÓN URL DE \_ DESTINO DE \_ \_ WPD MEDIA](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [GÉNERO MULTIMEDIA DE WPD \_ \_](media-properties.md)                                    | Noticias                                                                                                                             |
| [GUID DE \_ MEDIOS DE \_ WPD](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [FECHA DE LANZAMIENTO \_ DE WPD \_ \_ MEDIA](media-properties.md)                     | Así, 1 de junio de 2006 14:00:28 EDT                                                                                                   |
| [DIRECCIÓN URL DE \_ ORIGEN \_ DE \_ WPD MEDIA](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)            | 0A1                                                                                                                              |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                  | IMAGEN MULTIMEDIA \_ DEL TIPO DE CONTENIDO \_ \_ \_ WPD                                                                                                 |
| [FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD](object-properties.md)                | Así, 1 de junio de 2006 14:00:28 EDT                                                                                                   |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                  | Así, 1 de junio de 2006 14:00:28 EDT                                                                                                   |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                | Así, 1 de junio de 2006 14:00:28 EDT                                                                                                   |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                               | WPD \_ OBJECT \_ FORMAT \_ MP3                                                                                                         |
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                       | Dependiente de la sesión. (Suponga "0A2" para este ejemplo).                                                                              |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                   | La publicación digital                                                                                                          |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                        | 0A0                                                                                                                              |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md) | Independiente de la sesión.                                                                                                             |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 




