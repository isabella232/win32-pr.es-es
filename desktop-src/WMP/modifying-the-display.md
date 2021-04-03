---
title: Modificar la presentación
description: Modificar la presentación
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Listas de reproducción de metarchivos de Windows Media, modificar pantallas
- listas de reproducción, modificar pantallas
- listas de reproducción de metarchivos, modificar pantallas
- Listas de reproducción de metarchivos de Windows Media, modificación de pantalla
- listas de reproducción, modificación de pantalla
- listas de reproducción de metarchivos, modificación de pantalla
- Windows Media Player, modificación de la presentación
- Windows Media Player, modificar pantallas
- Media Player de Windows, propiedades de texto
- Windows Media Player, propiedades de imagen
- Media Player de Windows, propiedades de MOREINFO
- Media Player de Windows, texto ABSTRACTo
- Propiedades de MOREINFO
- Texto ABSTRACTo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075508"
---
# <a name="modifying-the-display"></a>Modificar la presentación

Las listas de reproducción pueden modificar la interfaz de usuario de Media Player de Windows de cuatro maneras principales:

-   Propiedades de texto
-   Propiedades de la imagen
-   Propiedades de MOREINFO
-   Texto ABSTRACTo

## <a name="text-properties"></a>Propiedades de texto

Windows Media Player habilita la presentación de texto de metadatos de título, autor, copyright y descripción. Los metadatos de clip pueden provienen de la secuencia o el archivo multimedia, o pueden proviene de una lista de reproducción. Mostrar metadatos proceden de la lista de reproducción. En general, las listas de reproducción son un método mejor para pasar las propiedades de texto a Windows Media Player, especialmente si es probable que los elementos de texto cambien. Es más fácil editar el texto de una lista de reproducción que volver a crear un archivo multimedia. Y dado que las propiedades leídas de una lista de reproducción invalidan las contenidas en el archivo multimedia, puede actualizar fácilmente el texto de la pantalla agregando el nuevo texto a la propiedad correspondiente en una lista de reproducción. En el ejemplo siguiente, el texto de los metadatos de título y de autor de la lista de reproducción invalida el título y el texto del autor contenidos en el archivo multimedia, sample. WMA.

El texto de **Descripción** se recupera de un archivo de Windows Media al que se hace referencia en un elemento de **entrada** a menos que haya un elemento **abstracto** en una lista de reproducción de metarchivo. Si hay texto **abstracto** , se mostrará, reemplazando el texto de **Descripción** .


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

Se pueden agregar imágenes de banner a la interfaz de usuario de Windows Media Player. El gráfico se puede usar para anunciar, proporcionar información y proporcionar acceso a sitios web, para nombrar algunas posibilidades.

Use el elemento **banner** para especificar una imagen gráfica (32 píxeles de alto por 194 píxeles de ancho) para que la muestre Windows Media Player. El gráfico se muestra debajo de cualquier contenido de vídeo. Se puede Agregar un hipervínculo al banner mediante el elemento secundario **MOREINFO** .

Una información sobre herramientas se puede definir mediante un elemento **abstract** dentro del ámbito del elemento **banner** . Cualquier texto de información sobre herramientas definido se puede mostrar al pausar el puntero del mouse sobre el gráfico del banner. Al seleccionar el gráfico de encabezado con el puntero del mouse se activará cualquier hipervínculo definido con el elemento **MOREINFO** .

El formato de gráfico de **banner** preferido es el formato GIF. Se puede usar el formato JPG si el gráfico tiene el tamaño adecuado.

En el ejemplo anterior se muestra el uso del elemento **banner** .

> [!Note]  
> Las imágenes de **banner** no son compatibles con los archivos DRM o cuando Windows Media Player está incrustado en una página web.

 

Para obtener más información sobre los banners, vea [gráficos personalizados en Windows Media Player](custom-graphics-in-windows-media-player.md).

## <a name="moreinfo-properties"></a>Propiedades de MOREINFO

Las áreas de texto e imagen de la interfaz de usuario pueden asociarse con direcciones URL. Durante la reproducción, los usuarios pueden seleccionar una de estas secciones para conectarse a la dirección URL asociada a ella en su explorador Web. Por ejemplo, puede asociar el sitio web de un anunciante a una imagen de banner de ad, como se muestra en el siguiente fragmento de código.


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a>Texto ABSTRACTo

Texto **abstracto** se usa para mostrar una breve descripción emergente de las áreas de texto o imagen de la interfaz de usuario a la que está asociada. Durante la reproducción, si el puntero del mouse se desplaza sobre una de estas áreas, aparece una información sobre herramientas junto al puntero del mouse que muestra el texto **abstracto** asociado al área. El texto **abstracto** se recupera de un metarchivo y se define con el elemento **abstracto** . El elemento **abstracto** puede ser un elemento secundario de una **entrada** o un elemento **banner** .

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

 

 




