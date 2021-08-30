---
title: Método fastForward de IWMPControls
description: El método fastForward inicia el juego rápido del elemento multimedia en la dirección hacia delante. | Método fastForward de IWMPControls
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- Método fastForward Reproductor de Windows Media
- Método fastForward Reproductor de Windows Media interfaz , IWMPControls
- Interfaz IWMPControls Reproductor de Windows Media método , fastForward
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
ms.openlocfilehash: f283ef56f3831f58b8d57f3d172ad3b80163ee62fdaa24b05bdca02c68cafcf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031335"
---
# <a name="iwmpcontrolsfastforward-method"></a>IWMPControls::fastForward (método)

El **método fastForward** inicia el juego rápido del elemento multimedia en la dirección hacia delante.

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

## <a name="remarks"></a>Comentarios

El **método fastForward** reproduce el clip a una velocidad cinco veces mayor que la normal. Llamar **a fastForward** equivale a especificar 5,0 para la velocidad estableciendo la **propiedad IWMPSettings.rate.** Si posteriormente se cambia la velocidad, o si se llama a **IWMPControls.play** o **IWMPControls.stop,** Reproductor de Windows Media el reenvío rápido.

El **método fastForward** no funciona para difusiones en directo y determinados tipos de medios. Para determinar si puede avanzar rápidamente en un clip, pase el valor **System.String** "FastForward" a la propiedad **IWMPControls.isAvailable** (el método **IWMPControls.get \_ isAvailable** en C#).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa fastForward para** reenviar rápidamente el elemento multimedia actual en respuesta al evento Click de un botón. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


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
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.isAvailable (VB y C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls.stop (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.rate (VB y C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





