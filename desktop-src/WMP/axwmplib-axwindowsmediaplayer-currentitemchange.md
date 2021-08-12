---
title: Evento CurrentItemChange del objeto AxWindowsMediaPlayer
description: El evento CurrentItemChange tiene lugar cuando cambia el valor de IWMPControls.currentItem.
ms.assetid: c5eeafd2-405b-4808-97d1-399a2344ca42
keywords:
- Evento CurrentItemChange del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CurrentItemChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1786fab3e312f95550103cdc6cf4f2558e25e883df9c7be2d6f850a7f8a5ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582561"
---
# <a name="currentitemchange-event-of-the-axwindowsmediaplayer-object"></a>Evento CurrentItemChange del objeto AxWindowsMediaPlayer

El evento CurrentItemChange tiene lugar cuando el valor de IWMPControls. **currentItem** cambia.

``` syntax
[C#]
private void player_CurrentItemChange(
  object sender,
  _WMPOCXEvents_CurrentItemChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentItemChange(  
  sender As Object,
  e As _WMPOCXEvents_CurrentItemChangeEvent
) Handles player.CurrentItemChange
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad   | Descripción                                                                                                   |
|------------|---------------------------------------------------------------------------------------------------------------|
| pdispMedia | System.ObjectEl nuevo elemento multimedia actual. Puede convertir esto en una interfaz IWMPMedia para acceder a ella.<br/> |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un controlador de eventos para el evento CurrentItemChange. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


```CSharp
// Add a delegate for the CurrentItemChange event
player.CurrentItemChange += new AxWMPLib._WMPOCXEvents_CurrentItemChangeEventHandler(player_CurrentItemChange);

private void player_CurrentItemChange(object sender, AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent e)
{
    // Display the name of the new media item.
    mediaText.Text = player.currentMedia.name;
}
```


```VB

Public Sub player_CurrentItemChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent) Handles player.CurrentItemChange

    &#39; Display the name of the new media item.
    mediaText.Text = player.currentMedia.name

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentItem (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





