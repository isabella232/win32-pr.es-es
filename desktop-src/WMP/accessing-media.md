---
title: Obtener acceso a medios
description: Obtener acceso a medios
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Listas de reproducción de metarchivos de Windows Media, acceso a medios
- listas de reproducción, acceso a medios
- listas de reproducción de metarchivos, acceso a medios
- Listas de reproducción de metarchivos de Windows Media, acceso a medios
- listas de reproducción, acceso a medios
- listas de reproducción de metarchivos, acceso a medios
- Listas de reproducción de metarchivo de Windows Media, controlar la reproducción
- listas de reproducción, controlar la reproducción
- listas de reproducción de metarchivos, controlar la reproducción
- Listas de reproducción de metarchivos de Windows Media, configuración de duración
- listas de reproducción, configuración de la duración
- listas de reproducción de metarchivos, establecer duración
- Windows Media Player, acceso a medios
- Media Player de Windows, acceso a medios
- Windows Media Player, controlar la reproducción
- Windows Media Player, establecer la duración
- obtener acceso a medios
- acceso a medios
- controlar la reproducción
- configuración de la duración
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5a995a6816e3c46a002bd1ea924c9ea9a207000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695406"
---
# <a name="accessing-media"></a>Obtener acceso a medios

Use listas de reproducción para especificar y controlar los archivos multimedia o multimedia de streaming que reproduce Windows Media Player.

Use el elemento **entry** para especificar un elemento multimedia único (un archivo multimedia o una secuencia en directo) y los elementos secundarios (como imágenes, vínculos **MOREINFO** y texto **abstracto** ). Use un elemento **ENTRYREF** para especificar una lista de reproducción. Una lista de reproducción puede contener uno o varios elementos de **entrada** o **ENTRYREF** . Windows Media Player ejecuta una lista de reproducción empezando por la primera entrada y reproduciendo cada entrada a su vez hasta que se complete la lista.

Un elemento de **entrada** puede apuntar a cualquier tipo de medio que Windows Media Player pueda reproducir. Esto incluye no solo archivos. WMA,. wmv,. ASF y. avi, por nombrar algunos, pero también secuencias en directo. Mediante el uso de una serie de elementos **entry** o **ENTRYREF** para hacer referencia a contenido multimedia, puede usar una lista de reproducción para enviar un flujo único compuesto por varios orígenes. Los flujos a los que se hace referencia se reproducirán secuencialmente y el visor lo verá como una secuencia continua. Por ejemplo, la lista de reproducción puede contener dos elementos de **entrada** : una introducción estándar de un archivo de Windows Media con una extensión. WMA y una secuencia de medios de Windows activa.

> [!Note]  
> Una lista de reproducción no debe contener vínculos a archivos multimedia que tengan contenido creado con versiones diferentes de Rights Management digitales (DRM). En una lista de reproducción de metarchivo, si hay vínculos para archivos multimedia con contenido de DRM versión 1 y para archivos multimedia creados con versiones posteriores de DRM, Windows Media Player solo reproducirá el contenido de DRM versión 1.

 

## <a name="controlling-playback"></a>Controlar la reproducción

Use listas de reproducción para controlar no solo qué clip multimedia se reproduce, sino también qué partes del clip se reproducen y cómo. Puede usar listas de reproducción para definir un conjunto de clips que se repiten o se repiten, para establecer la duración de la reproducción y para asignar las horas de inicio, así como los marcadores de inicio y finalización de cada entrada. Los elementos **STARTTIME**, **STARTMARKER** y **ENDMARKER** funcionan junto con los marcadores del archivo multimedia.

Por ejemplo, la siguiente lista de reproducción usa un banner de AD y el vínculo de **MOREINFO** asociado en una **entrada** y hace referencia a **STARTMARKER** y **ENDMARKER**.


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a>Configuración de la duración

Use el elemento **Duration** para especificar cuánto tiempo se reproduce un clip o un conjunto de clips. También puede usar el atributo **PREVIEWMODE** del elemento **ASX** junto con el elemento **PREVIEWDURATION** para especificar cuánto tiempo se reproduce un clip o un conjunto de clips. Establezca el atributo **PREVIEWMODE** en sí para usar el elemento **PREVIEWDURATION** para especificar cuánto tiempo se va a reproducir el clip asociado. Los elementos **PREVIEWDURATION** y **Duration** tienen el mismo comportamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Usar listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




