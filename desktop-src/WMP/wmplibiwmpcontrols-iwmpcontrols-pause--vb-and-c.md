---
title: IWMPControls PAUSE (método)
description: El método PAUSE pausa la reproducción del elemento multimedia. | IWMPControls PAUSE (método)
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- pausar el método Windows Media Player
- pausar el método Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, pausar método
topic_type:
- apiref
api_name:
- IWMPControls.pause
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf89cfef66c84be76a529d9c0cef6ec3ae6ac40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690876"
---
# <a name="iwmpcontrolspause-method"></a>IWMPControls::p método ause

El método **PAUSE pausa** la reproducción del elemento multimedia.

## <a name="syntax"></a>Sintaxis


```CSharp
public void pause();
```


```VB

Public Sub pause()
Implements IWMPControls.pause
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando un archivo está en pausa, Windows Media Player no proporciona ningún recurso del sistema, como el dispositivo de audio.

Para determinar si un tipo de medio determinado se puede pausar, pase el valor **System. String** "PAUSE" a la propiedad **IWMPControls. isavailable** (el método **IWMPControls. Get \_ isavailable** en C#).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **PAUSE** para pausar la reproducción del elemento multimedia actual en respuesta al evento click de un botón. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void pauseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("pause"))
    {
        controls.pause();
    }
}
```


```VB

Public Sub pauseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles pauseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;pause&quot;)) Then

        controls.pause()

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
</dt> </dl>

 

 





