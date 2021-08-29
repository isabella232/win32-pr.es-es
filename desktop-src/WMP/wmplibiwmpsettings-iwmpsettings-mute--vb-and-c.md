---
title: Propiedad de exclusión mutua IWMPSettings
description: La propiedad mute obtiene o establece un valor que indica si el audio está silenciado.
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- exclusión de la propiedad Reproductor de Windows Media
- mute property Reproductor de Windows Media , IWMPSettings (interfaz)
- Interfaz IWMPSettings Reproductor de Windows Media , propiedad mute
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
ms.openlocfilehash: f6d4cb13fd8884df7779b2780fd7014d058f32086d67ace286d9d8a9fd57cb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053413"
---
# <a name="iwmpsettingsmute-property"></a>Propiedad IWMPSettings::mute

La **propiedad mute** obtiene o establece un valor que indica si el audio está silenciado.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Valor **System.Boolean** que indica si el audio está silenciado. El valor predeterminado es **false**.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea  una casilla y se alterna la propiedad mute para silenciar y desactivar el audio cuando se cambia el estado activado de la casilla. **El objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


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



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.rate (VB y C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





