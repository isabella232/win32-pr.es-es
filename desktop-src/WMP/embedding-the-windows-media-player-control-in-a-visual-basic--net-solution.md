---
title: Incrustar el control Media Player de Windows en una solución Visual Basic .NET
description: Incrustar el control Media Player de Windows en una solución Visual Basic .NET
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, Visual Basic .NET
- Modelo de objetos de Windows Media Player, Visual Basic .NET
- modelo de objetos, Visual Basic .NET
- Windows Media Player Mobile, Visual Basic .NET
- Control ActiveX de Windows Media Player, Visual Basic .NET
- Control ActiveX de Windows Media Player Mobile, Visual Basic .NET
- Control ActiveX, Visual Basic .NET
- incrustación, Visual Basic programas .NET
- Incrustación de programas de Visual Basic .NET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d578b456a5064f1846ead7f074f178753dbc7c97
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "104357823"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a>Incrustar el control Media Player de Windows en una solución Visual Basic .NET

Para usar la funcionalidad de Windows Media Player 9 series o posterior en una aplicación Visual Basic .NET, primero agregue el componente a un formulario tal y como se describe en [usar el Control Media Player de Windows con Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

En esta sección se describe cómo crear una aplicación que reproduzca vídeo y que tenga botones personalizados de reproducción y detención.

## <a name="add-the-video-window"></a>Agregar la ventana de vídeo

Agregue el control Media Player de Windows a un formulario. Cambie el tamaño del control y colóquelo donde desee que aparezca la ventana de vídeo.

Seleccione el control Media Player de Windows y, a continuación, cambie la propiedad **uiMode** a "none". Esta configuración oculta los controles de interfaz de usuario. Cuando el usuario reproduzca un vídeo, aparecerá en la ventana de. En el caso de contenido de solo audio, aparecerá una visualización.

## <a name="add-two-buttons-and-adjust-the-form"></a>Agregar dos botones y ajustar el formulario

Ahora, agregue dos botones al formulario. Seleccione el primer botón y cambie la propiedad **texto** a "reproducir". Seleccione el segundo botón y cambie su propiedad **texto** a "detener".

## <a name="add-the-play-code"></a>Agregar el código de reproducción

Haga doble clic en el botón **reproducir** para mostrar la ventana de código. Se muestra el código siguiente:


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



Agregue esta línea a la subrutina:


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



En el ejemplo de código anterior, "axWindowsMediaPlayer1" es el nombre predeterminado del control Media Player de Windows y "c: \\ MediaFile. WMV" es un marcador de posición para el nombre del medio que desea reproducir.

Si ha agregado el contenido multimedia digital del SDK de Windows Media Player a la biblioteca de Windows Media Player, puede usar este código en su lugar:


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



Dado que la propiedad **autoStart** es true de forma predeterminada, Windows Media Player comenzará a reproducirse cuando establezca la propiedad **currentPlaylist** o **URL** .

## <a name="add-the-stop-code"></a>Agregar el código para detener

Haga doble clic en el botón **detener** para mostrar la ventana de código. Se muestra el código siguiente:


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



Agregue esta línea a la subrutina:


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> El contenedor de código administrado para el control Windows Media Player expone el objeto **Controls** como **Ctlcontrols** para evitar conflictos con la propiedad **Controls** heredada de **System. Windows. Forms. control**.

 

## <a name="add-error-handling"></a>Agregar control de errores

El control Media Player de Windows no genera una excepción cuando encuentra un error como una dirección URL no válida. En su lugar, el control señala un evento. La aplicación debe controlar los eventos de error enviados por el reproductor.

Para crear un controlador de eventos, abra la ventana de código para la clase de formulario. En la lista desplegable de la parte superior de la ventana, seleccione el control Media Player de Windows. Aparece una lista de eventos en la lista desplegable de la derecha. En esa lista, seleccione [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md). Se muestra el código siguiente:


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



El siguiente código se puede insertar en la subrutina para proporcionar una capacidad de control de errores mínima. Tenga en cuenta que la información sobre el error se puede recuperar del argumento **\_ \_ MediaErrorEvent de WMPOCXEvents** .


```VB
Try
    ' If the file is corrupt or missing, show the 
    ' hexadecimal error code and URL.
    Dim errSource As WMPLib.IWMPMedia2 = e.pMediaObject
    Dim errorItem As WMPLib.IWMPErrorItem = errSource.Error
    MessageBox.Show("Media error " + errorItem.errorCode.ToString("X") _
                    + " in " + errSource.sourceURL)
Catch ex As InvalidCastException
    ' In case pMediaObject is not an IWMPMedia item.
    MessageBox.Show("Player error.")
End Try

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Incrustar el control Media Player de Windows en una solución de .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




