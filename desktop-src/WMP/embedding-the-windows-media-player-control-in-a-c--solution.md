---
title: Incrustar el control Media Player de Windows en una solución de C
description: Incrustar el control de Media Player de Windows en una solución de C \
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, C
- Modelo de objetos de Windows Media Player, C
- modelo de objetos, C
- Windows Media Player Mobile, C
- Control ActiveX de Windows Media Player, C
- Control ActiveX móvil de Windows Media Player, C
- Control ActiveX, C
- incrustación, programas de C
- Incrustación de programas de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c950bed9812cea0aa6ce28995fd6998bb8417ac
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "105695490"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>Incrustar el control Media Player de Windows en una solución de C#

Para usar la funcionalidad de Windows Media Player en una aplicación de C#, agregue primero el componente a un formulario tal y como se describe en [usar el Control Media Player de Windows con Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

En las secciones siguientes se describe cómo crear una aplicación que reproduzca vídeo y use botones personalizados de reproducción y detención.

## <a name="add-the-video-window"></a>Agregar la ventana de vídeo

Agregue el control ActiveX de Windows Media Player a un formulario. Cambie el tamaño del control y colóquelo donde desee que aparezca la ventana de vídeo.

Seleccione el control Media Player de Windows y, a continuación, cambie la propiedad **uiMode** a "none". Esta configuración oculta los controles de interfaz de usuario. Cuando el usuario reproduzca un vídeo, aparecerá en la ventana de. En el caso de contenido de solo audio, aparecerá una visualización.

## <a name="add-two-buttons-and-adjust-the-form"></a>Agregar dos botones y ajustar el formulario

Ahora, agregue dos botones al formulario. Seleccione el primer botón y cambie la propiedad **texto** a "reproducir". Seleccione el segundo botón y cambie su propiedad **texto** a "detener".

## <a name="add-the-play-code"></a>Agregar el código de reproducción

Haga doble clic en el botón **reproducir** para mostrar la ventana de código. En C#, se mostrará el siguiente código:


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



Agregue esta línea entre las dos llaves:


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



En el ejemplo de código anterior, "axWindowsMediaPlayer1" es el nombre predeterminado del control Media Player de Windows y "c: \\ MediaFile. WMV" es un marcador de posición para el nombre del elemento multimedia que desea reproducir. Se puede usar cualquier ruta de acceso de archivo válida. El símbolo @ indica al compilador que no interprete las barras diagonales inversas como caracteres de escape.

Si ha agregado el contenido multimedia digital del SDK de Windows Media Player a la biblioteca de Windows Media Player, puede usar este código en su lugar:


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



Dado que la propiedad **autoStart** es true de forma predeterminada, Windows Media Player comenzará a reproducirse cuando establezca la propiedad **currentPlaylist** o **URL** .

## <a name="add-the-stop-code"></a>Agregar el código para detener

Haga doble clic en el botón **detener** para mostrar la ventana de código. En C#, se mostrará el siguiente código:


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



Agregue esta línea entre las dos llaves:


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> El contenedor de código administrado para el control Windows Media Player expone el objeto **Controls** como **Ctlcontrols** para evitar conflictos con la propiedad **Controls** heredada de **System. Windows. Forms. control**.

 

## <a name="add-error-handling"></a>Agregar control de errores

El control Media Player de Windows no genera una excepción cuando encuentra un error como una dirección URL no válida. En su lugar, indica un evento. La aplicación debe controlar los eventos de error enviados por el reproductor.

Para crear un controlador de eventos, abra primero el ventana Propiedades para el control Media Player de Windows. En la lista de eventos, haga doble clic en **MediaError**. Se muestra el código siguiente:


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



El siguiente código se puede insertar en el método para proporcionar una capacidad de control de errores mínima. Tenga en cuenta que la información sobre el error se puede recuperar del argumento **\_ \_ MediaErrorEvent de WMPOCXEvents** .


```CSharp
try
// If the Player encounters a corrupt or missing file, 
// show the hexadecimal error code and URL.
{
    IWMPMedia2 errSource = e.pMediaObject as IWMPMedia2;
    IWMPErrorItem errorItem = errSource.Error;
    MessageBox.Show("Error " + errorItem.errorCode.ToString("X") 
                    + " in " + errSource.sourceURL);
}
catch(InvalidCastException)
// In case pMediaObject is not an IWMPMedia item.
{
    MessageBox.Show("Error.");
} 

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Incrustar el control Media Player de Windows en una solución de .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




