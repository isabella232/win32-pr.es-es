---
title: Método IWMPPlaylistCollection newPlaylist
description: El método newPlaylist devuelve una interfaz IWMPPlaylist para una nueva lista de reproducción vacía en la biblioteca.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- Método newPlaylist Reproductor de Windows Media
- Método newPlaylist Reproductor de Windows Media , interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Reproductor de Windows Media , método newPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3971e8cd63a9d78f1c12cb912e6888d51abc9635e78be8d291a1d5535647292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053453"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a>IWMPPlaylistCollection::newPlaylist (Método)

El **método newPlaylist** devuelve una **interfaz IWMPPlaylist** para una nueva lista de reproducción vacía en la biblioteca.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrName* \[ En\]
</dt> <dd>

**System.String que** es el nombre de la nueva lista de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPPlaylist** para la nueva lista de reproducción.

## <a name="remarks"></a>Comentarios

Este método crea una lista de reproducción vacía en la biblioteca. Para rellenar la lista de reproducción con elementos multimedia, use **IWMPPlaylist.appendItem** o **IWMPPlaylist.insertItem**.

Se permiten varias listas de reproducción con el mismo nombre en la biblioteca. Para evitar la creación de un nombre de lista de reproducción duplicado con este método, use el método **getByName** y **IWMPPlaylistArray.count** para detectar si ya existe una lista de reproducción con un nombre determinado.

Los espacios iniciales y finales no se permiten en los nombres de lista de reproducción y se quitan automáticamente del valor especificado para el *parámetro bstrName.*

Antes de llamar a este método, debe tener acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea una nueva lista de reproducción vacía denominada "ThreeList", se agrega a la colección de listas de reproducción y se devuelve una interfaz a ella. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.appendItem (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.insertItem (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray.count (VB y C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistCollection (VB y C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getByName (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





