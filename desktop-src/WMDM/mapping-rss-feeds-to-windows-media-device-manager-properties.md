---
title: Asignación de fuentes RSS a Windows propiedades Administrador de dispositivos multimedia
description: Asignación de fuentes RSS a Windows propiedades Administrador de dispositivos multimedia
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Fuente Administrador de dispositivos multimedia, fuentes RSS
- Administrador de dispositivos,fuentes RSS
- guía de programación, fuentes RSS
- aplicaciones de escritorio, fuentes RSS
- crear Windows aplicaciones de Administrador de dispositivos multimedia, fuentes RSS
- Fuentes RSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355515217db31740603d5c6323ef8455da4b29ee80bec508897d2d4df5d59bde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031685"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>Asignación de fuentes RSS a Windows propiedades Administrador de dispositivos multimedia

Reproductor de Windows Media 11 proporciona una característica de agregador RSS que permite a los usuarios almacenar contenido obtenido de podcasts en sus equipos. En este tema se describen los elementos XML que se encuentran en una fuente RSS. Además, asigna estos elementos RSS a las Windows de Administrador de dispositivos multimedia.

Los elementos de una fuente RSS tienen la siguiente jerarquía y atributos:


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



En la tabla siguiente se enumeran los elementos de canal de una fuente RSS y las propiedades Windows media Administrador de dispositivos correspondientes.



| Elemento Channel | Estado         | Propiedad Windows media Administrador de dispositivos correspondiente   |
|-----------------|----------------|-------------------------------------------------------|
| category        | Opcionales       | [g \_ wszWMDMGenre](metadata-constants.md)             |
| cloud           | No aplicable | No aplicable                                        |
| copyright       | Opcionales       | [g \_ wszWMDMProviderCopyright](metadata-constants.md) |
| description     | Requerido       | [g \_ wszWMDMDescription](metadata-constants.md)       |
| Documentación            | No aplicable | No aplicable                                        |
| generador       | No aplicable | No aplicable                                        |
| language        | No aplicable | No aplicable                                        |
| lastBuildDate   | Opcionales       | [g \_ wszWMDMLastModifiedDate](metadata-constants.md)  |
| link            | Requerido       | [g \_ wszWMDMDestinationURL](metadata-constants.md)    |
| managingEditor  | Opcionales       | [g \_ wszWMDMEditor](metadata-constants.md)            |
| pubDate         | Opcionales       | [g \_ wszWMDMYear](metadata-constants.md)              |
| rating          | No aplicable | No aplicable                                        |
| skipDays        | No aplicable | No aplicable                                        |
| skipHours       | No aplicable | No aplicable                                        |
| Textinput       | No aplicable | No aplicable                                        |
| title           | Requerido       | [g \_ wszWMDMTitle](metadata-constants.md)             |
| ttl             | Opcionales       | [g \_ wszWMDMTimeToLive](metadata-constants.md)        |
| Webmaster       | Opcionales       | [g \_ wszWMDMWebMaster](metadata-constants.md)         |



 

En la tabla siguiente se enumeran los elementos de imagen de una fuente RSS y las propiedades WMDM correspondientes.



| Elemento Image | Estado   | Propiedad Windows media Administrador de dispositivos correspondiente |
|---------------|----------|-----------------------------------------------------|
| description   | Opcionales | [g \_ wszWMDMDescription](metadata-constants.md)     |
| height        | Opcionales | [g \_ wszWMDMHeight](metadata-constants.md)          |
| link          | Opcionales | [g \_ wszWMDMDestinationURL](metadata-constants.md)  |
| title         | Opcionales | [g \_ wszWMDMTitle](metadata-constants.md)           |
| url           | Opcionales | [g \_ wszWMDMSourceURL](metadata-constants.md)       |
| width         | Opcionales | [g \_ wszWMDMWidth](metadata-constants.md)           |



 

En la tabla siguiente se enumeran los elementos de elemento de una fuente RSS y las propiedades Windows media Administrador de dispositivos correspondientes.



| Elemento Item | Atributo   | Estado         | Propiedad Windows media Administrador de dispositivos correspondiente            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| autor       |             | Opcionales       | [g \_ wszWMDMAuthor](metadata-constants.md)                     |
| category     |             | Opcionales       | [g \_ wszWMDMGenre](metadata-constants.md)                      |
|              | dominio      | No aplicable | No aplicable                                                 |
| description  |             | Opcionales       | [g \_ wszWMDMDescription](metadata-constants.md)                |
| Recinto    |             | Opcionales       | No aplicable                                                 |
|              | length      | Requerido       | [g \_ wszWMDMFileSize](metadata-constants.md)                   |
|              | type        | Obligatorio       | (El tipo MIME debe asignarse al tipo de contenido de la propiedad). |
|              | url         | Requerido       | [g \_ wszWMDMSourceURL](metadata-constants.md)                  |
| guid         |             | Opcionales       | [g \_ wszWMDMediaGuid](metadata-constants.md)                   |
|              | isPermaLink | No aplicable | No aplicable                                                 |
| link         |             | Opcionales       | [g \_ wszWMDMDestinationURL](metadata-constants.md)             |
| pubDate      |             | Opcionales       | [g \_ wszWMDMYear](metadata-constants.md)                       |
| source       |             | No aplicable | No aplicable                                                 |
| title        |             | Opcionales       | [g \_ wszWMDMTitle](metadata-constants.md)                      |



 

Ejemplo

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



Asignación de elementos de canal RSS a Windows de Administrador de dispositivos valores de propiedad

En la tabla siguiente se describe cómo los valores de los elementos del canal RSS del ejemplo anterior se asignan a propiedades Windows de Administrador de dispositivos medios.



| Windows Propiedad Administrador de dispositivos multimedia                    | Value                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthorDate](metadata-constants.md)           | Viernes, 9 de junio de 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMDESCRIPTION](metadata-constants.md)          | El director general de lucerne Publishing, Peter Bankov, se fija en las tendencias más recientes de las publicaciones en línea. |
| [g \_ wszWMDMDESTINATION \_ URL](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [g \_ wszWMDMEDITOR](metadata-constants.md)               | someone@example.com                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md)     | Viernes, 9 de junio de 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMFileName](metadata-constants.md)             | La publicación digital                                                                       |
| [g \_ wszWMDMFileSize](metadata-constants.md)             | 13,790                                                                                        |
| [g \_ wszWMDMFormatCode](metadata-constants.md)           | WMDM \_ FORMATCODE \_ MEDIA \_ CAST                                                                 |
| [g \_ wszWMDMGENRE](metadata-constants.md)                | Noticias                                                                                          |
| [g \_ wszWMDMLAST \_ MODIFIED \_ DATE](metadata-constants.md) | Viernes, 9 de junio de 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md)     | Viernes, 9 de junio de 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMProviderCopyright](metadata-constants.md)    | 2006 Lucerne Publishing LP, LLLP. All Rights Reserved.                                        |
| [g \_ wszWMDMTimeToLive](metadata-constants.md)           | 240                                                                                           |
| [g \_ wszWMDMTitle](metadata-constants.md)                | La publicación digital                                                                       |
| [g \_ wszWMDMWEBMASTER](metadata-constants.md)            | someone@example.com                                                                           |
| [g \_ wszWMDMYear](metadata-constants.md)                 | Viernes, 9 de junio de 2006 14:00:28 EDT                                                                 |



 

Asignación de elementos de imagen RSS a Windows valores de Administrador de dispositivos de contenido multimedia

En la tabla siguiente se describe cómo se asignan los valores de los elementos rss Image del ejemplo anterior a propiedades Windows media Administrador de dispositivos propiedades.



| Windows Propiedad Administrador de dispositivos multimedia                | Value                                            |
|------------------------------------------------------|--------------------------------------------------|
| [g \_ wszWMDMAlbumCoverFormat](metadata-constants.md) | GIF CON \_ FORMATO DE \_ OBJETO \_ WPD                         |
| [g \_ wszWMDMAlbumCoverSize](metadata-constants.md)   | 512                                              |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Logotipo de Lucerne                                     |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [g \_ wszWMDMHeight](metadata-constants.md)           | 300                                              |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [g \_ wszWMDMTitle](metadata-constants.md)            | Publicación de Lucerne                               |
| [g \_ wszWMDMWidth](metadata-constants.md)            | 300                                              |



 

Asignación de elementos rss a Windows de Administrador de dispositivos de elementos multimedia

En la tabla siguiente se describe cómo se asignan los valores de los elementos RSS Item del ejemplo anterior a propiedades Windows media Administrador de dispositivos propiedades.



| Windows Propiedad Administrador de dispositivos multimedia                | Value                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthor](metadata-constants.md)           | Lucerna                                                                                                                             |
| [g \_ wszWMDMAuthorDate](metadata-constants.md)       | Así, 1 de junio de 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Las publicaciones en línea cambian rápidamente. Un director general de una casa de publicación examina las tendencias de los últimos cinco años y sus implicaciones. |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMDuration](metadata-constants.md)         | 120325445                                                                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md) | Así, 1 de junio de 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMFileSize](metadata-constants.md)         | 10329011                                                                                                                            |
| [g \_ wszWMDMFormatCode](metadata-constants.md)       | WMDM \_ FORMATCODE \_ MP3                                                                                                               |
| [g \_ wszWMDMGenre](metadata-constants.md)            | Noticias                                                                                                                                |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md) | Así, 1 de junio de 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMMediaGuid](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMTitle](metadata-constants.md)            | La publicación digital                                                                                                             |
| [g \_ wszWMDMYear](metadata-constants.md)             | Así, 1 de junio de 2006 14:00:28 EDT                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes de metadatos**](metadata-constants.md)
</dt> </dl>

 

 




