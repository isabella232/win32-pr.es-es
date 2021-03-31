---
title: Usar listas de reproducción en paquetes de descarga de Windows Media (en desuso)
description: Usar listas de reproducción en paquetes de descarga de Windows Media (en desuso)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Metaarchivos de Windows Media, paquetes de descarga de Windows Media
- Windows Media Player, paquetes de descarga de Windows Media
- metaarchivos, paquetes de descarga de Windows Media
- Windows Media, paquetes de descarga de Windows Media
- listas de reproducción, paquetes de descarga de Windows Media
- listas de reproducción de metarchivos, paquetes de descarga de Windows Media
- Listas de reproducción de metarchivos de Windows Media, paquetes de descarga de Windows Media
- Paquetes de descarga de Windows Media, listas de reproducción
- Paquetes de descarga de Windows Media, listas de reproducción de metarchivos
- Paquetes de descarga de Windows Media, listas de reproducción de metarchivo de Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418960"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a>Usar listas de reproducción en paquetes de descarga de Windows Media (en desuso)

En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.

Las listas de reproducción son metaarchivos de Windows Media con una extensión de nombre de archivo. ASX que proporcionan información que indica a Windows Media Player Cómo reproducir el contenido empaquetado. Mediante la combinación de varios archivos de contenido en un único paquete de descarga de Windows Media, puede controlar y personalizar el paquete de descarga de Windows Media mediante la lista de reproducción.

> [!Note]  
> En general, los paquetes de descarga de Windows Media usan listas de reproducción de metarchivos para hacer referencia al contenido multimedia del paquete en lugar de a un flujo de un servidor en una intranet o en Internet. Sin embargo, se admiten las referencias URL dentro del archivo. ASX.

 

Con XML, el metarchivo proporciona la información que Windows Media Player usa para reproducir y mostrar el contenido. Las listas de reproducción se componen de varios elementos de código XML con sus etiquetas y atributos asociados. Cada elemento de una lista de reproducción de metarchivo de Windows Media define una opción o acción determinada en Windows Media Player.

El equipo del usuario asocia un metarchivo de Windows Media que tiene una extensión de nombre de archivo. ASX con Windows Media Player. Windows Media Player abre y analiza el código XML del metarchivo, que contiene la ruta de acceso para buscar los archivos de audio o vídeo empaquetados. A continuación, el script de metarchivo controla el audio, el vídeo y la experiencia gráfica. El metarchivo también contiene información que Windows Media Player procesa y muestra en el cuadro desplegable lista de reproducción. Inmediatamente después de que se muestre la lista, se reproducirá el primer elemento de la lista.

Una lista de reproducción de metarchivo es un acceso directo a los archivos que contienen el contenido empaquetado. El código siguiente es un ejemplo de un metarchivo que especifica el borde que se va a mostrar mediante el elemento **Skin** , dos canciones que se van a reproducir y la información de la lista de reproducción de cada canción.


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

[**Bordes de Media Player de Windows (desusado)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Paquetes de descarga de Windows Media (en desuso)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Metaarchivos de Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 




