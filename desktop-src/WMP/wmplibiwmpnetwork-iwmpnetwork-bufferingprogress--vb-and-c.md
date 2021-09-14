---
title: Propiedad IWMPNetwork bufferingProgress
description: La propiedad bufferingProgress obtiene el porcentaje de almacenamiento en búfer completado.
ms.assetid: 8dc9f31e-7c34-4714-a633-d92c3da3052b
keywords:
- bufferingProgress, propiedad Reproductor de Windows Media
- bufferingProgress property Reproductor de Windows Media , IWMPNetwork (interfaz)
- Interfaz IWMPNetwork Reproductor de Windows Media , propiedad bufferingProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da8a27ba41e5c4e201a5bdf0197992c30bce80b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241695"
---
# <a name="iwmpnetworkbufferingprogress-property"></a>Propiedad IWMPNetwork::bufferingProgress

La **propiedad bufferingProgress** obtiene el porcentaje de almacenamiento en búfer completado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el progreso de almacenamiento en búfer expresado como porcentaje.

## <a name="remarks"></a>Observaciones

Cada vez que se detiene y reinicia la reproducción, esta propiedad se restablece a cero. No se restablece si la reproducción está en pausa.

El almacenamiento en búfer solo se aplica al contenido de streaming. Esta propiedad obtiene información válida solo durante el tiempo de ejecución cuando la dirección URL para la reproducción se establece mediante la **propiedad AxWindowsMediaPlayer.URL.**

Use **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** para determinar cuándo se inicia o detiene el almacenamiento en búfer.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa bufferingProgress** para mostrar el porcentaje de almacenamiento en búfer completado en una etiqueta, en respuesta al evento de almacenamiento en búfer. En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the buffering progress in a timer event handler.
private void UpdateBufferingProgress(object sender, EventArgs e)
{
    bufferingProgressLabel.Text = ("Buffering progress: " + player.network.bufferingProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the buffering progress in a timer event handler.
Public Sub UpdateBufferingProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    bufferingProgressLabel.Text = (&quot;Buffering progress: &quot; + player.network.bufferingProgress + &quot; percent complete&quot;)

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

[**AxWindowsMediaPlayer.URL (VB y C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer.Buffering (VB y C#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





