---
title: Método playItem de IWMPControls
description: El método playItem reproduce el elemento multimedia especificado. | Método playItem de IWMPControls
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- Método playItem Reproductor de Windows Media
- Método playItem Reproductor de Windows Media interfaz , IWMPControls
- Interfaz IWMPControls Reproductor de Windows Media , método playItem
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070752"
---
# <a name="iwmpcontrolsplayitem-method"></a>IWMPControls::p layItem (método)

El **método playItem** reproduce el elemento multimedia especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIWMPMedia* \[ En\]
</dt> <dd>

Interfaz **WMPLib.IWMPMedia** al elemento multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El elemento multimedia se cargará y reproducirá automáticamente, independientemente del valor de la **propiedad IWMPSettings.autoStart.** Para cargar un elemento sin reproducirlo automáticamente, establezca **IWMPSettings.autoStart** en **false** y asigne un valor a **AxWindowsMediaPlayer.URL**, después del cual se puede llamar a **IWMPControls.play** para empezar a reproducir el elemento.

Nota:

**playItem solo** funciona con elementos de **AxWindowsMediaPlayer.currentPlaylist.** No se admite la llamada a **playItem** con una referencia a un elemento multimedia guardado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa playItem** para reproducir un elemento multimedia de la lista de reproducción actual. El elemento que se va a reproducir se elige en función de su posición en la lista de reproducción. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AxWindowsMediaPlayer.currentPlaylist (VB y C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB y C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.Item (VB y C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.autoStart (VB y C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





