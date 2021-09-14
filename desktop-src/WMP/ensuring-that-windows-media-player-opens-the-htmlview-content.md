---
title: Asegurarse de que Reproductor de Windows Media abre el contenido HTMLView
description: Asegurarse de que Reproductor de Windows Media abre el contenido HTMLView
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Windows Listas de reproducción de metarchivos multimedia, Reproductor de Windows Media contenido HTMLView
- listas de reproducción, Reproductor de Windows Media contenido HTMLView
- listas de reproducción de metarchivo, Reproductor de Windows Media abrir contenido HTMLView
- Windows Listas de reproducción de metarchivos multimedia, abrir contenido HTMLView
- listas de reproducción, abrir contenido HTMLView
- listas de reproducción de metarchivo, abrir contenido HTMLView
- abrir contenido HTMLView
- Reproductor de Windows Media, abrir contenido HTMLView
- Reproductor de Windows Media,HTMLView content
- HTMLView, abrir contenido
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241977"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a>Asegurarse de que Reproductor de Windows Media abre el contenido HTMLView

Actualmente, Reproductor de Windows Media serie 9 y Reproductor de Windows Media 10 son los únicos reproductores que admiten el parámetro *HTMLView* en archivos .asx. Esto significa que debe tomar medidas para asegurarse de que el contenido HTMLView se reproduce en estas versiones de Reproductor de Windows Media.

Primero debe determinar si Reproductor de Windows Media serie 9 o Reproductor de Windows Media 10 está instalado en el equipo del usuario. El SDK Reproductor de Windows Media incluye un ejemplo completo que muestra cómo detectar diferentes versiones de Reproductor de Windows Media en distintos exploradores web. Aunque un análisis completo del ejemplo de detección está fuera del ámbito de esta sección, hay algunos pasos básicos que puede realizar para determinar qué versión de Reproductor de Windows Media el equipo del usuario está ejecutando.

En su forma más sencilla, la detección de Reproductor de Windows Media implica insertar el control Player en la página web que vincula al contenido HTMLView y, a continuación, inspeccionar el valor recuperado por el *reproductor*. **propiedad versionInfo.** Una vez que haya comprobado que el usuario tiene instalado Reproductor de Windows Media serie 9 o Reproductor de Windows Media 10, puede usar el método [Player.openPlayer](player-openplayer.md) para abrir el contenido en el reproductor en modo completo. El **método openPlayer** garantiza que el contenido se  muestra inicialmente en la característica Reproducción ahora del reproductor en modo completo, en lugar de en una máscara, en modo mini Player o en otro reproductor que se ha registrado como el programa predeterminado para archivos con una extensión de nombre de archivo .asx, pero no admite HTMLView. Sin embargo, una vez que se muestra el contenido, el usuario tiene control total de Reproductor de Windows Media, lo que significa que puede optar por mostrar una característica que no sea **Reproducción** ahora, cambiar al modo de máscara o incluso salir del reproductor.

El código de ejemplo siguiente crea una página web para Internet Explorer. Esta página abre un archivo .asx, que especifica una página web HTMLView que aparece en el reproductor en modo completo cuando Reproductor de Windows Media serie 9 o posterior está instalado.


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



El código del ejemplo anterior inserta el control Reproductor de Windows Media con la propiedad **uiMode** establecida en "invisible" y los atributos alto y ancho del reproductor establecidos en cero. Esto se debe a que la página web no requiere que la interfaz de usuario del control Player se muestre inicialmente; solo requiere acceso al modelo de objetos player. La página también muestra un botón de entrada que permite al usuario reproducir el archivo .asx.

Cuando el usuario hace clic en el botón Reproducir ASX, se ejecuta JScript la función PlayASX de Microsoft. En primer lugar, esta función recupera el valor de la propiedad **VersionInfo** del reproductor mediante el método **JScript parseInt** para inspeccionar el valor numérico de la cadena recuperada. Si el valor numérico es mayor o igual que 9 (lo que significa que el usuario tiene instalado Reproductor de Windows Media serie 9), el código de script llama al método **openPlayer** y pasa la dirección URL del archivo .asx que contiene el parámetro HTMLView. Este método abre el archivo .asx mediante Reproductor de Windows Media en modo completo, reproduce el contenido multimedia digital en la lista de reproducción .asx y muestra el contenido basado en web HTMLView en la característica **Reproducción** ahora.

Si el valor numérico de la cadena de versión no es mayor o igual que 9 (lo que significa que el usuario no tiene instalado Reproductor de Windows Media serie 9 o posterior en su equipo), el código de script cambia **uiMode** del control Player a "full", establece un nuevo ancho y alto para el control y, a continuación, abre el archivo .asx en el reproductor incrustado especificando un valor para la propiedad **URL.** Cuando esto sucede, el contenido multimedia digital se reproduce en la página web, pero se omiten los valores HTMLView especificados en el archivo .asx.

La forma en que se reproduce el contenido cuando el usuario no tiene instalado Reproductor de Windows Media serie 9 o Reproductor de Windows Media 10 es su función. En el ejemplo anterior se muestra cómo especificar que el contenido se reproduce en la página web en lugar del reproductor en modo completo, omitiendo cualquier contenido HTMLView del proceso. Hay otros enfoques que puede tomar. Por ejemplo, podría pedir al usuario que instale una versión más reciente de Reproductor de Windows Media, lo que hace que esa versión del reproductor sea un requisito para reproducir el contenido multimedia digital.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Reproductor de Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player.uiMode**](player-uimode.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 




