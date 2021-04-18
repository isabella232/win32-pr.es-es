---
title: Propiedad AxWindowsMediaPlayer. uiMode
description: La propiedad uiMode obtiene o establece un valor que indica qué controles se muestran en la interfaz de usuario.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- propiedades de uiMode Media Player de Windows
- propiedad uiMode Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad uiMode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699988"
---
# <a name="axwindowsmediaplayeruimode-property"></a>Propiedad AxWindowsMediaPlayer. uiMode

La propiedad uiMode obtiene o establece un valor que indica qué controles se muestran en la interfaz de usuario.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a>Valor de propiedad

System. String que es uno de los valores siguientes.



| Value     | Descripción                                                                                                                                                                                                     | Ejemplo de audio                                                   | Ejemplo de vídeo                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| invisibles | Windows Media Player está incrustado sin ninguna interfaz de usuario visible (controles, vídeo o ventana de visualización).                                                                                                  | (No se muestra nada).                                         | (No se muestra nada).                                         |
| ninguno      | Windows Media Player está incrustado sin controles y solo se muestra la ventana de vídeo o visualización.                                                                                                   | ![uiMode = ' none ' con audio](images/uimode-none-audio-v11.png) | ![uiMode = ' none ' con vídeo](images/uimode-none-video-v11.png) |
| pequeño      | Windows Media Player está incrustado con los controles ventana de estado, reproducir/pausar, detener, silenciar y volumen mostrados además de la ventana de vídeo o visualización.                                                    | ![uiMode = ' Mini ' con audio](images/uimode-mini-audio-v11.png) | ![uiMode = ' Mini ' con vídeo](images/uimode-mini-video-v11.png) |
| full      | Predeterminada. Windows Media Player está incrustado con los controles ventana de estado, barra de búsqueda, reproducir/pausar, detener, silenciar, siguiente, anterior, avance rápido, rebobinar y volumen, además de la ventana de vídeo o visualización. | ![uiMode = ' Full ' con audio](images/uimode-full-audio-v11.png) | ![uiMode = ' Full ' con vídeo](images/uimode-full-video-v11.png) |
| custom    | Windows Media Player está incrustado con una interfaz de usuario personalizada. Solo se puede usar en programas de C++.                                                                                                                | (Se muestra la interfaz de usuario personalizada).                           | (Se muestra la interfaz de usuario personalizada).                           |



 

## <a name="remarks&quot;></a>Observaciones

Esta propiedad especifica la apariencia del Media Player de Windows incrustado. Cuando **uiMode** se establece en &quot;none&quot;, &quot;mini&quot; o &quot;Full&quot;, hay una ventana para la presentación de clips de vídeo y visualizaciones de audio. Esta ventana se puede ocultar en el modo mini o completo estableciendo el atributo de **alto** de la etiqueta de **objeto** en 40, que se mide desde la parte inferior, y deja visible la parte controles de la interfaz de usuario. Si no se desea ninguna interfaz incrustada, establezca los atributos **ancho** y **alto** en cero.

Si **uiMode** se establece en &quot;invisible&quot;, no se muestra ninguna interfaz de usuario, pero el espacio se reserva en la página según lo especificado en **ancho** y **alto**. Esto resulta útil para conservar el diseño de página cuando **uiMode** puede cambiar. Además, el espacio reservado es transparente, por lo que todos los elementos que estén en capas detrás del control serán visibles.

Si **uiMode** se establece en &quot;Full&quot; o &quot;mini&quot;, Windows Media Player muestra los controles de transporte en modo de pantalla completa. Si **uiMode** se establece en &quot;none&quot;, no se muestra ningún control en el modo de pantalla completa.

Si la ventana está visible y el contenido de audio se está reproduciendo, la visualización que se muestra será la que se usó más recientemente en Windows Media Player.

Si **uiMode** se establece en &quot;Custom&quot; en un programa de C++ que implementa **IWMPRemoteMediaServices**, se muestra el archivo de máscara indicado por **IWMPRemoteMediaServices. GetCustomUIMode** .

Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a &quot;none&quot;.

## <a name=&quot;examples&quot;></a>Ejemplos

En el ejemplo siguiente se crea un cuadro de lista que permite al usuario cambiar el modo de interfaz de usuario para un objeto incrustado de Media Player de Windows. El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player versión 7,0 o posterior. Windows Media Player 9 series o posterior para "invisible" o "personalizado"<br/>   |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. enableContextMenu (VB y C#)**](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





