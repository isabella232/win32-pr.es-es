---
title: IWMPMedia imageSourceHeight, propiedad
description: La propiedad imageSourceHeight obtiene el alto del elemento multimedia actual en píxeles.
ms.assetid: d60f1713-7110-4605-9009-45825c380546
keywords:
- ImageSourceHeight, propiedad Reproductor de Windows Media
- Propiedad imageSourceHeight Reproductor de Windows Media , interfaz IWMPMedia
- Interfaz IWMPMedia Reproductor de Windows Media , propiedad imageSourceHeight
topic_type:
- apiref
api_name:
- IWMPMedia.imageSourceHeight
- IWMPMedia.get_imageSourceHeight
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b2e50aecc0efc13db4fe8f2a78cffe4ed95833d55ca9b1de70af31191aec1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861794"
---
# <a name="iwmpmediaimagesourceheight-property"></a>Propiedad IWMPMedia::imageSourceHeight

La **propiedad imageSourceHeight** obtiene el alto del elemento multimedia actual en píxeles.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 imageSourceHeight {get;}
```


```VB

Public ReadOnly Property imageSourceHeight As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32** que es el alto del elemento multimedia.

## <a name="remarks"></a>Comentarios

Si el elemento multimedia no es el actual, esta propiedad devuelve cero.

Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa imageSourceHeight** para mostrar el tamaño de imagen, en píxeles, del elemento multimedia actual en un cuadro de texto. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Store the height and width of the new media item.
         int height = player.currentMedia.imageSourceHeight;
         int width = player.currentMedia.imageSourceWidth;

         // Clear all the information in the text box.
         videoSize.Clear();

         // Test whether an image is visible.
         if (height != 0 && width != 0)
         {
            // Display the image size information.
            videoSize.Text = (width.ToString() + " x " + height.ToString());
         }
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = WMPLib.WMPOpenState.wmposMediaOpen) Then

        &#39; Store the height and width of the new media item.
        Dim Height As Integer = player.currentMedia.imageSourceHeight
        Dim Width As Integer = player.currentMedia.imageSourceWidth

        &#39; Clear all the information in the text box.
        videoSize.Clear()

        &#39; Test whether an image is visible.
        If (Height <> 0 And Width <> 0) Then

            &#39; Display the image size information.
            videoSize.Text = (Width.ToString() + &quot; x &quot; + Height.ToString())

        End If

    End If

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

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





