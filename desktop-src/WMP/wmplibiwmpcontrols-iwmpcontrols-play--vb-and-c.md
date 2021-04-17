---
title: IWMPControls Play (método)
description: El método play comienza la reproducción del elemento multimedia actual o reanuda la reproducción de un elemento en pausa.
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- método play Windows Media Player
- método play Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método play
topic_type:
- apiref
api_name:
- IWMPControls.play
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd87a2e2ba3d53b119df328fa68668c91c78d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690875"
---
# <a name="iwmpcontrolsplay-method"></a>IWMPControls::p establecer método

El método **Play** comienza la reproducción del elemento multimedia actual o reanuda la reproducción de un elemento en pausa.

## <a name="syntax"></a>Sintaxis


```CSharp
public void play();
```


```VB

Public Sub play()
Implements IWMPControls.play
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si se llama a este método durante el reenvío rápido o el rebobinado, la velocidad de reproducción (el valor de **IWMPSettings. rate**) se establece en 1,0.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **Play** para reproducir el elemento multimedia actual en respuesta al evento click de un botón. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void playButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("play"))
    {
        controls.play();
    }
}
```


```VB

Public Sub playButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;play&quot;)) Then

        controls.play()

    End If

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. playItem (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. Rate (VB y C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





