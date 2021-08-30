---
title: Problemas de la página web
description: Problemas de la página web
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Windows Listas de reproducción de metarchivos multimedia, páginas web
- listas de reproducción, páginas web
- listas de reproducción de metarchivo, páginas web
- Windows Listas de reproducción de metarchivos multimedia, personalización de HTMLView
- listas de reproducción, personalización de HTMLView
- listas de reproducción de metarchivo, personalización de HTMLView
- Windows Listas de reproducción de metarchivos multimedia, personalización de HTMLView
- listas de reproducción, personalización de HTMLView
- listas de reproducción de metarchivo, personalización de HTMLView
- personalizar HTMLView
- Reproductor de Windows Media,páginas web
- Reproductor de Windows Media, personalizar HTMLView
- Reproductor de Windows Media,personalización de HTMLView
- HTMLView, personalización
- HTMLView,Páginas web
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c952d143e260aac5613fccdc3d6f8ed3403801441a000b953ef5e8387c924857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001285"
---
# <a name="web-page-issues"></a>Problemas de la página web

Hay algunos aspectos que se deben tener en cuenta al crear una página web que se mostrará en la Reproductor de Windows Media **De reproducción** ahora. En esta sección se de abordan algunos de los problemas que pueden surgir al crear el contenido basado en web.

## <a name="customizing-htmlview"></a>Personalización de HTMLView

La página web de HTMLView puede ser tan sencilla o compleja como desee. Puede incluir cualquiera de los elementos que suele usar en el contenido basado en web. Si inserta el control Reproductor de Windows Media, puede mostrar una de las interfaces de usuario proporcionadas por el control, crear su propia interfaz de usuario mediante CÓDIGO HTML y código de script o no proporcionar ninguna interfaz de usuario (lo que significa que el usuario puede usar los controles de transporte del reproductor en modo completo).

El tamaño recomendado para las páginas web mostradas mediante la característica HTMLView es de 575 x 345 píxeles. Sin embargo, el usuario tiene la capacidad de cambiar el tamaño Reproductor de Windows Media y elegir la resolución de pantalla. Si la página web HTMLView es mayor que el tamaño que se adapta a la característica **Reproducción** ahora, el reproductor muestra barras de desplazamiento horizontales y verticales que permiten al usuario ver toda la página. Debe probar el contenido HTMLView con una variedad de resoluciones de pantalla y tamaños de reproductor para determinar el mejor tamaño para la página web.

Reproductor de Windows Media no proporciona un método que le permita especificar un tamaño para el reproductor en modo completo.

## <a name="web-page-navigation"></a>Navegación por páginas web

Reproductor de Windows Media no proporciona una barra de herramientas de navegación para las páginas web que se muestran en la **característica Reproducción** ahora. Esto significa que tiene un control total sobre si los usuarios pueden salir de la página web HTMLView. Si desea permitir que los usuarios naveguen a otras páginas web, debe incluir elementos en el código HTML para proporcionar esa funcionalidad.

## <a name="retrieving-the-parent-window"></a>Recuperación de la ventana primaria

Si el código de script existente usa **window.parent para** recuperar el objeto de ventana primario, este código no funcionará en la página web HTMLView. Cuando se usa HTMLView, no hay ningún objeto de ventana primario; por lo tanto, esta característica de scripting no está disponible.

## <a name="about-the-embedded-browser"></a>Acerca del explorador incrustado

Dado Reproductor de Windows Media una instancia insertada de Internet Explorer para mostrar contenido HTMLView, la configuración de usuario y las directivas de Internet Explorer se aplican a las páginas web que se muestran en el Reproductor. Por ejemplo, si el usuario ha configurado Internet Explorer para impedir que las páginas web descarguen cookies en el equipo, también se impide que la página web HTMLView lo haga.

Las páginas web abiertas mediante la característica HTMLView siempre se ejecutan en la Internet Explorer **seguridad de Internet.**

El control de explorador web incrustado usa las mismas reglas para almacenar en caché las páginas web que la versión independiente de Internet Explorer. Es una buena idea usar Active Server Pages (ASP) al crear el contenido para asegurarse de que el contenido se entrega desde el servidor web cada vez que Reproductor de Windows Media accede a la página web HTMLView. El uso de páginas ASP puede ser tan sencillo como cambiar el nombre de la página web para usar una extensión de nombre de archivo .asp.

## <a name="about-local-web-content"></a>Acerca del contenido web local

La característica HTMLView no permite abrir páginas web almacenadas en el equipo del usuario.

## <a name="prompting-the-user"></a>Preguntar al usuario

Puede usar **window.prompt para** solicitar información al usuario. Sin embargo, **window.alert** y **window.confirm** no están disponibles cuando se usa HTMLView.

## <a name="timing-issues"></a>Problemas de control de tiempo

Puede encontrar problemas de control de tiempo al usar un control Reproductor de Windows Media insertado en la página web htmlView. En HTMLView, un control Player incrustado comparte su motor de reproducción con el Reproductor de Windows Media. Es posible que el reproductor independiente se abra y comience a reproducir la primera entrada de la lista de reproducción antes de que la página web (y, por tanto, el control Player) termine de cargarse. Esto significa que si controla los eventos **OpenStateChange** o **PlayStateChange,** el código de script no recibirá notificaciones de eventos para estos eventos hasta que se carguen el control Player y sus objetos asociados.

Puede realizar pasos en el código para retrasar la reproducción hasta que Reproductor de Windows Media se cree una instancia del control . Una manera de hacerlo es hacer que la primera entrada de la lista de reproducción de metarchivo apunte a un archivo de imagen y establezca la duración del archivo en un período de tiempo que permita que el control Player se cargue. En el código de ejemplo siguiente se muestra esta opción:


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



Cuando se abre la lista de reproducción anterior, Reproductor de Windows Media espera en la primera entrada de la lista de reproducción hasta un minuto mientras el reproductor carga la página web HTMLView.

A continuación, en la página web de HTMLView, escriba código de script para controlar el evento **de** carga del **elemento BODY.** En la función de controlador de eventos, llame al método **Player Controls.Next** para comenzar la reproducción de la segunda entrada de la lista de reproducción.


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



Cuando la página web del ejemplo anterior termina de cargarse, Reproductor de Windows Media avanza inmediatamente a la segunda entrada de la lista de reproducción. Esto invalida la duración especificada para el primer elemento de la lista de reproducción, lo que significa que el usuario no tiene que esperar el minuto completo antes de ver el contenido deseado. Solo tiene que esperar a que la página web termine de cargarse. Dado que en este momento se crea una instancia completa del control Player, los eventos **OpenStateChange** y **PlayStateChange** se pueden controlar de la manera habitual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Reproductor de Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Evento Player.PlayStateChange**](player-player-playstatechange.md)
</dt> <dt>

[**Evento Player.OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 




