---
title: Propiedad durationString de IWMPMedia
description: La propiedad durationString obtiene una cadena que indica la duración del elemento multimedia actual en formato HH MM SS.
ms.assetid: de33c737-d73e-41f0-9c1b-944279194738
keywords:
- propiedad durationString Reproductor de Windows Media
- propiedad durationString Reproductor de Windows Media , interfaz IWMPMedia
- Interfaz IWMPMedia Reproductor de Windows Media propiedad , durationString
topic_type:
- apiref
api_name:
- IWMPMedia.durationString
- IWMPMedia.get_durationString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e6bc732388036aa9e79aeedd988de94fa263bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473302"
---
# <a name="iwmpmediadurationstring-property"></a>Propiedad IWMPMedia::d urationString

La **propiedad durationString** obtiene una cadena que indica la duración del elemento multimedia actual en formato HH:MM:SS.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String durationString {get;}
```


```VB

Public ReadOnly Property durationString As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es la duración.

## <a name="remarks"></a>Observaciones

Si esta propiedad se usa con un elemento multimedia distinto del especificado en AxWindowsMediaPlayer.currentMedia, es posible que no contenga un valor válido. Si el elemento multimedia tiene menos de una hora de duración, se omite la parte de horas del valor devuelto.

Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa durationString** para mostrar la duración del elemento multimedia actual como texto con formato en una etiqueta. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Display the formatted duration string in the label.
         mediaDuration.Text = player.currentMedia.durationString;
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = 13) Then

        &#39; Display the formatted duration string in the label.
        mediaDuration.Text = player.currentMedia.durationString

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

[**AxWindowsMediaPlayer.currentMedia (VB y C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.duration (VB y C#)**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)
</dt> </dl>

 

 





