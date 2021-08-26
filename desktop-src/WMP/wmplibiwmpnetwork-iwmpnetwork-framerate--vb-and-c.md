---
title: Propiedad frameRate de IWMPNetwork
description: La propiedad frameRate obtiene la velocidad de fotogramas de vídeo actual.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- Propiedad frameRate Reproductor de Windows Media
- Propiedad frameRate Reproductor de Windows Media , interfaz IWMPNetwork
- Interfaz IWMPNetwork Reproductor de Windows Media , propiedad frameRate
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3169cc21eee2317da45db3cb3ca9ceffffa01c85479312defe63cda1fa09796f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956165"
---
# <a name="iwmpnetworkframerate-property"></a>Propiedad IWMPNetwork::frameRate

La **propiedad frameRate** obtiene la velocidad de fotogramas de vídeo actual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es la velocidad de fotogramas actual en fotogramas por cien segundos.

> [!Note]  
> Aunque la **propiedad encodedFrameRate** mide la velocidad de fotogramas codificada en fotogramas por segundo, la propiedad **frameRate** mide la velocidad de fotogramas actual en fotogramas por cien segundos. Vea la sección Comentarios.

 

## <a name="remarks"></a>Comentarios

El valor de velocidad de fotogramas actual se devuelve en fotogramas por cien segundos. Por ejemplo, un valor de 2998 indica 29,98 fotogramas por segundo (fps).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **usa frameRate** para mostrar la velocidad de fotogramas especificada cuando se codificó el archivo. La información se muestra en una etiqueta en respuesta al **evento PlayStateChange.** El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.encodedFrameRate (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





