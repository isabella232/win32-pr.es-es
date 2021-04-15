---
title: IWMPPlaylistCollection reproducción, método
description: El método reproducción devuelve una interfaz IWMPPlaylist para una nueva lista de reproducción vacía en la biblioteca.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- método reproducción de Windows Media Player
- método reproducción Windows Media Player, interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Windows Media Player, método reproducción
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
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708219"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a>IWMPPlaylistCollection:: reproducción (método)

El método **reproducción** devuelve una interfaz **IWMPPlaylist** para una nueva lista de reproducción vacía en la biblioteca.

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

*bstrName* \[ de\]
</dt> <dd>

**System. String** que es el nombre de la nueva lista de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una interfaz **WMPLib. IWMPPlaylist** para la nueva lista de reproducción.

## <a name="remarks"></a>Observaciones

Este método crea una lista de reproducción vacía en la biblioteca. Para rellenar la lista de reproducción con elementos multimedia, use **IWMPPlaylist. appendItem** o **IWMPPlaylist. insertItem**.

En la biblioteca se permiten varias listas de reproducción con el mismo nombre. Para evitar la creación de un nombre de lista de reproducción duplicado con este método, use el método **getByName** y **IWMPPlaylistArray. Count** para detectar si ya existe una lista de reproducción con un nombre determinado.

Los espacios iniciales y finales no se permiten en los nombres de las listas de reproducción y se quitan automáticamente del valor especificado para el parámetro *bstrName* .

Antes de llamar a este método, debe tener acceso total a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea una nueva lista de reproducción vacía denominada "ThreeList", se agrega a la colección de listas de reproducción y se le devuelve una interfaz. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. appendItem (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray. Count (VB y C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistCollection (VB y C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





