---
title: Propiedad AxWindowsMediaPlayer.uiMode
description: La propiedad uiMode obtiene o establece un valor que indica qué controles se muestran en la interfaz de usuario.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- propiedad uiMode Reproductor de Windows Media
- propiedad uiMode Reproductor de Windows Media clase , AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media propiedad , uiMode
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243327"
---
# <a name="axwindowsmediaplayeruimode-property"></a>Propiedad AxWindowsMediaPlayer.uiMode

La propiedad uiMode obtiene o establece un valor que indica qué controles se muestran en la interfaz de usuario.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a>Valor de propiedad

System.String que es uno de los valores siguientes.



| Value     | Descripción                                                                                                                                                                                                     | Ejemplo de audio                                                   | Ejemplo de vídeo                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| invisibles | Reproductor de Windows Media se inserta sin ninguna interfaz de usuario visible (controles, vídeo o ventana de visualización).                                                                                                  | (No se muestra nada).                                         | (No se muestra nada).                                         |
| ninguno      | Reproductor de Windows Media se inserta sin controles y solo se muestra la ventana de vídeo o visualización.                                                                                                   | ![uimode = 'none' con audio](images/uimode-none-audio-v11.png) | ![uimode = 'none' con vídeo](images/uimode-none-video-v11.png) |
| Mini      | Reproductor de Windows Media se inserta con los controles de ventana de estado, reproducir/pausar, detener, silenciar y volumen que se muestran además de la ventana de vídeo o visualización.                                                    | ![uimode = 'mini' con audio](images/uimode-mini-audio-v11.png) | ![uimode = 'mini' con vídeo](images/uimode-mini-video-v11.png) |
| full      | Predeterminada. Reproductor de Windows Media se incrusta con la ventana de estado, buscar barra, reproducir/pausar, detener, silenciar, siguiente, anterior, avance rápido, rebobinar y controles de volumen además de la ventana de vídeo o visualización. | ![uimode = 'full' con audio](images/uimode-full-audio-v11.png) | ![uimode = 'full' con vídeo](images/uimode-full-video-v11.png) |
| custom    | Reproductor de Windows Media se inserta con una interfaz de usuario personalizada. Solo se puede usar en programas de C++.                                                                                                                | (Se muestra la interfaz de usuario personalizada).                           | (Se muestra la interfaz de usuario personalizada).                           |



 

## <a name="remarks"></a>Observaciones

Esta propiedad especifica la apariencia de la Reproductor de Windows Media. Cuando **uiMode** se establece en "none", "mini" o "full", hay una ventana para mostrar clips de vídeo y visualizaciones de audio. Esta ventana se puede ocultar en modo mini o completo estableciendo el atributo **height** de la etiqueta **OBJECT** en 40, que se mide desde la parte inferior, y deja visible la parte de los controles de la interfaz de usuario. Si no se desea ninguna interfaz incrustada, establezca los atributos **de** ancho y **alto** en cero.

Si **uiMode** está establecido en "invisible", no se muestra ninguna interfaz de usuario, pero el espacio todavía está reservado en la página según lo especificado por **el** ancho y **el alto**. Esto resulta útil para conservar el diseño de página cuando **uiMode** puede cambiar. Además, el espacio reservado es transparente, por lo que todos los elementos situados detrás del control serán visibles.

Si **uiMode** está establecido en "full" o "mini", Reproductor de Windows Media controles de transporte en modo de pantalla completa. Si **uiMode** está establecido en "none", no se muestra ningún control en modo de pantalla completa.

Si la ventana está visible y se reproduce contenido de audio, la visualización mostrada será la que se usó más recientemente en Reproductor de Windows Media.

Si **uiMode** se establece en "custom" en un programa de C++ que implementa **IWMPRemoteMediaServices**, se muestra el archivo de máscara indicado por **IWMPRemoteMediaServices.GetCustomUIMode.**

Durante la reproducción a pantalla completa, Reproductor de Windows Media el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un cuadro de lista que permite al usuario cambiar el modo de interfaz de usuario para un objeto Reproductor de Windows Media incrustado. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add("invisible");
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
| Versión<br/>   | Reproductor de Windows Media versión 7.0 o posterior. Reproductor de Windows Media serie 9 o posterior para "invisible" o "personalizado"<br/>   |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.enableContextMenu (VB y C#)**](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





