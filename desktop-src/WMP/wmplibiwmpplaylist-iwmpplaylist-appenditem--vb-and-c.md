---
title: IWMPPlaylist appendItem (método)
description: El método appendItem agrega un elemento multimedia al final de una lista de reproducción.
ms.assetid: d659298b-ec4e-4771-8e9b-8cfd7b3e0eb2
keywords:
- Método appendItem Reproductor de Windows Media
- Método appendItem Reproductor de Windows Media , interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Reproductor de Windows Media método , appendItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.appendItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de67c7bbd3448e4b4fcdb562b2b10ace68ed7a2c92020650c79fdd90b05366b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098705"
---
# <a name="iwmpplaylistappenditem-method"></a>IWMPPlaylist::appendItem (método)

El **método appendItem** agrega un elemento multimedia al final de una lista de reproducción.

## <a name="syntax"></a>Sintaxis


```CSharp
public void appendItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub appendItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.appendItem
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIWMPMedia* \[ En\]
</dt> <dd>

Interfaz **WMPLib.IWMPMedia** que representa el elemento multimedia que se va a anexar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, debe tener acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa appendItem para** agregar el elemento multimedia actual a la lista de reproducción denominada "ThreeList". El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Get an interface to the current media item.
WMPLib.IWMPMedia currMedia = player.currentMedia;

// Get an interface to the playlist named "ThreeList".
WMPLib.IWMPPlaylist plThreeList = player.playlistCollection.getByName("ThreeList").Item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);
```


```VB

' Get an interface to the current media item.
Dim currMedia As WMPLib.IWMPMedia = player.currentMedia

&#39; Get an interface to the playlist named &quot;ThreeList&quot;.
Dim plThreeList As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;ThreeList&quot;).Item(0)

&#39; Append the media item to the playlist.
plThreeList.appendItem(currMedia)
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
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





