---
title: Crear una presentación de HTMLView
description: Crear una presentación de HTMLView
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Listas de reproducción de metarchivos de Windows Media, presentaciones de HTMLView
- listas de reproducción, presentaciones de HTMLView
- listas de reproducción de metarchivos, presentaciones de HTMLView
- Listas de reproducción de metarchivos de Windows Media, crear presentaciones HTMLView
- listas de reproducción, creación de presentaciones HTMLView
- listas de reproducción de metarchivos, crear presentaciones HTMLView
- crear presentaciones de HTMLView
- Windows Media Player, crear presentaciones de HTMLView
- Media Player de Windows, presentaciones de HTMLView
- HTMLView, crear presentaciones
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418857"
---
# <a name="creating-an-htmlview-presentation"></a>Crear una presentación de HTMLView

Para crear una presentación HTMLView básica, necesita al menos tres elementos:

-   **Contenido multimedia digital.** Se trata de uno o más archivos de audio o vídeo que Windows Media Player reproduce.
-   **Una página web.** Este es el contenido basado en Web que se muestra en la característica **reproducción en curso** de la interfaz de usuario del reproductor.
-   **Un metarchivo de Windows Media.** Esta es la lista de reproducción de metarchivo que dirige a Windows Media Player para combinar el contenido multimedia digital con la Página Web.

Un archivo. ASX es un archivo de texto que proporciona información acerca de una secuencia de archivos y su presentación. En función de la sintaxis de lenguaje de marcado extensible (XML), los archivos. ASX pueden contener una variedad de elementos, cada uno identificado por una etiqueta con atributos asociados. El elemento **param** proporciona una manera de asociar un parámetro personalizado a una entrada determinada en una lista de reproducción de metarchivo o en todo el metarchivo. Uno de los nombres de parámetro predefinidos disponibles para su uso es "HTMLView". Este es el parámetro que hace que la Página Web especificada por el valor de dirección URL se muestre en Windows Media Player.

En el ejemplo de código siguiente se muestra un archivo. ASX que combina un solo archivo multimedia digital con una única página web:


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



Cuando Windows Media Player abre el archivo. asx en el ejemplo anterior, reproduce el audio desde el archivo denominado Content1. WMA y abre la página web llamada htmlview.htm en la característica **reproducción en curso** del reproductor en modo completo. El usuario puede pausar, buscar y detener el contenido de audio mediante los controles de Media Player de Windows.

Puede cambiar fácilmente la página web que se muestra para cada elemento de contenido asociando un elemento **param** a cada entrada, como se muestra en el ejemplo de código siguiente:


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



En el ejemplo anterior, Windows Media Player primero muestra la página web htmlview1.htm mientras se reproduce el archivo de audio digital Content1. WMA. Cuando el reproductor Abra la entrada siguiente en la lista de reproducción, content2. WMA, la página web que se muestra en **ahora se reproducen** los cambios en htmlview2.htm. De esta forma, puede especificar la página web que el usuario verá para cada parte de contenido multimedia digital.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> </dl>

 

 




