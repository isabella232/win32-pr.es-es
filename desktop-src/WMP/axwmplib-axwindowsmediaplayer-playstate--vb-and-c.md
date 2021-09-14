---
title: Propiedad AxWindowsMediaPlayer.playState
description: La propiedad playState obtiene un valor de enumeración que indica el estado de la Reproductor de Windows Media operación.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- Propiedad playState Reproductor de Windows Media
- propiedad playState Reproductor de Windows Media clase , AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media , propiedad playState
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889625"
---
# <a name="axwindowsmediaplayerplaystate-property"></a>Propiedad AxWindowsMediaPlayer.playState

La propiedad playState obtiene un valor de enumeración que indica el estado de la Reproductor de Windows Media operación.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a>Valor de propiedad

Valor de enumeración WMPLib.WMPPlayState.

## <a name="remarks"></a>Observaciones

Reproductor de Windows Media se garantiza que los estados se produzcan en un orden determinado. Además, no todos los estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de estado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa la propiedad playState para mostrar el estado de reproducción actual del reproductor en una etiqueta. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer.PlayStateChange (VB y C#)**](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





