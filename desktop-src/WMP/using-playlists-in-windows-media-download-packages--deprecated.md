---
title: Uso de listas de reproducción Windows paquetes de descarga multimedia (en desuso)
description: Uso de listas de reproducción Windows paquetes de descarga multimedia (en desuso)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Windows Metarchivos multimedia, Windows paquetes de descarga multimedia
- Reproductor de Windows Media,Windows paquetes de descarga multimedia
- metarchivos, Windows paquetes de descarga multimedia
- Windows Media,Windows paquetes de descarga multimedia
- listas de reproducción, Windows paquetes de descarga multimedia
- listas de reproducción de metarchivo, Windows paquetes de descarga multimedia
- Windows Listas de reproducción de metarchivos multimedia, Windows paquetes de descarga multimedia
- Windows Paquetes de descarga multimedia, listas de reproducción
- Windows Paquetes de descarga multimedia, listas de reproducción de metarchivo
- Windows Paquetes de descarga multimedia, listas Windows de metarchivo multimedia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65edfa1c49ae1f6a0573110a06d910d04c31e42d4744e88578f72220bf020272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134378"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a>Uso de listas de reproducción Windows paquetes de descarga multimedia (en desuso)

En esta página se documenta una característica que puede no estar disponible en versiones futuras de Reproductor de Windows Media y el SDK Reproductor de Windows Media.

Las listas de reproducción Windows metarchivos multimedia con una extensión de nombre de archivo .asx que proporcionan información Reproductor de Windows Media cómo reproducir el contenido empaquetado. Al combinar varios archivos de contenido en un único paquete de descarga multimedia Windows, puede controlar y personalizar el paquete de descarga multimedia de Windows mediante la lista de reproducción.

> [!Note]  
> En general, los paquetes de descarga multimedia de Windows usan listas de reproducción de metarchivos para hacer referencia al contenido multimedia del paquete en lugar de a una secuencia de un servidor en una intranet o En Internet. Sin embargo, se admiten referencias URL dentro del archivo .asx.

 

Con XML, el metarchivo proporciona la información que Reproductor de Windows Media para reproducir y mostrar contenido. Las listas de reproducción se han creado con varios elementos de código XML con sus etiquetas y atributos asociados. Cada elemento de una lista Windows de metarchivo multimedia define una configuración o acción determinadas en Reproductor de Windows Media.

El equipo del usuario asocia un metarchivo Windows multimedia que tiene una extensión de nombre de archivo .asx con Reproductor de Windows Media. Reproductor de Windows Media abre y analiza el código XML en el metarchivo, que contiene la ruta de acceso para buscar los archivos de audio o vídeo empaquetados. A continuación, el script de metarchivo controla la experiencia de audio, vídeo y gráfico. El metarchivo también contiene información que Reproductor de Windows Media procesos y se muestra en el cuadro desplegable de lista de reproducción. Inmediatamente después de mostrar la lista, se reproduce el primer elemento de la lista.

Una lista de reproducción de metarchivo es un acceso directo a los archivos que contienen el contenido empaquetado. El código siguiente es un ejemplo de un metarchivo que especifica el borde que se va a mostrar mediante el elemento **SKIN,** dos canciones que se reproducirán y la información de la lista de reproducción de cada canción.


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Bordes para Reproductor de Windows Media (en desuso)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Paquetes de descarga de medios (en desuso)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Windows Metarchivos multimedia**](windows-media-metafiles.md)
</dt> </dl>

 

 




