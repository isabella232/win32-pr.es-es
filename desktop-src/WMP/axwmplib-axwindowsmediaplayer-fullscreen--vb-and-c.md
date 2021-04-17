---
title: Propiedad AxWindowsMediaPlayer. fullScreen
description: La propiedad fullScreen obtiene o establece un valor que indica si el contenido de vídeo se reproduce en el modo de pantalla completa.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- propiedad fullScreen Media Player Windows
- propiedad fullScreen Media Player Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad fullScreen
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698543"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a>Propiedad AxWindowsMediaPlayer. fullScreen

La propiedad fullScreen obtiene o establece un valor que indica si el contenido de vídeo se reproduce en el modo de pantalla completa.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Valor System. Boolean que indica si el contenido se reproduce en modo de pantalla completa. El valor predeterminado es false.

## <a name="remarks"></a>Observaciones

Para que el modo de pantalla completa funcione correctamente al insertar el control Media Player de Windows, el área de presentación del vídeo debe tener un alto y un ancho de al menos un píxel. Si **uiMode** se establece en "mini" o "Full", el alto del propio control debe ser 65 o superior para dar cabida al área de presentación de vídeo además de la interfaz de usuario.

Si **uiMode** se establece en "invisible", al establecer esta propiedad en true se genera un error y no se ve afectado el comportamiento del control.

Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) es igual a false y **uiMode** es igual a "none".

Si **uiMode** se establece en "Full" o "mini", Windows Media Player muestra los controles de transporte en modo de pantalla completa cuando se mueve el cursor del mouse. Después de un breve intervalo de ausencia de movimiento del mouse, se ocultan los controles de transporte. Si **uiMode** se establece en "none", no se muestra ningún control en el modo de pantalla completa.

> [!Note]  
> Para mostrar los controles de transporte en modo de pantalla completa, se requiere el sistema operativo Windows XP.

 

Si los controles de transporte no se muestran en el modo de pantalla completa, Windows Media Player sale automáticamente del modo de pantalla completa cuando se detiene la reproducción.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un botón que utiliza la propiedad fullScreen para cambiar un objeto reproductor incrustado al modo de pantalla completa. El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                  |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                            |
| Ensamblado<br/>  | <dl> <dt>AxInterop. WMPLib (AxInterop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. uiMode (VB y C#)**](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





