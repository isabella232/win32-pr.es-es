---
title: Asignar fuentes RSS a propiedades de Administrador de dispositivos de Windows Media
description: Asignar fuentes RSS a propiedades de Administrador de dispositivos de Windows Media
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Media Administrador de dispositivos, fuentes RSS
- Administrador de dispositivos, fuentes RSS
- Guía de programación, fuentes RSS
- aplicaciones de escritorio, fuentes RSS
- crear aplicaciones de Windows Media Administrador de dispositivos, fuentes RSS
- Fuentes RSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903188"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>Asignar fuentes RSS a propiedades de Administrador de dispositivos de Windows Media

Windows Media Player 11 proporciona una característica de agregador RSS que permite a los usuarios almacenar contenido obtenido de podcasts en sus equipos. En este tema se describen los elementos XML que se encuentran en una fuente RSS. Además, asigna estos elementos RSS a las propiedades de Administrador de dispositivos de Windows Media.

Los elementos de una fuente RSS tienen la jerarquía y los atributos siguientes:


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



En la tabla siguiente se enumeran los elementos de canal en una fuente RSS y las propiedades correspondientes de Windows Media Administrador de dispositivos.



| Elemento Channel | Status         | Propiedad de Administrador de dispositivos de Windows Media correspondiente   |
|-----------------|----------------|-------------------------------------------------------|
| category        | Opcionales       | [g \_ wszWMDMGenre](metadata-constants.md)             |
| cloud           | No aplicable | No aplicable                                        |
| copyright       | Opcionales       | [g \_ wszWMDMProviderCopyright](metadata-constants.md) |
| description     | Obligatorio       | [g \_ wszWMDMDescription](metadata-constants.md)       |
| Documentación            | No aplicable | No aplicable                                        |
| generador       | No aplicable | No aplicable                                        |
| language        | No aplicable | No aplicable                                        |
| lastBuildDate   | Opcionales       | [g \_ wszWMDMLastModifiedDate](metadata-constants.md)  |
| link            | Obligatorio       | [g \_ wszWMDMDestinationURL](metadata-constants.md)    |
| managingEditor  | Opcionales       | [g \_ wszWMDMEditor](metadata-constants.md)            |
| pubDate         | Opcionales       | [g \_ wszWMDMYear](metadata-constants.md)              |
| rating          | No aplicable | No aplicable                                        |
| skipDays        | No aplicable | No aplicable                                        |
| skipHours       | No aplicable | No aplicable                                        |
| textInput       | No aplicable | No aplicable                                        |
| title           | Obligatorio       | [g \_ wszWMDMTitle](metadata-constants.md)             |
| ttl             | Opcionales       | [g \_ wszWMDMTimeToLive](metadata-constants.md)        |
| webmaster       | Opcionales       | [g \_ wszWMDMWebMaster](metadata-constants.md)         |



 

En la tabla siguiente se enumeran los elementos de imagen de una fuente RSS y las propiedades de WMDM correspondientes.



| Elemento Image | Status   | Propiedad de Administrador de dispositivos de Windows Media correspondiente |
|---------------|----------|-----------------------------------------------------|
| description   | Opcionales | [g \_ wszWMDMDescription](metadata-constants.md)     |
| height        | Opcionales | [g \_ wszWMDMHeight](metadata-constants.md)          |
| link          | Opcionales | [g \_ wszWMDMDestinationURL](metadata-constants.md)  |
| title         | Opcionales | [g \_ wszWMDMTitle](metadata-constants.md)           |
| url           | Opcionales | [g \_ wszWMDMSourceURL](metadata-constants.md)       |
| width         | Opcionales | [g \_ wszWMDMWidth](metadata-constants.md)           |



 

En la tabla siguiente se enumeran los elementos de elemento de una fuente RSS y las propiedades correspondientes de Windows Media Administrador de dispositivos.



| Elemento Item | Atributo   | Status         | Propiedad de Administrador de dispositivos de Windows Media correspondiente            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| autor       |             | Opcionales       | [g \_ wszWMDMAuthor](metadata-constants.md)                     |
| category     |             | Opcionales       | [g \_ wszWMDMGenre](metadata-constants.md)                      |
|              | dominio      | No aplicable | No aplicable                                                 |
| description  |             | Opcionales       | [g \_ wszWMDMDescription](metadata-constants.md)                |
| caja    |             | Opcionales       | No aplicable                                                 |
|              | length      | Obligatorio       | [g \_ wszWMDMFileSize](metadata-constants.md)                   |
|              | type        | Obligatorio       | (El tipo MIME debe asignarse al tipo de contenido de la propiedad). |
|              | url         | Obligatorio       | [g \_ wszWMDMSourceURL](metadata-constants.md)                  |
| guid         |             | Opcionales       | [g \_ wszWMDMediaGuid](metadata-constants.md)                   |
|              | isPermaLink | No aplicable | No aplicable                                                 |
| link         |             | Opcionales       | [g \_ wszWMDMDestinationURL](metadata-constants.md)             |
| pubDate      |             | Opcionales       | [g \_ wszWMDMYear](metadata-constants.md)                       |
| source       |             | No aplicable | No aplicable                                                 |
| title        |             | Opcionales       | [g \_ wszWMDMTitle](metadata-constants.md)                      |



 

Ejemplo

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
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
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



Asignación de elementos de canal RSS a Windows Media Administrador de dispositivos valores de propiedad

En la tabla siguiente se describe cómo se asignan los valores de los elementos de canal RSS en el ejemplo anterior a determinadas propiedades de Administrador de dispositivos de Windows Media.



| Propiedad Administrador de dispositivos de Windows Media                    | Value                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthorDate](metadata-constants.md)           | Vie, 9 de junio 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMDESCRIPTION](metadata-constants.md)          | Lucerne Publishing CEO Peter Bankov examina las últimas tendencias de las publicaciones en línea. |
| [\_ \_ dirección URL de g wszWMDMDESTINATION](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [g \_ wszWMDMEDITOR](metadata-constants.md)               | someone@example.com                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md)     | Vie, 9 de junio 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMFileName](metadata-constants.md)             | La publicación digital                                                                       |
| [g \_ wszWMDMFileSize](metadata-constants.md)             | 13.790                                                                                        |
| [g \_ wszWMDMFormatCode](metadata-constants.md)           | \_ \_ conversión multimedia FORMATCODE de WMDM \_                                                                 |
| [g \_ wszWMDMGENRE](metadata-constants.md)                | Noticias                                                                                          |
| [g \_ wszWMDMLAST \_ fecha de modificación \_](metadata-constants.md) | Vie, 9 de junio 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md)     | Vie, 9 de junio 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMProviderCopyright](metadata-constants.md)    | 2006 Lucerne Publishing LP, LLLP. All Rights Reserved.                                        |
| [g \_ wszWMDMTimeToLive](metadata-constants.md)           | 240                                                                                           |
| [g \_ wszWMDMTitle](metadata-constants.md)                | La publicación digital                                                                       |
| [g \_ wszWMDMWEBMASTER](metadata-constants.md)            | someone@example.com                                                                           |
| [g \_ wszWMDMYear](metadata-constants.md)                 | Vie, 9 de junio 2006 14:00:28 EDT                                                                 |



 

Asignación de elementos de imagen RSS a Windows Media Administrador de dispositivos valores de propiedad

En la tabla siguiente se describe cómo se asignan los valores de los elementos de imagen RSS en el ejemplo anterior a determinadas propiedades de Administrador de dispositivos de Windows Media.



| Propiedad Administrador de dispositivos de Windows Media                | Value                                            |
|------------------------------------------------------|--------------------------------------------------|
| [g \_ wszWMDMAlbumCoverFormat](metadata-constants.md) | \_formato de objeto WPD \_ \_ GIF                         |
| [g \_ wszWMDMAlbumCoverSize](metadata-constants.md)   | 512                                              |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Logotipo de Lucerne                                     |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [g \_ wszWMDMHeight](metadata-constants.md)           | 300                                              |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [g \_ wszWMDMTitle](metadata-constants.md)            | Publicación de Lucerne                               |
| [g \_ wszWMDMWidth](metadata-constants.md)            | 300                                              |



 

Asignación de elementos RSS Item a Windows Media Administrador de dispositivos valores de propiedad

En la tabla siguiente se describe cómo se asignan los valores de los elementos RSS del ejemplo anterior a determinadas propiedades de Administrador de dispositivos de Windows Media.



| Propiedad Administrador de dispositivos de Windows Media                | Value                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthor](metadata-constants.md)           | Lucerne                                                                                                                             |
| [g \_ wszWMDMAuthorDate](metadata-constants.md)       | Jue, 1 de junio 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Las publicaciones en línea cambian rápidamente. El CEO de un centro de publicaciones examina las tendencias de los últimos cinco años y sus implicaciones. |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMDuration](metadata-constants.md)         | 120325445                                                                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md) | Jue, 1 de junio 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMFileSize](metadata-constants.md)         | 10329011                                                                                                                            |
| [g \_ wszWMDMFormatCode](metadata-constants.md)       | \_Mp3 FORMATCODE de WMDM \_                                                                                                               |
| [g \_ wszWMDMGenre](metadata-constants.md)            | Noticias                                                                                                                                |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md) | Jue, 1 de junio 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMMediaGuid](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMTitle](metadata-constants.md)            | La publicación digital                                                                                                             |
| [g \_ wszWMDMYear](metadata-constants.md)             | Jue, 1 de junio 2006 14:00:28 EDT                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes de metadatos**](metadata-constants.md)
</dt> </dl>

 

 




