---
title: Propiedad AxWindowsMediaPlayer.fullScreen
description: La propiedad fullScreen obtiene o establece un valor que indica si el contenido del vídeo se reproduce en modo de pantalla completa.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- propiedad fullScreen Reproductor de Windows Media
- propiedad fullScreen Reproductor de Windows Media clase , AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media , propiedad fullScreen
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
ms.openlocfilehash: e128d8c7e0cf49d3feaae723a7fb5a51740cda47e5016df6290b4852c20ec27b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902625"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a>Propiedad AxWindowsMediaPlayer.fullScreen

La propiedad fullScreen obtiene o establece un valor que indica si el contenido del vídeo se reproduce en modo de pantalla completa.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Valor System.Boolean que indica si el contenido se reproduce en modo de pantalla completa. El valor predeterminado es false.

## <a name="remarks"></a>Comentarios

Para que el modo de pantalla completa funcione correctamente al insertar el control Reproductor de Windows Media, el área de visualización del vídeo debe tener un alto y un ancho de al menos un píxel. Si **uiMode** se establece en "mini" o "full", el alto del propio control debe ser 65 o superior para alojar el área de presentación de vídeo además de la interfaz de usuario.

Si **uiMode** se establece en "invisible", establecer esta propiedad en true genera un error y no afecta al comportamiento del control.

Durante la reproducción a pantalla completa, Reproductor de Windows Media el cursor del mouse cuando [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) es igual a false y **uiMode** es igual a "none".

Si **uiMode** está establecido en "full" o "mini", Reproductor de Windows Media controles de transporte en modo de pantalla completa cuando se mueve el cursor del mouse. Después de un breve intervalo sin movimiento del mouse, se ocultan los controles de transporte. Si **uiMode** está establecido en "none", no se muestra ningún control en modo de pantalla completa.

> [!Note]  
> La visualización de controles de transporte en modo de pantalla completa requiere el Windows operativo XP.

 

Si los controles de transporte no se muestran en modo de pantalla completa, Reproductor de Windows Media automáticamente sale del modo de pantalla completa cuando se detiene la reproducción.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un botón que usa la propiedad fullScreen para cambiar un objeto de reproductor incrustado al modo de pantalla completa. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


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
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                  |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                            |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib (AxInterop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.uiMode (VB y C#)**](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





