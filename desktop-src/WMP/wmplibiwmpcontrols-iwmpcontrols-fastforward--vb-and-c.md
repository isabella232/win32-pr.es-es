---
title: IWMPControls fastForward, método
description: El método fastForward inicia la reproducción rápida del elemento multimedia en la dirección de avance. | IWMPControls fastForward, método
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- método fastForward de Windows Media Player
- método fastForward Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método fastForward
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d99307a7b188b238157af62833273b8c724eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690887"
---
# <a name="iwmpcontrolsfastforward-method"></a>IWMPControls:: fastForward (método)

El método **fastForward** inicia la reproducción rápida del elemento multimedia en la dirección de avance.

## <a name="syntax"></a>Sintaxis


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método **fastForward** reproduce el clip cinco veces la velocidad normal. Llamar a **fastForward** es equivalente a especificar 5,0 para la velocidad estableciendo la propiedad **IWMPSettings. rate** . Si posteriormente se cambia la frecuencia, o si se llama a **IWMPControls. Play** o **IWMPControls. stop** , Windows Media Player dejará de reenviar rápidamente.

El método **fastForward** no funciona para las difusiones en vivo y determinados tipos de medios. Para determinar si puede avanzar rápidamente en un clip, pase el valor **System. String** "Fastforward" a la propiedad **IWMPControls. isavailable** (el método **IWMPControls. Get \_ isavailable** en C#).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **fastForward** para reenviar rápidamente el elemento multimedia actual en respuesta al evento click de un botón. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

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

[**IWMPControls. isAvailable (VB y C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. STOP (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. Rate (VB y C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





