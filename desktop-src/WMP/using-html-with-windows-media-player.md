---
title: Usar HTML con Windows Media Player
description: Usar HTML con Windows Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Media Player de Windows, HTML
- Modelo de objetos de Windows Media Player, HTML
- modelo de objetos, HTML
- Control ActiveX de Windows Media Player, HTML para el modelo de objetos
- Control ActiveX, HTML para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, HTML para el modelo de objetos
- Windows Media Player Mobile, HTML para el modelo de objetos
- HTML con Media Player de Windows
- Incrustación de páginas web, HTML
- incrustación, páginas web
- comandos de script
- Volteo de URL
- transmisión por secuencias multimedia enriquecida
- compatibilidad de exploradores
- Mostrar páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903533"
---
# <a name="using-html-with-windows-media-player"></a>Usar HTML con Windows Media Player

## <a name="overview"></a>Información general

Usar HTML con Windows Media Player es una forma excelente de combinar audio y vídeo con texto y gráficos. Puede incrustar el control Media Player de Windows en una página web si desea complementar el contenido estático o crear aplicaciones web con medios digitales. Si desea complementar los medios digitales con HTML, puede mostrar las páginas web en el modo completo del reproductor haciendo referencia a ellas en las listas de reproducción de metarchivos de Windows Media.

Si escribe programas personalizados que insertan el control de Media Player de Windows en modo remoto, también puede controlar las páginas web que se muestran en los distintos paneles del modo completo del reproductor cuando los usuarios desacoplan el control. Esto le permite conservar la continuidad entre los Estados acoplado y desacoplado.

## <a name="web-embedding"></a>Incrustación Web

Puede usar el control Media Player de Windows como parte de una página web que cree. Vea [incrustar el Control Media Player de Windows en una página web](embedding-the-windows-media-player-control-in-a-web-page.md).

## <a name="script-commands-and-url-flipping"></a>Comandos de script y volteo de direcciones URL

Los comandos de script son pares de texto/valor que se pueden insertar en los archivos multimedia digitales o en las secuencias. Puede usar comandos de script personalizados únicamente para desencadenar código de script y permitir que Windows Media Player Controle automáticamente otros comandos de script.

Si tiene varias páginas web que acompañan a una presentación multimedia digital, los comandos de la secuencia de comandos de dirección URL pueden cambiar automáticamente la página en un marco mientras el control Media Player de Windows continúa reproduciendo medios digitales en otro marco. Esto se denomina volteo de URL y es una manera excelente de crear una presentación multimedia. Otros comandos de script controlados automáticamente permiten cambiar la reproducción a un archivo o secuencia de medios diferente, mostrar texto de subtítulos o desencadenar eventos como inserciones de anuncios definidas en una lista de reproducción de metarchivo de Windows Media.

Para obtener más información sobre el volteo de direcciones URL, vea [crear Web-Based presentaciones](creating-web-based-presentations.md).

## <a name="rich-media-streaming"></a>Transmisión por secuencias multimedia enriquecida

El volteo de direcciones URL funciona mejor con páginas simples que se cargan rápidamente. Con páginas más complejas, se transfieren varios componentes individualmente, lo que dificulta la sincronización de la presentación de la página con los medios digitales. Para permitir presentaciones multimedia complejas, las páginas web se pueden agregar a una secuencia de medios y entregarse al reproductor de la misma manera que el audio y el vídeo. Esto le permite sincronizar los componentes de la presentación mucho más fácilmente, especialmente en las conexiones de baja velocidad.

Para obtener más información sobre la transmisión por secuencias de multimedia enriquecida, consulte [creación de Web-Based presentaciones](creating-web-based-presentations.md).

## <a name="browser-support"></a>Compatibilidad con exploradores

Puede incrustar el control de Windows Media Player en Microsoft Internet Explorer, Firefox y Netscape Navigator, aunque el proceso es ligeramente diferente para cada uno. También puede crear páginas Web diseñadas para trabajar con los tres exploradores.

Con Internet Explorer y Firefox, se incrusta el control mediante el elemento de objeto HTML. Sin embargo, el navegador requiere un enfoque diferente porque no admite directamente los controles ActiveX. Con Navigator, se usa el elemento APPLET para insertar un applet Java especial en la página. Este applet controla la comunicación con el control ActiveX del reproductor.

Para obtener más información sobre la compatibilidad con Firefox, consulte [uso del control de Media Player de Windows con Firefox](using-the-windows-media-player-control-with-firefox.md).

Para obtener más información acerca de la compatibilidad con Netscape Navigator, consulte [uso de Windows Media Player con netscape 7,1](using-windows-media-player-with-netscape-7-1.md).

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a>Mostrar páginas web en el modo completo del reproductor

Puede ampliar la funcionalidad de Windows Media Player o proporcionar una vista personalizada de la información que acompaña a los archivos multimedia digitales al mostrar las páginas web en el modo completo del reproductor. Esta es la característica HTMLView de los metaarchivos de Windows Media. Los metaarchivos proporcionan un gran control sobre el contenido de la lista de reproducción, lo que le permite realizar una transición sin problemas entre clips, insertar anuncios y mostrar imágenes fijas en Windows Media Player. Para mostrar las páginas web en el modo completo del reproductor, use el elemento PARAM para agregar referencias de URL a las entradas de la lista de reproducción o a todas las listas de reproducción.

Para obtener más información sobre el uso de páginas web en los metaarchivos, vea [Mostrar páginas web en Windows Media Player](displaying-web-pages-in-windows-media-player.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos de Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




