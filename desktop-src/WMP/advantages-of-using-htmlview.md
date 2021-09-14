---
title: Ventajas de usar HTMLView
description: Ventajas de usar HTMLView
ms.assetid: bbec9471-87f1-4c41-a322-f11e9e1dec37
keywords:
- Windows Listas de reproducción de metarchivos multimedia, ventajas de HTMLView
- listas de reproducción, ventajas de HTMLView
- listas de reproducción de metarchivo, ventajas de HTMLView
- Windows Listas de reproducción de metarchivos multimedia, ventajas de HTMLView
- listas de reproducción, ventajas de HTMLView
- listas de reproducción de metarchivo, ventajas de HTMLView
- ventajas de HTMLView
- Reproductor de Windows Media,ventajas de HTMLView
- Reproductor de Windows Media, ventajas de HTMLView
- HTMLView, ventajas
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5e5409db969f5e9a8e0df18738f4995490b1d83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890188"
---
# <a name="advantages-of-using-htmlview"></a>Ventajas de usar HTMLView

La característica HTMLView facilita la creación de una experiencia de usuario basada en web integrada que reproduce contenido multimedia digital mediante el aspecto conocido de la Web. Al combinar contenido basado en web con contenido multimedia digital en la interfaz de usuario (UI) de Reproductor de Windows Media, el resultado puede tener un mayor impacto en el usuario que cuando los elementos se ven por separado. El contenido multimedia digital se mejora con información relacionada interesante, mientras que la página web puede proporcionar vínculos a contenido similar, lo que crea nuevas oportunidades de negocio.

## <a name="htmlview-provides-a-better-user-experience"></a>HTMLView proporciona una mejor experiencia de usuario

Los usuarios desean y disfruten el acceso a la información que se puede ofrecer con contenido multimedia digital, pero no quieren tratar con una serie aparentemente infinita de anuncios emergentes. El uso de ventanas emergentes del explorador para mostrar publicidad en la Web se ha vuelto tan habitual que ahora hay software que impide que se abran estas ventanas. Este software puede tener el efecto secundario no deseado de impedir que se muestren páginas web legítimas, lo que a veces suprime una presentación de medios digitales completa.

Cuando se usa la característica HTMLView, los usuarios ya no tienen que tratar con ventanas emergentes. En lugar de tener que abrir una ventana del explorador independiente para proporcionar información  adicional al usuario, puede mostrar contenido personalizado basado en web en la característica Reproducción ahora de la interfaz de usuario de Reproductor de Windows Media mientras el reproductor reproduce el contenido de audio o vídeo que el usuario desea. Los usuarios pueden controlar la reproducción mediante Reproductor de Windows Media controles. Dado que el contenido se reproduce en el reproductor de modo completo, el software diseñado para evitar anuncios emergentes no impedirá que los usuarios disfruten del contenido.

## <a name="htmlview-content-is-easy-to-create"></a>El contenido HTMLView es fácil de crear

Como el nombre de la característica implica, se crea contenido basado en web que se muestra mediante la característica HTMLView mediante Lenguaje de marcado de hipertexto (HTML). Si ya crea contenido para la Web, esto significa que no es necesario aprender un nuevo lenguaje de programación para crear contenido enriquecido fácilmente con la característica HTMLView. Si ya tiene páginas web con un control Reproductor de Windows Media ActiveX incrustado, puede hacer que estas páginas aparezcan en la interfaz de usuario del reproductor simplemente apuntando a estas páginas web desde un metarchivo multimedia de Windows (archivo .asx) mediante un parámetro especial.

Reproductor de Windows Media usa una instancia incrustada de Microsoft Internet Explorer para mostrar contenido HTMLView. Esto significa que no tiene que tener en cuenta distintos exploradores de Internet, varios modelos de scripting o lenguajes de scripting diferentes al crear las páginas web. Incluso si el usuario no usa Internet Explorer como explorador predeterminado, la página web todavía se muestra correctamente en el reproductor.

Es posible que un programa que no sea Reproductor de Windows Media se registre como el programa predeterminado para abrir archivos .asx. El Reproductor de Windows Media de objetos de la serie 9 o posterior incluye un nuevo método, **openPlayer**, que le permite especificar un localizador uniforme de recursos (URL) para el contenido que desea reproducir. Cuando se usa el **método openPlayer,** Reproductor de Windows Media siempre se abre en modo completo para reproducir el contenido especificado. Con este método, puede asegurarse de que el contenido HTMLView se muestra en Reproductor de Windows Media, en lugar de alguna otra aplicación que se haya hecho cargo de la asociación de tipo de archivo .asx.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Reproductor de Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player.openPlayer**](player-openplayer.md)
</dt> </dl>

 

 




