---
title: Propiedad sourceURL de IWMPMedia
description: La propiedad sourceURL obtiene la dirección URL del elemento multimedia.
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- Propiedad sourceURL Reproductor de Windows Media
- Propiedad sourceURL Reproductor de Windows Media , interfaz IWMPMedia
- Interfaz IWMPMedia Reproductor de Windows Media , propiedad sourceURL
topic_type:
- apiref
api_name:
- IWMPMedia.sourceURL
- IWMPMedia.get_sourceURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ad2cdb2c0a67f65f7b0cf722d1b613307806d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172726"
---
# <a name="iwmpmediasourceurl-property"></a>Propiedad IWMPMedia::sourceURL

La **propiedad sourceURL** obtiene la dirección URL del elemento multimedia.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String sourceURL {get;}
```


```VB

Public ReadOnly Property sourceURL As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es la dirección URL de origen.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa sourceURL** para recuperar la dirección URL del primer elemento multimedia de la lista de reproducción "All Música"; A continuación, la dirección URL del elemento multimedia se asigna a la propiedad de dirección URL del objeto de reproductor. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Get an interface to the All Music Playlist. 
WMPLib.IWMPPlaylist pl = player.playlistCollection.getByName("All Music").Item(0);

// Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)pl.get_Item(0);

// Change the URL property of the player to the URL of the media item.
player.URL = media.sourceURL;

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Get an interface to the All Music Playlist. 
Dim pl As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
Dim media As WMPLib.IWMPMedia3 = pl.Item(0)

&#39; Change the URL property of the player to the URL of the media item.
player.URL = Media.sourceURL

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





