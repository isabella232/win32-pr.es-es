---
title: Crear el control Reproductor de Windows Media mediante programación
description: Crear el control Reproductor de Windows Media mediante programación
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- Reproductor de Windows Media, crear un control ActiveX mediante programación
- Reproductor de Windows Media de objetos, crear un control ActiveX mediante programación
- modelo de objetos, crear ActiveX control mediante programación
- Reproductor de Windows Media Móvil, creación de ActiveX mediante programación
- Reproductor de Windows Media ActiveX control, crear mediante programación
- Reproductor de Windows Media Control de ActiveX móvil, creación mediante programación
- ActiveX control, crear mediante programación
- crear ActiveX control mediante programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57b3f4ba9d8c297aee9feb14fc05a35306e1a85d8a718aef6721b92475e19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340968"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a>Crear el control Reproductor de Windows Media mediante programación

Al agregar el control Reproductor de Windows Media a un formulario desde el Cuadro de herramientas, se crea un objeto de la clase **AxWMPLib.AxWindowsMediaPlayer.** Esta clase contenedora proporciona al reproductor toda la funcionalidad de un control ActiveX, incluido el acceso a las propiedades de la interfaz de usuario, como **Ubicación** y **Tamaño.**

Si no necesita las propiedades expuestas por **AxWindowsMediaPlayer** o si la aplicación no tiene una interfaz gráfica de usuario, puede crear un control Player mediante programación. En este caso, se crea un objeto de la **clase WMPLib.WindowsMediaPlayer.**

> [!Note]  
> Dado que **el objeto WindowsMediaPlayer** no está encapsulado como un control ActiveX, no tiene ninguna propiedad heredada de **System.Windows. Forms.Control**. Como resultado, no se **cambia el** nombre de la propiedad Controls a **CtlControls**, como en **AxWindowsMediaPlayer.**

 

Para crear el control Reproductor de Windows Media mediante programación, primero debe agregar una referencia a wmp.dll, que se encuentra en la carpeta \\ \\ Windows system32. Agregar esta referencia crea WMPLib.dll en la carpeta del proyecto y aparece una referencia a WMPLib en Explorador de soluciones.

El código de ejemplo siguiente, que forma parte de una clase Form1, muestra cómo crear un objeto **Player** y reproducir un archivo. Cuando finaliza la reproducción, o si no se puede reproducir el archivo, se cierra el formulario.


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

[**Inserción del control Reproductor de Windows Media en una solución .NET Framework de integración**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




