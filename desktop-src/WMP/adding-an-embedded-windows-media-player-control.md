---
title: Adición de un control Reproductor de Windows Media integrado
description: Adición de un control Reproductor de Windows Media integrado
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Windows Listas de reproducción de metarchivos multimedia, agregar controles Reproductor de Windows Media insertados
- listas de reproducción, agregar controles Reproductor de Windows Media integrados
- listas de reproducción de metarchivo, agregar controles Reproductor de Windows Media insertados
- Windows Listas de reproducción de metarchivos multimedia, controles Reproductor de Windows Media insertados
- listas de reproducción, controles Reproductor de Windows Media insertados
- listas de reproducción de metarchivo, controles Reproductor de Windows Media insertados
- agregar controles Reproductor de Windows Media insertados
- controles Reproductor de Windows Media insertados
- Reproductor de Windows Media, agregar controles incrustados
- Reproductor de Windows Media,controles incrustados
- HTMLView, agregar controles Reproductor de Windows Media insertados
- HTMLView, controles Reproductor de Windows Media insertados
- HTMLView,Reproductor de Windows Media de objetos
- HTMLView,Player object model
- Reproductor de Windows Media de objetos, acerca de
- modelo de objetos, acerca de
- Objeto Player
- Windows Media,Player object model
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e6d4b2f6fcbadde7b8914571af7e56f18c546fddfe10cfe0069e795f6f275e39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055523"
---
# <a name="adding-an-embedded-windows-media-player-control"></a>Adición de un control Reproductor de Windows Media integrado

Hay dos razones por las que podría considerar la posibilidad de agregar una instancia insertda de Reproductor de Windows Media a la presentación de HTMLView. En primer lugar, si desea mostrar contenido de vídeo, debe usar el control Reproductor de Windows Media ActiveX vídeo. En segundo lugar, si desea aprovechar las características del modelo de objetos Reproductor de Windows Media desde la página web htmlView, debe usar una instancia del control Player para hacerlo.

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a>Uso del control Player para mostrar vídeo en contenido HTMLView

Normalmente, Reproductor de Windows Media vídeo mediante el panel Vídeo y visualización de la **característica Reproducción** ahora. Puesto que HTMLView usa esta área para mostrar la página web, debe proporcionar un área de visualización de vídeo adicional si desea que el reproductor reprodgue vídeo. Esto es fácil de hacer mediante el control Reproductor de Windows Media ActiveX.

Para usar el control Player para mostrar vídeo, inserte el control en la página web HTMLView mediante la **etiqueta OBJECT.** Esta es la misma técnica que se usa para insertar el control Player en cualquier página web en la que quiera mostrar el vídeo. El código de ejemplo siguiente muestra la sintaxis básica para insertar el control Player en Internet Explorer:


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



El *parámetro autoStart* garantiza que el contenido se reproduce automáticamente cada vez que se especifica una nueva dirección URL. El valor que especifique para *uiMode* es usted, pero normalmente querrá especificar "none" al crear contenido para presentaciones HTMLView. Al insertar el control Reproductor de Windows Media para mostrar vídeo de esta manera, el usuario puede controlar la reproducción mediante los controles del reproductor en modo completo, por lo que no es necesario proporcionar controles de transporte adicionales en la página web. Puede usar el espacio que normalmente asignaría a los controles de transporte para mostrar más texto, gráficos o vínculos a otro contenido.

No especifique un parámetro *de dirección URL* al insertar el control Reproductor de Windows Media en una página web diseñada para mostrarse en una presentación HTMLView. En su lugar, especifique los archivos multimedia digitales en el archivo .asx que abre el contenido.

Dado que proporciona la región de visualización de vídeo en la página web HTMLView, puede decidir dónde colocar el vídeo y el tamaño que desea que sea la región de presentación. Por ejemplo, puede contener el objeto **Player** dentro de un elemento **DIV HTML** y, a continuación, especificar la posición del **DIV** para situar la presentación del vídeo en la página web. Puede cambiar las dimensiones de la presentación de vídeo especificando valores para los atributos de alto y ancho del **elemento OBJECT.** También puede especificar estos valores mediante código de script.

## <a name="using-the-player-object-model"></a>Uso del modelo de objetos player

El Reproductor de Windows Media de objetos expone propiedades, métodos y eventos que puede usar en las páginas web de HTMLView. Al insertar el control Reproductor de Windows Media ActiveX en la página web HTMLView, tendrá acceso automáticamente al modelo de objetos Player.

Si inserta el control Reproductor de Windows Media en la página web HTMLView, no use el modelo de objetos Player para especificar el archivo multimedia digital que se va a reproducir. Por ejemplo, si usa código de script para especificar un valor para la propiedad **URL** del control incrustado, la página web HTMLView se descargará de la característica **Reproducción** ahora cuando se reproduce el archivo multimedia digital. Para evitar que esto suceda, abra siempre archivos .asx que incluyan parámetros HTMLView cuando necesite usar el script para abrir contenido multimedia digital desde la página web htmlView.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Reproductor de Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player.uiMode**](player-uimode.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> <dt>

[**Configuración.autoStart**](settings-autostart.md)
</dt> </dl>

 

 




