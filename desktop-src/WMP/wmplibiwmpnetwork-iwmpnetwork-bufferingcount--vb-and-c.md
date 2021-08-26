---
title: Propiedad IWMPNetwork bufferingCount
description: La propiedad bufferingCount obtiene el número de veces que se produjo el almacenamiento en búfer durante la reproducción.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- bufferingCount, propiedad Reproductor de Windows Media
- bufferingCount, propiedad Reproductor de Windows Media , interfaz IWMPNetwork
- Interfaz IWMPNetwork Reproductor de Windows Media , propiedad bufferingCount
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b69169e950cf3794d613bfd1d79d4953ce8f8a8bb01efe9ff17d6fa5961071
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899975"
---
# <a name="iwmpnetworkbufferingcount-property"></a>IWMPNetwork::bufferingCount, propiedad

La **propiedad bufferingCount** obtiene el número de veces que se produjo el almacenamiento en búfer durante la reproducción.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el recuento de almacenamiento en búfer.

## <a name="remarks"></a>Comentarios

Cada vez que se detiene y reinicia la reproducción, esta propiedad se restablece en cero. No se restablece si la reproducción está en pausa.

El almacenamiento en búfer solo se aplica al contenido de streaming. Esta propiedad obtiene información válida solo durante el tiempo de ejecución cuando se establece la dirección URL para la reproducción mediante la **propiedad AxWindowsMediaPlayer.URL.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se *usa bufferingCount para* mostrar el número de veces que se produce el almacenamiento en búfer durante la reproducción. La información se muestra en una etiqueta en respuesta al evento de almacenamiento en búfer. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

    End If

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

[**AxWindowsMediaPlayer.URL (VB y C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





