---
title: Inserción del control Reproductor de Windows Media en una solución de C
description: Inserción del control Reproductor de Windows Media en una solución de C\
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móviles, inserción
- ActiveX control, inserción
- Reproductor de Windows Media,C
- Reproductor de Windows Media modelo de objetos, C
- object model,C
- Reproductor de Windows Media Mobile,C
- Reproductor de Windows Media ActiveX control, C
- Reproductor de Windows Media Control de ActiveX móvil, C
- ActiveX control, C
- embedding,C programs
- Inserción de programas de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a067a407fccdd78d71d9e60bc00d1eae6950e3fdaf204f886c5e96edf372eb07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901985"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>Inserción del control Reproductor de Windows Media en una solución de C#

Para usar la funcionalidad de Reproductor de Windows Media en una aplicación de C#, primero agregue el componente a un formulario como se describe en Uso del [control Reproductor de Windows Media con Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

En las secciones siguientes se describe cómo crear una aplicación que reproduce vídeo y usa botones de reproducción y de detenerse personalizados.

## <a name="add-the-video-window"></a>Agregar la ventana de vídeo

Agregue el Reproductor de Windows Media ActiveX control a un formulario. Cambie el tamaño del control y colómelo donde quiera que aparezca la ventana de vídeo.

Seleccione el Reproductor de Windows Media y, a continuación, cambie la **propiedad uiMode** a "none". Esta configuración oculta los controles de interfaz de usuario. Cuando el usuario reproduce un vídeo, aparecerá en la ventana. Para el contenido de solo audio, aparecerá una visualización.

## <a name="add-two-buttons-and-adjust-the-form"></a>Agregar dos botones y ajustar el formulario

Ahora, agregue dos botones al formulario. Seleccione el primer botón y cambie la **propiedad Texto** a "Reproducir". Seleccione el segundo botón y cambie su **propiedad Text** a "Stop".

## <a name="add-the-play-code"></a>Agregar el código de reproducción

Haga doble clic en **el botón Reproducir** para mostrar la ventana Código. En C#, se mostrará el código siguiente:


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



Agregue esta línea entre las dos llaves:


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



En el ejemplo de código anterior, "axWindowsMediaPlayer1" es el nombre predeterminado del control Reproductor de Windows Media y "c: mediafile.wmv" es un marcador de posición para el nombre del elemento multimedia que desea \\ reproducir. Se puede usar cualquier ruta de acceso de archivo válida. El símbolo @ indica al compilador que no interprete las barras diagonales inversas como caracteres de escape.

Si ha agregado el contenido multimedia digital del SDK de Reproductor de Windows Media a la biblioteca de Reproductor de Windows Media, puede usar este código en su lugar:


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



Dado que **la propiedad autoStart** es true de forma predeterminada, Reproductor de Windows Media se iniciará la reproducción al establecer la **propiedad currentPlaylist** o **URL.**

## <a name="add-the-stop-code"></a>Agregar el código de detenerse

Haga doble clic en **el botón Detener** para mostrar la ventana Código. En C#, se mostrará el código siguiente:


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
> El contenedor de código administrado para el control Reproductor de Windows Media expone el objeto **Controls** como **Ctlcontrols** para evitar la colisión con la propiedad **Controls** heredada de **System.Windows. Forms.Control**.

 

## <a name="add-error-handling"></a>Agregar control de errores

El Reproductor de Windows Media no genera una excepción cuando encuentra un error como una dirección URL no válida. En su lugar, señala un evento. La aplicación debe controlar los eventos de error enviados por el reproductor.

Para crear un controlador de eventos, primero abra el ventana Propiedades para el control Reproductor de Windows Media eventos. En la lista de eventos, haga doble clic en **MediaError**. Se muestra el código siguiente:


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



El código siguiente se podría insertar en el método para proporcionar una funcionalidad mínima de control de errores. Tenga en cuenta que la información sobre el error se puede recuperar del **\_ argumento \_ MediaErrorEvent de WMPOCXEvents.**


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

[**Inserción del control Reproductor de Windows Media en una solución .NET Framework de integración**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




