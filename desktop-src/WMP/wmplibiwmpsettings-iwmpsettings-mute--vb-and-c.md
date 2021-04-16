---
title: Propiedad IWMPSettings MUTE
description: La propiedad MUTE obtiene o establece un valor que indica si el audio está silenciado.
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- silenciar las ventanas de propiedades Media Player
- propiedad silenciar Media Player de Windows, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad MUTE
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67518bb9a6eccee13e4cc262f37341d30689439e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105719025"
---
# <a name="iwmpsettingsmute-property"></a>IWMPSettings:: MUTE (propiedad)

La propiedad **MUTE** obtiene o establece un valor que indica si el audio está silenciado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Un valor **System. Boolean** que indica si el audio está silenciado. El valor predeterminado es **false**.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea una casilla y se alterna la propiedad **MUTE** para silenciar el audio y dejar de silenciarlo cuando se cambia el estado de activación del cuadro. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

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

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. Rate (VB y C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





