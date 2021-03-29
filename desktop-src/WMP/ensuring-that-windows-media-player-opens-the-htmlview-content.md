---
title: Asegurarse de que Windows Media Player abre el contenido de HTMLView
description: Asegurarse de que Windows Media Player abre el contenido de HTMLView
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Listas de reproducción de metarchivo de Windows Media, Windows Media Player abrir el contenido de HTMLView
- listas de reproducción, Windows Media Player abrir el contenido de HTMLView
- listas de reproducción de metarchivos, Windows Media Player abrir el contenido de HTMLView
- Listas de reproducción de metarchivos de Windows Media, abrir contenido de HTMLView
- listas de reproducción, abrir contenido de HTMLView
- listas de reproducción de metarchivos, abrir contenido de HTMLView
- abrir el contenido de HTMLView
- Windows Media Player, abrir contenido de HTMLView
- Media Player de Windows, contenido de HTMLView
- HTMLView, abrir contenido
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776512"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a>Asegurarse de que Windows Media Player abre el contenido de HTMLView

Actualmente, las series Windows Media Player 9 y Windows Media Player 10 son los únicos reproductores que admiten el parámetro *HTMLView* en los archivos. ASX. Esto significa que debe tomar medidas para asegurarse de que el contenido de HTMLView se reproduce en estas versiones de Windows Media Player.

En primer lugar, debe determinar si Windows Media Player 9 series o Windows Media Player 10 está instalado en el equipo del usuario. El SDK de Windows Media Player incluye un ejemplo completo que muestra cómo detectar diferentes versiones de Windows Media Player en diferentes exploradores Web. Aunque un análisis completo del ejemplo de detección está fuera del ámbito de esta sección, hay algunos pasos básicos que puede seguir para determinar qué versión de Windows Media Player el equipo del usuario está ejecutando.

En su forma más sencilla, la detección de Media Player de Windows implica la inserción del control Player en la página web que se vincula al contenido de HTMLView y, a continuación, la inspección del valor recuperado por el *reproductor*. propiedad **versionInfo** . Una vez que haya comprobado que el usuario tiene Windows Media Player 9 series o Windows Media Player 10 instalado, puede usar el método [Player. openPlayer](player-openplayer.md) para abrir el contenido en el reproductor en modo completo. El método **openPlayer** garantiza que el contenido se muestra inicialmente en la característica **reproducción en curso** del reproductor en modo completo, en lugar de en una máscara, en el modo de mini reproductor o en otro reproductor que se ha registrado como el programa predeterminado para los archivos con la extensión de nombre de archivo. ASX, pero no es compatible con HTMLView. Sin embargo, una vez que se muestra el contenido, el usuario tiene el control completo de Windows Media Player, lo que significa que puede elegir mostrar una característica que no sea **reproducción**, cambiar al modo de máscara o incluso salir del reproductor.

En el código de ejemplo siguiente se crea una página web para Internet Explorer. Esta página abre un archivo. ASX, que especifica una página web de HTMLView que aparece en el reproductor de modo completo cuando se instala Windows Media Player 9 series o posterior.


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



En el código del ejemplo anterior se inserta el control Media Player de Windows con la propiedad **uiMode** establecida en "invisible" y los atributos height y width del reproductor establecidos en cero. Esto se debe a que la página web no requiere que la interfaz de usuario de control del reproductor se muestre inicialmente, solo requiere acceso al modelo de objetos del reproductor. La página también muestra un botón de entrada que permite al usuario reproducir el archivo. ASX.

Cuando el usuario hace clic en el botón reproducir ASX, se ejecuta la función PlayASX de Microsoft JScript. Esta función recupera primero el valor de la propiedad **versionInfo** del reproductor, utilizando el método **parseInt** de JScript para inspeccionar el valor numérico de la cadena recuperada. Si el valor numérico es mayor o igual que 9 (lo que significa que el usuario tiene instalada la serie Windows Media Player 9), el código de script llama al método **openPlayer** y pasa la dirección URL del archivo. ASX que contiene el parámetro HTMLView. Este método abre el archivo. ASX con Windows Media Player en modo completo, reproduce el contenido multimedia digital en la lista de reproducción. ASX y muestra el contenido basado en Web HTMLView en la característica de **reproducción en curso** .

Si el valor numérico de la cadena de versión no es mayor o igual que 9 (lo que significa que el usuario no tiene Windows Media Player 9 series o posterior instalado en su equipo), el código de script cambia el **uiMode** del control Player a "Full", establece un nuevo ancho y alto para el control y, a continuación, abre el archivo. asx en el reproductor incrustado especificando un valor para la propiedad **URL** . Cuando esto sucede, el contenido multimedia digital se reproduce en la página web, pero se omiten los valores de HTMLView especificados en el archivo. ASX.

Cómo se reproduce el contenido cuando el usuario no tiene Windows Media Player 9 series o Windows Media Player 10 instalado depende de usted. En el ejemplo anterior se muestra cómo especificar que el contenido se reproduzca en la página web en lugar de en el reproductor de modo completo, omitiendo el contenido de HTMLView en el proceso. Hay otros métodos que puede llevar a cabo. Por ejemplo, puede pedir al usuario que instale una versión más reciente de Windows Media Player, lo que hace que esa versión del reproductor sea un requisito para reproducir el contenido multimedia digital.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 




