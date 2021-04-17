---
title: IWMPControls currentItem (propiedad)
description: La propiedad currentItem obtiene o establece el elemento multimedia actual en una lista de reproducción.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- propiedad currentItem Media Player de Windows
- propiedad currentItem Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, propiedad currentItem
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae04eb333e2fd347fa6f88b33ec2482a4dd8fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690891"
---
# <a name="iwmpcontrolscurrentitem-property"></a>IWMPControls:: currentItem (propiedad)

La propiedad **CurrentItem** obtiene o establece el elemento multimedia actual en una lista de reproducción.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a>Valor de propiedad

Una interfaz **WMPLib. IWMPMedia** que representa el elemento multimedia.

## <a name="remarks"></a>Observaciones

Esta propiedad solo funciona con los elementos de la lista de reproducción actual. No se admite el establecimiento de **CurrentItem** en la interfaz de un elemento multimedia guardado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **CurrentItem** para establecer el elemento multimedia actual del reproductor en un elemento seleccionado en un cuadro de lista. El cuadro de lista se ha rellenado con todos los elementos de la lista de reproducción actual. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
    player.Ctlcontrols.play()

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

[**IWMPControlsInterface (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPMediaInterface (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





