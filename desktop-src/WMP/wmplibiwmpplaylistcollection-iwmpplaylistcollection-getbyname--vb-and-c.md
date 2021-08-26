---
title: IWMPPlaylistCollection getByName (método)
description: El método getByName devuelve una interfaz IWMPPlaylistArray que proporciona acceso a las listas de reproducción con el nombre especificado, si existe alguna.
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- Método getByName Reproductor de Windows Media
- Método getByName Reproductor de Windows Media , interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Reproductor de Windows Media método , getByName
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fcee45af3ef55d53a05bab290fa92d3e6842fbb097358235b6720cbb1b54e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999745"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a>IWMPPlaylistCollection::getByName (método)

El **método getByName** devuelve una interfaz **IWMPPlaylistArray** que proporciona acceso a las listas de reproducción con el nombre especificado, si existe alguna.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylistArray getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getByName
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrName* \[ En\]
</dt> <dd>

**System.String que** es el nombre de la lista de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPPlaylistArray** para la matriz recuperada de listas de reproducción.

## <a name="remarks"></a>Comentarios

Use **IWMPPlaylistArray.count para** determinar si existe una lista de reproducción. Si **count** es cero, la matriz está vacía.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa getByName para** comprobar la colección de listas de reproducción de una lista de reproducción denominada "Favoritos: 4 y 5 estrellas clasificadas". Si existe una lista de reproducción por ese nombre, **getByName** la establece como la lista de reproducción actual. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Get the count of the playlists named "Favorites -- 4 and 5 star rated".
int checkit = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").count;

// Since duplicate playlist names are allowed, the count returned
// will be either zero (no playlist) or greater than zero (playlist exists).
if (checkit > 0)
{
    // Retrieve a playlist array containing "Favorites -- 4 and 5 star rated".
    // Assume that there is only one playlist with that name, and assign it to the 
    // current playlist.
    player.currentPlaylist = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").Item(0);
}
```


```VB

'  Get the count of the playlists named &quot;Favorites -- 4 and 5 star rated&quot;.
Dim checkit As Integer = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).count

&#39;  Since duplicate playlist names are allowed, the count returned
&#39;  will be either zero (no playlist) or greater than zero (playlist exists).
If (checkit > 0) Then

    &#39;  Retrieve a playlist array object containing &quot;Favorites -- 4 and 5 star rated&quot;.
    &#39;  Assume that there is only one playlist with that name, and assign it to the 
    &#39;  current playlist.
    player.currentPlaylist = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).Item(0)

End If
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPPlaylistArray (VB y C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray.count (VB y C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistCollection (VB y C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





