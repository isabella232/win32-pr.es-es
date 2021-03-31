---
title: Ventajas del uso de HTMLView
description: Ventajas del uso de HTMLView
ms.assetid: bbec9471-87f1-4c41-a322-f11e9e1dec37
keywords:
- Listas de reproducción de metarchivos de Windows Media, ventajas de HTMLView
- listas de reproducción, ventajas de HTMLView
- listas de reproducción de metarchivos, ventajas de HTMLView
- Listas de reproducción de metarchivos de Windows Media, ventajas de HTMLView
- listas de reproducción, ventajas de HTMLView
- listas de reproducción de metarchivos, ventajas de HTMLView
- ventajas de HTMLView
- Windows Media Player, ventajas de HTMLView
- Media Player de Windows, ventajas de HTMLView
- HTMLView, ventajas
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5e5409db969f5e9a8e0df18738f4995490b1d83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418920"
---
# <a name="advantages-of-using-htmlview"></a>Ventajas del uso de HTMLView

La característica HTMLView facilita la creación de una experiencia de usuario integrada basada en Web que reproduce contenido multimedia digital mediante el conocido aspecto de la Web. Al combinar contenido basado en Web con contenido multimedia digital en la interfaz de usuario (IU) de Windows Media Player, el resultado puede tener un mayor impacto en el usuario que cuando los elementos se ven por separado. El contenido multimedia digital se ha mejorado mediante información relacionada interesante, mientras que la página web puede proporcionar vínculos a contenido similar, lo que crea nuevas oportunidades de negocio.

## <a name="htmlview-provides-a-better-user-experience"></a>HTMLView ofrece una mejor experiencia de usuario

Los usuarios quieren tener acceso a la información que se puede ofrecer con el contenido multimedia digital, pero no quieren tratar con una serie aparentemente infinita de anuncios emergentes. El uso de ventanas emergentes del explorador para mostrar publicidad en la web ha dejado de ser tan frecuente que hay software que impide que se abran estas ventanas. Este software puede tener el efecto secundario de evitar que se muestren páginas web legítimas, a veces suprimir una presentación completa de medios digitales.

Cuando se usa la característica HTMLView, los usuarios ya no tienen que tratar con ventanas emergentes. En lugar de tener que abrir una ventana independiente del explorador para proporcionar información adicional al usuario, puede mostrar contenido personalizado basado en Web en la característica **reproducción en curso** de la interfaz de usuario de Windows Media Player mientras el reproductor reproduce el contenido de audio o vídeo que el usuario desea. Los usuarios pueden controlar la reproducción mediante los controles de Media Player de Windows. Puesto que el contenido se reproduce en el reproductor en modo completo, el software diseñado para evitar anuncios emergentes no impide que los usuarios disfruten del contenido.

## <a name="htmlview-content-is-easy-to-create"></a>El contenido de HTMLView es fácil de crear

Como implica el nombre de la característica, se crea contenido basado en Web que se muestra mediante la característica HTMLView mediante Lenguaje de marcado de hipertexto (HTML). Si ya crea contenido para la web, esto significa que no tiene que aprender un nuevo lenguaje de programación para crear fácilmente contenido enriquecido con la característica HTMLView. Si ya tiene páginas web con un control ActiveX de Windows Media Player incrustado, puede hacer que estas páginas aparezcan en la interfaz de usuario del reproductor simplemente apuntando a estas páginas web de un metarchivo de Windows Media (archivo. ASX) mediante un parámetro especial.

Windows Media Player usa una instancia incrustada de Microsoft Internet Explorer para mostrar el contenido de HTMLView. Esto significa que no tiene que tener en cuenta diferentes exploradores de Internet, varios modelos de scripting o distintos lenguajes de scripting al crear las páginas Web. Aunque el usuario no use Internet Explorer como su explorador predeterminado, la página web se seguirá mostrando correctamente en el reproductor.

Es posible que un programa distinto de Windows Media Player se registre como el programa predeterminado para abrir archivos. ASX. El modelo de objetos de la serie Windows Media Player 9 o posterior incluye un nuevo método, **openPlayer**, que le permite especificar un localizador uniforme de recursos (URL) para el contenido que desea reproducir. Cuando se usa el método **openPlayer** , Windows Media Player siempre se abre en modo completo para reproducir el contenido especificado. Con este método, puede asegurarse de que el contenido de HTMLView se muestra en Windows Media Player, en lugar de en otra aplicación que ha asumido la Asociación de tipo de archivo. ASX.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. openPlayer**](player-openplayer.md)
</dt> </dl>

 

 




