---
title: PlaylistCollection. getByName, método
description: El método getByName recupera un objeto PlaylistArray que contiene listas de reproducción con el nombre especificado, si existe alguno.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- método getByName de Windows Media Player
- método getByName de Windows Media Player, clase PlaylistCollection
- Clase PlaylistCollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718883"
---
# <a name="playlistcollectiongetbyname-method"></a>PlaylistCollection. getByName, método

El método **getByName** recupera un objeto **PlaylistArray** que contiene listas de reproducción con el nombre especificado, si existe alguno.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre de las listas de reproducción que se van a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **PlaylistArray** .

## <a name="remarks"></a>Observaciones

Use *PlaylistArray*. **recuento** para determinar si existe una lista de reproducción. Si **Count** es cero, no existe ninguna lista de reproducción.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *playlistCollection*. **getByName** para comprobar el objeto **playlistCollection** para una lista de reproducción denominada "ThreeList". Si existe la lista de reproducción "Threelist", **getByName** establece "Threelist" como la lista de reproducción actual. El objeto **Player** se creó con el identificador = "Player".


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**PlaylistArray. Count**](playlistarray-count.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





