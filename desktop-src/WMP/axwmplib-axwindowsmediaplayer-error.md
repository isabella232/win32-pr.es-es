---
title: Evento de error del objeto AxWindowsMediaPlayer
description: El evento de error se produce cuando el control de Media Player de Windows tiene una condición de error.
ms.assetid: d28c18a9-c650-4169-989b-8727b7a5a831
keywords:
- Evento de error del objeto AxWindowsMediaPlayer de Windows Media Player
topic_type:
- apiref
api_name:
- Error Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfd3571538aa2cdd263a9f5d57e479e73818806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698546"
---
# <a name="error-event-of-the-axwindowsmediaplayer-object"></a>Evento de error del objeto AxWindowsMediaPlayer

El evento de error se produce cuando el control de Media Player de Windows tiene una condición de error.

``` syntax
[C#]
private void player_ErrorEvent(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_ErrorEvent(  
  sender As Object,  
  e As System.EventArgs
) Handles player.ErrorEvent
```

## <a name="event-data"></a>Datos del evento

Este evento no contiene datos.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un controlador de eventos para el evento de error con el fin de mostrar el texto de la descripción del primer error en la cola de errores. El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.


```CSharp
// Add a delegate for the Error event.
player.ErrorEvent += new EventHandler(player_ErrorEvent);

private void player_ErrorEvent(object sender, System.EventArgs e)
{
    // Get the description of the first error. 
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the description of the first error. 
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPError. Item (VB y C#)**](iwmperror-item--vb-and-c.md)
</dt> <dt>

[**IWMPErrorItem. errorDescription (VB y C#)**](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md)
</dt> </dl>

 

 





