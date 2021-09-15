---
title: Propiedad bitRate de IWMPNetwork
description: La propiedad bitRate obtiene la velocidad de bits actual que se recibe.
ms.assetid: f7dda557-3954-45ed-9eac-6d27109e2dfa
keywords:
- bitRate, propiedad Reproductor de Windows Media
- Propiedad bitRate Reproductor de Windows Media , interfaz IWMPNetwork
- Interfaz IWMPNetwork Reproductor de Windows Media , propiedad bitRate
topic_type:
- apiref
api_name:
- IWMPNetwork.bitRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64039eb960a928f5268643e18d1a01b9034d5d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270399"
---
# <a name="iwmpnetworkbitrate-property"></a>IWMPNetwork::bitRate, propiedad

La **propiedad bitRate** obtiene la velocidad de bits actual que se recibe.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 bitRate {get; set;}
```


```VB

Public ReadOnly Property bitRate As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32** que es la velocidad de bits.

## <a name="remarks"></a>Observaciones

El valor de esta propiedad es una combinación de las velocidades de bits de las secuencias de vídeo y audio.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa bitRate para** mostrar la velocidad de bits del medio actual. La información se muestra en una etiqueta en respuesta al **evento PlayStateChange.** El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bitRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bitRate != 0)
            {
                bitRateLabel.Text = "Current Bit Rate: " + player.network.bitRate + " K bits/second";
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

    &#39; Display the bitRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bitRate <> 0) Then

                bitRateLabel.Text = &quot;Current Bit Rate: &quot; + player.network.bitRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





