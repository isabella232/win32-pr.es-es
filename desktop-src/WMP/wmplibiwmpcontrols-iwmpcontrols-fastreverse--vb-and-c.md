---
title: IWMPControls fastReverse, método
description: El método fastReverse inicia la reproducción rápida del elemento multimedia en la dirección inversa.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- método fastReverse de Windows Media Player
- método fastReverse Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método fastReverse
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690884"
---
# <a name="iwmpcontrolsfastreverse-method"></a>IWMPControls:: fastReverse (método)

El método **fastReverse** inicia la reproducción rápida del elemento multimedia en la dirección inversa.

## <a name="syntax"></a>Sintaxis


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método **fastReverse** recorre el clip en orden inverso cinco veces la velocidad normal, mostrando solo los fotogramas clave si se trata de un archivo de vídeo. Llamar a **fastReverse** es equivalente a especificar-5,0 para la tasa estableciendo la propiedad **IWMPSettings. rate** . Si posteriormente se cambia la frecuencia, o si se llama a **IWMPControls. Play** o **IWMPControls. stop** , Windows Media Player dejará de ser inversa rápido.

Si el elemento forma parte de una lista de reproducción, **fastReverse** se detiene al principio de la pista actual. Por ejemplo, si el seguimiento 3 está en **fastReverse**, cuando se alcanza el comienzo de la pista 3, Windows Media Player no irá al seguimiento 2. El recuento de reproducción no se incrementa al llamar a **fastReverse**.

Si llama a **IWMPControls. fastForward** mientras **fastReverse** se está ejecutando, se detendrá **fastReverse** y **IWMPControls. fastForward** comenzará.

Este método no funciona para las difusiones en vivo y determinados tipos de medios digitales. Para determinar si puede usar Fast inverso en un clip, pase el valor **System. String** "FastReverse" a la propiedad **IWMPControls. isavailable** (el método **IWMPControls. Get \_ isavailable** en C#).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **fastReverse** para invertir el elemento multimedia actual en respuesta al evento click de un botón. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

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

[**IWMPControls. fastForward (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls. isAvailable (VB y C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. STOP (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. Rate (VB y C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





