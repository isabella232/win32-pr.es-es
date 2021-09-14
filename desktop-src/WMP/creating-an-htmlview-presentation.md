---
title: Creación de una presentación HTMLView
description: Creación de una presentación HTMLView
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Windows Listas de reproducción de metarchivos multimedia, presentaciones de HTMLView
- listas de reproducción, presentaciones de HTMLView
- listas de reproducción de metarchivo, presentaciones HTMLView
- Windows Listas de reproducción de metarchivos multimedia, creación de presentaciones HTMLView
- listas de reproducción, crear presentaciones HTMLView
- listas de reproducción de metarchivo, crear presentaciones HTMLView
- crear presentaciones HTMLView
- Reproductor de Windows Media, crear presentaciones HTMLView
- Reproductor de Windows Media,presentaciones HTMLView
- HTMLView, crear presentaciones
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967659"
---
# <a name="creating-an-htmlview-presentation"></a>Creación de una presentación HTMLView

Para crear una presentación básica de HTMLView, necesita al menos tres elementos:

-   **Contenido multimedia digital.** Se trata de uno o varios archivos de audio o vídeo que Reproductor de Windows Media reproducir.
-   **Una página web.** Este es el contenido basado en web que se muestra en la **característica Reproducción** ahora de la interfaz de usuario del reproductor.
-   **Un Windows metarchivo multimedia.** Esta es la lista de reproducción de metarchivo que Reproductor de Windows Media para combinar el contenido multimedia digital con la página web.

Un archivo .asx es un archivo de texto que proporciona información sobre una secuencia de archivos y su presentación. Según la lenguaje de marcado extensible (XML), los archivos .asx pueden contener una variedad de elementos, cada uno identificado por una etiqueta con atributos asociados. El **elemento PARAM** proporciona una manera de asociar un parámetro personalizado a una entrada determinada en una lista de reproducción de metarchivo o a todo el metarchivo. Uno de los nombres de parámetro predefinidos disponibles para su uso es "HTMLView". Este es el parámetro que hace que la página web especificada por el valor de dirección URL se muestre en Reproductor de Windows Media.

El código de ejemplo siguiente muestra un archivo .asx que combina un único archivo multimedia digital con una sola página web:


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



Cuando Reproductor de Windows Media el archivo .asx en el ejemplo anterior, reproduce el audio del archivo denominado content1.wma y abre la página web denominada htmlview.htm en la característica **Reproducción** ahora del reproductor en modo completo. El usuario puede pausar, buscar y detener el contenido de audio mediante Reproductor de Windows Media controles.

Puede cambiar fácilmente la página web que se muestra para cada fragmento de contenido asociando un elemento **PARAM** a cada entrada, como se muestra en el ejemplo de código siguiente:


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



En el ejemplo anterior, Reproductor de Windows Media muestra primero la página web htmlview1.htm mientras se reproduce el archivo de audio digital content1.wma. Cuando el reproductor abre la siguiente entrada en la lista de reproducción, content2.wma, la página web que se muestra en **Reproducción** ahora cambia a htmlview2.htm. De este modo, puede especificar qué página web ve el usuario para cada parte del contenido multimedia digital.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Reproductor de Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> </dl>

 

 




