---
title: Inserción del control Reproductor de Windows Media en una Visual Basic .NET
description: Inserción del control Reproductor de Windows Media en una Visual Basic .NET
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media modelo de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móvil, inserción
- ActiveX control, inserción
- Reproductor de Windows Media,Visual Basic .NET
- Reproductor de Windows Media de objetos, Visual Basic .NET
- object model,Visual Basic .NET
- Reproductor de Windows Media Mobile,Visual Basic .NET
- Reproductor de Windows Media ActiveX control, Visual Basic .NET
- Reproductor de Windows Media Control de ActiveX móvil, Visual Basic .NET
- ActiveX control, Visual Basic .NET
- embedding,Visual Basic programas .NET
- Visual Basic inserción de programas .NET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819387ac9d04f1ff229ff3665257324eddd042b15dff562a55f085a0fc86ca48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935257"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a>Inserción del control Reproductor de Windows Media en una Visual Basic .NET

Para usar la funcionalidad de Reproductor de Windows Media serie 9 o posterior en una aplicación .NET de Visual Basic, primero agregue el componente a un formulario como se describe en Uso del [control Reproductor de Windows Media con Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

En esta sección se describe cómo crear una aplicación que reproduce vídeo y tiene botones de reproducción y de detenerse personalizados.

## <a name="add-the-video-window"></a>Agregar la ventana de vídeo

Agregue el control Reproductor de Windows Media a un formulario. Cambie el tamaño del control y colómelo donde quiera que aparezca la ventana de vídeo.

Seleccione el Reproductor de Windows Media y, a continuación, cambie la **propiedad uiMode** a "none". Esta configuración oculta los controles de interfaz de usuario. Cuando el usuario reproduce un vídeo, aparecerá en la ventana. Para el contenido de solo audio, aparecerá una visualización.

## <a name="add-two-buttons-and-adjust-the-form"></a>Agregar dos botones y ajustar el formulario

Ahora agregue dos botones al formulario. Seleccione el primer botón y cambie la **propiedad Texto** a "Reproducir". Seleccione el segundo botón y cambie su **propiedad Text** a "Stop".

## <a name="add-the-play-code"></a>Agregar el código de reproducción

Haga doble clic en **el botón Reproducir** para mostrar la ventana Código. Se muestra el código siguiente:


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



Agregue esta línea a la subrutina:


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



En el ejemplo de código anterior, "axWindowsMediaPlayer1" es el nombre predeterminado del control Reproductor de Windows Media y "c: mediafile.wmv" es un marcador de posición para el nombre del medio que desea \\ reproducir.

Si ha agregado el contenido multimedia digital del SDK de Reproductor de Windows Media a la biblioteca de Reproductor de Windows Media, puede usar este código en su lugar:


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



Dado que **la propiedad autoStart** es true de forma predeterminada, Reproductor de Windows Media se iniciará la reproducción al establecer la **propiedad currentPlaylist** o **URL.**

## <a name="add-the-stop-code"></a>Agregar el código de detenerse

Haga doble clic en **el botón Detener** para mostrar la ventana Código. Se muestra el código siguiente:


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
> El contenedor de código administrado para el control Reproductor de Windows Media expone el objeto **Controls** como **Ctlcontrols** para evitar la colisión con la propiedad **Controls** heredada de **System.Windows. Forms.Control**.

 

## <a name="add-error-handling"></a>Agregar control de errores

El Reproductor de Windows Media no genera una excepción cuando encuentra un error como una dirección URL no válida. En su lugar, el control señala un evento. La aplicación debe controlar los eventos de error enviados por el reproductor.

Para crear un controlador de eventos, abra la ventana de código de la clase de formulario. En la lista desplegable de la parte superior de la ventana, seleccione Reproductor de Windows Media control. Aparece una lista de eventos en la lista desplegable de la derecha. En esa lista, seleccione [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md). Se muestra el código siguiente:


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



El código siguiente se podría insertar en la subrutina para proporcionar una funcionalidad mínima de control de errores. Tenga en cuenta que la información sobre el error se puede recuperar del **\_ argumento \_ MediaErrorEvent de WMPOCXEvents.**


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

[**Inserción del control Reproductor de Windows Media en una solución .NET Framework de integración**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




