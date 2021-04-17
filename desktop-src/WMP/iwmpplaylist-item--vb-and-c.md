---
title: IWMPPlaylist. Item (VB y C)
description: La propiedad Item (el \_ método get item en C \) obtiene una interfaz para el elemento multimedia en el índice especificado.
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- IWMPPlaylist. Item (VB y C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1318f37c3f590eec2c97252e2f484b0d1bc6d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689958"
---
# <a name="iwmpplaylistitem-vb-and-c"></a>IWMPPlaylist. Item (VB y C#)

La propiedad **Item** (el método **Get \_ Item** en C#) obtiene una interfaz para el elemento multimedia en el índice especificado.


```
[Visual Basic]
ReadOnly Property Item(
  lIndex As System.Int32
) As IWMPMedia
```




```
[C#]
IWMPMedia get_Item (
  System.Int32 lIndex 
);
```



## <a name="parameters"></a>Parámetros

*lIndex*

**System. Int32** que es el índice del elemento multimedia de la lista de reproducción.

## <a name="property-value"></a>Valor de propiedad

Una interfaz **WMPLib. IWMPMedia** que proporciona acceso al elemento multimedia en el índice especificado.

## <a name="remarks"></a>Observaciones

**IWMPPlaylist. Item** es una propiedad de solo lectura en Visual Basic que toma un parámetro, mientras que en C# se conoce como el método **IWMPPlaylist. Get \_ Item** .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa la propiedad **Item** (el método **Get \_ Item** en C#) para recuperar un elemento multimedia de una lista de reproducción basada en una selección de usuario. Se ha creado un cuadro de lista con el nombre weblist y se han rellenado con los títulos de la lista de reproducción denominada audioPlaylist. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void weblist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the selected item in the list box.
    int index = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Store the corresponding media item from the playlist.
    WMPLib.IWMPMedia listItem = audioPlaylist.get_Item(index);

    // Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL;
}
```


```VB

Public Sub weblist_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles weblist.SelectedIndexChanged

    &#39; Store the index of the selected item in the list box.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim index As Integer = lb.SelectedIndex

    &#39; Store the corresponding media item from the playlist.
    Dim listItem As WMPLib.IWMPMedia = audioPlaylist.Item(index)

    &#39; Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL

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

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. removeItem (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





