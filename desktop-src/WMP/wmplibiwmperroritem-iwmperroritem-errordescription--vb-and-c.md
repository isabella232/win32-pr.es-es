---
title: IWMPErrorItem errorDescription, propiedad
description: La propiedad errorDescription obtiene una descripción del error.
ms.assetid: a9914c24-1d10-422a-bcba-80be9fb85108
keywords:
- errorDescription, propiedad Reproductor de Windows Media
- Propiedad errorDescription Reproductor de Windows Media , interfaz IWMPErrorItem
- Interfaz IWMPErrorItem Reproductor de Windows Media , propiedad errorDescription
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2976db1b8c67a3b467dfed87eeab13ff9ab46d21f0778dc0542b97080f231943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031195"
---
# <a name="iwmperroritemerrordescription-property"></a>IWMPErrorItem::errorDescription, propiedad

La **propiedad errorDescription** obtiene una descripción del error.

## <a name="syntax"></a>Syntax


```CSharp
public System.String errorDescription {get; set;}
```


```VB

Public ReadOnly Property errorDescription As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es la descripción del error.

## <a name="remarks"></a>Comentarios

Debe establecer **IWMPSettings.enableErrorDialogs en** **false** si decide mostrar mensajes de error personalizados.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa errorDescription en** un controlador de eventos Error para mostrar la descripción del error al usuario. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
private void player_ErrorEvent_errorDescription(object sender, System.EventArgs e)
{
    // Get the error description for the first error item.
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show("Error: " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorDescription(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error description for the first error item.
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(&quot;Error: &quot; + errDesc)

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

[**Interfaz IWMPErrorItem (VB y C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.enableErrorDialogs (VB y C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





