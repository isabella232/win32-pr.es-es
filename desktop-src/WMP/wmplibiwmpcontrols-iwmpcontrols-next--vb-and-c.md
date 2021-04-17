---
title: Método Next IWMPControls
description: El siguiente método establece el elemento siguiente de la lista de reproducción como el elemento actual.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- siguiente método de Windows Media Player
- siguiente método de Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método Next
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690877"
---
# <a name="iwmpcontrolsnext-method"></a>IWMPControls:: Next (método)

El **siguiente** método establece el elemento siguiente de la lista de reproducción como el elemento actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la lista de reproducción está en la última entrada cuando se invoca **siguiente** , la primera entrada de la lista de reproducción se convertirá en la actual.

En las listas de reproducción del lado servidor, este método omite el siguiente elemento de la lista de reproducción del servidor, no la lista de reproducción del cliente.

Al reproducir un DVD, este método omite el siguiente capítulo lógico de la secuencia de reproducción, que puede no ser el siguiente capítulo de la lista de reproducción. Al reproducir imágenes de DVD seguidas, este método pasa a la siguiente imagen.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **Next** para moverse al siguiente elemento de la lista de reproducción actual en respuesta al evento click de un botón. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

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

[**IWMPControls. Previous (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[**IWMPControls. STOP (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





