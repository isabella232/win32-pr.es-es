---
title: Problemas de páginas web
description: Problemas de páginas web
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Listas de reproducción de metarchivos de Windows Media, páginas web
- listas de reproducción, páginas web
- listas de reproducción de metarchivos, páginas web
- Listas de reproducción de metarchivos de Windows Media, personalizar HTMLView
- listas de reproducción, personalizar HTMLView
- listas de reproducción de metarchivos, personalizar HTMLView
- Listas de reproducción de metarchivos de Windows Media, personalización de HTMLView
- listas de reproducción, personalización de HTMLView
- listas de reproducción de metarchivos, personalización de HTMLView
- Personalización de HTMLView
- Windows Media Player, páginas web
- Windows Media Player, personalizar HTMLView
- Windows Media Player, personalización de HTMLView
- HTMLView, personalizar
- HTMLView, páginas web
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778937"
---
# <a name="web-page-issues"></a>Problemas de páginas web

Hay algunos aspectos que se deben tener en cuenta al crear una página web que se mostrará en la característica Windows Media Player **Now jugando** . En esta sección se tratan algunos de los problemas que pueden surgir al crear el contenido basado en Web.

## <a name="customizing-htmlview"></a>Personalización de HTMLView

La Página Web de HTMLView puede ser tan simple o compleja como desee. Puede incluir cualquiera de los elementos que utiliza normalmente en el contenido basado en Web. Si incrusta el control Media Player de Windows, puede mostrar una de las interfaces de usuario proporcionadas por el control, crear su propia interfaz de usuario mediante código HTML y código de script, o no proporcionar ninguna interfaz de usuario (lo que significa que el usuario puede usar los controles de transporte del reproductor en modo completo).

El tamaño recomendado para las páginas web que se muestran mediante la característica HTMLView es 575 x 345 píxeles. Sin embargo, el usuario tiene la capacidad de cambiar el tamaño de Windows Media Player y elegir la resolución de pantalla. Si la Página Web de HTMLView es mayor que el tamaño que admite la característica de **reproducción en curso** , el reproductor muestra barras de desplazamiento horizontal y vertical que permiten al usuario ver toda la página. Debe probar el contenido de HTMLView con una variedad de resoluciones de pantalla y tamaños de reproductor para determinar el mejor tamaño de la Página Web.

Windows Media Player no proporciona un método que le permita especificar un tamaño para el reproductor en modo completo.

## <a name="web-page-navigation"></a>Navegación de páginas web

Windows Media Player no proporciona una barra de herramientas de navegación para las páginas web que se muestran en la característica **reproducción en curso** . Esto significa que tiene un control total sobre si los usuarios pueden salir de la Página Web de HTMLView. Si desea permitir que los usuarios naveguen a otras páginas web, debe incluir elementos en el código HTML para proporcionar esa funcionalidad.

## <a name="retrieving-the-parent-window"></a>Recuperar la ventana primaria

Si el código de script existente utiliza **window. Parent** para recuperar el objeto de ventana principal, este código no funcionará en la Página Web de HTMLView. Cuando se usa HTMLView, no hay ningún objeto de ventana principal; por lo tanto, esta característica de scripting no está disponible.

## <a name="about-the-embedded-browser"></a>Acerca del explorador incrustado

Dado que Windows Media Player usa una instancia incrustada de Internet Explorer para mostrar el contenido de HTMLView, la configuración de usuario y las directivas de Internet Explorer se aplican a las páginas web que se muestran en el reproductor. Por ejemplo, si el usuario ha configurado Internet Explorer para evitar que las páginas web descarguen cookies en el equipo, la Página Web de HTMLView también se impide hacerlo.

Las páginas web que se abren mediante la característica HTMLView siempre se ejecutan en la zona de seguridad de **Internet** de Internet Explorer.

El control de explorador Web incrustado utiliza las mismas reglas para almacenar en caché las páginas web como la versión independiente de Internet Explorer. Se recomienda usar páginas de Active Server (ASP) al crear el contenido para asegurarse de que el contenido se entregue desde el servidor web cada vez que Windows Media Player acceda a la Página Web de HTMLView. El uso de páginas ASP puede ser tan sencillo como cambiar el nombre de la página web para usar una extensión de nombre de archivo. asp.

## <a name="about-local-web-content"></a>Acerca del contenido Web local

La característica HTMLView no permite abrir páginas web almacenadas en el equipo del usuario.

## <a name="prompting-the-user"></a>Preguntar al usuario

Puede usar **window. prompt** para solicitar información al usuario. Sin embargo, **window. Alert** y **window. CONFIRM** no están disponibles cuando se usa HTMLView.

## <a name="timing-issues"></a>Problemas de temporización

Puede encontrar problemas de temporización al utilizar un control de Media Player de Windows incrustado en la Página Web de HTMLView. En HTMLView, un control de reproductor incrustado comparte su motor de reproducción con la Media Player de Windows independiente. Es posible que el reproductor independiente pueda abrir y comenzar a reproducir la primera entrada de la lista de reproducción antes de que la página web (y, por lo tanto, el control del reproductor) termine de cargarse. Esto significa que, si controla los eventos **OpenStateChange** o **PlayStateChange** , el código de script no recibirá notificaciones de eventos para estos eventos hasta que se carguen el control de reproducción y sus objetos asociados.

Puede realizar los pasos del código para retrasar la reproducción hasta que se cree una instancia del control de Media Player de Windows. Una manera de hacerlo es hacer que la primera entrada de la lista de reproducción del metarchivo apunte a un archivo de imagen y establecer la duración del archivo en un período de tiempo que permita que se cargue el control del reproductor. En el código de ejemplo siguiente se muestra esta opción:


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



Cuando se abre la lista de reproducción anterior, Windows Media Player espera en la primera entrada de la lista de reproducción hasta un minuto mientras el reproductor carga la Página Web de HTMLView.

Después, en la Página Web de HTMLView, escriba el código de script para controlar el evento **OnLoad** del elemento **Body** . En la función de controlador de eventos, llame al método Player **Controls. Next** para comenzar la reproducción de la segunda entrada en la lista de reproducción.


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



Cuando finaliza la carga de la página web en el ejemplo anterior, Windows Media Player avanza inmediatamente a la segunda entrada de la lista de reproducción. Esto invalida la duración especificada para el primer elemento de la lista de reproducción, lo que significa que el usuario no tiene que esperar todo un minuto antes de ver el contenido deseado. solo tiene que esperar a que la página web termine de cargarse. Dado que en este punto se crean instancias completas del control Player, los eventos **OpenStateChange** y **PlayStateChange** se pueden controlar de la manera habitual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Evento Player. PlayStateChange**](player-player-playstatechange.md)
</dt> <dt>

[**Evento Player. OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 




