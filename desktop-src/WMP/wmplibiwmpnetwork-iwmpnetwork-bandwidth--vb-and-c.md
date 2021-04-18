---
title: Propiedad de ancho de banda IWMPNetwork
description: La propiedad de ancho de banda obtiene el ancho de banda actual del elemento multimedia.
ms.assetid: 4355aa14-bca7-4b46-aad5-3e3796a54735
keywords:
- propiedades de ancho de banda Media Player de Windows
- propiedad de ancho de banda Media Player de Windows, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad ancho de banda
topic_type:
- apiref
api_name:
- IWMPNetwork.bandWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df9a55f9d5c6724c428b75a4171c2e8b7ca13d18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699578"
---
# <a name="iwmpnetworkbandwidth-property"></a>IWMPNetwork:: bandWidth (propiedad)

La propiedad de **ancho** de banda obtiene el ancho de banda actual del elemento multimedia.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 bandWidth {get; set;}
```


```VB

Public ReadOnly Property bandWidth As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System. Int32** que es el ancho de banda.

## <a name="remarks"></a>Observaciones

El valor recuperado a través de **AxWindowsMediaPlayer. URL** será cero si no se establece la dirección URL. Esta propiedad solo es válida para los medios de streaming.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **ancho de banda** para mostrar el ancho de banda multimedia actual. La información se muestra en una etiqueta en respuesta al evento **PlayStateChange** . El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bandwidth when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bandWidth != 0)
            {
                bandWidthLabel.Text = "Current Bandwidth: " + player.network.bandWidth + " K bits/second";
            }
            else
            {
                bandWidthLabel.Text = "Bandwidth is only available for streaming media.";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the bandWidth when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bandWidth <> 0) Then

                bandWidthLabel.Text = &quot;Current Bandwidth: &quot; + player.network.bandWidth + &quot; K bits/second&quot;

            Else

                bandWidthLabel.Text = &quot;Bandwidth is only available for streaming media.&quot;

            End If

    End Select

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

[**AxWindowsMediaPlayer. URL (VB y C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





