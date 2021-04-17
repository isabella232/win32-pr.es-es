---
title: Método anterior IWMPControls
description: El método anterior establece el elemento anterior de la lista de reproducción como el elemento actual.
ms.assetid: 380524f5-e8b6-45c4-9f6c-3dbb49b1ac9f
keywords:
- método anterior de Windows Media Player
- método anterior de Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método Previous
topic_type:
- apiref
api_name:
- IWMPControls.previous
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823038205a026afb7141491f562698eb60515a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690873"
---
# <a name="iwmpcontrolsprevious-method"></a>IWMPControls::p método rior

El método **anterior** establece el elemento anterior de la lista de reproducción como el elemento actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public void previous();
```


```VB

Public Sub previous()
Implements IWMPControls.previous
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la lista de reproducción está en la primera entrada cuando se invoca el **anterior** , la última entrada de la lista de reproducción se convertirá en la actual.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **Previous** para moverse al elemento anterior de la lista de reproducción actual en respuesta al evento click de un botón. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void previousButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("previous"))
    {
        controls.previous();
    }
}
```


```VB

Public Sub previousButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles previousButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;previous&quot;)) Then

        controls.previous()

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

[**IWMPControls. Next (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[**IWMPControls. STOP (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





