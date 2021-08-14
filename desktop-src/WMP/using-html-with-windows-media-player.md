---
title: Uso de HTML con Reproductor de Windows Media
description: Uso de HTML con Reproductor de Windows Media
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Reproductor de Windows Media,HTML
- Reproductor de Windows Media modelo de objetos,HTML
- object model,HTML
- Reproductor de Windows Media ActiveX control,HTML para el modelo de objetos
- ActiveX control,HTML para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil,HTML para el modelo de objetos
- Reproductor de Windows Media Mobile,HTML para el modelo de objetos
- HTML con Reproductor de Windows Media
- Inserción de páginas web, HTML
- embedding,Web pages
- comandos de script
- Cambio de dirección URL
- streaming multimedia enriquecido
- compatibilidad de exploradores
- mostrar páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72185dec8ae9a2119d8c3218478e7ebb5a2df4d7740b25c9f4ecc016aa392e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465925"
---
# <a name="using-html-with-windows-media-player"></a>Uso de HTML con Reproductor de Windows Media

## <a name="overview"></a>Introducción

El uso de HTML Reproductor de Windows Media es una excelente manera de combinar audio y vídeo con texto y gráficos. Puede insertar el control Reproductor de Windows Media en una página web si desea complementar el contenido estático o crear aplicaciones web con medios digitales. Si desea complementar los medios digitales con HTML, por otro lado, puede mostrar páginas web en el modo completo del Reproductor haciendo referencia a ellas en listas de reproducción de metarchivo de Windows Media.

Si escribe programas personalizados que insertan el control Reproductor de Windows Media en modo remoto, también puede controlar las páginas web que se muestran en los distintos paneles del modo completo del Reproductor cuando los usuarios desacoplan el control. Esto le permite conservar la continuidad entre los estados acoplados y desacoplados.

## <a name="web-embedding"></a>Inserción web

Puede usar el control Reproductor de Windows Media como parte de una página web que cree. Vea [Insertar el control Reproductor de Windows Media en una página web](embedding-the-windows-media-player-control-in-a-web-page.md).

## <a name="script-commands-and-url-flipping"></a>Comandos de script y volteo de direcciones URL

Los comandos de script son pares de texto/valor que se pueden insertar en los archivos multimedia digitales o secuencias. Puede usar comandos de script personalizados únicamente para desencadenar código de script, al tiempo que Reproductor de Windows Media otros comandos de script automáticamente.

Cuando tiene varias páginas web que acompañan a una presentación de medios digitales, los comandos de script de dirección URL pueden cambiar automáticamente la página en un fotograma mientras el control Reproductor de Windows Media sigue reproduciendo medios digitales en otro marco. Esto se denomina volteo de dirección URL y es una excelente manera de crear una presentación de diapositivas multimedia. Otros comandos de script que se controlan automáticamente permiten cambiar la reproducción a otro archivo multimedia o secuencia, mostrar texto de subtítulos o desencadenar eventos como inserciones de anuncios definidas en una lista de reproducción de metarchivo multimedia de Windows.

Para obtener más información sobre el cambio de dirección URL, vea [Creating Web-Based Presentations](creating-web-based-presentations.md).

## <a name="rich-media-streaming"></a>Rich Media Streaming

El cambio de dirección URL funciona mejor con páginas sencillas que se cargan rápidamente. Con páginas más complejas, varios componentes se transfieren individualmente, lo que dificulta la sincronización de la presentación de páginas con medios digitales. Para permitir presentaciones multimedia complejas, las páginas web se pueden agregar a una secuencia multimedia y entregarse al reproductor de la misma manera que el audio y el vídeo. Esto le permite sincronizar los componentes de la presentación mucho más fácilmente, especialmente en conexiones de baja velocidad.

Para obtener más información sobre el streaming multimedia enriquecido, vea [Creating Web-Based Presentations](creating-web-based-presentations.md).

## <a name="browser-support"></a>Compatibilidad con exploradores

Puede insertar el control Reproductor de Windows Media en Microsoft Internet Explorer, Firefox y Netscape Navigator, aunque el proceso es ligeramente diferente para cada uno. También puede crear páginas web diseñadas para trabajar con los tres exploradores.

Con Internet Explorer y Firefox, puede insertar el control mediante el elemento HTML OBJECT. El navegador requiere un enfoque diferente, sin embargo, porque no admite directamente ActiveX controles. Con Navigator, se usa el elemento APPLET para insertar un applet especial de Java en la página. Este applet controla la comunicación con el control player ActiveX.

Para obtener más información sobre la compatibilidad con Firefox, consulte [Uso del Reproductor de Windows Media Control con Firefox.](using-the-windows-media-player-control-with-firefox.md)

Para obtener más información sobre la compatibilidad con Netscape Navigator, consulte [Uso de Reproductor de Windows Media con Netscape 7.1.](using-windows-media-player-with-netscape-7-1.md)

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a>Mostrar páginas web en el modo completo del reproductor

Puede ampliar la funcionalidad de Reproductor de Windows Media o proporcionar una vista personalizada de la información que acompaña a los medios digitales mediante la visualización de páginas web en el modo completo del Reproductor. Esta es la característica HTMLView de Windows metarchivos multimedia. Los metarchivos le dan un gran control sobre el contenido de la lista de reproducción, lo que le permite realizar una transición sin problemas entre clips, insertar anuncios y mostrar imágenes fijas en Reproductor de Windows Media. Para mostrar páginas web en el modo completo del reproductor, use el elemento PARAM para agregar referencias DE URL a las entradas de la lista de reproducción o a listas de reproducción enteras.

Para obtener más información sobre el uso de páginas web en metarchivos, vea [Mostrar páginas web en Reproductor de Windows Media](displaying-web-pages-in-windows-media-player.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> </dl>

 

 




