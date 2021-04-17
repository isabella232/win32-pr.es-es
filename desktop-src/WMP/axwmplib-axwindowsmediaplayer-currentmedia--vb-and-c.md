---
title: Propiedad AxWindowsMediaPlayer. currentMedia
description: La propiedad currentMedia obtiene o establece la interfaz IWMPMedia que corresponde al elemento multimedia actual.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- propiedades de currentMedia Media Player de Windows
- propiedad currentMedia Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad currentMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3720a36d2a1969c652ed757f31301cf6a9ead706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700090"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a>Propiedad AxWindowsMediaPlayer. currentMedia

La propiedad currentMedia obtiene o establece la interfaz IWMPMedia que corresponde al elemento multimedia actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a>Valor de propiedad

La interfaz WMPLib. IWMPMedia que proporciona acceso al elemento multimedia actual.

## <a name="remarks"></a>Observaciones

Si AxWindowsMediaPlayer. Settings. la propiedad **autoStart** es true, la reproducción se inicia automáticamente cada vez que se establece **currentMedia**.

Puede recuperar una interfaz IWMPMedia para un elemento multimedia determinado a través de la propiedad IWMPPlaylist. Item (el método IWMPPlaylist. Get \_ Item en C#). Para cargar un elemento multimedia con un nombre de archivo, establezca la propiedad URL o use newMedia.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se recupera el primer elemento multimedia de la biblioteca y se usa la propiedad currentMedia para establecer el elemento multimedia recuperado como el elemento multimedia actual y mostrar su nombre. El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
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

[**AxWindowsMediaPlayer. newMedia (VB y C#)**](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB y C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. Item (VB y C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. autoStart (VB y C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





