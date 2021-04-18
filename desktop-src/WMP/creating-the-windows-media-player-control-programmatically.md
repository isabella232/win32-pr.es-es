---
title: Crear el control Media Player de Windows mediante programación
description: Crear el control Media Player de Windows mediante programación
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- Windows Media Player, crear controles ActiveX mediante programación
- Modelo de objetos de Windows Media Player, crear controles ActiveX mediante programación
- modelo de objetos, crear controles ActiveX mediante programación
- Windows Media Player Mobile, crear controles ActiveX mediante programación
- Control ActiveX de Windows Media Player, crear mediante programación
- Control ActiveX móvil de Windows Media Player, crear mediante programación
- Control ActiveX, crear mediante programación
- crear un control ActiveX mediante programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222c207b33dcc13a5392f79dad267d6ee82a677c
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "104357821"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a>Crear el control Media Player de Windows mediante programación

Al agregar el control Media Player de Windows a un formulario desde el cuadro de herramientas, se crea un objeto de la clase **AxWMPLib. AxWindowsMediaPlayer** . Esta clase contenedora proporciona al reproductor toda la funcionalidad de un control ActiveX, incluido el acceso a las propiedades de la interfaz de usuario, como la **Ubicación** y **el tamaño**.

Si no necesita las propiedades expuestas por **AxWindowsMediaPlayer**, o si la aplicación no tiene una interfaz gráfica de usuario, puede crear un control de reproductor mediante programación. En este caso, se crea un objeto de la clase **WMPLib. WindowsMediaPlayer** .

> [!Note]  
> Dado que el objeto **WindowsMediaPlayer** no se ajusta como un control ActiveX, no tiene ninguna propiedad heredada de **System. Windows. Forms. control**. Como resultado, no se cambia el nombre de la propiedad **Controls** a **CtlControls**, ya que está en **AxWindowsMediaPlayer**.

 

Para crear el control de Media Player de Windows mediante programación, primero debe agregar una referencia a wmp.dll, que se encuentra en \\ la \\ carpeta system32 de Windows. Al agregar esta referencia, se crea WMPLib.dll en la carpeta del proyecto y aparece una referencia a WMPLib en Explorador de soluciones.

En el código de ejemplo siguiente, que forma parte de una clase Form1, se muestra cómo crear un objeto **Player** y reproducir un archivo. Cuando finaliza la reproducción, o si no se puede reproducir el archivo, el formulario está cerrado.


```VB
Dim WithEvents Player As WMPLib.WindowsMediaPlayer

Private Sub PlayFile(ByVal url As String)
    Player = New WMPLib.WindowsMediaPlayer
    Player.URL = url
    Player.controls.play()
End Sub

Private Sub Form1_Load(ByVal sender As Object, ByVal e As System.EventArgs) _
                       Handles MyBase.Load
    ' TODO  Insert a valid path in the line below.
    PlayFile("c:\media\myaudio.wma")
End Sub

Private Sub Player_MediaError(ByVal pMediaObject As Object) _
                              Handles Player.MediaError
    MessageBox.Show("Cannot play media file.")
    Me.Close()
End Sub

Private Sub Player_PlayStateChange(ByVal NewState As Integer) _
                                   Handles Player.PlayStateChange
    If NewState = WMPLib.WMPPlayState.wmppsStopped Then
        Me.Close()
    End If
End Sub

```




```CSharp
WMPLib.WindowsMediaPlayer Player;

private void PlayFile(String url)
{
    Player = new WMPLib.WindowsMediaPlayer();
    Player.PlayStateChange += 
        new WMPLib._WMPOCXEvents_PlayStateChangeEventHandler(Player_PlayStateChange);
    Player.MediaError += 
        new WMPLib._WMPOCXEvents_MediaErrorEventHandler(Player_MediaError);
    Player.URL = url;
    Player.controls.play();
}

private void Form1_Load(object sender, System.EventArgs e)
{
    // TODO  Insert a valid path in the line below.
    PlayFile(@"c:\myaudio.wma");
}

private void Player_PlayStateChange(int NewState)
{
    if ((WMPLib.WMPPlayState)NewState == WMPLib.WMPPlayState.wmppsStopped)
    {
        this.Close();
    }
}

private void Player_MediaError(object pMediaObject)
{
    MessageBox.Show("Cannot play media file.");
    this.Close();
}


```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Incrustar el control Media Player de Windows en una solución de .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




