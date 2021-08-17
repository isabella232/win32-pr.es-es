---
title: Acceso a medios
description: Acceso a medios
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Windows Listas de reproducción de metarchivo multimedia, acceso a medios
- listas de reproducción, acceso a medios
- listas de reproducción de metarchivo, acceso a medios
- Windows Listas de reproducción de metarchivo multimedia, acceso multimedia
- listas de reproducción, acceso multimedia
- listas de reproducción de metarchivo, acceso multimedia
- Windows Listas de reproducción de metarchivo multimedia, controlar la reproducción
- listas de reproducción, controlar la reproducción
- listas de reproducción de metarchivo, controlar la reproducción
- Windows Listas de reproducción de metarchivo multimedia, establecer la duración
- playlists,setting duration
- listas de reproducción de metarchivo, establecer la duración
- Reproductor de Windows Media, acceso a medios
- Reproductor de Windows Media,acceso multimedia
- Reproductor de Windows Media, controlar la reproducción
- Reproductor de Windows Media, establecer la duración
- acceso a medios
- acceso multimedia
- controlar la reproducción
- duración de la configuración
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c1a0846be4e8b9b62e424ce24d1b1800bc361c6a28f52a323c6bfa8511ae040b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956405"
---
# <a name="accessing-media"></a>Acceso a medios

Use listas de reproducción para especificar y controlar los archivos multimedia o multimedia de streaming que Reproductor de Windows Media reproducir.

Use el **elemento ENTRY** para especificar un único elemento multimedia (un archivo multimedia o una secuencia en vivo) y cualquier elemento secundario (como imágenes, vínculos **MOREINFO** y **texto ABSTRACTo).** Use un **elemento ENTRYREF** para especificar una lista de reproducción. Una lista de reproducción puede contener uno o varios **elementos ENTRY** **o ENTRYREF.** Reproductor de Windows Media una lista de reproducción empezando por la primera entrada y, a continuación, reproduciendo cada entrada a su vez hasta que finalice la lista.

Un **elemento ENTRY** puede apuntar a cualquier tipo de medio que Reproductor de Windows Media reproducir. Esto incluye no solo archivos .wma, .wmv, .asf y .avi, por nombrar algunos, sino también transmisiones en vivo. Mediante el uso de una serie de **elementos ENTRY** o **ENTRYREF** para hacer referencia al contenido multimedia, puede usar una lista de reproducción para enviar una única secuencia que consta de varios orígenes. Las secuencias a las que se hace referencia se reproducirán secuencialmente y el visor las verá como una secuencia continua. Por ejemplo, la lista de reproducción puede contener dos elementos **ENTRY:** una introducción estándar de un archivo Windows Media con una extensión .wma y una secuencia multimedia Windows en directo.

> [!Note]  
> Una lista de reproducción no debe contener vínculos a archivos multimedia que tengan contenido creado con diferentes versiones de Digital Rights Management (DRM). En una lista de reproducción de metarchivo, si hay vínculos para archivos multimedia con contenido drm versión 1 y para archivos multimedia creados con versiones posteriores de DRM, Reproductor de Windows Media reproducirá solo el contenido de la versión 1 de DRM.

 

## <a name="controlling-playback"></a>Controlar la reproducción

Use listas de reproducción para controlar no solo qué clip multimedia se reproduce, sino también qué partes del clip se reproducen y cómo. Puede usar listas de reproducción para definir un conjunto de clips que se va a recorrer en bucle o repetir, para establecer la duración del juego y para asignar horas de inicio y marcadores de inicio y finalización para cada entrada. Los **elementos STARTTIME,** **STARTMARKER** y **ENDMARKER** funcionan junto con marcadores en el archivo multimedia.

Por ejemplo, la siguiente lista de reproducción usa un banner de anuncio y el vínculo **MOREINFO** asociado en una **entrada** y hace referencia a **STARTMARKER** **y ENDMARKER**.


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



## <a name="setting-duration"></a>Establecer duración

Use el **elemento DURATION** para especificar cuánto tiempo se va a reproducir un clip o un conjunto de clips. También puede usar el atributo **PREVIEWMODE** del elemento **ASX** junto con el elemento **PREVIEWDURATION** para especificar cuánto tiempo se debe reproducir un clip o un conjunto de clips. Establezca el **atributo PREVIEWMODE** en YES para usar el **elemento PREVIEWDURATION** para especificar cuánto tiempo se reproducirá el clip asociado. Los **elementos PREVIEWDURATION** **y DURATION** tienen el mismo comportamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Listas de reproducción de metarchivo**](metafile-playlists.md)
</dt> <dt>

[**Uso de listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




