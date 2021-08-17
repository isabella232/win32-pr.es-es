---
title: Propiedad downloadProgress de IWMPNetwork
description: La propiedad downloadProgress obtiene el porcentaje de descarga completada.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- downloadProgress, propiedad Reproductor de Windows Media
- downloadProgress, propiedad Reproductor de Windows Media , interfaz IWMPNetwork
- Interfaz IWMPNetwork Reproductor de Windows Media , downloadProgress, propiedad
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c2b47895d595a570191d9aa66b90b1cdc53392f8f111d64307074e5689f2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331985"
---
# <a name="iwmpnetworkdownloadprogress-property"></a>Propiedad IWMPNetwork::d ownloadProgress

La **propiedad downloadProgress** obtiene el porcentaje de descarga completada.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el progreso de descarga expresado como porcentaje.

## <a name="remarks"></a>Comentarios

Cuando el control Reproductor de Windows Media está conectado a un archivo multimedia digital que se puede reproducir y descargar al mismo tiempo, la propiedad **downloadProgress** obtiene el porcentaje del archivo total que se ha descargado. Esta característica solo se admite actualmente para archivos multimedia digitales descargados de servidores web. Se puede descargar y reproducir simultáneamente un archivo de cualquiera de los siguientes formatos:

-   Formato ASF
-   Audio de Windows Media (WMA)
-   Vídeo de Windows Media (WMV)
-   MP3
-   MPEG
-   WAV

Además, algunos archivos AVI se pueden descargar y reproducir simultáneamente.

Use **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** para determinar cuándo se inicia o se detiene el almacenamiento en búfer.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **usa downloadProgress** para mostrar el porcentaje de descarga completada. La información se muestra en una etiqueta, en respuesta al **evento de almacenamiento en** búfer. En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


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

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
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

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Evento AxWindowsMediaPlayer.Buffering (VB y C#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





