---
title: Agregar un control de Media Player de Windows incrustado
description: Agregar un control de Media Player de Windows incrustado
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Listas de reproducción de metarchivos de Windows Media, agregar controles de Media Player de Windows incrustados
- listas de reproducción, agregar controles de Media Player de Windows incrustados
- listas de reproducción de metarchivos, agregar controles de Media Player de Windows incrustados
- Listas de reproducción de metarchivo de Windows Media, controles de Media Player de Windows incrustados
- listas de reproducción, controles de Media Player de Windows incrustados
- listas de reproducción de metarchivos, controles de Media Player de Windows incrustados
- Agregar controles de Media Player de Windows incrustados
- controles de Media Player de Windows incrustados
- Windows Media Player, agregar controles incrustados
- Windows Media Player, controles incrustados
- HTMLView, agregar controles de Media Player de Windows incrustados
- HTMLView, controles de Windows Media Player insertados
- HTMLView, modelo de objetos de Windows Media Player
- HTMLView, modelo de objetos de Player
- Modelo de objetos de Windows Media Player, acerca de
- modelo de objetos, acerca de
- Objeto Player
- Windows Media, modelo de objetos de reproductor
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418904"
---
# <a name="adding-an-embedded-windows-media-player-control"></a>Agregar un control de Media Player de Windows incrustado

Hay dos razones por las que podría considerar la posibilidad de agregar una instancia incrustada de Windows Media Player a la presentación de HTMLView. En primer lugar, si desea mostrar el contenido de vídeo, debe utilizar el control ActiveX de Windows Media Player. En segundo lugar, si desea sacar partido de las características del modelo de objetos de Windows Media Player desde la Página Web de HTMLView, debe usar una instancia del control del reproductor para hacerlo.

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a>Usar el control Player para mostrar vídeo en el contenido de HTMLView

Normalmente, Windows Media Player muestra vídeo con el panel de vídeo y visualización de la característica de **reproducción en curso** . Puesto que HTMLView usa esta área para mostrar la página web, debe proporcionar un área de presentación de vídeo adicional si desea que el reproductor Reproduzca vídeo. Esto es fácil de hacer mediante el control ActiveX de Windows Media Player.

Para usar el control de reproducción para mostrar vídeo, inserte el control en la Página Web de HTMLView mediante la etiqueta de **objeto** . Se trata de la misma técnica que se usa para incrustar el control de reproductor en cualquier página web en la que desee mostrar vídeo. En el ejemplo de código siguiente se muestra la sintaxis básica para insertar el control Player en Internet Explorer:


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



El parámetro de *Inicio automático* garantiza que el contenido se reproduzca automáticamente cada vez que se especifique una nueva dirección URL. El valor que especifique para *uiMode* depende de usted, pero normalmente querrá especificar "none" al crear contenido para las presentaciones de HTMLView. Al incrustar el control Media Player de Windows para mostrar vídeo de esta manera, el usuario puede controlar la reproducción mediante los controles del reproductor en modo completo, por lo que no es necesario proporcionar controles de transporte adicionales en la Página Web. Puede usar el espacio que normalmente asignaría a los controles de transporte para mostrar más texto, gráficos o vínculos a otro contenido.

No especifique un parámetro de *dirección URL* al insertar el control Media Player de Windows en una página web diseñada para mostrarse en una presentación de HTMLView. En su lugar, especifique los archivos multimedia digitales en el archivo. ASX que abre el contenido.

Dado que proporciona la región de presentación de vídeo en la Página Web de HTMLView, puede decidir dónde colocar el vídeo y el tamaño que desea que tenga la región de visualización. Por ejemplo, puede contener el objeto **Player** dentro de un elemento HTML **div** y, a continuación, especificar la posición del **div** para situar la presentación de vídeo en la Página Web. Puede cambiar las dimensiones de la presentación de vídeo especificando los valores de los atributos de alto y ancho del elemento de **objeto** . También puede especificar estos valores mediante el código de script.

## <a name="using-the-player-object-model"></a>Usar el modelo de objetos Player

El modelo de objetos de Windows Media Player expone propiedades, métodos y eventos que se pueden usar en las páginas web de HTMLView. Al incrustar el control ActiveX de Windows Media Player en la Página Web de HTMLView, tiene acceso automáticamente al modelo de objetos de Player.

Si incrusta el control Media Player de Windows en la Página Web de HTMLView, no use el modelo de objetos del reproductor para especificar el archivo multimedia digital que se va a reproducir. Por ejemplo, si utiliza código de script para especificar un valor para la propiedad **URL** del control incrustado, la Página Web de HTMLView se descargará de la característica **reproducción en curso** cuando se reproduzca el archivo multimedia digital. Para evitar que esto suceda, abra siempre los archivos. ASX que incluyen los parámetros HTMLView cuando necesite usar el script para abrir el contenido multimedia digital de la Página Web de HTMLView.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Configuración. Inicio automático**](settings-autostart.md)
</dt> </dl>

 

 




