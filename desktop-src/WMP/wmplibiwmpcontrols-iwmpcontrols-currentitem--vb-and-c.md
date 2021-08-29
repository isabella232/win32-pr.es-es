---
title: Propiedad currentItem de IWMPControls
description: La propiedad currentItem obtiene o establece el elemento multimedia actual en una lista de reproducción.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- propiedad currentItem Reproductor de Windows Media
- Propiedad currentItem Reproductor de Windows Media interfaz , IWMPControls
- Interfaz IWMPControls Reproductor de Windows Media , propiedad currentItem
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
ms.openlocfilehash: 8d8193dc349524495e021dc048ac4be3673d38ec7da30aa1bb72d94960a0989f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053665"
---
# <a name="iwmpcontrolscurrentitem-property"></a>Propiedad IWMPControls::currentItem

La **propiedad currentItem** obtiene o establece el elemento multimedia actual en una lista de reproducción.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a>Valor de propiedad

Interfaz **WMPLib.IWMPMedia** que representa el elemento multimedia.

## <a name="remarks"></a>Comentarios

Esta propiedad solo funciona con elementos de la lista de reproducción actual. No se admite el establecimiento de **currentItem** en la interfaz de un elemento multimedia guardado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa currentItem** para establecer el elemento multimedia actual del reproductor en un elemento seleccionado de un cuadro de lista. El cuadro de lista se ha rellenado con todos los elementos de la lista de reproducción actual. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


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



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPControlsInterface (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPMediaInterface (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getByName(VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





