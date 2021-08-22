---
title: Modificar la pantalla
description: Modificar la pantalla
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Windows Listas de reproducción de metarchivo multimedia, pantallas de modificación
- listas de reproducción, pantallas de modificación
- listas de reproducción de metarchivo, pantallas de modificación
- Windows Listas de reproducción de metarchivo multimedia, modificación de pantalla
- playlists,display modification
- listas de reproducción de metarchivo, visualización de la modificación
- Reproductor de Windows Media, mostrar modificación
- Reproductor de Windows Media, se muestra la modificación
- Reproductor de Windows Media,propiedades de texto
- Reproductor de Windows Media,propiedades de imagen
- Reproductor de Windows Media,PROPIEDADES MOREINFO
- Reproductor de Windows Media,texto ABSTRACT
- Propiedades MOREINFO
- Texto abstracto
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e18ca15f71d9d25d9c99db36683a61b52057580022805c9d5f0f0d250aa738a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054613"
---
# <a name="modifying-the-display"></a>Modificar la pantalla

Las listas de reproducción pueden modificar Reproductor de Windows Media interfaz de usuario de cuatro maneras principales:

-   Propiedades de texto
-   Propiedades de la imagen
-   Propiedades MOREINFO
-   Texto abstracto

## <a name="text-properties"></a>Propiedades de texto

Reproductor de Windows Media permite mostrar texto de metadatos title, author, copyright y description. Los metadatos de recorte pueden proceden de la secuencia o del archivo multimedia, o bien pueden proceder de una lista de reproducción. Mostrar metadatos procede de la lista de reproducción. En general, las listas de reproducción son un mejor método para pasar propiedades de texto a Reproductor de Windows Media, especialmente si es probable que cambien los elementos de texto. Es más fácil editar texto en una lista de reproducción que volver a crear un archivo multimedia. Y dado que las propiedades leídas de una lista de reproducción invalidan las contenidas en el archivo multimedia, puede actualizar fácilmente el texto para mostrar agregando el nuevo texto a la propiedad correspondiente en una lista de reproducción. En el ejemplo siguiente, el texto de los metadatos Title y Author de la lista de reproducción invalida el texto Title y Author contenido en el archivo multimedia, sample.wma.

**El** texto DESCRIPTION se recupera de un archivo Windows Media al que se hace referencia en un **elemento ENTRY,** a menos que haya un elemento **ABSTRACT** en una lista de reproducción de metarchivo. Si hay texto **ABSTRACTo,** se mostrará, reemplazando el texto **DESCRIPTION.**


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a>Propiedades de la imagen

Las imágenes de banner se pueden agregar a la interfaz de usuario de Reproductor de Windows Media. El gráfico se puede usar para anunciar, proporcionar información y proporcionar acceso a sitios web, por nombrar algunas posibilidades.

Use el **elemento BANNER** para especificar una imagen gráfica (32 píxeles de alto por 194 píxeles de ancho) para mostrarla Reproductor de Windows Media. El gráfico se muestra debajo de cualquier contenido de vídeo. Se puede agregar un hipervínculo al banner mediante el **elemento secundario MOREINFO.**

Una información sobre herramientas se puede definir mediante un **elemento ABSTRACT** dentro del ámbito del **elemento BANNER.** Cualquier texto de información sobre herramientas definido se puede mostrar pausando el puntero del mouse sobre el gráfico de banner. Al seleccionar el gráfico de banner con el puntero del mouse, se activará cualquier hipervínculo definido con el **elemento MOREINFO.**

El formato de **gráfico BANNER** preferido es el formato GIF. El formato JPG se puede usar si el gráfico tiene el tamaño correcto.

En el ejemplo anterior se muestra el uso del **elemento BANNER.**

> [!Note]  
> **Las imágenes BANNER** no se admiten con archivos DRM o cuando Reproductor de Windows Media se inserta en una página web.

 

Para obtener más información sobre los banners, vea [Gráficos personalizados en Reproductor de Windows Media](custom-graphics-in-windows-media-player.md).

## <a name="moreinfo-properties"></a>Propiedades MOREINFO

Las áreas de texto e imagen de la interfaz de usuario se pueden asociar a direcciones URL. Durante la reproducción, los usuarios pueden seleccionar una de estas secciones para conectarse a la dirección URL asociada a ella en su explorador web. Por ejemplo, puede asociar el sitio web de un anunciante a una imagen de banner de anuncio, como se muestra en el siguiente fragmento de código.


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a>Texto abstracto

**El** texto abstracto se usa para mostrar una breve descripción emergente de las áreas de texto o imagen de la interfaz de usuario a la que está asociada. Durante la reproducción, si el puntero del mouse mantiene el puntero sobre una de estas áreas, aparece una información sobre herramientas junto al puntero del mouse que muestra el texto **ABSTRACT** asociado al área. **El** texto ABSTRACT se recupera de un metarchivo y se define con el **elemento ABSTRACT.** El **elemento ABSTRACT** puede ser un elemento secundario de un elemento **ENTRY** o **banner.**

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

 

 




